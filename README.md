# dockerization-firefox-mac


## Setup XQuartz
1. Install XQuartz
`brew install xquartz`
2. Launch XQuartz.  Under the XQuartz menu, select Preferences
3. Go to the security tab and ensure "Allow connections from network clients" is checked.
4. _Restart XQuartz_.
5. (optional) Add to path `/opt/X11/bin`
6. Execute `xhost +` or  `/opt/X11/bin/xhost +`

## Starutp
Build docker `docker build --build-arg version=60.8.0esr -t firefox .`
** default version=60.0

Run docker `docker run -e DISPLAY=host.docker.internal:0 firefox`

IP_HOST = 192.168.65.2

** List releases firefox - http://ftp.mozilla.org/pub/firefox/releases/
