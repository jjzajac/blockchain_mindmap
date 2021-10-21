#tool 
## Truffle
## Instalacja:
 
```bash
npm install -g truffle
```

## Inicjalizacja repo:

Puste:
```bash
truffle init
```

Można użyć gotowych templatów: [link](https://www.trufflesuite.com/boxes).

## Struktura Repo

```
.
├── contracts
│   └── Migrations.sol
├── migrations
│   └── 1_initial_migration.js
├── test
└── truffle-config.js

```


## Komendy

### Kompilowanie [[Smart Contract]]

```bash
truffle compile
```

### Uruchamianie migracji

Odpala skrypty z domyślego folderu `Migrations`

```bash
truffle migrate
```

 #### Skrypt migracji
 
```javascript
// File: 4_example_migration.js

const MyContract = artifacts.require("MyContract");

module.exports = async function (deployer, network, accounts) {
  // deployment steps
  await deployer.deploy(MyContract);
};
```

Konwencja nazewnicza  tzn. `numer_nazwa.js` number jest wymagany aby migracje odpalały się pokolei. Funkcja może być `async` i zawierać argumenty:
1.  `deployer` - self explanatory
2.  `network` - nazwa sieci używana podczas migracji
3.  `accounts` - konta które są używane podczas migracji