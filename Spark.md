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
1. compile from 2.4.1 source codes and start server. But when connecting from browser, it shows always loading. Some JS script files failed to be loaded.
2. install 2.2.2 from public repostitory fixed it.
3. after step 1 and 2, when connecting from browser, it shows always same error as step 1 - always loading. Reinstalling several times did not fix it. It was fixed finially by clearing browser cach. Not sure if recompiling 2.4.1 source code would succeed or not after clearing browser cash.
4. when registering node which installed ambari-server, it failed to start. Fixed by removing /usr/lib/pyton2.6/site-packages/ambari\* and reinstall ambari-agent.
