# debian:jessie docker image with locale set to en_US.UTF-8

This Docker image is to work around an [AppArmor issue with LXC][apparmor-lxc] which affects Docker builds on CircleCI that attempt to change the locale.  You will see this kind of error message:

```
Generating locales...
cannot change mode of new locale archive: No such file or directory
  en_US.UTF-8... failed
Generation complete.
Generating locales...
cannot change mode of new locale archive: No such file or directory
  en_US.UTF-8... failed
Generation complete.
```

The suggested workaround from CircleCI is to create a separate image with the locale already set, so that's what this is.

[apparmor-lxc]: https://bugs.launchpad.net/ubuntu/+source/apparmor/+bug/969299

## License

MIT license.

## Credit

https://github.com/abevoelker/docker-ubuntu-locale
