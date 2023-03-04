#docker buildx build --platform linux/amd64,linux/arm64 --push -t samychbinou/docker-stress:tagtest .
#time docker run --env timeout=5s samychbinou/docker-stress:tagtest

FROM ubuntu:18.04
RUN apt update && apt install -y stress-ng
COPY joblist.txt .
CMD ["/bin/sh", "-c" , "stress-ng --job joblist.txt"]
