# Install ruby

On shell:

```sh
sudo apt-get install ruby-full build-essential zlib1g-dev
```

## Set a local gem env

On bash:

```sh
echo '# Install Ruby Gems to ~/.gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/.gems"' >> ~/.bashrc
echo 'export PATH="$HOME/.gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```


## Set gem env

Your global (system-wide) config file probably has the --no-user-install flag set. 

Create/edit your local `~/.gemrc` file and append the following line(s):

```
:gemdir:
    - ~/.gem/ruby
install: --user-install
```

## Install Jekyll

```sh
gem install jekyll bundler
```

and then:

```
jekyll server
```