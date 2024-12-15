
FROM ubuntu:20.04


RUN apt-get update && \
    apt-get install -y ansible git sshpass && \
    apt-get clean


WORKDIR /ansible


# Configure Git to treat the directory as safe
RUN git config --global --add safe.directory /ansible/sync

# Copy required files into the container
COPY sync_git.yml inventory /ansible/

# Default command (will be overridden by `entrypoint` in `docker-compose.yml`)
CMD [ "ansible-playbook", "-i", "inventory", "sync_git.yml" ]
