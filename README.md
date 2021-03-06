# 24chevres.com

Website of 24chevres.com

24chevres.com is a domain name with a great potential. Every idea is welcomed and every one can contribute.

[![Build Status](https://travis-ci.org/24chevres/24chevres.com.svg?branch=master)](https://travis-ci.org/24chevres/24chevres.com)

## How to contribute ?

  - fork the project
  - do some crazy shit and propose a pull request
  - folks in 24chevres organization will vote the PR (with :+1: and :-1: on the PR's description)
  - prefix the PR's description with `[RDY]` when the PR is ready to be merged
  - wait 24 hours after the last commit
  - if vote result is positive, the PR will be merged
  - code is then automatically deployed upon merge

## HTTP Live Server

In order to test your modification locally, we use `live-server`:

```sh
npm install
npm start
```

If you encounter the error *ENOSPC* try the following:

  - Debian:
```sh
echo fs.inotify.max_user_watches=582222 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
```

  - ArchLinux:
```sh
echo fs.inotify.max_user_watches=524288 | sudo tee /etc/sysctl.d/40-max-user-watches.conf && sudo sysctl --system
```

Listen uses inotify by default on Linux to monitor directories for changes. It's not uncommon to encounter a system limit on the number of files you can monitor. For example, Ubuntu Lucid's (64bit) inotify limit is set to 8192. [Source](https://github.com/guard/listen/wiki/Increasing-the-amount-of-inotify-watchers)

