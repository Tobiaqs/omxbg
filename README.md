# omxbg
Lil' script that helps you run OMXPlayer in the background. It's meant to work with audio streams, but it could probably work with videos as well.

### Installation
```
$ sudo bash -c '$(P="/usr/local/bin/omxbg"; wget -O "$P" https://raw.githubusercontent.com/Tobiaqs/omxbg/master/omxbg && chmod +x "$P")'
```

### Usage
```
# No options
$ omxbg http://pub2.di.fm/di_trance
345
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
$ sudo usermod -a -G audio tobias
