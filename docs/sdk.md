---
sidebar_position: 2
---

# The SDK

The SDK is a JS/TS module for developers, allowing anyone to retrieve NFT data in a few lines of codes.

For example:
```ts
import sdk from "NFtez";

sdk.getNFTCollection("<contract-address>")
.then(console.log);
```

This small script will print out basic informations for each NFT of a collection.

---

## Functions list
`getCollectionAttributes()`: Get all the available attributes across the NFT of a collection.
```ts
getCollectionAttributes: (contractAddress: string) => Promise<CollectionAttributes>
```

`getNFTCollection()`: Get all NFTs of a collection.
```ts
getNFTCollection: (contractAddress: string) => Promise<GetNftCollectionQuery>
```

`getWalletNFTs()`: Get all NFTs for a given wallet address.
```ts
getWalletNFTs: (walletAddress: string) => Promise<GetWalletNfTsQuery>
```

`getNFTMetadata()`: Get all metadata of a given collection address / token ID pair.
```ts
getNFTMetadata: (contractAddress: string, tokenId: string) => Promise<Record<string, any>>
```

`verifyOwnership()`: Return `true` if the given wallet address hold any NFT of a given collection.
```ts
verifyOwnership: (walletAddress: string, contractAddress: string) => Promise<boolean>
```

`verifyTokenOwnership()`: Return `true` if the given wallet address hold the specified token in the given collection.
```ts
verifyTokenOwnership: (tokenId: string, walletAddress: string, contractAddress: string) => Promise<boolean>
```
