Blinky for the Blue Pill
************************

Just embedded *Hello, World!*

- `Original blogpost <https://jonathanklimt.de/electronics/programming/embedded-rust/rust-on-stm32-2/>`__

Development
===========

- `Format Rust code <https://github.com/rust-lang/rustfmt>`__

Build
-----

- `Upgrade toolchain <https://stackoverflow.com/questions/69848319/unable-to-specify-edition2021-in-order-to-use-unstable-packages-in-rust>`__ if necessary:

::

    $ rustup default nightly && rustup update

- Useful `magic <https://github.com/rust-lang/rust/issues/91702>`__

::

    $ cargo clean

::

    $ cargo build --release

Format
------

::

    $ cargo fmt

Test
----

::

    TODO

Install
-------

- `A cargo extension for programming microcontrollers <https://github.com/probe-rs/cargo-flash>`__ (*cargo-flash*)

::

    $ cargo install cargo-flash

::

    $ cargo flash --chip stm32f103C8 --release
