<p align=center>
<br>
<a href="http://makeapullrequest.com"><img src="https://img.shields.io/badge/PRs-welcome-darkred.svg"></a>
<img src="https://img.shields.io/badge/os-linux-darkred">
<img src="https://img.shields.io/badge/os-mac-darkred">
<img src="https://img.shields.io/badge/os-windows-darkred">
<img src="https://img.shields.io/badge/os-android-darkred">
<br>
</p>

<p align="center">
<a><img title="Made in INDIA" src="https://img.shields.io/badge/MADE%20IN-INDIA-SCRIPT?colorA=%23ff8100&colorB=%23017e40&colorC=%23ff0000&style=for-the-badge"></a>
</p>

<h1 align="center">crawl<h1>

<p align="center">
<img src="https://imgur.com/kN5LnMQ.jpg" alt="Spider's image"/>
</p>

<h3 align="center">
A simple web crawler written in shell script, designed to efficiently discover endpoints and assets within a web application.
</h3>

##  Usage

```bash
$ crawl
```

<p align="center">
<img src="https://imgur.com/tsLsR6Z.png" alt="ASCII Spider's image"/>
</p>

```
$ crawl -h
|Usage:
|  ${0##*/} [-f] [href|script|form] 
|
|Options:
|  -h show help menu
|  -f attr a type of link. [href|script|form]
|
|Example:
|  crawl -f script [domain].[TLD]
|  crawl [domain].[TLD]/directory
|  crawl -f href [domain].[TLD]/directory?key=value
|
|Fetches all href, script and form links, if no flags are specified.
|Uses HTTPs as default protocol, if no protocol is specified.

```

```bash
$ crawl github.com
```

![crawl](https://imgur.com/eKjKYil.png)

*This web crawler is getting some exciting updates soon! In addition to its current capabilities, we will be adding a timeout feature and the ability to send requests through a proxy server.*

##  Tool Chain

Get all subdomains of owasp.org and crawl the ones that are alive.

```bash
subfinder -d owasp.org | httpx | crawl
```
  
## Features
-   Fetches all href, script and form links.
-   Uses HTTPs as default protocol, if no protocol is specified.
-   Can be linked with other tool(s)/command(s) using pipes to create a tool chain.
  
##  Installation

```bash
git clone https://github.com/synacktraa/crawl.git && cd ./crawl
sudo mv ./crawl /usr/local/bin
cd .. && rm -rf "./crawl"
```

##  Dependencies

- curl
- sed
- grep
- awk
- wc
