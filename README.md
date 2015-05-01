# Slackboard

Slackboard is a board server for Slack.

## Status

Slackboard is production ready.

## Build

```
make gom
make bundle
make
```

## Configuration

See [CONFIGURATION.md](https://github.com/cubicdaiya/slackboard/blob/master/CONFIGURATION.md) about details.

## Specification

See [SPEC.md](https://github.com/cubicdaiya/slackboard/blob/master/SPEC.md) about details.

## Run

```
slackboard -c conf/slackboard.toml
```

## Client for Slackboard

`slackboard-cli` is a client for `slackboard`. It reads `stdin` and sends a message to `slackboard`.

```
echo message | slackboard-cli -t test -s slackboard-host:29800
```

### Synchronous notification with slackboard-cli

From v0.3.0 `slackboard-cli` sends a notification-request to Slackboard asynchronously by default.
If you want to send a notification-request to Slackboard synchronously, you may add the option `-sync` to `slackboard-cli`.

```
echo message | slackboard-cli -t test -s slackboard-host:29800 -sync
```

## License

Copyright 2014-2015 Tatsuhiko Kubo


Licensed under the MIT License.
