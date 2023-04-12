---
title: kbcli cluster edit-config
---

Edit the config file of the component.

```
kbcli cluster edit-config [flags]
```

### Examples

```
  # edit config for component
  kbcli cluster edit-config <cluster-name> [--component=<component-name>] [--config-spec=<config-spec-name>] [--config-file=<config-file>]
  
  # update mysql max_connections, cluster name is mycluster
  kbcli cluster edit-config mycluster --component=mysql --config-spec=mysql-3node-tpl --config-file=my.cnf
```

### Options

```
      --component string             Specify the name of Component to be updated. If the cluster has only one component, unset the parameter.
      --config-file string           Specify the name of the configuration file to be updated (e.g. for mysql: --config-file=my.cnf). What templates or configure files are available for this cluster can refer to kbcli sub command: 'kbcli cluster describe-config'.
      --config-spec string           Specify the name of the configuration template to be updated (e.g. for apecloud-mysql: --config-spec=mysql-3node-tpl). What templates or configure files are available for this cluster can refer to kbcli sub command: 'kbcli cluster describe-config'.
  -h, --help                         help for edit-config
      --name string                  OpsRequest name. if not specified, it will be randomly generated 
      --replace                      Specify whether to replace the config file. Default to false.
      --set strings                  Specify updated parameter list. For details about the parameters, refer to kbcli sub command: 'kbcli cluster describe-config'.
      --ttlSecondsAfterSucceed int   Time to live after the OpsRequest succeed
```

### Options inherited from parent commands

```
      --as string                      Username to impersonate for the operation. User could be a regular user or a service account in a namespace.
      --as-group stringArray           Group to impersonate for the operation, this flag can be repeated to specify multiple groups.
      --as-uid string                  UID to impersonate for the operation.
      --cache-dir string               Default cache directory (default "$HOME/.kube/cache")
      --certificate-authority string   Path to a cert file for the certificate authority
      --client-certificate string      Path to a client certificate file for TLS
      --client-key string              Path to a client key file for TLS
      --cluster string                 The name of the kubeconfig cluster to use
      --context string                 The name of the kubeconfig context to use
      --disable-compression            If true, opt-out of response compression for all requests to the server
      --insecure-skip-tls-verify       If true, the server's certificate will not be checked for validity. This will make your HTTPS connections insecure
      --kubeconfig string              Path to the kubeconfig file to use for CLI requests.
      --match-server-version           Require server version to match client version
  -n, --namespace string               If present, the namespace scope for this CLI request
      --request-timeout string         The length of time to wait before giving up on a single server request. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). A value of zero means don't timeout requests. (default "0")
  -s, --server string                  The address and port of the Kubernetes API server
      --tls-server-name string         Server name to use for server certificate validation. If it is not provided, the hostname used to contact the server is used
      --token string                   Bearer token for authentication to the API server
      --user string                    The name of the kubeconfig user to use
```

### SEE ALSO

* [kbcli cluster](kbcli_cluster.md)	 - Cluster command.

#### Go Back to [CLI Overview](cli.md) Homepage.
