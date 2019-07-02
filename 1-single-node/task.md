#### Task
You need to setup single node cluster using kubeadm utility.

#### Reading:
1. https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/

#### Environment:
1. Use local virtualbox and vagrant to maintain your dev environment.
2. Use template Vagrantfile supplied in repository. It's sufficient to create clean CentOS sandbox.
3. Vagrantfile contain shell provisioner example. Make sure you understand it.

#### Steps and tips
1. Prepare environment.
  1. Install virtualbox, vagrant.
  2. Navigate to folder with Vagrantfile
  3. Vagrant up, vagrant ssh
  4. Make sure you're able to reach internet from inside your environment.

2. Read and understand reading materials
3. Follow guide to create single-node control-plane k8s cluster
4. Untaint your master node.
5. Make sure you're able to see nodes, pods, namespaces.
6. Record your steps into bash-like script.
7. Find out and read about Vagrant provisioning.
8. Inject your automated cluster creation steps into Vagrantfile
9. Reach state when Vagrant up on cold environment will create working k8s cluster.
10. Answer questions. Put answers into answers.md file in `1-single-node` folder. Use MD markup cheatsheet.
11. Think about what reader will find out. Make navigation, colors, markup user-friendly and readable.

#### Questions
1. Definition of Kubernetes. Give answer to question "What is Kubernetes":
  1. In 2 words.
  2. In 1 sentence.
  3. in 5 sentences.
2. What is node?
3. What is master node?
4. What is control plane?
5. What is kubeadm?
6. Explain difference between kubespray and kubeadm.
7. Explain difference between minikube and kubeadm.
8. What language kubeadm was written on?
9. What company writes and maintain kubeadm?
10. What version of kubernetes was installed in your workshop?
11. What is official **release** version of kubernetes?
12. What is k8s acronym?
13. What is i18n, l10n acronyms?
14. What networking plugin you where used in your installation? Why?
15. What is kube-proxy?
16. What is kubelet?
17. What is name of plugin for internal k8s DNS service?
18. What is kube-scheduler?
19. What is kube-apiserver?
20. What is kube-controller-manager?
21. What is etcd?
22. What is worker node?
23. What is pod?
24. What k8s components running on master node?
25. What k8s components running on worker node?
26. What k8s components in your setup running in containers?
27. What k8s components in your setup running as host OS services?
28. What k8s components in your environment running and k8s managed pods?
29. What is container runtime environment?
30. What container runtime environment you're using in your setup?
31. What host system modification required to make possible k8s cluster creation?
32. What is idempotency in general?
