#### Goal
- Understand k8s api versioning system.
- Understand k8s object configuration syntax
- Build working docker registry in k8s

#### Task
You need to create environment using kubeadm on platform of your choice ( e.g. AWS).
Develop simple set of k8s manifests/objects to deploy application
Build local docker registry application inside your cluster.


#### Reading:
1. https://kubernetes.io/docs/concepts/workloads/controllers/deployment/
2. https://kubernetes.io/docs/concepts/services-networking/service/
3. https://kubernetes.io/docs/setup/release/version-skew-policy/
4. https://kubernetes.io/docs/concepts/overview/kubernetes-api/#api-versioning
5. https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api_changes.md#alpha-beta-and-stable-versions
6. https://kubernetes.io/docs/concepts/services-networking/service/#nodeport
7. https://kubernetes.io/docs/concepts/storage/volumes/#hostpath
8. https://docs.docker.com/registry/

#### Environment:
1. Use single all-in-one AWS-based k8s kubadm based deployment. Minikube also an option.
2. Used official docker registry containter as a base

#### Steps and tips
1. Prepare environment: use automation of your choice
2. Prepare Deployment/Service manifest to deploy docker registry inside k8s.
3. Expose docker registry service on 80 port using NodePort LB type.
4. Build local "hello-world" docker image and upload it to docker registry.
5. Restart pod: remove pod - observe what happens after that
6. Restart pod2: change number of pod replicas to 0. Wait for changes. Return back to 1.
7. Check if you image available in docker registry.
8. Modify your manifests. Add hostpath volume to pod.
9. Re-upload your hello world docker image back to registry.
10. Restart docker registry pod.
11. Check if your image available in docker registry.
12. Create your own nginx-based "hello-world" docker image.
13. Create microservice based on your internal docker registry and "hello-world" image.
14. Expose microservice with NodePort.

#### Questions
1. What versions of kubelet supported by kube-apiserver v1.15
2. What versions of kubelet supported by kube-apiserver v1.14
3. What API levels used to label API object readiness? Briefly explain API levels designations.
4. What is API group?
5. You're using API object with version: `v1alpha1`. How many guarantied minor releases this api will exists?
6. You're using API object with verions `v1beta1`. How many many guarantied minor releases this api will exists?
7. What is Deployment?
8. What is ReplicaSet?
9. What is Controller?
10. Explain difference between declarative and imperative approach?
12. What is manifest?
13. What is volume?
