FROM shinezyy/ubuntu-18.04:gem5-dep
## CREATE APP USER ##

# Create the home directory for the new ygbao user.
RUN mkdir -p /home/ygbao

# Create an ygbao user so our program doesn't run as root.
RUN useradd -r -g users -d /home/ygbao -s /bin/bash -u 795 -c "Docker image user" ygbao

# Set the home directory to our ygbao user's home.
ENV HOME=/home/ygbao
ENV APP_HOME=/home/ygbao/gem5

## SETTING UP THE APP ##
WORKDIR $APP_HOME

# Change to the ygbao user.
USER ygbao
