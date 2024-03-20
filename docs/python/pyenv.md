# [Pyenv](https://github.com/pyenv/pyenv)

<br>

## [Installation on Ubuntu](https://www.dedicatedcore.com/blog/install-pyenv-ubuntu/)

#### Step 1: Install and Update Dependencies

```bash
sudo apt update

sudo apt install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
```

#### Step 2: Download Pyenv

```bash
curl https://pyenv.run | bash
```

#### Step 3: Setup Environment

```bash
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n eval "$(pyenv init -)"\nfi' >> ~/.bashrc

exec "$SHELL"
```

<br>

## Basic CLI

#### Check installed python versions

`pyenv versions`

#### Check the list of all available versions

`pyenv install -l`

#### Install additional Python versions

`pyenv install <version>`

#### Uninstall Python versions

`pyenv uninstall <versions>`

#### Switch between Python versions

- `pyenv shell ` -- select just for current shell session
- `pyenv local ` -- automatically select whenever you are in the current directory (or its subdirectories)
- `pyenv global ` -- select globally for your user account

