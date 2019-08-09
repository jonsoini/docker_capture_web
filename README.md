About
=======

This is adapted from the original version `mokemokechicken/capture_web`. 

Captures web screenshots with headless Chrome 76 & Selenium.

Tested on macOS Mojave w/ Docker CE 19.03.1, it should work fine elsewhere?

How To Use
=========

```bash
docker run -v `pwd`:/tmp/screenshot jonsoini/capture_web <URL> <output_image.png> [options]
```

or

```bash
./capture <URL> <output_image.png> [options]
```

## Running with arguments
----

### PC
```bash
docker run -v `pwd`:/tmp/screenshot jonsoini/capture_web "https://news.google.com/" google_news.png
```

### iPhone
```bash
docker run -v `pwd`:/tmp/screenshot jonsoini/capture_web "https://news.google.com/" google_news_sp.png -w 414x735 --ua 'Mozilla/5.0 (iPhone; CPU iPhone OS 11_0 like Mac OS X) AppleWebKit/604.1.38 (KHTML, like Gecko) Version/11.0 Mobile/15A372 Safari/604.1'
```

HELP
----

```bash
% docker run -v `pwd`:/tmp/screenshot jonsoini/capture_web
usage: screenshot.py [-h] [-w WINDOW_SIZE] [--ua USER_AGENT] [--wait WAIT]
                     [-v] [--vv]
                     url filename

required arguments:
  url              specify URL
  filename         specify capture image filename

optional arguments:
  -h, --help       show this help message and exit
  -w WINDOW_SIZE   specify window size like 1200x800
  --ua USER_AGENT  specify user-agent
  --wait WAIT      specify wait seconds after scroll
  -v               set LogLevel to INFO
  --vv             set LogLevel to DEBUG
```

How To Build
===========

```bash
./build
```
