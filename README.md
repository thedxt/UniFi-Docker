# UniFi-Docker
This will spawn everything needed to run a UniFi Network Application in a container including a container for the MongoDB database. Using the [LinuxServer.io UniFi Network Application](https://github.com/linuxserver/docker-unifi-network-application) image and the [official MongoDB](https://github.com/docker-library/mongo) image.

use .env to define your variables

### .env Variables
 - `CONTAINER_NAME` the name of your UniFi stack. There will be two containers spawned.
   - The one with `_CORE` appended to it is the LinuxServer.io UniFi Network Application image.
   - The one with `_DB` appended to it is the official MongoDB image. Currently pinned to version 7.0 as that's the highest UniFi supports.
 - `MONGO_DBNAME` the name of the MongoDB database. The stats DB will have `_stat` appended to it.
 - `MONGO_USER` the database user
 - `MONGO_PASS` the password for the database user
 - `TIME_ZONE` Time Zone for the UniFi Network Application

[More detailed documentation](https://thedxt.ca/2023/12/unifi-network-server-with-docker/)

If you have been running my docker compose file for a while it's possible that you are running MongoDB 4.4. Here are the details for [upgrading the Mongo database from 4.4 to 7.0](https://thedxt.ca/2024/06/unifi-mongodb-upgrade/). The database upgrade is not needed on new installs.
