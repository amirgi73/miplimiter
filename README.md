
# MIPLimiter

Imposing restrictions on the number of IP addresses a user can simultaneously connect from.
Works with latest version of Marzban.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

![Static Badge](https://img.shields.io/badge/works_with-marzban-blue)



## Features

- Supports gozargah/marzban
- Supports Marzban-Node
- Easy on system resources


## License

[MIT](https://choosealicense.com/licenses/mit/)
This software comes with ABSOLUTELY NO WARRANTY.

## Installation

### Add the following to the xray-config.json of your master server
```json
  "log": {
    "access": "",
    "loglevel": "error",
    "dnsLog": false
  }
```

### You need Docker installed on your server

```sh
  curl -fsSL https://get.docker.com | sh
```
### Clone this Repo

```sh
  git clone https://github.com/amirgi73/miplimiter.git
  cd miplimiter
```
### Edit `config.yml` based on your needs

- `url`: domain/subdomain of your Marzban Panel (ie. sub.example.com). Your Panel should have `https` enabled.
- `username`: username of Marzban admin account
- `password`: password of Marzban admin account
In the `users` section you will write username of users, that you want to limit and the number of IPs, that they're allowed. for example `hasan: 2` will limit username `hasan` with only 2 simultaneous IPs.

### Run the app

```sh
docker compose up -d
```



## Usage/Examples

### Checking logs

```sh
cd miplimiter
docker compose logs -f
```
### Stoping the app
```sh
cd miplimiter
docker compose down
```
### Updating the app
```sh
cd miplimiter
docker compose down
docker compose pull
docker compose up -d
```
## Acknowledgements

 - [V2IpLimit Script](https://github.com/houshmand-2005/V2IpLimit/blob/houshmand/Marzban)
 - [Marzban](https://github.com/Gozargah/Marzban)
 


## TO DO
- [ ]  Implementing REST API for adding/removing users to the list
- [ ]  Using a datatbase to store data
