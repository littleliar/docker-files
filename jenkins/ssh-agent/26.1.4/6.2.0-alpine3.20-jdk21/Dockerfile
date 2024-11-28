FROM jenkins/ssh-agent:6.2.0-alpine3.20-jdk21@sha256:a663d837aed3115937073a3c19604cfb8898f41fc26c7345d65ce887bf752122

# Copy the docker binary from the official docker image
COPY --from=docker:26.1.4-cli-alpine3.20@sha256:f13cbf1ea352bdbdc825a9233fc56716bdf818e4f608f63280a1aa0b3dc1f2f7 /usr/local/bin/docker /usr/local/bin/docker

# Allow jenkins user to run docker as root due to socket mount permissions
RUN chmod -v a+s $(which docker)