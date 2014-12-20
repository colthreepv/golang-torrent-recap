# A torrent library for Golang
Is that even possible to put together a native Golang torrent library covering most use cases?  
Given the number of singular implementations I begin to wonder it's not going to be easy.

A recap of projects found on the web is [below](#existing-projects-recap), the pro/cons list is totally ongoing work, I tried a raw estimation of a project's value, so is mostly rubbish, but it should be used to understand what to recycle and when.

To discuss whether this optimistic project can be a reality, open an [Issue](/issues), or propose edits as [Pull Request](/pulls)

## Aim of the project
Let developers work together towards an usable torrent library for Go language community.  
It's reasonable to realize an efficient pure Go implementation, comparable in speed, but easier to read than lower level libraries.

Feature list
--------
- [x] [BEP 3: The BitTorrent Protocol Specification](http://bittorrent.org/beps/bep_0003.html)
- [x] [BEP 5: DHT Protocol](http://bittorrent.org/beps/bep_0005.html), from [nictuku/dht](https://github.com/nictuku/dht)
- [ ] [BEP 6: Fast Extension](http://bittorrent.org/beps/bep_0006.html)
- [x] [BEP 7: IPv6 Tracker Extension](http://bittorrent.org/beps/bep_0007.html)
- [x] [BEP 9: Extension for Peers to Send Metadata Files](http://bittorrent.org/beps/bep_0009.html)
- [x] [BEP 10: Extension Protocol](http://bittorrent.org/beps/bep_0010.html)
- [x] [BEP 12: Multitracker Metadata Extension](http://bittorrent.org/beps/bep_0012.html)
- [ ] [BEP 15: UDP Tracker Protocol](http://bittorrent.org/beps/bep_0015.html)
- [x] [BEP 16: Superseeding](http://bittorrent.org/beps/bep_0016.html)
- [x] [BEP 17: HTTP Seeding (Hoffman-style)](http://bittorrent.org/beps/bep_0017.html)
- [ ] [BEP 18: Search Engine Specification](http://bittorrent.org/beps/bep_0018.html)
- [x] [BEP 19: HTTP/FTP Seeding (GetRight-style)](http://bittorrent.org/beps/bep_0019.html)
- [x] [BEP 21: Extension for Partial Seeds](http://bittorrent.org/beps/bep_0021.html)
- [ ] [BEP 22: BitTorrent Local Tracker Discovery Protocol](http://bittorrent.org/beps/bep_0022.html)
- [x] [BEP 24: Tracker Returns External IP](http://bittorrent.org/beps/bep_0024.html)
- [ ] [BEP 26: Zeroconf Peer Advertising and Discovery](http://bittorrent.org/beps/bep_0026.html)
- [x] [BEP 27: Private Torrents](http://bittorrent.org/beps/bep_0027.html)
- [ ] [BEP 28: Tracker exchange](http://bittorrent.org/beps/bep_0028.html)
- [x] [BEP 29: uTorrent transport protocol](http://bittorrent.org/beps/bep_0029.html), also more detailed on [libtorrent docs](http://www.libtorrent.org/utp.html)
- [ ] [BEP 30: Merkle tree torrent extension](http://bittorrent.org/beps/bep_0030.html)
- [ ] [BEP 31: Tracker Failure Retry Extension](http://bittorrent.org/beps/bep_0031.html)
- [ ] [BEP 32: IPv6 extension for DHT](http://bittorrent.org/beps/bep_0032.html)
- [ ] [BEP 33: DHT scrape](http://bittorrent.org/beps/bep_0033.html)
- [ ] [BEP 34: DNS Tracker Preferences](http://bittorrent.org/beps/bep_0034.html)
- [ ] [BEP 35: Torrent Signing](http://bittorrent.org/beps/bep_0035.html)
- [ ] [BEP 36: Torrent RSS feeds](http://bittorrent.org/beps/bep_0036.html)
- [ ] [BEP 38: Finding Local Data Via Torrent File Hints](http://bittorrent.org/beps/bep_0038.html)
- [ ] [BEP 39: Updating Torrents Via Feed URL](http://bittorrent.org/beps/bep_0039.html)
- [ ] [BEP 40: Canonical Peer Priority](http://bittorrent.org/beps/bep_0040.html)
- [ ] [BEP 41: UDP Tracker Protocol Extensions](http://bittorrent.org/beps/bep_0041.html)
- [ ] [BEP 42: DHT Security Extension](http://bittorrent.org/beps/bep_0042.html)
- [ ] [BEP 43: Read-only DHT Nodes](http://bittorrent.org/beps/bep_0043.html)

- [x] [uTorrent Peer Exchange Protocol](http://en.wikipedia.org/wiki/Peer_exchange)
- [x] [Local Peer Discovery](http://en.wikipedia.org/wiki/Local_Peer_Discovery)
- [ ] NAT-PMP support, from [TaiPei-Torrent](https://github.com/jackpal/Taipei-Torrent)
- [ ] UPNP support, from [TaiPei-Torrent](https://github.com/jackpal/Taipei-Torrent)


## Existing projects recap:

Torrent libraries written in Golang (or attempts to!), let's recap them:

- [ ] [cenkalti/rain](https://github.com/cenkalti/rain)
  - [x] Nice implemented feature list
  - [x] Tests, unknown coverage
  - [ ] Blank commits, or single worded commits
- [ ] [torrance/libtorrent](https://github.com/torrance/libtorrent)
  - [ ] Seems abandoned since Aug 2014
- [ ] [deoxxa/libtorrent](https://github.com/deoxxa/libtorrent), `torrance/libtorrent`'s fork
  - [x] Fork from [torrance/libtorrent](https://github.com/torrance/libtorrent)
  - [x] Tests, unknown coverage
  - [x] Seems better coded than the original
  - [ ] Issue tracker not active despite being a full-fledged fork
  - [ ] README missing
- [ ] [nsf/libtorgo/](https://github.com/nsf/libtorgo/)
  - [ ] Re-implemented already existing libraries, bencode
  - [ ] README missing
  - [ ] Seems abandoned since March 2014


Bencode libraries recap (most of them lead to torrent libraries):

- [ ] [zeebo/bencode](https://github.com/zeebo/bencode)
  - [x] Recently updated
  - [x] 8 Packages using it
  - [x] Tested
  - [x] Example Usage
- [ ] [chihaya/bencode](https://github.com/chihaya/bencode)
  - [x] Appreciate the idea, not using reflect package
  - [x] Used by chihaya tracker
  - [ ] Seems not developed since July 2014, stable?
  - [ ] Would really love benchmarks comparing use of reflection and not
- [ ] [jackpal/bencode-go](https://github.com/jackpal/bencode-go)
  - [x] Seems stable, is it?
  - [x] Used by both `tulva` and `Taipei-Torrent`
  - [ ] Tests all written in one file


Other libraries recap:

- [ ] [nictuku/dht](https://github.com/nictuku/dht)
  - [x] BEP 5 functionality
  - [x] Test coverage seems adequate
  - [x] Used by `Taipei-Torrent`


Full fledged packages:

- [ ] [jackpal/Taipei-Torrent](https://github.com/jackpal/Taipei-Torrent): BitTorrent client
  - [x] Oldest project of the list, co-written with nicktutu, something good must come out of this
  - [ ] Many features without tests
  - [ ] BEP feature support list is not there
  - [ ] Not coded to be embeddable
- [ ] [jtakkala/tulva](https://github.com/jtakkala/tulva): BitTorrent client
  - [ ] Feature list, but no BEP feature support
  - [ ] No tests whatsoever
  - [ ] Single torrent support
- [ ] [drbawb/babou](https://github.com/drbawb/babou): BitTorrent HTTP tracker
  - [ ] Test coverage is so-so
  - [ ] Not followed much, despite it's large development effort
  - [ ] Final product, don't know if it might be useful code-wise to a torrent library
- [ ] [chihaya/chihaya](https://github.com/chihaya/chihaya): BitTorrent HTTP tracker
  - [x] BitTorrent tracker, working
  - [x] Follows a clever driver system
  - [x] Benchmarks!
  - [ ] Final product, don't know if it might be useful code-wise to a torrent library

