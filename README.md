Instructions
============

# Start Karaf (contains the Package Ingest Service), Fedora, and Samba
$ docker-compose up -d
$ docker exec -ti pis_samba chmod 777 /shared/package-ingest/packages/

Karaf web console is located at: http://localhost:8181/system/console/components/
* karaf:karaf

Fedora repository is located at: http://localhost:8080/fcrepo/rest/

Network drive is exported as: cifs://localhost/shared/
* connect as a guest

docker-machine users
====================
1. Create a docker-machine
$ docker-machine create -d virtualbox --virtualbox-disk-size 40000 --virtualbox-memory "2048" pis

2. Start it
$ docker-machine start pis

3. Update your shell environment to talk to the new docker-machine
$ eval $(docker-machine env pis)

4. Note the IP address of your active docker-machine and use it in place of *localhost* in the above instructions
$ docker-machine ls
