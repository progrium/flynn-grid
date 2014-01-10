# The Grid

The Grid is a distributed, container-based Unix process scheduling framework and service platform. It turns a set of networked hosts into a mostly homogeneous grid of nodes ready to run heterogeneous jobs. It is the "layer 0" of Flynn.

[Read more in the documentation.](http://flynn.viewdocs.io/flynn-grid)

## Development

### Setting up development VM

Get the project and its sub repos:

	$ git clone https://github.com/flynn/flynn-grid
	$ cd flynn-grid
	$ scripts/pull

Install Vagrant and then run:

	$ vagrant up

This will provision a development VM. You can SSH in:

	$ vagrant ssh

Now build the entire project from inside the VM:

	$ build-all

### See it working

The VM acts mostly like a target host, except it has all the development tooling and source ready to play with. In order to start a host as you would a cluster node, for now run:

	$ start-host

This runs the host service (aka lorne), which will bootstrap all the other services needed to be running on a host. These are all run in Docker containers, so you can manage/debug them using Docker commands if you wish.

You can also use the grid CLI tool that was built with the source to work with this one node cluster. It auto-targets localhost, so it should just work:

	$ grid jobs

## License

BSD
