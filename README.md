# Kubernetes Components & Concepts:


This repo is a result of [Kubernetes in Action](https://www.manning.com/books/kubernetes-in-action) reading. which is one of the best books that have been written to explore the Kubernetes World.

## Persistent Volumes

#### Volumes Type:

* emptyDir: a simple empty directory used for storing transient data.

* hostPath: used for mounting directories from the worker node's filesystem into the pod.

* gitRepo: a volume initialized by checking out the contents of a Git Repository.

* nfs: an NFS share mounted into the pod.

* gcePersistentDisk: (Google Compute Engine Persistent Disk), awsElasticBlockStore (Amazon Web Services Elastic Block Store Volume), azureDisk (Azure Disk Volume)
used for mounting cloud provide-specific storage.

* cinder, cephfs, iscsi, flocker, glusterfs, quobyte, rbd, flexVolume, vsphereVolume, photonPersistentDisk, scalaIO: used for mounting other types of network storage.

* configMap, secrets, downwardAPI: special types of volumes used to expose certain kubernetes resources and cluster information to the pod.

* persistentVolumeClaim: a way to use pre- or dynamically provisioned persistent storage.


#### gitRepo: Using Git Repo as the starting point for a volume:

