# bitssh

Run SSH over the [BitWeb DHT](https://github.com/bitwebs/dht)!

### Installation
```
npm install -g @web4/ssh
```

### Usage

On a server or some laptop with ssh-server running run

```sh
bitssh-server
```

This will start announcing the server on the DHT, and will print out the Noise public key of the server.

To connect to the server on another computer simply pass the Noise public key to the `bitssh` command, along with an optional username:

```sh
bitssh ab01f... maf
```

That's it! No more remembering hostnames :D

Bitswarm will do UDP holepunching under the hood, so even if your server is located on a home network it should be accessible.

### Windows RDP

You can also use bitssh with Windows RDP to remotely log in to your windows machines over Bitswarm.

On the machine you want to log in to (make sure you have RDP enabled)

```sh
bitssh-server --rdp
```

Then on another computer somewhere on the internet do

```sh
bitssh --rdp ab0f...
```

And open your favorite RDP client, configure it to connect to localhost over port 3389 (default),
with the Windows username etc.

## License

MIT
