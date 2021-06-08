juju-kubectl
===========

[![Snap Status](https://build.snapcraft.io/badge/knkski/juju-kubectl.svg)](https://build.snapcraft.io/user/knkski/juju-kubectl)

Juju plugin that makes it easy to run the `kubectl` command for K8s models.


Setup
-----

You can install this plugin with `snap`:

    sudo snap install juju-kubectl --classic --edge

Or if you want to run this plugin from source, clone this repo with

    https://github.com/knkski/juju-kubectl.git
    cd juju-kubectl

You will also need to install the Rust compiler. Instructions can be found at
https://rustup.rs/.


Usage
-----

You can run this plugin with:

    # Installed via snap
    juju kubectl get pods

    # Running from source
    cargo run --bin juju-kubectl get pods

Note that both `cargo` and this plugin can take arguments, so to pass
options or parameters to the underlying `kubectl` command, you will want
to call it like so:

    # Installed via snap
    juju kubectl -- -v=1 get pods

    # Running from source
    cargo run --bin juju-kubectl -- -- -v=1 get pods
