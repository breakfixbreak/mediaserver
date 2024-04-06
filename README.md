# Media Server Setup

2 docker compose files to create a media server with VPN torrenting.
Nb. This specifically uses NordVPN but can be amended for other providers.

Torrent traffic is over VPN. If the VPN fails then there'll be no more traffic.

## torrent_stack.yaml
Things to edit:
- `TOKEN`
- `CONNECT`
- Volumes

Your `TOKEN` can be found via the NordVPN web portal.

The `CONNECT` value can found from the server list here [here](https://nordvpn.com/servers/tools/).

Add values for the volume as per your set up.

## plex_stack.yaml
Things to edit:
- `PLEX_CLAIM`
- Volumes

Add values for the volume as per your set up. Make the media directory the same as the host save lcoation from the torrent_stack. Media will then save in a location Plex can see, re-scan to update or set up scheduled scans. Maybe pick up a lifetime Plex Pass around Black Friday when it's discounted.
