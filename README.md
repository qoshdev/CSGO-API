# Introduction

Welcome to the unofficial JSON API for Counter-Strike 2. This API provides access to various data aspects of the game, parsed into JSON format for easier integration and use.

Data are sourced from files maintained at [this repository](https://github.com/ByMykel/counter-strike-file-tracker/tree/main/static).

## Usage

This API supports over 20 languages. To access information in a specific language, replace `{language}` in the URL with one of the supported language codes listed below.

```http
GET https://bymykel.github.io/CSGO-API/api/{language}
```

Supported Languages:

| Language Name         | Language Code |
| --------------------- | ------------- |
| Bulgarian             | bg            |
| Czech                 | cs            |
| Danish                | da            |
| German                | de            |
| Greek                 | el            |
| English               | en            |
| Spanish (Spain)       | es-ES         |
| Spanish (Mexico)      | es-MX         |
| Finnish               | fi            |
| French                | fr            |
| Hungarian             | hu            |
| Italian               | it            |
| Japanese              | ja            |
| Korean                | ko            |
| Dutch                 | nl            |
| Norwegian             | no            |
| Polish                | pl            |
| Portuguese (Brazil)   | pt-BR         |
| Portuguese (Portugal) | pt-PT         |
| Romanian              | ro            |
| Russian               | ru            |
| Slovak                | sk            |
| Swedish               | sv            |
| Thai                  | th            |
| Turkish               | tr            |
| Ukrainian             | uk            |
| Chinese (Simplified)  | zh-CN         |
| Chinese (Traditional) | zh-TW         |
| Vietnamese            | vi            |

### All items

```http
GET https://bymykel.github.io/CSGO-API/api/en/all.json
```

Object with all items accessible by their id.

### List skins

```http
GET https://bymykel.github.io/CSGO-API/api/en/skins.json
```

Example response:

```json
[
  {
    id: "skin-65604",
    name: "Desert Eagle | Urban DDPAT",
    description:
      "As expensive as it is powerful, the Desert Eagle is an iconic pistol that is difficult to master but surprisingly accurate at long range. It has been painted using a Digital Disruptive Pattern (DDPAT) hydrographic.\\n\\n<i>By the time you're close enough to notice the pixels it's already too late</i>",
    weapon: {
      id: "weapon_deagle",
      weapon_id: 1,
      name: "Desert Eagle",
    },
    category: {
      id: "csgo_inventory_weapon_category_pistols",
      name: "Pistols",
    },
    pattern: {
      id: "hy_ddpat_urb",
      name: "Urban DDPAT",
    },
    min_float: 0.06,
    max_float: 0.8,
    rarity: {
      id: "rarity_uncommon_weapon",
      name: "Industrial Grade",
      color: "#5e98d9",
    },
    stattrak: false,
    souvenir: true,
    paint_index: "17",
    wears: [
      {
        id: "SFUI_InvTooltip_Wear_Amount_0",
        name: "Factory New",
      },
      // ...
    ],
    collections: [
      {
        id: "collection-set-overpass",
        name: "The Overpass Collection",
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/set_icons/set_overpass_png.png",
      },
    ],
    crates: [
      {
        id: "crate-4028",
        name: "ESL One Cologne 2014 Overpass Souvenir Package",
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/weapon_cases/crate_esl14_promo_de_overpass_png.png",
      },
      // ...
    ],
    team: {
      id: "both",
      name: "Both Teams",
    },
    legacy_model: true,
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/default_generated/weapon_deagle_hy_ddpat_urb_light_png.png",
  },
  // ...
]
```

### List skins not grouped

```http
GET https://bymykel.github.io/CSGO-API/api/en/skins_not_grouped.json
```

Similar to the previous but in this case is not grouped by wear (Factory New, Field-Tested, etc) and state (normal, stattrak, souvenir).

Example response:

```json
[
  {
    id: "skin-65604_0",
    skin_id: "skin-65604",
    name: "Desert Eagle | Urban DDPAT (Factory New)",
    description:
      "As expensive as it is powerful, the Desert Eagle is an iconic pistol that is difficult to master but surprisingly accurate at long range. It has been painted using a Digital Disruptive Pattern (DDPAT) hydrographic.\\n\\n<i>By the time you're close enough to notice the pixels it's already too late</i>",
    weapon: {
      id: "weapon_deagle",
      weapon_id: 1,
      name: "Desert Eagle",
    },
    category: {
      id: "csgo_inventory_weapon_category_pistols",
      name: "Pistols",
    },
    pattern: {
      id: "hy_ddpat_urb",
      name: "Urban DDPAT",
    },
    min_float: 0.06,
    max_float: 0.8,
    wear: {
      id: "SFUI_InvTooltip_Wear_Amount_0",
      name: "Factory New",
    },
    stattrak: false,
    souvenir: false,
    paint_index: "17",
    rarity: {
      id: "rarity_uncommon_weapon",
      name: "Industrial Grade",
      color: "#5e98d9",
    },
    market_hash_name: "Desert Eagle | Urban DDPAT (Factory New)",
    team: {
      id: "both",
      name: "Both Teams",
    },
    style: {
      id: 2,
      name: "Hydrographic",
      url: "https://www.counter-strike.net/workshop/workshopfinishes#hydrographic",
    },
    legacy_model: true,
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/default_generated/weapon_deagle_hy_ddpat_urb_light_png.png",
  },
  // ...
]
```

### List stickers

```http
GET https://bymykel.github.io/CSGO-API/api/en/stickers.json
```

Example response:

```json
[
  {
    id: "sticker-75",
    name: "Sticker | Titan | Katowice 2014",
    description:
      "<span style='color:#ffd700;'>This item commemorates the The 2014 EMS One Katowice CS:GO Championship.</span><br/><br/> This sticker can be applied to any weapon you own and can be scraped to look more worn. You can scrape the same sticker multiple times, making it a bit more worn each time, until it is removed from the weapon.",
    rarity: {
      id: "rarity_rare",
      name: "High Grade",
      color: "#4b69ff",
    },
    crates: [
      {
        id: "crate-4015",
        name: "EMS Katowice 2014 Legends",
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/weapon_cases/crate_sticker_pack_kat2014_02_png.png",
      },
    ],
    tournament_event: "Katowice 2014",
    tournament_team: "Titan",
    type: "Team",
    market_hash_name: "Sticker | Titan | Katowice 2014",
    effect: "Other",
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/stickers/emskatowice2014/titan_png.png",
  },
  // ...
]
```

### List keychains (charms)

```http
GET https://bymykel.github.io/CSGO-API/api/en/keychains.json
```

Example response:

```json
[
  {
    id: "keychain-1",
    name: "Charm | Lil' Ava",
    description:
      "This charm can be attached to any weapon you own. Each attached charm can be detached by using a Charm Detachment. Detached charms will be returned to your inventory.",
    rarity: {
      id: "rarity_rare",
      name: "High Grade",
      color: "#4b69ff",
    },
    collections: [
      {
        id: "collection-set-kc-missinglink",
        name: "Missing Link Charm Collection",
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/set_icons/set_kc_missinglink_png.png",
      },
    ],
    market_hash_name: "Charm | Lil' Ava",
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/keychains/missinglink/kc_missinglink_ava_png.png",
  },
  // ...
]
```

### List collections

```http
GET https://bymykel.github.io/CSGO-API/api/en/collections.json
```

Example response:

```json
[
  {
    id: "collection-set-community-3",
    name: "The Huntsman Collection",
    crates: [
      {
        id: "crate-4017",
        name: "Huntsman Weapon Case",
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/weapon_cases/crate_community_3_png.png",
      },
    ],
    contains: [
      {
        id: "skin-1967292",
        name: "Tec-9 | Isaac",
        rarity: {
          id: "rarity_rare_weapon",
          name: "Mil-Spec Grade",
          color: "#4b69ff",
        },
        paint_index: "303",
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/default_generated/weapon_tec9_cu_tec9_asiimov_light_png.png",
      },
      // ...
    ],
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/set_icons/set_community_3_png.png",
  },
  // ...
]
```

### List crates

This list includes cases, capsules, graffiti boxes, music kit boxes and souvenir packages.

```http
GET https://bymykel.github.io/CSGO-API/api/en/crates.json
```

Example response:

```json
[
  {
    id: "crate-4904",
    name: "Kilowatt Case",
    description: null,
    type: "Case",
    first_sale_date: "2024-01-16",
    contains: [
      {
        id: "skin-135748",
        name: "Dual Berettas | Hideout",
        rarity: {
          id: "rarity_rare_weapon",
          name: "Mil-Spec Grade",
          color: "#4b69ff",
        },
        paint_index: "1169",
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/default_generated/weapon_elite_dual_berettas_lethal_grin_light_png.png",
      },
      // ...
    ],
    contains_rare: [
      {
        id: "skin-vanilla-weapon_knife_kukri",
        name: "★ Kukri Knife",
        rarity: {
          id: "rarity_ancient_weapon",
          name: "Covert",
          color: "#eb4b4b",
        },
        paint_index: null,
        phase: null,
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/weapons/base_weapons/weapon_knife_kukri_png.png",
      },
      // ...
    ],
    market_hash_name: "Kilowatt Case",
    rental: true,
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/weapon_cases/crate_community_33_png.png",
    model_player: "models/props/crates/csgo_drop_crate_community_33.vmdl",
  },
  // ...
]
```

### List keys

```http
GET https://bymykel.github.io/CSGO-API/api/en/keys.json
```

Example response:

```json
[
  {
    id: "key-generic_valve_key",
    name: "CS:GO Case Key",
    description:
      "This key will open any Valve Series Weapon Case. Non-Valve Series cases (e.g. eSports Case) require their own key to open.",
    market_hash_name: "CS:GO Case Key",
    crates: [
      {
        id: "crate-4001",
        name: "CS:GO Weapon Case",
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/weapon_cases/crate_valve_1_png.png",
      },
      // ...
    ],
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/tools/weapon_case_key_png.png",
  },
  // ...
]
```

### List collectibles

```http
GET https://bymykel.github.io/CSGO-API/api/en/collectibles.json
```

Example response:

```json
[
  {
    id: "collectible-874",
    name: "5 Year Veteran Coin",
    description:
      "Has been a member of the Counter-Strike community for over 5 years.",
    rarity: {
      id: "rarity_ancient",
      name: "Extraordinary",
      color: "#eb4b4b",
    },
    type: null,
    genuine: false,
    market_hash_name: null,
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/status_icons/5yearcoin_png.png",
  },
  // ...
]
```

### List agents

```http
GET https://bymykel.github.io/CSGO-API/api/en/agents.json
```

Example response:

```json
[
  {
    id: "agent-4613",
    name: "Bloody Darryl The Strapped | The Professionals",
    description:
      "Before he was leader of the heist gang 'The Professionals' Sir Bloody Darryl was more simply called, Bloody Darryl. Still your friendly neighborhood psychopath in every sense of the word. Not actually Australian according to Australians. \\n\\n<i>I'm just gonna give them a bit of Razzle Dazzle.</i>",
    rarity: {
      id: "rarity_legendary_character",
      name: "Superior",
      color: "#d32ce6",
    },
    collections: [
      {
        id: "collection-set-op11-characters",
        name: "Operation Riptide Agents",
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/set_icons/set_op11_characters_png.png",
      },
    ],
    team: {
      id: "terrorists",
      name: "Terrorist",
    },
    market_hash_name: "Bloody Darryl The Strapped | The Professionals",
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/characters/customplayer_tm_professional_varf5_png.png",
  },
  // ...
]
```

### List patches

```http
GET https://bymykel.github.io/CSGO-API/api/en/patches.json
```

Example response:

```json
[
  {
    id: "patch-5126",
    name: "Patch | FaZe Clan (Gold) | Stockholm 2021",
    description:
      "This patch can be applied to any agent you own. Once applied, it can be removed but not recovered.",
    rarity: {
      id: "rarity_mythical",
      name: "Remarkable",
      color: "#8847ff",
    },
    market_hash_name: "Patch | FaZe Clan (Gold) | Stockholm 2021",
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/patches/stockh2021/patch_faze_gold_png.png",
  },
  // ...
]
```

### List graffiti

```http
GET https://bymykel.github.io/CSGO-API/api/en/graffiti.json
```

Example response:

```json
[
  {
    id: "graffiti-1654",
    name: "Sealed Graffiti | Chabo",
    description:
      "This is a sealed container of a graffiti pattern. Once this graffiti pattern is unsealed, it will provide you with enough charges to apply the graffiti pattern <b>50</b> times to the in-game world.",
    rarity: {
      id: "rarity_rare",
      name: "High Grade",
      color: "#4b69ff",
    },
    crates: [
      {
        id: "crate-4234",
        name: "Community Graffiti Box 1",
        image:
          "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/weapon_cases/crate_spray_pack_community_1_png.png",
      },
    ],
    market_hash_name: "Sealed Graffiti | Chabo",
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/stickers/community_mix01/chicken_png.png",
  },
  // ...
]
```

### List music kits

```http
GET https://bymykel.github.io/CSGO-API/api/en/music_kits.json
```

Example response:

```json
[
  {
    id: "music_kit-39",
    name: "Music Kit | The Verkkars, EZ4ENCE",
    description:
      "The Verkkars rise through the Finnish charts with a heart-pounding tribute to ENCE. Can it really be so EZ?",
    rarity: {
      id: "rarity_rare",
      name: "High Grade",
      color: "#4b69ff",
    },
    market_hash_name: "Music Kit | The Verkkars, EZ4ENCE",
    exclusive: false,
    image:
      "https://raw.githubusercontent.com/ByMykel/counter-strike-image-tracker/main/static/panorama/images/econ/music_kits/theverkkars_01_png.png",
  },
  // ...
]
```
