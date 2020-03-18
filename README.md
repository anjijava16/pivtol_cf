# pivtol_cf

# Login URL
 ```
 https://console.run.pivotal.io/organizations/6be96811-fa48-48c2-bacb-ce5038211806/spaces/ecc4a05b-3844-46f6-81c4-b7cc781de4c6
 Email : XXXX@gmail.com
 Password: XXXXX
 
 ```
 
# Application URL :
    https://cf-demo-bright-koala-jt.cfapps.io/

 
 
  
# Install URL :
   https://docs.cloudfoundry.org/cf-cli/install-go-cli.html
 
 # cf connection Setps
 
 ```
 welcome@welcome-Inspiron-5558:~/cloudFoundry_pivotal/cf-sample-app-spring-master$ cf login
API endpoint: https://api.run.pivotal.io

Email: anjaiahspr@gmail.com

Password: 
Authenticating...
OK

Select an org:
1. mmtech-quiz
2. mmtechsoft

Org (enter to skip): 2
Targeted org mmtechsoft

Select a space:
1. development
2. mmtech-webservice

Space (enter to skip): 2
Targeted space mmtech-webservice



API endpoint:   https://api.run.pivotal.io (API version: 3.81.0)
User:           anjaiahspr@gmail.com
Org:            mmtechsoft
Space:          mmtech-webservice
welcome@welcome-Inspiron-5558:~/cloudFoundry_pivotal/cf-sample-app-spring-master$ cf push
Pushing from manifest to org mmtechsoft / space mmtech-webservice as anjaiahspr@gmail.com...
Using manifest file /home/welcome/cloudFoundry_pivotal/cf-sample-app-spring-master/manifest.yml
Getting app info...
Creating app with these attributes...
+ name:         cf-demo
  path:         /home/welcome/cloudFoundry_pivotal/cf-sample-app-spring-master
  buildpacks:
+   https://github.com/cloudfoundry/java-buildpack.git
+ instances:    1
+ memory:       768M
  routes:
+   cf-demo-bright-koala-jt.cfapps.io

Creating app cf-demo...
Mapping routes...
Comparing local files to remote cache...
Packaging files to upload...
Uploading files...
 713.63 KiB / 713.63 KiB [======================================================================================================================================================================] 100.00% 2s

Waiting for API to complete processing files...

Staging app and tracing logs...
   Cell 00dd954f-9796-43d5-a0fb-1ba8e9906a49 creating container for instance 61f98234-92e3-4e7b-b1e8-200ff3aa081e
   Cell 00dd954f-9796-43d5-a0fb-1ba8e9906a49 successfully created container for instance 61f98234-92e3-4e7b-b1e8-200ff3aa081e
   Downloading app package...
   Downloaded app package (1.2M)
   -----> Java Buildpack 380fabd | https://github.com/cloudfoundry/java-buildpack.git#380fabd
   -----> Downloading Jvmkill Agent 1.16.0_RELEASE from https://java-buildpack.cloudfoundry.org/jvmkill/bionic/x86_64/jvmkill-1.16.0-RELEASE.so (0.0s)
   -----> Downloading Open Jdk JRE 1.8.0_242 from https://java-buildpack.cloudfoundry.org/openjdk/bionic/x86_64/openjdk-jre-1.8.0_242-bionic.tar.gz (0.9s)
          JVM DNS caching disabled in lieu of BOSH DNS caching
   -----> Downloading Open JDK Like Memory Calculator 3.13.0_RELEASE from https://java-buildpack.cloudfoundry.org/memory-calculator/bionic/x86_64/memory-calculator-3.13.0-RELEASE.tar.gz (0.0s)
          Loaded Classes: 8132, Threads: 250
   -----> Downloading Client Certificate Mapper 1.11.0_RELEASE from https://java-buildpack.cloudfoundry.org/client-certificate-mapper/client-certificate-mapper-1.11.0-RELEASE.jar (0.0s)
   -----> Downloading Container Security Provider 1.16.0_RELEASE from https://java-buildpack.cloudfoundry.org/container-security-provider/container-security-provider-1.16.0-RELEASE.jar (0.0s)
   -----> Downloading Spring Boot CLI 2.2.5_RELEASE from https://java-buildpack.cloudfoundry.org/spring-boot-cli/spring-boot-cli-2.2.5-RELEASE.tar.gz (0.5s)
          Expanding Spring Boot CLI to .java-buildpack/spring_boot_cli (0.1s)
   Exit status 0
   Uploading droplet, build artifacts cache...
   Uploading droplet...
   Uploading build artifacts cache...
   Uploaded build artifacts cache (51.2M)
   Uploaded droplet (52.7M)
   Uploading complete
   Cell 00dd954f-9796-43d5-a0fb-1ba8e9906a49 stopping instance 61f98234-92e3-4e7b-b1e8-200ff3aa081e
   Cell 00dd954f-9796-43d5-a0fb-1ba8e9906a49 destroying container for instance 61f98234-92e3-4e7b-b1e8-200ff3aa081e
   Cell 00dd954f-9796-43d5-a0fb-1ba8e9906a49 successfully destroyed container for instance 61f98234-92e3-4e7b-b1e8-200ff3aa081e

Waiting for app to start...

name:              cf-demo
requested state:   started
routes:            cf-demo-bright-koala-jt.cfapps.io
last uploaded:     Tue 17 Mar 20:15:20 EDT 2020
stack:             cflinuxfs3
buildpacks:        https://github.com/cloudfoundry/java-buildpack.git

type:            web
instances:       1/1
memory usage:    768M
start command:   JAVA_OPTS="-agentpath:$PWD/.java-buildpack/open_jdk_jre/bin/jvmkill-1.16.0_RELEASE=printHeapHistogram=1 -Djava.io.tmpdir=$TMPDIR -XX:ActiveProcessorCount=$(nproc)
                 -Djava.ext.dirs=$PWD/.java-buildpack/container_security_provider:$PWD/.java-buildpack/open_jdk_jre/lib/ext -Djava.security.properties=$PWD/.java-buildpack/java_security/java.security
                 $JAVA_OPTS" && CALCULATED_MEMORY=$($PWD/.java-buildpack/open_jdk_jre/bin/java-buildpack-memory-calculator-3.13.0_RELEASE -totMemory=$MEMORY_LIMIT -loadedClasses=8328 -poolType=metaspace
                 -stackThreads=250 -vmOptions="$JAVA_OPTS") && echo JVM Memory Configuration: $CALCULATED_MEMORY && JAVA_OPTS="$JAVA_OPTS $CALCULATED_MEMORY" && MALLOC_ARENA_MAX=2 JAVA_OPTS=$JAVA_OPTS
                 SERVER_PORT=$PORT JAVA_HOME=$PWD/.java-buildpack/open_jdk_jre exec $PWD/.java-buildpack/spring_boot_cli/bin/spring run -cp
                 $PWD/.java-buildpack/client_certificate_mapper/client_certificate_mapper-1.11.0_RELEASE.jar app.groovy
     state     since                  cpu      memory           disk           details
#0   running   2020-03-18T00:16:02Z   116.6%   142.1M of 768M   147.2M of 1G   

welcome@welcome-Inspiron-5558:~/cloudFoundry_pivotal/cf-sample-app-spring-master$ 

```
