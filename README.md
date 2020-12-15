# What is xmr-node-proxy 

[xmr-node-proxy](https://github.com/MoneroOcean/xmr-node-proxy) is a multi-algorithm protocol proxy. xmr-node-proxy is written in node and is extremely lightweight. It can easily be deployed on an AWS T2.Micro instance and handle up to 2000 connections. 

## How to use this image


- Launch a container:

    In order to function, the proxy needs a [`config.json`](https://github.com/moneroocean/xmr-node-proxy/blob/master/config_example.json) file properly configure and present in its app directory. 

    - Create the appropriate `config.json` file
    - Launch a container with the previously created config file

            docker container run -v $(pwd)/config.json:/app/config.json -p PORT:PORT \
            [-p PORTn:PORTn] --name proxy -d mattvirus/xmr-node-proxy

        **Where:** PORT is the port you configured in your `config.json` in the `listeningPorts` object. If you have multiple ports simply add as many `-p PORT:PORT` parameters as needed.

- Check the logs:

        docker container logs -f proxy


## Donations

Nope.
