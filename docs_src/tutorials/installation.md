# Installation & compilation
## Compile scaphandre from source

We recommand using this version of the rust toolchain or later:

    cargo --version
    cargo 1.48.0 (65cbdd2dc 2020-10-14)
    rustc --version
    rustc 1.48.0 (7eac88abb 2020-11-16)

To be sure to be up to date, you may install rust from the [official website](https://www.rust-lang.org/) instead of your package manager.

To hack *scaph*, or simply be up to date with latest developments, you can download scaphandre from the main branch:

    git clone https://github.com/hubblo-org/scaphandre.git
    cd scaphandre
    cargo build # binary path is target/debug/scaphandre

To use the latest code for a true use case, build for release instead of debug:

    cargo build --release

Binary path is `target/release/scaphandre`.
## More to come

More tutorials to come, for a proper installation, like:

- install scaphandre as a proper systemd service
- scaphandre in your favorite GNU/Linux distribution (package creators)
- run scaphandre in a container
- run scaphandre on kubernetes
- scaphandre on MacOSX
- and more...
