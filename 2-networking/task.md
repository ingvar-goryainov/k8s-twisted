#### Goal
- Understand how nodes/pods/service communicates
- Understand basic objects: Deployment, Service, Pods.
- Get hands-on experience troubleshooting k8s low-level stack

#### Task
You need to setup 2 nodes(master,worker) cluster using kubeadm utility and make it work.

#### Reading:
1. https://kubernetes.io/docs/concepts/cluster-administration/networking/#kubernetes-model
2. https://kubernetes.io/docs/concepts/extend-kubernetes/compute-storage-net/network-plugins/
3. https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/
4. https://kubernetes.io/docs/concepts/workloads/controllers/deployment/
5. https://kubernetes.io/docs/concepts/services-networking/service/

#### Environment:
1. Use local virtualbox and vagrant to maintain your dev environment.
2. Use template Vagrantfile supplied in repository. It's sufficient to create clean 2-nodes CentOS sandbox.

#### Steps and tips
1. Prepare environment.

   1. Install virtualbox, vagrant.
   2. Navigate to folder with Vagrantfile
   3. Vagrant up master, vagrant up worker
   4. Make sure you're able to reach internet from inside your environment.
2. Read and understand materials
3. Follow guide to create 2-node control-plane k8s cluster
  1. Configure cluster to use only worker node for workloads
4. Use `weave` networking plugin
5. Make cluster working ( resolve all inconsistencies in given environment)
6. Create simple pair of Deployment/Service.
  1. Use community docker nginx image as workload.
  2. Save .yaml manifests in your answers folder.
7. Create simple troubleshooting pod inside k8s.
  1. You should be able to attach/detach it on-demand.
8. Make sure you're able to reach your nginx pod AND Service from:
  1. Master node
  2. Worker node
  3. service pod
9. Replicate above behavior using `flanel` networking plugin.
10. Write provisioner(s) that configures master-worker k8s in given environment with `weave` plugin.
11. Write provisioner(s) that configures master-worker k8s in given environment with `flannel` plugin
12. Answer questions.

#### Questions
