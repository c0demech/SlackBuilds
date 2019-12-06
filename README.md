# SlackBuilds

These are the packages I maintain over at SlackBuilds.org

SlackBuilds are shell scripts that automate compiling and packaging software on Slackware Linux. 

While you can definitely compile and run software on Slackware without using slackbuilds, it
is the preferred way. The benefits can be seen in the self documenting nature of the scripts
as well as the ability to reduce repetitive tasks.


| Folder | Description |
| --- | --- |
| dirb | Web content scanner for auditing |
| dnsmasq | lightweight, easy to configure, DNS forwarder and DHCP server. |
| fpc-source | Open source compiler for Pascal and Object Pascal |
| lastpass-cli | LastPass command line interface tool |
| usbguard | rogue USB device protection |
| zeek | Network Security Monitor |


## Installation
The preferred way is to use [sbotools](https://pink-mist.github.io/sbotools/) which will grab these packages and many others at [SlackBuilds.org](https://www.slackbuilds.org)

## Usage
```
cd /tmp
git clone https://github.com/tankmek/SlackBuilds.git
cd SlackBuilds/<appname>
wget $(grep DOWNLOAD= *.info | grep -Eoi '(http|https):[^"]+' )
md5sum <appname>.xx (compare with md5sum in .info file)
sudo su -
cd /tmp/SlackBuilds/<appname>
chmod a+x <appname>.SlackBuild
./<appname>.SlackBuild
```
