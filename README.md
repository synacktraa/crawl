<p align=center>
<br>
<a href="http://makeapullrequest.com"><img src="https://img.shields.io/badge/PRs-welcome-darkred.svg"></a>
<img src="https://img.shields.io/badge/os-linux-darkred">
<img src="https://img.shields.io/badge/os-mac-darkred">
<img src="https://img.shields.io/badge/os-windows-darkred">
<img src="https://img.shields.io/badge/os-android-darkred">
<br>
</p>

<h1 align="center">crawl<h1>

<p align="center">
  <img src="https://imgur.com/kN5LnMQ.jpg" alt="Spider's image"/>
</p>

<h3 align="center">
A simple web crawler written in shell script, designed to efficiently discover endpoints and assets within a web application. 
</h3>
<br>

> This web crawler has a crawling depth of 2, but I am actively working on improving it in the near future. Stay tuned for updates on the increased depth capabilities of this tool.

## Usage

```bash
$ crawl
```

<p align="center">
 <img src="https://imgur.com/IBtC01a.png" alt="ASCII Spider's image"/>
</p>

```bash
$ crawl -h

|Usage:
|  crawl [-f] (href|script)
|
|Options:
|  -h show help menu
|  -f fetch a type of link. [href|script]
|
|Example:
|  crawl -f script [domain].[TLD]
|  crawl [domain].[TLD]/directory
|  crawl -f href [domain].[TLD]/directory?key=value
|
|By default, crawl fetches both href and script links
```

```bash
$ crawl github.com
```
![crawl](https://imgur.com/eKjKYil.png)

*This web crawler is getting some exciting updates soon! In addition to its current capabilities, we will be adding a timeout feature and the ability to send requests through a proxy server.*

## Tool Chain

Get all subdomains of owasp, crawl the ones that are alive.
```bash
subfinder -d owasp.org | httpx | crawl
```

## Installation

```sh
git clone https://github.com/synacktraa/crawl.git && cd ./crawl
sudo mv ./crawl /usr/local/bin
cd .. && rm -rf "./crawl"
```
## Dependencies

- curl
- sed
- grep
- cut

