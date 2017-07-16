# Overload-DoS

This a very powerful denial of service (DDoS) program. It is very efficient and portable, it is stable and useful for stress-testing companies, it currently has three attack methods. 1) SYN/ICMP with 6 flags including fin, syn, rst, ack, psh and urg. 2) Slowloris/SLOW uses sock.connect to attack. 3) Request/Requester uses httplib to attack
## Getting Started

You will need a few diffrent modules installed to execute Overload.

### Modules

You will have to use pip to install the modules, colorama, termcolor & requests
```
sudo apt-get install python-pip
```
```
sudo yum install python-pip
```
### Module Installing

Using pip you can install the following modules

```
sudo pip install colorama termcolor requests
```


## Install Overload-Dos

```
git clone https://github.com/codingplanets/Overload-DoS
```
```
cd Overload-DoS
```
```
chmod +x *
```
```
./install-overload
```
## Commands
```
usage: ./Overload-DoS.py -t [target] -p [port] -t [number threads]

optional arguments:
  -h, --help           show this help message and exit

options:

  -target <ip/domain>  Specify your target
  -timeout <timeout>   Timeout for socket
  -threads <threads>   Set threads number for connection (default = 1000)
  -port <port>         Specify port target (default = 80)
  -sleep <sleep time>  Set sleep time for reconnection
  -spoof <spoofed ip>  Specify spoofed IP address
  -request             Enable request target
  -syn                 Enable syn attack
  -slow                Enable slow attack
  -fakeip              Option to create fake ip if not specifed for spoofed ip
```

## Built With

* [Python 2.7](https://www.python.org/download/releases/2.7/) - The code framework used
* [Requests](http://docs.python-requests.org/en/master/) - Used to send DoS attack
* [Colorama](https://pypi.python.org/pypi/colorama) - Used to generate text color
* [Termcolor](https://pypi.python.org/pypi/termcolor) - Used to generate text color



## Authors

* **Chris Poole** - [codingplanets](https://github.com/codingplanets)


## License

This project is licensed under the MIT License

