# ActivityWatcher Barrier

## What is it for?
A custom watcher for users using ActivityWatcher together with [Barrier](https://github.com/debauchee/barrier)

Most of the code is borrowed from [ActivityWatch](https://github.com/ActivityWatch/activitywatch), as it doesn't allow for easy extendability, so we are reimplementing aw-watcher-afk functionality and just extending it to monitor the Barrier status.

## Instructions
Needs to run only on Barrier host.

1. Disable default ActivityWatch `aw-watcher-afk`. Easiest way to do so is to increase `aw-watcher-afk` `poll-time` and `timeout` to `999999999`(~10 years in seconds) in [config](https://docs.activitywatch.net/en/latest/configuration.html).
2. Run main.py and optionally add it to your systems autostart

### aw-watcher-afk.toml config example

    [aw-watcher-afk]
    timeout = 180
    poll_time = 5


## Support
Linux support only for now. Feel free to do a PR for your own platform, by copying `your-os.py` from [here](https://github.com/ActivityWatch/aw-watcher-afk/tree/master/aw_watcher_afk) and adding the barrier checking.