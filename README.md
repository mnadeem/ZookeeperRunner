## Zookeeper Runner ##


After downloading the zip file, copy your zookeeper related jar files, and log4j.properties file to [RUNNER_HOME]/lib, based on your environment start the appropriate script, you are done.

Zookeeper Runner is based on [Java Service Wrapper][jswId]



### FEATURES ###

---

* Pre bundled script which would allow you to manage jenkins instance in different environments seamlessly
* Configurations can be changed/added very easily
* Scripts supports init.d configuration and Windows Service modes
* Upgrading jenkins is just a matter of replacing __jenkins.war__ in lib folder
* Pre configured plugins can be provided with the bundle.
* you can added other jar files easily in the class path
* _application parameters_ and _jmv parameters_ can configured very easily



### DIRECTORY DETAILS ###

---


* __data__ ==> Zookeeper data directory, contains the **myid** file as well

* __logs__ ==> this where Wrapper/Zookeeper will spit out logs

* __conf__ ==> contains wrapper and zookeeper configuration files

* __lib__ ==> this folder contains __wrapper.jar__ and zookeeper related jars, and any other jars you want to make available to classpath

* __bin__ ==> binary executables are present here, based on you environment you have to execute one of the files in this directory



### FAQ ###

---


#### 1 How do I change the client port? ####

_Modify the [RUNNER_HOME]/conf/zoo.cfg file (line number 14) as follows_

	clientPort=2182
	
#### 2 How do I change the NtService ####

_Modify the [RUNNER_HOME]/conf/wrapper.conf file (line number 95) as follows_

	wrapper.ntservice.name=Zookeeper2

#### 3 How do I change myid ####

_Modify the [RUNNER_HOME]/data/myid file to store the id you want_

#### 4 How do I Run multiple instances of zookeeper on same machine ####

##### Step 1 : Copy/Paste 3 runners into your local drive
##### Step 2 : Change zoo config in each instance

* uncomment line number 31-33, in [RUNNER_HOME]/conf/zoo.cfg file
* Make sure each instance has unique clientPort (Refer to FAQ#1)
* Make sure each instance has unique myid (Refer to FAQ#3)

##### Step 3 :  Make sure each instance has unique NtService Name
Refer to FAQ#2

##### Step 4 :  Start each zookeeper instance
  
  [jswId]: http://wrapper.tanukisoftware.com/  "Java Service Wrapper"
 