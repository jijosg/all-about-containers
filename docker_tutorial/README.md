# Docker demo

## Build the docker image
```bash
./build.sh
```

## List the docker image
```bash
docker images | grep -i quokka
```

## Run the docker image
```bash
docker run -d quokka:1.0 
```

## Check exposed ports
```bash
docker ps -a
```

## Stop existing container
```bash
docker ps --filter 'ancestor=quokka:1.0' --format '{{.Names}}' | xargs docker stop
```

## Run by exposing the port
```bash
docker run -d -p 8088:80 quokka:1.0 
```
