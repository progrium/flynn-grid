# The Grid

The Grid is a distributed, container-based Unix process scheduling framework and service platform. It turns a set of networked hosts into a mostly homogeneous grid of nodes ready to run heterogeneous jobs.

[Read more in the documentation.](http://flynn.viewdocs.io/flynn-grid)

## Development

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

## License

BSD
