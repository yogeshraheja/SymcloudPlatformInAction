# Kubernetes_Demo_for_Voting_App

- Python webapp which allow you to vote with two options "Thumb up OR Thumb down"
- Redis queue which collects new votes
- .NET worker which consumes votes and stores them in the DB (Postgres)
- Postgres database backed by a Persistent Volume (NFS) and Persistent Volume Claim
- Node.js webapp which shows the results of the voting in real time

## Step1:
=====

### Deploy K8s application:
=======================
- Clone the repository "git clone https://github.com/yogeshraheja/SymcloudPlatformInAction.git"
- cd SymcloudPlatformInAction/KubernetesAppDemo
- kubectl apply -f .

## Step2:
=====

### Verify K8s objects:
===================

- kubectl get namespaces
- kubectl get deployment -n symcloudinaction
- kubectl get replicasets -n symcloudinaction
- kubectl get pods -n symcloudinaction
- kubectl get services -n symcloudinaction
- kubectl get secrets -n symcloudinaction
- kubectl get configmaps -n symcloudinaction
- kubectl get persistentvolumes -n symcloudinaction
- kubectl get persistentvolumeclaims -n symcloudinaction

## Step3:
=====

### Access Voting app and test its functionality

