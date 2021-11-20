---
tags : [Tutorial]
---
# [[Solidity]] setup
  
## quick setup
webowy IDE do [[Solidity]]: [[Remix]].

## lokalny setup
[[Ganache]], lokalną wersję node'a [[Ethereum]]: [link](https://www.trufflesuite.com/ganache).

[[Truffle]] czyli dev suite do kompliacji, testowania, ogólne CLI [[Smart Contract]].
 
```bash
npm install -g truffle
```

### Bootstrap projektu

Można użyć gotowych templatów: [link](https://www.trufflesuite.com/boxes).

Albo zacząć od 'pustego' projektu:

```bash
truffle init
```

Jeśli chcemy korzystać z [[Ganache]] do deploy naszych [[Smart Contract]] musimy dodać, musimy dodać w pole `port`, port [[Ganache]]:
```javascript
// file: truffle-config.js
module.exports = {
	// ... 
	networks:{
	// ... 
		development: {
			host: "127.0.0.1",
			port: PORT,
			network_id: "*",
		},
	// ... 
	},
	// ... 
};
```

