Use native kubernetes commands (kubectl) to deploy your applications

Steps:
======

- Create a namespace "kubectl create ns thinknyxns"

- Create a deployment using yogeshraheja/devopsinaction:v1 image "kubectl create deployment thinknyxdep --image=yogeshraheja/devopsinaction:v1 -n thinknyxns"

- List the objects in thinknyxns namespace "kubectl get all -n thinknyxns"

- Expose your application by creating a service "kubectl expose deployment conftestdep --port=80 --protocol=TCP --target-port=80 --name=conftestdepsvc --type=NodePort -n thinknyxns"

- List the objects in thinknyxns namespace "kubectl get all -n thinknyxns"

- Check the expose port (range of 30000-32767) and check your application on browser "ip:<nodeport_number"
