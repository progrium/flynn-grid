# Getting Started with The Grid

## Setting up your first host

The only pre-requisite for turning a Linux host into a Grid node is Docker to be installed. Once you have this, download The Grid node container with the Docker command:

	$ docker pull flynn/thegrid

Normally you'll want to start The Grid on boot using Upstart or Systemd, but for now we'll run it by hand. We just need to know the external IP of this host. 

	$ docker run -v /var/run/:/docker flynn/thegrid 10.0.0.1

This will configure and start up the components of The Grid. You now have a single host grid!

## Setting up more hosts

Further hosts are set up the exact same way, except that you need to point them to an existing node of the grid. We might as well use the first host. 

	$ docker run -v /var/run/:/docker flynn/thegrid 10.0.0.2 10.0.0.1


gridutil 