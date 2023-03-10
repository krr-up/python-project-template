# fillname

This project template is configured to ease collaboration. Linters, formatters,
and actions are already configured and ready to use.

To use the project template, run the `init.py` script to give the project a
name and some metadata. The script can then be removed afterward and the
`setup.cfg` file adjusted.

## Installation

```shell
pip install fillname
```

## Usage

```shell
fillname -h
```

## Development

To improve code quality, we run linters, type checkers, and unit tests. The
tools can be run using [nox]. We recommend installing nox using [pipx] to have
it available globally:

```bash
python -m pip install pipx
python -m pipx install nox
nox
```

Note that `nox --no-install -r` can be used to speed up subsequent runs. It
avoids recreating virtual environments. For example, to run the unit tests
without recreating the corresponding environment and installing packages each
time, you can use

```bash
nox --no-install -rs test
```

Furthermore, we auto format code using [black]. We provide a [pre-commit][pre]
config to automate this process. It can be set up using the following commands:

```bash
python -m pipx install pre-commit
pre-commit install
```

This blackens the source code whenever `git commit` is used.

There is also a format session for nox. It can be run as follows:

```bash
nox -rs format
nox -rs format -- check
```

The latter command can be used to inspect changes before applying them.

[doc]: https://potassco.org/clingo/python-api/current/
[nox]: https://nox.thea.codes/en/stable/index.html
[pipx]: https://pypa.github.io/pipx/
[pre]: https://pre-commit.com/
[black]: https://black.readthedocs.io/en/stable/
