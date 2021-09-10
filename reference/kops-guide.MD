sat853.net

aws s3 mb s3://demo2.k8s.sat853.net

export KOPS_STATE_STORE=s3://demo2.k8s.sat853.net

kops create cluster --cloud=aws --zones=us-east-1b --name=demo2.k8s.sat853.net --dns-zone=sat853.net --dns private 

----------------
Terminal Output:

Cluster configuration has been created.

Suggestions:
 * list clusters with: kops get cluster
 * edit this cluster with: kops edit cluster demo2.k8s.sat853.net
 * edit your node instance group: kops edit ig --name=demo2.k8s.sat853.net nodes
 * edit your master instance group: kops edit ig --name=demo2.k8s.sat853.net master-us-east-1b

Finally configure your cluster with: kops update cluster --name demo2.k8s.sat853.net --yes
-------------------


kops update cluster demo2.k8s.sat853.net --yes

-----------
Terminal Output:

Cluster is starting.  It should be ready in a few minutes.

Suggestions:
 * validate cluster: kops validate cluster
 * list nodes: kubectl get nodes --show-labels
 * ssh to the master: ssh -i ~/.ssh/id_rsa admin@api.demo2.k8s.sat853.net
 * the admin user is specific to Debian. If not using Debian please use the appropriate user based on your OS.
 * read about installing addons at: https://github.com/kubernetes/kops/blob/master/docs/addons.md.


----------
 
ssh -i ~/.ssh/id_rsa admin@api.demo2.k8s.sat853.net

kops delete cluster demo2.k8s.sat853.net --yes

ssh-keygen -f "/root/.ssh/known_hosts" -R "api.demo2.k8s.sat853.net"
