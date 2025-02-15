<img width="1280" alt="Loot Rarity" src="https://user-images.githubusercontent.com/36158/131253911-12092434-7325-4d7b-b1f2-5a752937bdfc.png">

Rarity levels for [Loot](https://lootproject.com) items.

## How are the rarity levels determined?

The rarity level of any given item is deducted from its number of occurrences in the total number of Loot items.

| Rarity                                                                                                                                    | Description                                        | Occurrences           |
| ----------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | --------------------- |
| <img width="10" alt="" src="https://user-images.githubusercontent.com/36158/131379065-5eef7b05-458c-4717-bfa8-c2d086283f0b.png"> Level 1 | **Common** items appear **375** or more times.     | 47.25% - 30,237 items |
| <img width="10" alt="" src="https://user-images.githubusercontent.com/36158/131379064-442c9a9e-90c9-4cb9-8fac-1ed0dbed5609.png"> Level 2 | **Uncommon** items appear less than **375** times. | 12.61% - 8,073 items  |
| <img width="10" alt="" src="https://user-images.githubusercontent.com/36158/131379063-1b6fa149-945f-467a-893e-e90eab48c20c.png"> Level 3 | **Rare** items appear less than **358** times.     | 11.78% - 7,537 items  |
| <img width="10" alt="" src="https://user-images.githubusercontent.com/36158/131379062-4847e475-8250-4e17-bec1-71c586b4e419.png"> Level 4 | **Epic** items appear less than **101** times.     | 10.29% - 6,587 items  |
| <img width="10" alt="" src="https://user-images.githubusercontent.com/36158/131379061-acead0af-797b-47f9-9d71-db8c7d6b1696.png"> Level 5 | **Legendary** items appear less than **10** times. | 9.67% - 6,189 items   |
| <img width="10" alt="" src="https://user-images.githubusercontent.com/36158/131379060-7fa91e93-dbc2-4a55-8d0c-125bc43e16e1.png"> Level 6 | **Mythic** items appear exactly **1** time.        | 8.4% - 5,377 items    |

## Installation

```sh
npm i --save loot-rarity # npm
yarn add loot-rarity # yarn
pnpm add loot-rarity # pnpm
```

## API

```tsx
// Rarity goes from 1 (common) to 6 (mythic).
type Rarity = 1 | 2 | 3 | 4 | 5 | 6;

// Get the rarity of an item given its name.
function itemRarity(itemName: string): Rarity;

// Get the color of an item given its name or rarity.
function rarityColor(itemOrRarity: string | Rarity): string;

// Get the description of a rarity given an item name or rarity level.
function rarityDescription(itemOrRarity: string | Rarity): string;

// Transforms an SVG image (SVG, URL or data URI) to add rarity colors.
function imageRarity(image: string, { displayLevels?: Boolean }): Promise<string>;

// Generates an image with colors from a list of items.
function imageRarityFromItems(items: string[], { displayLevels?: Boolean }): string;
```

## Demo

Have a look at [the demo app](https://ky7e7.csb.app/) on CodeSandbox to see how it works.

You can also run it from this repository:

```sh
# Install pnpm if needed
npm i -g pnpm

# Build loot-rarity
pnpm i
pnpm build

# Run the demo app
cd demo
pnpm i
pnpm dev
```

## Thanks

- [@scotato](https://github.com/scotato) for [github.com/scotato/inventory](https://github.com/scotato/inventory), loot-rarity was heavily inspired by it.
- [@Anish-Agnihotri](https://github.com/Anish-Agnihotri) for [the data](https://github.com/Anish-Agnihotri/dhof-loot) he extracted from Loot and that loot-rarity is using.

## License

MIT
