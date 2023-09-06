Creation of Robin Bundle:
=========================

Step1:
=====

mkdir /var/tmp/thinknyxappbundle
cd /var/tmp/thinknyxappbundle
mkdir scripts icons sources
touch manifest.yaml (check the manifest file in the repository)
ls -lrt

Step2:
======

Create a tar file of these files & directories "cd /var/tmp/thinknyxappbundle && tar -cvzf thinknyxappbundle.tar.gz *"

Step3:
=====

Upload and List your robin bundle

robin bundle add thinknyxappbundle 1.0.0 thinknyxappbundle.tar.gz
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
