# ocp-cluster

# Setup Storage

This assumes you have setup storage for the cluster. An example of using the NFS client provisioner is located in the `/nfs-client-provisioner` folder. Documentation for this setup is located at https://github.com/kubernetes-retired/external-storage/tree/master/nfs-client

# Login to cluster

Before any scripts are executed, the assumption is that you are logged into the server as a cluster administrator.

`oc login --token=sha256~<yourtoken> --server=https://api.ocp.snimmo.com:6443`


# Additional Notes

## Describing the Operators

`oc get packagemanifests -n openshift-marketplace | grep <search-term>`  
`oc describe packagemanifests -n openshift-marketplace <name-of-package>`

