# OSX 10.8.x

## Package Management

### Homebrew

`ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"`

## Python

### PIP

`sudo easy_install pip`

### Virtual Environments

    sudo pip install virtualenv

    sudo pip install virtualenvwrapper

    cd $HOME

    mkdir .virtualenvs

Add `source /usr/local/bin/virtualenvwrapper.sh` to your .bash_profile file

## Postgres

### Via Homebrew

    brew install postgres

If brew fails to link you may have to change permission on some files. Run `brew doctor` to see what failed. If brew couldn't write to a folder run `sudo chown -R $USER /path/to/folder/`. Rerun the link process for Postgres, `brew link postgres`. Repeat as necessary.

    initdb /usr/local/var/postgres -E utf8

Add `export PATH=/usr/local/bin:$PATH` to your .bash_profile file

Run Postgres Server: `postgres -D /usr/local/var/postgres/`
