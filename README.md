# heady

First, create a "data volume". In the following example, I named this source
"jenkins". From the subsequent management, I will be referring to this
container.

docker run -v /jenkins -name jenkins busybox true

We then import our jenkins job by linking the volume to a tar command

tar -c jobs/*/config.xml | docker run -a stdin -i --volumes-from jenkins busybox tar -xC /jenkins

Now that the Jenkins workspace is pre-populated, the same volume can be referred
to when launching a container.

docker run --volumes-from jenkins -d manishmore14/jenkins
