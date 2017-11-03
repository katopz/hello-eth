# Setup `Ethereum` environments
We will do it with `Docker` for faster setup and `npm` for shorter command, feel free to dig in the source for long real command :)

## Prerequisites
> With regular download
- Docker : https://docs.docker.com/engine/installation/#desktop
- NodeJS : https://nodejs.org/en/download/
- Git : https://git-scm.com/downloads
- [Truffle](http://truffleframework.com/) : `npm install -g truffle`

## Optional
- VSCode : https://code.visualstudio.com/download

> Or via command line
```shell
# Install brew
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# Ensure update
brew update && brew upgrade

# Install NodeJS
brew install node

# Install Git
brew install git

# Install Docker
brew cask install docker
brew ls -l /usr/local/bin/docker*

# Optional IDE VSCode
brew cask install visual-studio-code

# Optional for Docker Machine
brew cask install virtualbox
```

## Get the source
```shell
# Pull source code to local
git clone https://github.com/katopz/ethereum-docker.git

# Get in folder
cd ethereum-docker
```

## Setup Ethereum Stacks with Docker Compose
```shell
npm run up
```
