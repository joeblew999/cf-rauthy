# cf-rauthy

https://github.com/sebadob/rauthy for cloudflare. The Rauthy server is self hosted on any standard server, and the client needs to run on Cloudflare workers using worker-rs so that its easy for Cloudflare apps to use Rauthy.

Rauthy provides the Admin GUI and User GUI and Server and replication, with OIDC and other standard enterprise protocols.

The work to do this as OIDC relay is at: https://github.com/sebadob/rauthy/issues/1582

Also Rauthy uses https://github.com/sebadob/hiqlite ( SQLITE with Raft ) to keep the Sqlite databases in sync between servers. We can look at using https://github.com/connyay/EdgeReplica, which has ConnectRPC for Admin, to allow developers to use CloudFlare for Sqlite sync and backups. This idea needs discussion with https://github.com/sebadob though.

Also Rauthy Server could also be adapter to work on Cloudflare. Another discussion ( idea for later ). The SQLIte is then replcation by Cloudflare inherent COLO sync. See https://github.com/joeblew999/cf-do-locator

Also Rauthy and ReBac using Cedar ( https://github.com/cedar-policy/cedar9 , allowing a clean and extensible security system with minimal resource usage. Cedar runs fine on Cloudflare. Rauthy client has the required primitives.

Then ConnectRPC ( for native and Cloudflare ) middlware can hook in. High quality ConnectRPC middleware for Native and Cloudflare provides easy and high quality operational needs.  See: https://github.com/joeblew999/cf-connectrpc-middleware

Connect RPC ,on Cloudflare, allows workers to interoperate over zero hops, and for any other clients in typescript and other ConnectRPC languages.  Thanks to https://github.com/anthropics/connect-rust and https://github.com/connyay/connectrpc-workers.










