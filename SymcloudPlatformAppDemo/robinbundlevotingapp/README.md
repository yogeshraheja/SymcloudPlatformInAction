Creation of Robin Bundle for Voting App:
=======================================

Step1:
=====

mkdir /var/tmp/votingapp
cd /var/tmp/votingapp
mkdir scripts icons sources
touch manifest.yaml (check the manifest file in the repository)
ls -lrt
cd scripts
mkdir k8s
cd k8s
mkdir pre
cd pre
And put Redis, Worker and DB yaml files for K8S objects here

Note: Thinknyx logo downloaded in icons directory from "https://upload.wikimedia.org/wikipedia/commons/e/e3/Thinknyx.png"

Step2:
======

Create a tar file of these files & directories "cd /var/tmp/votingapp && tar -cvzf votingapp.tar.gz *"

Step3:
=====

Upload and List your robin bundle

robin bundle add votingapp 1.0.0 votingapp.tar.gz
robin bundle list

Step4:
======

Deploy your application using CLI or GUI

Go to Robin Dashboard, click on applications --> bundles and you will see your uploaded bundle there, click on that and fill in the required information like:

- application name
- resource pool
- CPU
- Memory
- PDV's

Once done click on provision application, you can check your deployed application under "applications" section

Go to browser give a vote and verify if its getting reflected in the result UI
