#docker buildx build --platform linux/amd64,linux/arm64 --push -t samychbinou/docker-stress:tagtest .
#time docker run --env timeout=5s samychbinou/docker-stress:tagtest

FROM ubuntu:18.04
RUN apt-get update && apt-get install -y stress-ng=0.09.25-1
WORKDIR /
COPY joblist.txt .
CMD ["/bin/sh", "-c" , "stress-ng --job joblist.txt"]
