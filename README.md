docker network create polly-bridge
docker build -f Dockerfile -t pollyfrontend .

docker create --network polly-bridge --name pollyfrontendcontainer -p 3000:3000 pollyfrontend

docker start pollyfrontendcontainer