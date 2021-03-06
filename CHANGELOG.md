## Rails 5.2.0.beta2 (November 28, 2017) ##

*   No changes.


## Rails 5.2.0.beta1 (November 27, 2017) ##

*   Removed deprecated evented redis adapter.

    *Rafael Mendonça França*

*   Support redis-rb 4.0.

    *Jeremy Daer*

*   Hash long stream identifiers when using PostgreSQL adapter.

    PostgreSQL has a limit on identifiers length (63 chars, [docs](https://www.postgresql.org/docs/current/static/sql-syntax-lexical.html#SQL-SYNTAX-IDENTIFIERS)).
    Provided fix minifies identifiers longer than 63 chars by hashing them with SHA1.

    Fixes #28751.

    *Vladimir Dementyev*

*   Action Cable's `redis` adapter allows for other common redis-rb options (`host`, `port`, `db`, `password`) in cable.yml.

    Previously, it accepts only a [redis:// url](https://www.iana.org/assignments/uri-schemes/prov/redis) as an option.
    While we can add all of these options to the `url` itself, it is not explicitly documented. This alternative setup
    is shown as the first example in the [Redis rubygem](https://github.com/redis/redis-rb#getting-started), which
    makes this set of options as sensible as using just the `url`.

    *Marc Rendl Ignacio*


