# Function Signatures(Deprecated)
A Signatures to Function Reverse Query Set for Eathereum Smart Contracts.

*This repo is deprecated and [4byte.dictionary](https://www.4byte.directory/) API is hignly recommended.*

## Function Signature
In Ethereum smart contracts, all the functions are compiled into bytecode with address indicated by function selector. The function selector needs **function signature** to get the address in EVM by mapping. Thus invoking between smart contracts only needs(or provides) function signature, without knowing the function difinition.

Function signatures are generate by Hash method thus the generation is irreversible. EVM uses **keccak256** and select first 4 bytes as function signature.

``` python
import sha3
function_signature=sha3.keccak_256(str(function_name).encode('utf-8')).hexdigest().lower()[:8]
```

We collected 221725 function signatures for the query for function name.

Credits to [ethereum-lists/4bytes](ethereum-lists/4bytes) and [4byte.dictionary](https://www.4byte.directory/).

