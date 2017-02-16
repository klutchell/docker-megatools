# megatools docker image #

## Description ##

[Ubuntu](https://hub.docker.com/_/ubuntu/) base image with [megatools](https://github.com/megous/megatools) installed from package repo.

## Usage ##
```bash
$ docker run -it --rm -v "$(pwd)":/workdir -w /workdir klutchell/megatools <command> <parameters>
```

### Example: megaput ###
```bash
$ docker run -it --rm -v "$(pwd)":/workdir -w /workdir klutchell/megatools \
megaput \
--username "testuser@email.com" \
--password "topsecret" \
--path "/Root/backups" \
"file/to/upload"
```

### Example: megals ###
```bash
$ docker run -it --rm klutchell/megatools \
megals -hnl --header \
--username "testuser@email.com" \
--password "topsecret" \
"/Root/backups"
```

## Parameters ##

See the [megatools man page](https://megatools.megous.com/man/megatools.html) for available commands and parameters.

Note that only files within current directory and subdirectories will be available.

## Author ##

Kyle Harding <kylemharding@gmail.com>

## Credit ##

I give credit where it's due and would like to give a shoutout to the creators of the utilites/images used in this project:
* [megous](https://github.com/megous/)
