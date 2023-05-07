# homeMediaServer
To use reverse proxy you need set up base path in services settings:

| Service | Path to config | Change it | Change to |
| ------- | ------- | ------- | ------- |
| Jackett | ```jackett/Jackett/ServerConfig.json``` | "BasePathOverride": "", | "BasePathOverride": "/jackett", |
| Sonarr | ```sonarr/config.xml``` | ````<UrlBase></UrlBase>```` | ```<UrlBase>/sonarr</UrlBase>``` |
| Radarr | ```radarr/config.xml``` | ```<UrlBase></UrlBase>``` | ```<UrlBase>/radarr</UrlBase>``` |
| Lidarr | ```lidarr/config.xml``` | ```<UrlBase></UrlBase>``` | ```<UrlBase>/lidarr</UrlBase>``` |
| Readarr | ```readar/config.xml``` | ```<UrlBase></UrlBase>``` | ```<UrlBase>/readarr</UrlBase>``` |
| qBitTorrent | ```qbittorrent/qBittorrent/qBittorrent.conf``` | WebUI\TrustedReverseProxiesList= |WebUI\TrustedReverseProxiesList=* |

qBitTorrent settings:
+ Port used for incoming connections: 6882
+ And you can set up where qBit will download file:
+ + Default Save Path
+ + Keep incomplete torrents in
+ + Copy .torrent files to
+ + Copy .torrent files for finished downloads to

Add vpn config to ```./vpn/wireguard```