# netlify-ddns

![Travis-CI](https://img.shields.io/travis/com/lukehsiao/netlify-ddns-rs)
![Crates.io](https://img.shields.io/crates/v/netlify-ddns)
![License](https://img.shields.io/crates/l/netlify-ddns)

netlify-ddns is a simple command line tool for creating a DNS record for
[Netlify's Managed DNS][netlify] service. It is meant to be run as a cron job
and queries a third-party for your public IP, then updates or adds a DNS record
using the Netlify API.

## Installation

Install using [cargo][cargo]:

```
cargo install netlify-ddns
```

## Usage

```
netlify-ddns
A simple CLI tool for setting Netlify DNS records.

USAGE:
    netlify-ddns [FLAGS] [OPTIONS] --domain <domain>

FLAGS:
    -h, --help       Prints help information
        --ipv6       Whether an IPv6 'AAAA' record should be updated
    -V, --version    Prints version information

OPTIONS:
    -d, --domain <domain>          The full domain for the DNS record
    -s, --subdomain <subdomain>    The subdomain segment for the DNS record [default: www]
    -t, --token <token>            Your Netlify personal access token [env: NETLIFY_TOKEN=]
```

## Related

Check out [oscartbeaumont/netlify-dynamic-dns][netlify-ddns-go] for a similar
client written in [Go][go].

[cargo]: https://doc.rust-lang.org/cargo/getting-started/installation.html
[go]: https://golang.org/
[netlify-ddns-go]: https://github.com/oscartbeaumont/netlify-dynamic-dns
[netlify]: https://www.netlify.com/docs/dns/
