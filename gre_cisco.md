# Cisco GRE Tunnel configuration

###### GRE tunnel sample configuration between three routers(R1, R2, R3).

## Architecture diagram
![architecture diagram](/../addons/network_diagram_gre.png)

### Basic routers configuration

| Command | Description |
| ------------- | ------------- |
| `enable`  | Content Cell  |
| `conf t`  | Set configuration mode  |
| `hostname <hostname>`  | Set hostname  |
| `int <interface name>`  | Set interfaces for ex. fastethernet0/0 or loopback1|
| `no shutdown`  | Up interface  |
| `ip address <ip-address> <mask>`  | Assgn ip-address to interface  |
| `do copy r s`  | Save configuration |

### GRE configuration

| Command | Description |
| ------------- | ------------- |
| `enable`  | Content Cell  |
| `conf t`  | Set configuration mode  |
| `int tunnel <number>`  | Create tunnel interface  |
| `no shutdown`  | Up interface  |
| `ip address <ip-address> <mask>`  | Assgn ip-address to interface  |
| `tunnel source`  | Set tunnel source address  |
| `tunnel destination`  | Set tunnel destination address  |
| `do copy r s`  | Save configuration |




