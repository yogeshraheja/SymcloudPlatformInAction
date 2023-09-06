# DockerVotingApp

- Python webapp which allow you to vote with two options "Thumb up OR Thumb down"
- Redis queue which collects new votes
- .NET worker which consumes votes and stores them in the DB
- Postgres database backed by a Docker volume
- Node.js webapp which shows the results of the voting in real time

Step1:
=====

User-defined Bridge Network Creation:
=====================================
docker network create --driver=bridge --subnet=192.168.10.0/24 appnet

So its time to create our container inside this network, we need to make sure to put the name for redis container as redis, worker as worker and database as db as the names are hardcoded in the code itself.

Step2:
=====

Container Creation:
===================
docker container run -itd --net=appnet --name=vote -p 81:80 yogeshraheja/thinknyxvote:v2

docker container run -itd --net=appnet --name=redis yogeshraheja/thinknyxredis:v1

docker container run -itd --net=appnet --name=db yogeshraheja/thinknyxdb:v1

docker container run -itd --net=appnet --name=worker yogeshraheja/thinknyxworker:v1

docker container run -itd --net=appnet --name=result -p 82:80 yogeshraheja/thinknyxresult:v2

Now go to browser with your Host IP and access the Vote Front End at port 81 and Result Front End at Port 82.

Note: The images for vote, redis, worker, DB and result are already available publicly on Docker Hub.
