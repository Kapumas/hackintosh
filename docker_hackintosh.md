# Introduction

Docker.app will complain about incompatible processor, so we will use Docker Machine.

# Instalation

Download Docker for Mac (Docker.app). It contains some binaries that are necessary.

```bash
brew install virtualbox docker-machine

# Normally, those links are created automatically by running Docker.app,
# but it quits on us too early, so we need to do this manually
ln -s "/Applications/Docker.app/Contents//Resources/bin/docker-compose" /usr/local/bin/docker-compose
ln -s "/Applications/Docker.app/Contents//Resources/bin/docker-credential-desktop" /usr/local/bin/docker-credential-desktop
ln -s "/Applications/Docker.app/Contents//Resources/bin/docker-credential-osxkeychain" /usr/local/bin/docker-credential-osxkeychain
```

You can also use `brew` to install `docker` and `doccker-compose` and it should work without linking above.

# Running

```bash
docker-machine create
eval $(docker-machine env)
docker run hello-world
docker-compose up
```
