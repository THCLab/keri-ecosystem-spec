# API Proposal

[![hackmd-github-sync-badge](https://hackmd.io/Ae0qjHXaRcaEQP9LwsAiHg/badge)](https://hackmd.io/Ae0qjHXaRcaEQP9LwsAiHg)


### `Entity`
The current public keys store identified by unique `Identifier`. Allows retriving public keys currently stored by other entity.

##### Methods:
###### `new(KeyManager, CommunicationMethod) → Entity`
Creates new entity with specified key manager and method of communication with other entities.

###### `pair(Identifier)`
Establishes control authority between entity and entity of given `Identifier`.

###### `append(data)`
Computes hash for any given data and saves it as an conformation.

###### `new_key_set()`
Sets new keys as current.

###### `get_verification_method(Identifier) → DidDocument`
Retrieves all current public keys from entity with given identifier.

## Interfaces
### `CommunicationMethod`
A common set of methods for providing and establishing communication
between the entities.
##### Methods:
`send(Identifier)`

### `KeyManager`
A common set of methods for signing and generating new key pairs.

##### Methods:
`sign(something)`

`new_keypair()`
 