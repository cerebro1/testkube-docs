---
title: "testkube abort"
---
## testkube abort

Abort tests or test suites

```
testkube abort <resourceName> [flags]
```

### Options

```
  -h, --help   help for abort
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
* [testkube abort execution](testkube-abort-execution.md)	 - Aborts execution of the test
* [testkube abort executions](testkube-abort-executions.md)	 - Aborts all executions of the test
* [testkube abort testsuiteexecution](testkube-abort-testsuiteexecution.md)	 - Abort test suite execution
* [testkube abort testsuiteexecutions](testkube-abort-testsuiteexecutions.md)	 - Abort all test suite executions
* [testkube abort testworkflowexecution](testkube-abort-testworkflowexecution.md)	 - Abort test workflow execution
* [testkube abort testworkflowexecutions](testkube-abort-testworkflowexecutions.md)	 - Abort all test workflow executions

