# springzookepper



https://hub.docker.com/_/zookeeper/
docker pull zookeeper

#Start a Zookeeper server instance
docker run --name some-zookeeper --restart always -d zookeeper

Connect to Zookeeper from an application in another Docker container
$ docker run --name some-app --link some-zookeeper:zookeeper -d application-that-uses-zookeeper

Connect to Zookeeper from the Zookeeper command line client
$ docker run -it --rm --link some-zookeeper:zookeeper zookeeper zkCli.sh -server zookeeper
