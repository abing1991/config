###How To Use Shadowsocks Client For Proxy

####Shadowsocks 

- install 

```
sudo apt-get install python-pip
sudo pip install shwdowsocks
```

- config : create file named shadowsocks.json and insert follow conents.
```
{
    "server":"remote-shadowsocks-server-ip-addr",
    "server_port":443,
    "local_address":"127.0.0.1",
    "local_port":1080,
    "password":"your-passwd",
    "timeout":300,
    "method":"chacha20-ietf",
    "fast_open":false,
    "workers":1
}
```

- start 

```
sudo sslocal -c shadowsocks.json -d start 

```

####privoxy

- install privoxy 

```
sudo apt-get install privoxy
```

- config append 

```
forward-socks5 / 127.0.0.1:1080 .

```
