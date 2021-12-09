Blinky for the Blue Pill
************************

Just embedded *Hello, World!*

- `Original blogpost <https://jonathanklimt.de/electronics/programming/embedded-rust/rust-on-stm32-2/>`__

Development
===========

- `Format Rust code <https://github.com/rust-lang/rustfmt>`__

Build
-----

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

    $ cargo flash --chip stm32f103C8 --release
