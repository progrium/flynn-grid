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

## Flynn 

[Flynn](https://flynn.io) is a modular, open source Platform as a Service (PaaS). 

If you're new to Flynn, start [here](https://github.com/flynn/flynn).

### Status

Flynn is in active development and **currently unsuitable for production** use. 

Users are encouraged to experiment with Flynn but should assume there are stability, security, and performance weaknesses throughout the project. This warning will be removed when Flynn is ready for production use.

Please report bugs as issues on the appropriate repository. If you have a general question or don't know which repo to use, report them [here](https://github.com/flynn/flynn/issues).

## Contributing

We welcome and encourage community contributions to Flynn.

Since the project is still unstable, there are specific priorities for development. Pull requests that do not address these priorities will not be accepted until Flynn is production ready.

Please familiarize yourself with the [Contribution Guidelines](https://flynn.io/docs/contributing) and [Project Roadmap](https://flynn.io/docs/roadmap) before contributing.

There are many ways to help Flynn besides contributing code:

 - Fix bugs or file issues
 - Improve the [documentation](https://github.com/flynn/flynn.io) including this website
 - [Contribute](https://flynn.io/#sponsor) financially to support core development

Flynn is a [trademark](https://flynn.io/docs/trademark-guidelines) of Apollic Software, LLC.
