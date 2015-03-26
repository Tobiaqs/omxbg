# omxbg
Lil' script that helps you run OMXPlayer in the background. It's meant to work with audio streams, but it could probably work with videos as well.

### Installation
```
# apt-get update && apt-get install -y omxplayer
```
```
# bash -c '$(P="/usr/local/bin/omxbg"; wget -O "$P" https://raw.githubusercontent.com/Tobiaqs/omxbg/master/omxbg && chmod +x "$P")'
```

### Usage
```
$ omxbg [--wait] [--omxplayer-option] file

--wait: Don't go into background.
```

### Examples
```
# No options
$ omxbg http://pub2.di.fm/di_trance
345
```
```
# Don't go into background
$ omxbg --wait http://pub2.di.fm/di_trance
```
```
# HW audio decoding, output to HDMI
$ omxbg -w -o hdmi http://pub2.di.fm/di_trance
345
```
```
# Kill
$ pkill -P 345
```

Tip: In order for OMX to work at all, make sure your user is member of the audio group.

```
# usermod -a -G audio tobias
