**New: [wireguard-install](https://github.com/Nyr/wireguard-install) is also available.**

## openvpn-install
OpenVPN [road warrior](http://en.wikipedia.org/wiki/Road_warrior_%28computing%29) installer for Ubuntu, Debian, CentOS and Fedora.

This script will let you set up your own VPN server in no more than a minute, even if you haven't used OpenVPN before. It has been designed to be as unobtrusive and universal as possible.

### I want to run my own VPN but don't have a server for that
You can get a VPS from just $1/month at [VirMach](https://billing.virmach.com/aff.php?aff=4109&url=billing.virmach.com/cart.php?gid=18).

### Donations

If you want to show your appreciation, you can donate via [PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=VBAYDL34Z7J6L) or [cryptocurrency](https://pastebin.com/raw/M2JJpQpC). Thanks!

### Install On Ubuntu 20.04

####Install openvpn 

`wget https://git.io/vpn -O openvpn-install.sh && bash openvpn-install.sh`

####Change the configuration to login mutiuser with one config

```
vim /etc/openvpn/server/server.conf

Add duplicate-cn at the end of the config
```

####Install dynamic dns client no-ip to avoid ip address ban (Optional)

```
wget http://www.no-ip.com/client/linux/noip-duc-linux.tar.gz

tar -xvf noip-duc-linux.tar.gz

cd noip-2.1.9-1/

make

make install
```

####Install obfs4proxy to bypass DPI(Optional)

```
apt install obfs4proxy
mkdir -p /var/lib/tor/pt_state/obfs4/
cp obfs4.config /var/lib/tor/pt_state/obfs4/
cp obfs4proxy.service /etc/systemd/system/
```


