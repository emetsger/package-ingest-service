Instructions
============

# Start Karaf (contains the Package Ingest Service), Fedora, and Samba
$ docker-compose up -d

Karaf web console is located at: http://localhost:8181/system/console/components/
* admin:admin
Fedora repository is located at: http://localhost:8080/fcrepo/rest/
Network drive is exported as: cifs://localhost/shared/
* connect as a guest
