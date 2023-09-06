Creation and application deploymnt using Helm Chart:
====================================================

--> helm create thinknyxapp

-rw-r--r--   1 user1  staff  1878 Sep  6 22:26 values.yaml
-rw-r--r--   1 user1  staff   126 Sep  6 22:27 Chart.yaml
drwxr-xr-x  13 user1  staff   416 Sep  6 22:55 templates
drwxr-xr-x. 2  user1  staff     6 Sep  6 22:27 charts

where: value.yaml is the default file for values (all default values will come here)
where: chart.yaml is the metadata about the chart (details about charts)
templates: is the place where we will have our k8s files (k8s object files with dynamic variables)
charts: is a place where you can put dependent charts for this newly created chart

--> helm lint

--> helm package thinknyxapp
Successfully packaged chart and saved it to: /root/SymcloudPlatformInAction/SymcloudPlatformAppDemo/helmapproach/thinknyxapp-1.0.0.tgz

--> helm install thinknyxapp-v1 thinknyxapp-1.0.0.tgz

--> helm ls

--> helm status thinknyxapp-v1

Test your application using 32000 port for Vote and 32001 port for checking results

--> helm history  thinknyxapp-v1

--> helm uninstall thinknyxapp-v1
