FROM ubuntu:18.04
## CREATE APP USER ##

ARG user=zyy
ARG group=zyy
ARG uid=1000
ARG gid=1000

# Create the home directory for the new user.
RUN mkdir -p /home/${user}

# Create an user so our program doesn't run as root.
RUN groupadd -f --gid ${gid} ${group}
RUN useradd -r -g ${gid} -d /home/${user} -s /bin/bash -u ${uid} -c "Docker image user" ${user}

# Set the home directory to our ygbao user's home.
ENV HOME=/home/${user}
ENV APP_HOME=/home/${user}/lvna
ENV LD_LIBRARY_PATH=/home/${user}/lvna

## SETTING UP THE APP ##
WORKDIR $APP_HOME

# Change to the user.
USER ${user}
