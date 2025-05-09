---
title: "testkube install runner"
---
<head>
  <meta name="docsearch:indexPrefix" content="reference-doc" />
</head>

## testkube install runner



```
testkube install runner <name> [flags]
```

### Options

```
      --create                        auto create that agent
      --dry-run                       display helm commands only
  -e, --env strings                   (with --create) environment ID or slug that the agent have access to
  -N, --execution-namespace string    namespace to run executions (defaults to installation namespace)
      --floating                      (with --create) create as a floating runner
      --global                        make it global runner
  -g, --global-template-path string   include global template
      --group string                  make it grouped runner
  -h, --help                          help for runner
  -l, --label strings                 (with --create) label key value pair: --label key1=value1
  -n, --namespace string              namespace to install the agent
  -s, --secret string                 secret key for the selected agent
      --version string                agent version to use (defaults to latest)
```

### Options inherited from parent commands

```
  -a, --api-uri string          api uri, default value read from config if set (default "http://localhost:8088")
  -c, --client string           client used for connecting to Testkube API one of proxy|direct|cluster (default "proxy")
      --header stringToString   headers for direct client key value pair: --header name=value (default [])
      --insecure                insecure connection for direct client
      --verbose                 show additional debug messages
```

### SEE ALSO

* [testkube install](testkube-install.md)	 - 

