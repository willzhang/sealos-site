## sealos scp

copy local file to remote on all node.

```
sealos scp [flags]
```

### Examples

```

copy file to default cluster: default
	sealos scp "/root/aa.txt" "/root/dd.txt"
specify the cluster name(If there is only one cluster in the $HOME/.sealos directory, it should be applied. ):
    sealos scp -c my-cluster "/root/aa.txt" "/root/dd.txt"
set role label to copy file:
    sealos scp -c my-cluster -r master,slave,node1 "cat /etc/hosts"
set ips to copy file:
    sealos scp -c my-cluster --ips 172.16.1.38  "/root/aa.txt" "/root/dd.txt"

```

### Options

```
  -c, --cluster-name string   name of cluster to applied scp action (default "default")
  -h, --help                  help for scp
      --ips strings           copy file to nodes with ip address
  -r, --roles string          copy file to nodes with role
```

### Options inherited from parent commands

```
      --cluster-root string   cluster root directory (default "/var/lib/sealos")
      --debug                 enable debug logger
```

### SEE ALSO

* [sealos](sealos.md)	 - simplest way install kubernetes tools.

###### Auto generated by spf13/cobra on 13-Oct-2022
