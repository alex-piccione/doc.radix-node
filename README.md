# Radix Node
Documentation about running a Radix Node

Doc: https://docs.radixdlt.com/docs/running-a-node

Doc: https://docs.radixdlt.com/docs/running-a-node

Installation: https://docs-babylon.radixdlt.com/main/node-and-gateway/docker-install-node.html  


## Note of installation on local pc

Create a work directory

```bash
mkdir radixdlt
cd radixdlt
mkdir babylon-ledger
```

Copy there the ``radix-fullnode-compose.yml`` file.

> You’ll need the Radix Key Generator application to create secure keys for the node once it’s installed. (It’s a good idea to generate the keys first, just to get them out of the way).

Run this:
```bash
docker run --rm -v ${PWD}:/keygen/key radixdlt/keygen:v1.4.1 --keystore=/keygen/key/node-keystore.ks --password=node-password
```

When run it from a git bash terminal in Windows it fails with this error:
> Writing keypair 'node' [public key: 03fa413aa240762df5c86531be350143dead834efecfc4434fcc51a3e92ff11d64]
into new keystore C:/Program Files/Git/keygen/key/node-keystore.ks
ERROR: Unable to load keystore
