## osuapiproxy
## A simple osu!api proxy for local ripple servers
If you are running a ripple server locally and you want to use our new score server (which isn't ready yet) with osu!api features, you'll need this.  
If you are redirecting every connection from `osu.ppy.sh` to `127.0.0.1` with hosts file/switcher, you won't be able to access osu!api. To fix this problem, host this simple proxy script on a server and set your api url to the proxy one, so every api call from your ripple server gets redirected to the proxy, the proxy sends your request to `osu.ppy.sh`, it gets the response and it sends it back to you.  

## Installation
You need **python3**, tornado and requests:
```
$ pip install tornado
$ pip install requests
```
To start the server on port **5003**, run this command:
```
$ python3 osuapiproxy.py
```
If you want to use a different port, use `-p` argument, for example:
```
$ python3 osuapiproxy.py -p 1337
```
This will run the proxy on port **1337**

## License
All code in this repository is licensed under the GNU AGPL 3 License.  
See the "LICENSE" file for more information.
