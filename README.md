# A torrent library for Golang
Is that even possible to put together a native Golang torrent library covering most use cases?  
Given the number of singular implementations I begin to wonder it's not going to be easy.

A recap of projects found on the web is below, the pro/cons list is totally ongoing work, I tried a raw estimation of a project's value, so is mostly rubbish, but it should be used to understand what to recycle and when.

To discuss whether this optimistic project can be a reality, open an [Issue](/issues), or propose edits as [Pull Request](/pulls)

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

