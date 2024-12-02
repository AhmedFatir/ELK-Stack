
# ELK-Stack

## Project Overview
Log Management System Using Elasticsearch, Logstash, and Kibana With Docker.
## For the full explanation of the project, you can check out my [Medium blog](https://medium.com/@afatir.ahmedfatir/elk-stack-deep-dive-complete-guide-using-docker-fbf31aa842a6) for the complete details.

## Key Features
### Elasticsearch
This is the core of the stack, acting as a distributed, RESTful search and analytics engine capable of storing and searching large amounts of data rapidly. It functions like a high-powered database specifically tailored for search and analytics, enabling users to query logs in milliseconds and facilitating immediate identification of issues and trends.

### Logstash
Acting as the data processing pipeline, Logstash can ingest data from various sources, transform it, and then send it to Elasticsearch. It functions like a skilled plumber, capable of handling diverse data sources and formats, ensuring smooth data flow from its origin to its destination.

### Kibana
Serving as the visualization layer of the stack, Kibana enables users to explore and visualize data stored in Elasticsearch. With its powerful dashboard and visualization capabilities, Kibana transforms complex data into actionable insights. It provides a dynamic control panel where users can monitor and analyze data in real time, creating beautiful visualizations and dashboards with ease.

## Installation

### if you don't have docker and docker-compose on your machine
```bash
apt install curl

apt install docker.io

curl -O -J -L https://github.com/docker/compose/releases/download/v2.11.2/docker-compose-linux-x86_64

chmod +x docker-compose-linux-x86_64

cp ./docker-compose-linux-x86_64 /usr/bin/docker-compose
```

### if you already have docker and docker-compose installed on your machine
```bash
git clone https://github.com/AhmedFatir/ELK-Stack.git

cd ./ELK-Stack && make

# And then you can access Kibana through https://localhost:5601/
```
## if you are a 42 student and want to run this project on the school's Mac, you may need to change the path where Docker Desktop on Mac stores its data.
```bash
# Make sure Docker Desktop is not running.

# Use the rsync command to copy the Docker data directory to the new location.
rsync -a ~/Library/Containers/com.docker.docker ~/goinfre/DockerData

# Rename the original directory as a backup, just in case you need to revert(optional).
mv ~/Library/Containers/com.docker.docker ~/Library/Containers/com.docker.docker.backup

# Create a symbolic link from the new location back to the original location.
ln -s ~/goinfre/DockerData/com.docker.docker ~/Library/Containers/com.docker.docker

# Open Docker > Preferences > Resources > File Sharing > Add ~/goinfre to Shared Paths.
```
