Create the review-troubleshoot project
$ oc new-project review-troubleshoot
## create the hello-world-nginx deployment##
 $ oc new-app --name hello-world-nginx > https://github.com/RedHatTraining/DO280-apps  --context-dir hello-world-nginx

![application created 1](https://github.com/Aml286/openshift-labs-projects/assets/124487792/d0878dc9-26a3-4ac5-a673-317961fbb4f8)
##Create a route to the application by exposing the hello-world-nginx service##
![creATE ROUT FOR HELLO](https://github.com/Aml286/openshift-labs-projects/assets/124487792/8647de4c-9d2d-417a-a546-b6228be0ed6a)

Set the hostname to hello-world.apps.ocp4.example.com.
 $oc expose service hello-world-nginx >  --hostname hello-world.apps.ocp4.example.com
 $ oc get pods
![pods running for hello](https://github.com/Aml286/openshift-labs-projects/assets/124487792/3afc6e70-a81a-4835-9b58-36b0d3bc9c92)

##Verify access to the application.##

 curl -s "http://hello-world.apps.ocp4.example.com"
![verfiy access hello](https://github.com/Aml286/openshift-labs-projects/assets/124487792/89c0f641-6950-49cc-b7e4-e92fd75d7cd3






