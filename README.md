py-utorrent
=============
uTorrent WEB UI API Client Library written in Python


usage:

```
from utorrent.client import UTorrentClient

base_url = 'http://127.0.0.1:7070/gui/'
username = 'admin'
password = '123123'
client = UTorrentClient(base_url, username, password)


filename = 'test_utorrent'
filepath = r'E:\py-utorrent-master\py-utorrent-master\1.torrent'
# filename is useless, can not set download dir, that's why I add addfile2
client.addfile(filename, filepath)


filepath = r'E:\py-utorrent-master\py-utorrent-master\1.torrent'
dowload_dir = 1 # E:\
sub_dir = 'test_utorrent'
# must add dowload_dir to utorrent at first, it is an option at webui with value (1,2,3 ....)
client.addtorrent(torrent_path, dowload_dir, sub_dir)
```