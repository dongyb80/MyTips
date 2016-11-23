# Ambari
**download links**

wget http://www.apache.org/dist/ambari/ambari-2.4.1/apache-ambari-2.4.1-src.tar.gz

**Notes about compile source codes**
* JDK 1.8
* Git
* NodeJS
* Brunch package of NodeJS
* Maven

**experience** 
* compile from 2.4.1 source codes and start server. But when connecting from browser, it shows always loading. Some JS script files failed to be loaded. 
* install 2.2.2 from public repostitory fixed it. 
* after step 1 and 2, when connecting from browser, it shows always same error as step 1 - always loading. Reinstalling  several times did not fix it. It was fixed finially by clearing browser cach. Not sure if recompiling 2.4.1 source code would succeed or not after clearing browser cash. 
* when registering node which installed ambari-server before, it failed to start. Fixed by removing /usr/lib/pyton2.6/site-packages/ambari\* and reinstall ambari-agent. 
* when installing on one Cloud VMs, the VMs are using private IP for host names and it leads to access Yarn/HDSF from outside of Cloud VMs failed. Fix it by add publicIP/hostname pairs for all machines into each machine first before starting Ambari.

# Spark
* When running spark from my local machine on the yarn created above by ambari, create /user/<username> on HDFS first. It is done on Hadoop machies and run as hdfs account. Change owner to <username> after creating it.
* when running spart-submit command on yarn as cluster mode, change '-queue thequue' to '-queue default'
