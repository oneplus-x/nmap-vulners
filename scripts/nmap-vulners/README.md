# nmap_vulners

[![Current Release](https://img.shields.io/github/release/vulnersCom/nmap-vulners.svg "Current Release")](https://github.com/vulnersCom/nmap-vulners/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/vulnersCom/nmap-vulners/total.svg "Downloads")](https://github.com/vulnersCom/nmap-vulners/releases) [![PayPal](https://img.shields.io/badge/donate-PayPal-green.svg)](https://paypal.me/videns)

## Description

NSE script using some well-known service to provide info on vulnerabilities

![Result example](https://github.com/anonymansz/nmap-vulners/blob/master/example.png)

## Dependencies:
     nmap libraries:
         http
         json
         string

The only thing you should always keep in mind is that the script depends on having software versions at hand, so it only works with -sV flag.
## Installation

locate where nmap is located on your system

~~~
cd /usr/share/nmap/
git clone https://github.com/vulnersCom/nmap-vulners
cd /usr/share/nmap/nmap-vulners
sudo cp  vulners.nse http-vulners-regex.nse /usr/share/nmap/scripts/
sudo cp  http-vulners-regex.json http-vulners-paths /usr/share/nmap/nselib/data/
~~~
~~~
cd /usr/share/nmap/scripts/
git clone --recursive https://github.com/scipag/vulscan scipag_vulscan
ln -s `pwd`/scipag_vulscan /usr/share/nmap/scripts/vulscan
~~~	
Use it as straightforward as you can:
~~~	
nmap -sV --script vulners 80.74.154.114
~~~

![Result example](https://github.com/anonymansz/nmap-vulners/blob/master/simple_regex_example.png)

![Result example](https://github.com/anonymansz/nmap-vulners/blob/master/paths_regex_example.png)

It is KISS after all.
