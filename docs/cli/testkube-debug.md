---
title: "testkube debug"
---
## testkube debug

Print debugging info

### Options

```
  -h, --help   help for debug
```

### Options inherited from parent commands

```
  -a, --api-uri string          api uri, default value read from config if set (default "http://localhost:8088")
  -c, --client string           client used for connecting to Testkube API one of proxy|direct|cluster (default "proxy")
      --header stringToString   headers for direct client key value pair: --header name=value (default [])
      --insecure                insecure connection for direct client
      --namespace string        Kubernetes namespace, default value read from config if set (default "testkube")
      --verbose                 show additional debug messages
```

### SEE ALSO

* [testkube](testkube.md)	 - Testkube entrypoint for kubectl plugin
* [testkube debug agent](testkube-debug-agent.md)	 - Show Agent debug information
* [testkube debug controlplane](testkube-debug-controlplane.md)	 - Show Control Plane debug information
* [testkube debug oss](testkube-debug-oss.md)	 - Show OSS installation debug info

