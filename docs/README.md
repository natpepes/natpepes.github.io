# NatPepes 🐸


Welcome to **NatPepes**, an extremely premium on-chain generative art collection residing purely on Bitcoin through Digital Matter Theory (DMT). 

Instead of arbitrary minting, NatPepes are mathematically discovered by scanning the Bitcoin block data for the legendary hex pattern (`420`) inside the `nonce` field. Because `420` requires 3 exact hex digits, NatPepes have a mathematically enforced scarce supply—averaging only 1 valid block out of every 4,096 Bitcoin blocks.

## How it Works
Every Bitcoin block has a `nonce` value used by miners. When converted to hex, some blocks naturally contain the sequence `420`.
If a block contains `420` in its nonce, it is eligible to mint **1 unique NatPepe**.
The block number itself is the seed for the generative SVG art, ensuring fairness and full on-chain provenance without IPFS.

## Traits & Anatomy
NatPepes are drawn completely on-chain using precision SVG paths for true aesthetic quality.
Based on the digits of a valid block number, your NatPepe gets its unique properties:
- **Skin Color** (Variations of rare and common Pepe greens/golds)
- **Eyes Type** (Bulging, half-closed, stoned, laser)
- **Mouth/Expression** (Smug, sad, flat, lip-bite)
- **Headwear** (Wizard hat, cap, McDonald's hat, none)
- **Clothes** (Suit, hoodie, naked, chain)

### ⭐ Special Traits
Some blocks are mathematically special, granting the NatPepe inside a rare property:
- **Mirror Pepe (Palindrome)**: The block number reads the same forwards and backwards (e.g. 845548). The SVG is mirrored horizontally.
- **Halving Pepe**: The block is an exact Bitcoin Halving block (e.g. 210000, 420000). The frog features a legendary gold/diamond texture.
- **Milestone Pepe**: Block numbers ending in 00000.
- **Lucky Pepe**: Blocks with all identical digits (e.g. 444444).

## How to Mint (DMT)
Minting is purely decentralized via the Tap Protocol DMT specification.
You must inscribe the following JSON to claim a valid block. Only **1 claim per block** is allowed.

```json
{
  "p": "tap",
  "op": "dmt-mint",
  "dep": "DEPLOY_INSCRIPTION_ID",
  "tick": "natpepes",
  "blk": "BLOCK_NUMBER_YOU_ARE_CLAIMING"
}
```

## Contract Details
- **Protocol**: TAP (DMT)
- **Tick**: `natpepes`
- **Supply Element**: `natpepes.420.12.element` (Nonce field 12, pattern 420)
- **Render Script**: [Inscription ID pending deploy]
