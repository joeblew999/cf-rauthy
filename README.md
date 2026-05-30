# cf-rauthy

https://github.com/sebadob/rauthy for cloudflare. The Server is self hosted on any standard server, and the client runs on Cloudflare workers using worker-rs.

Rauthy provides the Admin GUI and User GUI and Server and replication, with OIDC.

The work to do this is here: https://github.com/sebadob/rauthy/issues/1582

Once this is done we can combine Auth and ReBac using Cedar ( https://github.com/cedar-policy/cedar9 , allowing a clean and extensible security system with minimal resource usage. Cedar runs fine on Cloudflare. Rauthy client has the required primitives.

Then ConnectRPC ( for native and Cloudflare ) middlware can hook in. See: https://github.com/joeblew999/cf-connectrpc-middleware

Connect RPC ,on Cloudflare, allows workers to interoperate over zero hops, and for any other clients in typescript and other ConnectRPC languages.  Thanks to https://github.com/anthropics/connect-rust and https://github.com/connyay/connectrpc-workers.






