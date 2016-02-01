# Simple Uber
Build a simple version of Uber's backend architecture.

1.`clone` from master

2.`npm install` if necessary

3.install [s2-geometry-library][https://github.com/micolous/s2-geometry-library/tree/b42d582e0d3986c44d18bc04dd074e6546181aa7]

4.run three nodes on local address `node uber/simple_uber.js -n le -s 3`

5.add three nodes into cluster `node uber/simple_uber.js -n le -s 3 -p 3003 -b '["127.0.0.1:3000"]'` (known bug: could not add into cluster that is runnign on different ip address)

# Next Step
In near future, I'm going to...

1. Add different requests to this backend system to implement Uber's most basic features.

2. Use [Riak][http://basho.com/products/riak-kv/] as a backup database to increment fault-tolerance.

3. Add rules when adding/removing nodes so to make full use of consistent hashing.

4. Use Kafka as streaming information provider and gatherer.

# Uber Backend
To know more about uber's backend architecture, checkout this [tech talk][http://basho.com/posts/technical/ubers-ringpop-and-riak/].

Here are some good references for...

### consistent hashing
[Consistent hashing][http://michaelnielsen.org/blog/consistent-hashing/]

[A number-theoretic approach to consistent hashing][http://michaelnielsen.org/blog/a-number-theoretic-approach-to-consistent-hashing/]

### SWIM membership protocol
[THE SWIM MEMBERSHIP PROTOCOL][http://prakhar.me/articles/swim/]

[SWIM: Scalable Weakly-consistent Infection-style Process Group Membership Protoco][https://www.cs.cornell.edu/~asdas/research/dsn02-swim.pdf]


