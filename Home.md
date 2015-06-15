# Introduction #
Welcome to the CephWin project! The home of the CEPH client. Windows has an integrated NFS client but it needs to support more network file systems.

See the CEPH web site at http://ceph.newdream.net


This client only supports the following Operating Systems:
  * Windows Server 2008/Windows Storage Server 2008
  * Windows Server 2008 [R2](https://code.google.com/p/cephwin/source/detail?r=2)/Windows Storage Server 2008 [R2](https://code.google.com/p/cephwin/source/detail?r=2)

The goal is to create 3 services that are part of this client
  * Monitor service
  * OSD device driver service (poll for new drives, expanded size)

### Future plans: ###
  * Hyper-V storage driver

Part currently under development: OSD storage device driver


## History ##

This project started because I felt that the storage provided by CEPH could be utilized on Windows. In order to provide a truly hybrid-capable storage environment, Windows needs to be included. Some purists may say that this is a stupid idea, I say maybe but it can't hurt to try. This will provide a Highly Available File Server Cluster with a massive storage backend. Current networked storage such as NFS and iSCSI are excellent but due come with limitations. For example, NFS on Windows performs well, but the user-mapping leaves a lot to be desired.


## Architecture ##

I will be using the RADOS API and/or RBD.