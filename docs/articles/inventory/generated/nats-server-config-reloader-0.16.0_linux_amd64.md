---
hide_table_of_contents: true
---

<table>
<tr><td>digest</td><td><code>sha256:6e1f185d0f39fdf6032872bd20f1ce134d4e18c923d55f7cf93d40afcf6a8ffe</code></td><tr><tr><td>vulnerabilities</td><td><img alt="critical: 0" src="https://img.shields.io/badge/critical-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/high-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/medium-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/low-0-lightgrey"/> <img alt="unspecified: 1" src="https://img.shields.io/badge/unspecified-1-lightgrey"/></td></tr>
<tr><td>size</td><td>4.8 MB</td></tr>
<tr><td>packages</td><td>22</td></tr>
</table>
</details></table>
</details>

<table>
<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <img alt="unspecified: 1" src="https://img.shields.io/badge/U-1-lightgrey"/><strong>openssl</strong> <code>3.3.2-r0</code> (apk)</summary>

<small><code>pkg:apk/alpine/openssl@3.3.2-r0?os_name=alpine&os_version=3.20</code></small><br/>

```dockerfile
# Dockerfile (4:31)
FROM alpine:3.20.3 as deps

ARG GO_APP
ARG GORELEASER_DIST_DIR=/go/src/dist

ARG TARGETOS
ARG TARGETARCH
ARG TARGETVARIANT

RUN mkdir -p /go/bin /go/src ${GORELEASER_DIST_DIR}

COPY --from=build ${GORELEASER_DIST_DIR}/ ${GORELEASER_DIST_DIR}

RUN <<EOT
  set -e 
  apk add --no-cache ca-certificates jq
  cd ${GORELEASER_DIST_DIR}/..

  if [[ ${TARGETARCH} == "arm" ]]; then VARIANT=$(echo ${TARGETVARIANT} | sed 's/^v//'); fi
  BIN_PATH=$(jq -r ".[] |select(.type   == \"Binary\" and \
                                .name   == \"${GO_APP}\" and \
                                .goos   == \"${TARGETOS}\" and \
                                .goarch == \"${TARGETARCH}\" and \
                                (.goarm == \"${VARIANT}\" or .goarm == null)) | .path" < /go/src/dist/artifacts.json)
  cp ${BIN_PATH} /go/bin
EOT

FROM alpine:3.20.3
```

<br/>

<a href="https://scout.docker.com/v/CVE-2024-9143?s=alpine&n=openssl&ns=alpine&t=apk&osn=alpine&osv=3.20&vr=%3C3.3.2-r1"><img alt="unspecified : CVE--2024--9143" src="https://img.shields.io/badge/CVE--2024--9143-lightgrey?label=unspecified%20&labelColor=lightgrey"/></a> 

<table>
<tr><td>Affected range</td><td><code>&lt;3.3.2-r1</code></td></tr>
<tr><td>Fixed version</td><td><code>3.3.2-r1</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.04%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>11th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>



</blockquote>
</details>
</details></td></tr>
</table>
