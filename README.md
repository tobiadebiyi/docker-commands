# docker-commands

- List all containers (only IDs) `docker ps -aq.`
- Stop all running containers. `docker stop $(docker ps -aq)`
- Remove all containers. `docker rm $(docker ps -aq)`
- Remove all images. `docker rmi $(docker images -q)`
- Remove all untagged images. `docker rmi $(docker images | grep "^<none>" | awk "{print $3}")`

### Aliases 
- alias containerIds='docker ps -aq'
- alias stopContainers='docker stop $(docker ps -aq)'
- alias removeContainers='docker rm $(docker ps -aq)'
- alias removeImages='docker rmi $(docker images -q)'
- alias removeImagesUntagged='docker rmi $(docker images | grep "^<none>" | awk "{print $3}")'
- alias reloadProfile=". ~/.bash_profile"
