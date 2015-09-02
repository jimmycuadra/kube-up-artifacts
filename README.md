# kube-up

[Kubernetes](https://github.com/kubernetes/kubernetes) is awesome, but setting up a cluster is very complicated and the docs are not very clear and consistent at this point. This repository contains artifacts created by using the official "kube-up.sh" script from the official Kubernetes v1.0.4 distribution to create a cluster on AWS. I found that no amount of reading and re-reading the docs was as clear as just seeing the results and inspecting files and processes myself. This information should be useful to anyone who wants to create a Kubernetes cluster from scratch and wants to see both the big picture and the details of all the components and configuration that are required.

## Included files

* kube-up.out: The shell output of running the official kube-up.sh script.
* local_kubeconfig.yml: The kubeconfig file placed on your local system at ~/.kube/config, used by `kubectl` to control the cluster remotely.
* master: The files placed on the filesystem of the Kubernetes master server. Note that /mnt/master-pd/srv/kubernetes is linked at /srv/kubernetes and referred to with that path in the various configuration files.
* master_units.txt: The systemd units Kubernetes runs on the master server.
* node: The files placed on the filesystem of all the Kubernetes node servers.
* node_units.txt: The systemd units Kubernetes runs on all the node servers.

## License

[MIT](http://opensource.org/licenses/MIT)
