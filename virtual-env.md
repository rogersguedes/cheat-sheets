## Virtual Env

### Installation

Using with Python 2.7

```shell
pip install virtualenv
virtualenv --version
```

Using with Python 3

In python 3, `virtualenv` can installed be installed fom `pip`.

```shell
apt install python3 python3-pip
pip3 install virtualenv
```

### Basic usage

#### Environment Operations

##### Creation

###### Python 2.7

```shell
virtualenv [options] [venv-folder-path]
```

creates a new virtual environment (from now on called virtualenv) in `[venv-folder-path]` folder.

options:

1. `-p <path-to-python-interpreter>`: set the python interpreter binary. Example:

   ```shell
   virtualenv -p /usr/bin/python3.6 venv_test
   ```

2. ..

###### Python 3

```shell
python3 -m venv [venv-folder-path]
```

##### Activation

```shell
source [venv-folder-path]/bin/activate
```

##### Deactivation

```shell
deactivate
```

##### Deletion

Removing a virtual environment is simply done by deactivating it and deleting the environment folder with all its contents:

```shell
deactivate
rm -r [venv-folder-path]
```

### References

1. [docs.python-guide.org - Pipenv & Virtual Environments — The Hitchhiker's Guide to Python](https://docs.python-guide.org/dev/virtualenvs/)