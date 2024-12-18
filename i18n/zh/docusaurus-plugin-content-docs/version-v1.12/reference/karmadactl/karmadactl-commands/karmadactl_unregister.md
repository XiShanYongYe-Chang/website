---
title: karmadactl unregister
---

Remove a pull mode cluster from Karmada control plane

### Synopsis

Unregister removes a member cluster from Karmada, it will clean up the cluster object in the control plane and Karmada resources in the member cluster.

```
karmadactl unregister CLUSTER_NAME
```

### Examples

```
  # Unregister cluster from karmada control plane
  karmadactl unregister CLUSTER_NAME --cluster-kubeconfig=<CLUSTER_KUBECONFIG> [--cluster-context=<CLUSTER_CONTEXT>]
  
  # Unregister cluster from karmada control plane with timeout
  karmadactl unregister CLUSTER_NAME --cluster-kubeconfig=<CLUSTER_KUBECONFIG> --wait 2m
  
  # Unregister cluster from karmada control plane, manually specify the location of the karmada config
  karmadactl unregister CLUSTER_NAME --karmada-config=<KARMADA_CONFIG> [--karmada-context=<KARMADA_CONTEXT>] --cluster-kubeconfig=<CLUSTER_KUBECONFIG> [--cluster-context=<CLUSTER_CONTEXT>]
```

### Options

```
      --agent-name string           Deployment name of the karmada-agent component deployed. (default "karmada-agent")
      --cluster-context string      Context in cluster-kubeconfig to access unregistering member cluster, optional, defaults to current context.
      --cluster-kubeconfig string   KUBECONFIG file path to access unregistering member cluster, required.
      --cluster-namespace string    Namespace in the control plane where member cluster secrets are stored. (default "karmada-cluster")
      --dry-run                     Run the command in dry-run mode, without making any server requests.
  -h, --help                        help for unregister
      --karmada-config string       Path of config to access karmada-apiserver, optional, defaults to fetch automatically from member cluster.
      --karmada-context string      Context in karmada-config to access karmada-apiserver, optional, defaults to current context.
  -n, --namespace string            Namespace of the karmada-agent component deployed. (default "karmada-system")
      --wait duration               wait for the unjoin command execution process(default 60s), if there is no success after this time, timeout will be returned. (default 1m0s)
```

### Options inherited from parent commands

```
      --add-dir-header                   If true, adds the file directory to the header of the log messages
      --alsologtostderr                  log to standard error as well as files (no effect when -logtostderr=true)
      --kubeconfig string                Paths to a kubeconfig. Only required if out-of-cluster.
      --log-backtrace-at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log-dir string                   If non-empty, write log files in this directory (no effect when -logtostderr=true)
      --log-file string                  If non-empty, use this log file (no effect when -logtostderr=true)
      --log-file-max-size uint           Defines the maximum size a log file can grow to (no effect when -logtostderr=true). Unit is megabytes. If the value is 0, the maximum file size is unlimited. (default 1800)
      --logtostderr                      log to standard error instead of files (default true)
      --one-output                       If true, only write logs to their native severity level (vs also writing to each lower severity level; no effect when -logtostderr=true)
      --skip-headers                     If true, avoid header prefixes in the log messages
      --skip-log-headers                 If true, avoid headers when opening log files (no effect when -logtostderr=true)
      --stderrthreshold severity         logs at or above this threshold go to stderr when writing to files and stderr (no effect when -logtostderr=true or -alsologtostderr=true) (default 2)
  -v, --v Level                          number for the log level verbosity
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [karmadactl](karmadactl.md)	 - karmadactl controls a Kubernetes Cluster Federation.

#### Go Back to [Karmadactl Commands](karmadactl_index.md) Homepage.


###### Auto generated by [spf13/cobra script in Karmada](https://github.com/karmada-io/karmada/tree/master/hack/tools/genkarmadactldocs).