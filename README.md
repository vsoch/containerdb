
containerdb is a memory-only database that is intended to storing container
metadata. It is a combined and tweaked module for all of this great work
by [tidewall](https://github.com/tidewall).

 - [tidewall/buntdb](https://github.com/tidwall/buntdb)
 - [tidewall/btree](https://github.com/tidewall/btree)
 - [tidewall/gjson](https://github.com/tidewall/gjson)
 - [tidewall/grect](https://github.com/tidewall/grect)
 - [tidewall/match](https://github.com/tidewall/match)
 - [tidewall/pretty](https://github.com/tidewall/pretty)
 - [tidewall/tinyqueue](https://github.com/tidewall/tinyqueue)

I was worried about reproducibility (and having all these different dependencies
separated like this) and along with wanting to tweak some of the code, wanted
to package them together. This is the rationale for creating containerdb.
The licenses for this previous work are packaged with the code under [.github](.github). Thank you [tidewall](https://github.com/tidewall), Google, and other developers that were a part of this
original work! Features below are from the original [README.md](https://github.com/tidwall/buntdb).

Features
========

- In-memory database for [fast reads and writes](#performance)
- Embeddable with a [simple API](https://godoc.org/github.com/tidwall/buntdb)
- [Spatial indexing](#spatial-indexes) for up to 20 dimensions; Useful for Geospatial data
- Index fields inside [JSON](#json-indexes) documents
- [Collate i18n Indexes](#collate-i18n-indexes) using the optional [collate package](https://github.com/tidwall/collate)
- Create [custom indexes](#custom-indexes) for any data type
- Support for [multi value indexes](#multi-value-index); Similar to a SQL multi column index
- [Built-in types](#built-in-types) that are easy to get up & running; String, Uint, Int, Float
- Flexible [iteration](#iterating) of data; ascending, descending, and ranges
- [Durable append-only file](#append-only-file) format for persistence
- Option to evict old items with an [expiration](#data-expiration) TTL
- Tight codebase, under 2K loc using the `cloc` command
- ACID semantics with locking [transactions](#transactions) that support rollbacks


## License

All source code is available under the MIT [License](/LICENSE). See
the [.github](.github) folder for dependency (included) licenses as well.
