# Kubernetes_Demo_for_Voting_App

- Python webapp which allow you to vote with two options "Thumb up OR Thumb down"
- Redis queue which collects new votes
- .NET worker which consumes votes and stores them in the DB
- Postgres database backed by a Docker volume
- Node.js webapp which shows the results of the voting in real time

Step1:
=====

Deploy K8s application:
=======================
- Clone the repository "git clone https://github.com/yogeshraheja/SymcloudPlatformInAction.git"
- cd SymcloudPlatformInAction/KubernetesAppDemo
- kubectl apply -f .

Step2:
=====

Verify K8s objects:
===================

- kubectl get ns
- kubectl get deployment -n symcloudinaction
- kubectl get rs -n symcloudinaction
- kubectl get pods -n symcloudinaction
- kubectl get svc -n symcloudinaction

Step3:
=====

Access Voting app and test its functionality

