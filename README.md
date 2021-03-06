# Soulseek CLI

[![Build Status](https://travis-ci.org/aeyoll/soulseek-cli.svg?branch=develop)](https://travis-ci.org/aeyoll/soulseek-cli)

A Soulseek Cli client.

Requirements
---

NodeJS >= 14

Installation
---

```sh
npm install -g soulseek-cli
```

Commands
---

### Login

Before being able to search, you need to be logged in.

Usage:
```
soulseek login
```

You will be prompted your Soulseek login and password. Credentials are stored and encrypted in your system keychain.

### Download

Download with required query.

Usage:
```
soulseek download|d [options] [query...]
```

:warning: This command used to be called `search` in versions prior to 0.1.0.

Options:

| Option                    | Description                                                                   |
| ------------------------- | ----------------------------------------------------------------------------- |
| -d --destination <folder> | downloads's destination                                                       |
| -q --quality <quality>    | show only mp3 with a defined quality                                          |
| -m --mode <mode>          | filter the kind of files you want (available: "mp3", "flac", default: "mp3")  |
| -h --help                 | display help for command                                                      |

Examples:

```sh
soulseek download "Your query" # Download in the current folder
soulseek download "Your query" --destination=/path/to/directory # Download in a defined folder (relative or absolute)
soulseek download "Your query" --quality=320 # Filter by quality
soulseek download "Your query" --mode=flac # Filter by file type
```

### Query

Search with required query, but don't download anything. If a result is found, the return code will be 0. Otherwise,
the return code will be 1 (useful for scripting)

Usage:

```
soulseek query|q [options] [query...]
```

Options:

| Option                 | Description                                                                  |
| ---------------------- | ---------------------------------------------------------------------------- |
| -q --quality <quality> | show only mp3 with a defined quality                                         |
| -m --mode <mode>       | filter the kind of files you want (available: "mp3", "flac", default: "mp3") |
| -h --help              | display help for command                                                     |



Contribution
---

See [CONTRIBUTING.md](CONTRIBUTING.md).
