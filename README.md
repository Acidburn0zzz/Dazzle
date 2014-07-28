# Dazzle, SparkleShare host setup script

An easier and less error prone way to set up a SparkleShare host.
Created to work on Debian and Red Hat based systems.

# Note on this fork:

This fork adds compatibility for FreeBSD & OpenBSD systems, and is based 
on a patch written by aXon (https://github.com/aXon/Dazzle). I made some 
improvements to his work and patched it against upstream master. I will
probably support this as long as my servers stay on the BSD's. =)

# Note for BSD users:

Before using this program, you are required to have installed bash. 

## Usage

Usage (as root):

    # Get Dazzle
    curl https://raw.github.com/hbons/Dazzle/master/dazzle.sh \
        --output /usr/local/bin/dazzle
    
    # Initial Dazzle setup
    chmod +x /usr/local/bin/dazzle
    dazzle setup

    # Link a SparkleShare client
    dazzle link

    # Create a new project
    dazzle create PROJECT_NAME


## Configuration

You can control almost all configuration options via environment variables:

    export DAZZLE_USER=dazzle
    export DAZZLE_HOME=/var/lib/stuff
    sudo dazzle setup

Available options are the following:

* DAZZLE_USER: the Dazzle user. Defaults to "storage".
* DAZZLE_GROUP: the Dazzle group. Defaults to "storage".
* DAZZLE_HOME: the directory used to store projects. Defaults to "/home/storage".
