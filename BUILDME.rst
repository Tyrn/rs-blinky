Blinky for the Blue Pill
************************

Just embedded *Hello, World!*

- `Original blogpost <https://jonathanklimt.de/electronics/programming/embedded-rust/rust-on-stm32-2/>`__

Development
===========

- `Format Rust code <https://github.com/rust-lang/rustfmt>`__
- Issue loading binary onto stm32f3discovery `#43 <https://github.com/rust-embedded/book/issues/43>`__

Build
-----

- `Upgrade toolchain <https://stackoverflow.com/questions/69848319/unable-to-specify-edition2021-in-order-to-use-unstable-packages-in-rust>`__ if necessary:

::

    $ rustup default nightly && rustup update

- Extend the toolchain, if necessary:

::

    $ rustup component add rustfmt
    $ cargo install cargo-generate
    $ cargo install cargo-binutils
    $ rustup component add llvm-tools-preview

- Check available targets:

::

    $ rustup target list

- Add a target, if necessary:

::

    $ rustup target add thumbv7m-none-eabi

- Useful `magic <https://github.com/rust-lang/rust/issues/91702>`__

::

    $ cargo clean

::

    $ cargo build --release

- Check:

::

    $ cargo readobj --bin <name> -- --file-headers
    $ cargo size --bin <name> --release -- -A

- Disassemble:

::

    $ cargo objdump --bin app --release -- --disassemble --no-show-raw-insn --print-imm-hex

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
    $ cargo flash --list-chips

::

    $ cargo flash --chip stm32f103C8 --release
