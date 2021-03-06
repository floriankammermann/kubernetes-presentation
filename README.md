# Kubernetes Presentation

A presentation about architecture, setup, usage of https://kubernetes.io/  
The slides are best viewed with https://www.libreoffice.org/

## Example

1. Build the dockerimage [example/dockerimage](example/dockerimage)
1. Upload docker image to your favourite registry (here I used [quay.io](https://quay.io/))
1. Refer the image in the [deployment config](example/kube-config/kube-presentation-deployment.yaml#L15)
1. Create the namespace `kubectl create namespace kubepresentation`
1. Apply the deployment `kubectl apply -f example/kube-config/kube-presentation-deployment.yaml`
1. Apply the service `kubectl apply -f example/kube-config/kube-presentation-service.yaml`
1. Apply the ingress `kubectl apply -f example/kube-config/kube-presentation-ingress.yaml`
1. Check state with `kubectl get all -n kubepresentation` and `kubectl get ingress -n kubepresentation`

## Links

### Architecture
* [Kubernetes Master Components](https://medium.com/jorgeacetozi/kubernetes-master-components-etcd-api-server-controller-manager-and-scheduler-3a0179fc8186)
* [Kubernetes Node Components](https://medium.com/jorgeacetozi/kubernetes-master-components-etcd-api-server-controller-manager-and-scheduler-3a0179fc8186)
* [A few things I've learned about Kubernetes](https://jvns.ca/blog/2017/06/04/learning-about-kubernetes/)
* [Core Controllers](https://github.com/kubernetes/kubernetes/blob/master/cmd/kube-controller-manager/app/controllermanager.go#L317)
* [Cluster Networking](https://kubernetes.io/docs/concepts/cluster-administration/networking/#how-to-achieve-this)
* [Operating a Kubernetes network](https://jvns.ca/blog/2017/10/10/operating-a-kubernetes-network/)
* [Understanding kubernetes networking: services](https://medium.com/google-cloud/understanding-kubernetes-networking-services-f0cb48e4cc82)
* [Strategies for kube-proxy implementation](https://www.youtube.com/watch?v=4-pawkiazEg)
* [Pods](https://kubernetes.io/docs/concepts/workloads/pods/pod/)
* [Container Storage Interface (CSI)](https://kubernetes.io/blog/2018/01/introducing-container-storage-interface/)

### Setup
* [Kubernetes the Hardway](https://github.com/kelseyhightower/kubernetes-the-hard-way)
* [Encrypting Secret Data at Rest](https://kubernetes.io/docs/tasks/administer-cluster/encrypt-data/)
* [Policy based networking](https://docs.projectcalico.org/v3.1/getting-started/kubernetes/installation/flannel)

### Usage 
* [Services](https://kubernetes.io/docs/concepts/services-networking/service/)
* [incoming traffic options](https://medium.com/google-cloud/kubernetes-nodeport-vs-loadbalancer-vs-ingress-when-should-i-use-what-922f010849e0)
* [Connecting Applications with Services](https://kubernetes.io/docs/concepts/services-networking/connect-applications-service/)
* [nginx ingress controller](https://github.com/kubernetes/ingress-nginx)
* [kubectl cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
* [kubernetes api reference](https://v1-9.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.9/)
* [custom controller](https://github.com/kubernetes/sample-controller)

### Community
* [Special Interest Groups](https://github.com/kubernetes/community/blob/master/sig-list.md)
