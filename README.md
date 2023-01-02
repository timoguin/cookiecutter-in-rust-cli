# cookiecutter-in-rust-cli

Experimenting with embedding Python's cookiecutter CLI and library within a Rust binary.

## Usage

Move to the [rustycookie](rustycookie/) directory with `cd rustycookie`.

Install Rust dependencies:

```shell
cargo install
```

This should give you the `pyoxidizer` CLI tool.

Build the `rustycookie` executable with PyOxidider:

```shell
pyoxider build
```

Run the debug build to see output from the standard Cookiecutter CLI:

```
$ ./build/x86_64-unknown-linux-gnu/debug/install/rustycookie
Usage: python -m cookiecutter.cli [OPTIONS] [TEMPLATE] [EXTRA_CONTEXT]...

  Create a project from a Cookiecutter project template (TEMPLATE).

  Cookiecutter is free and open source software, developed and managed by
  volunteers. If you would like to help out or fund the project, please get in
  touch at https://github.com/cookiecutter/cookiecutter.

Options:
  -V, --version                Show the version and exit.
  --no-input                   Do not prompt for parameters and only use
                               cookiecutter.json file content
  -c, --checkout TEXT          branch, tag or commit to checkout after git
                               clone
  --directory TEXT             Directory within repo that holds
                               cookiecutter.json file for advanced
                               repositories with multi templates in it
  -v, --verbose                Print debug information
  --replay                     Do not prompt for parameters and only use
                               information entered previously
  --replay-file PATH           Use this file for replay instead of the
                               default.
  -f, --overwrite-if-exists    Overwrite the contents of the output directory
                               if it already exists
  -s, --skip-if-file-exists    Skip the files in the corresponding directories
                               if they already exist
  -o, --output-dir PATH        Where to output the generated project dir into
  --config-file PATH           User configuration file
  --default-config             Do not load a config file. Use the defaults
                               instead
  --debug-file PATH            File to be used as a stream for DEBUG logging
  --accept-hooks [yes|ask|no]  Accept pre/post hooks
  -l, --list-installed         List currently installed templates.
  -h, --help                   Show this message and exit.
```
