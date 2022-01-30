## Installation
    locate where nmap is located on your system
	cd /usr/share/nmap/
	git clone https://github.com/scipag/nmap-vulners
	cd /usr/share/nmap/nmap-vulners
	sudo cp  vulners.nse http-vulners-regex.nse /usr/share/nmap/scripts/
	sudo cp  http-vulners-regex.json http-vulners-paths /usr/share/nmap/nselib/data/

	cd /usr/share/nmap/scripts/
	git clone https://github.com/scipag/vulscan scipag_vulscan
	ln -s `pwd`/scipag_vulscan /usr/share/nmap/scripts/vulscan

## Usage
[Alt text](https://github.com/anonymansz/nmap-vulners/blob/master/example.png)
