=============================
##### Persistent Volumes ####
=============================

* Pod volumes should also be mounted in the container image - at build time - in order to be accessed by the container.

*Volumes Type:
--------------

1) emptyDir: a simple empty directory used for storing transient data.

2) hostPath: used for mounting directories from the worker node's filesystem into the pod.

3) gitRepo: a volume initialized by checking out the contents of a Git Repository.

4) nfs: an NFS share mounted into the pod.

5) gcePersistentDisk: (Google Compute Engine Persistent Disk), awsElasticBlockStore (Amazon Web Services Elastic Block Store Volume), azureDisk (Azure Disk Volume)
used for mounting cloud provide-specific storage.

6) cinder, cephfs, iscsi, flocker, glusterfs, quobyte, rbd, flexVolume, vsphereVolume, photonPersistentDisk, scalaIO: used for mounting other types of network storage.

7) configMap, secrets, downwardAPI: special types of volumes used to expose certain kubernetes resources and cluster information to the pod.

8) persistentVolumeClaim: a way to use pre- or dynamically provisioned persistent storage.


### gitRepo: Using Git Repo as the starting point for a volume:
gitRepo:
  repository: https://...
  revision: masater # which branch
  directory: . # whether to clone the project in a new folder or in the root folder 


### PersistentVolume:
PersistentVolumes don;t belong to any namespace, they are cluster-level resources like nodes.
