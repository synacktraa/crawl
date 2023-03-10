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
|  crawl [-f] [href|script|form] 
|
|Options:
|  -h show help menu
|  -d number of depth to scrape.
|  -f attribute a type of link. [href|script|form]
|
|Example:
|  crawl -f script [domain].[TLD]
|  crawl -d 1 [domain].[TLD]/directory
|  crawl -f href [domain].[TLD]/directory?key=value
|
|Fetches all href, script and form links, if no flags are specified.
|Uses HTTPs as default protocol, if no protocol is specified.                                                               
```

```bash
$ echo google.com | crawl
```

[![asciicast](https://imgur.com/XmhgWm5.png)](https://asciinema.org/a/1nQQGtpE6q8qweVS2q9dfpAaa)

##  Tool Chain

Get all subdomains of owasp.org and crawl the ones that are alive.

```bash
subfinder -d owasp.org | httpx | crawl
```
  
## Features
-   Fetches all href, script and form links.
-   Highlights the Depth-1 URLs and indicates which Depth-2 URLs are included under each Depth-1 URL.
-   Uses HTTPs as default protocol, if no protocol is specified.
-   Depth is set to 1 by default, if depth is not specified.
-   Can be linked with other tool(s)/command(s) using pipes to create a tool chain.
-   Output will be color-less if it's redirected to a file or piped to a another command.
  
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
- sort
- uniq
