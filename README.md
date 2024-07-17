Py-EVM
Py-EVM is an implementation of the Ethereum protocol in Python. It contains the low level primitives for the original proof-of-work (POW), (formerly known as Ethereum 1.0) chain as well as emerging support for the proof-of-stake (POS) (formerly known as Ethereum 2.0) spec.

Goals
Py-EVM aims to eventually become the defacto Python implementation of the Ethereum protocol, enabling a wide array of use cases for both public and private chains.

In particular Py-EVM aims to:

be a reference implementation of the Ethereum POW and POS implementations in one of the most widely used and understood languages, Python.

be easy to understand and modifiable

have clear and simple APIs

come with solid, friendly documentation

deliver the low level primitives to build various clients on top (including full and light clients)

be highly flexible to support both research as well as alternate use cases like private chains.

Quickstart
python -m pip install py-evm
Get started in 5 minutes

Documentation
Check out the documentation on our official website

Developer Setup
If you would like to hack on py-evm, please check out the Snake Charmers Tactical Manual for information on how we do:

Testing
Pull Requests
Documentation
We use pre-commit to maintain consistent code style. Once installed, it will run automatically with every commit. You can also run it manually with make lint. If you need to make a commit that skips the pre-commit checks, you can do so with git commit --no-verify.

Development Environment Setup
git clone git@github.com:ethereum/py-evm.git
cd py-evm
virtualenv -p python3 venv
. venv/bin/activate
python -m pip install -e ".[dev]"
pre-commit install
Release setup
To release a new version:

make release bump=$$VERSION_PART_TO_BUMP$$
To issue the next version in line, specify which part to bump, like make release bump=minor or make release bump=devnum. This is typically done from the main branch, except when releasing a beta (in which case the beta is released from main, and the previous stable branch is released from said branch).

