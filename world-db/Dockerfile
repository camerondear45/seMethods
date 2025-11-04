# Use the latest MySQL image
FROM mysql/mysql-server:latest
# Set the working directory
WORKDIR /tmp
# Copy all the files to the working directory of the container
COPY world-db/*.sql /docker-entrypoint-initdb.d
COPY world-db/*.dump /docker-entrypoint-initdb.d
# Copy the main SQL file to docker-entrypoint-initdb.d.
# Scripts and SQL files in this folder are executed on container startup.
# This is specific to MySQL.
# Set the root password
ENV MYSQL_ROOT_PASSWORD my-secret-pw
ENV MYSQL_ROOT_HOST='%'