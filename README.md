### Install On Ubuntu 20.04

#### Install openvpn 

`wget https://git.io/vpn -O openvpn-install.sh && bash openvpn-install.sh`

#### Change the configuration to login mutiuser with one config

```
vim /etc/openvpn/server/server.conf

Add duplicate-cn at the end of the config
```

#### Install dynamic dns client no-ip to avoid ip address ban (Optional)

```
wget http://www.no-ip.com/client/linux/noip-duc-linux.tar.gz

tar -xvf noip-duc-linux.tar.gz

cd noip-2.1.9-1/

make

make install
```

#### Install obfs4proxy to bypass DPI(Optional)

```
apt install obfs4proxy
mkdir -p /var/lib/tor/pt_state/obfs4/
cp obfs4.config /var/lib/tor/pt_state/obfs4/
cp obfs4proxy.service /etc/systemd/system/
```

### Cost

| Provider      | Cost 			|
| -----------   | -----------	|
| Digital Ocean | $5			|
| Vultr			| $3.5			|
| AWS LightSail | $3.5			|
| LinNode		| $5			|

### Tested Client

| Platform		| Client 		|
| ____________	| ____________	|
| Windows 		| obfsproxy+openvpn client|
| Linux 		| obfsproxy+openvpn client|
| Android 		| VPN Client Pro		  |
| OSX			| ?						|
| IOS			| ?						|


