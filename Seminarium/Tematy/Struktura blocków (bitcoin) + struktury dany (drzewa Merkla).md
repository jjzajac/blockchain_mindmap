---
tags: [Zajęte,Seminarium]
---


[[Bitcoin]] [[Merkle Tree]]

Struktura [[Block|blocku]]

### Wstęp

### Transakcja

#### Co to jest transakcja?
Transakcja to sturktura jest danych która reprezentuje transfer funduszy.

Block Explorer można sobie zobaczyć co bloki mają w sobie.

#### Struktura transakcji

```
{
	version : string
	locktime : string
	vin : [{
		xid 
		vout 
		sciprtsig
		sequence
	}]
	vout : [{
		value
		scriptPubKey
	}]
}
```

Transfer odbywa się między grupą transakcją. Tzn Transakcja przyjmuje tablicę wejść i wystawia listę wyjść.  Bardziej konsumuje całe [[UTXO]] i tworzy nowe [[UTXO]] 

*dygresja*
##### Balans Konta
Balans Konta w [[Bitcoin]] to jest [[UTXO]] jako lista niewydanych transakcji.

*koniec dygresji*

*dygresja*
##### Problem minera
Miner musi rozwiązać problem plecakowy aby zoptymalizować swój zysk

*koniec dygresji*

Główną rzeczą jaką trzeba śledzić jest [[UTXO]] ponieważ ona zależy od validacja.


Wyjścia transakcji składa się z:
```
Amout - wartość transakcji 
Locking-Script-Size
Locking-Script - kryptograficzne puzzle które umożliwają potwierdzenie że to nasze fundusze
```

Wejścia transakcji skłąda sie z:
```
Transaction Hash - UTXO któy korzystamy
```

Coin Base transaction:
```
Transaction Hash - 32 bytes zeros
Output Index - 4bytes ones
Coinbase Data Size 
COinbase Data - 
```

#### Język `Script`

- Forth-like język
- stosowany do blokowania [[UTXO]] i odblokowania
- nie jest [[Turing Complete]] ([[Turing INcompleteness]])
- [[Stateless Verefication]] 

### Lock + Unlock
- Locking Script z UTXO
- Unlocking z TXIN
- Locking-Script zadaje warukni umożliwając użycie środków zawartyych w UTXO
- Unlocking-Script spełnia Locking-Sciprt 
- Transakcja może być zaakceptowana tzn. musi z Locking-Sciript sklejonego z Unlocking-Script musi po wyliczeniu tego dać wartość `True`

### Najprostszy przykład
```
// Unlocking Script
<Cafe Signature> <Cafe Public Key>
// Locking Script
OP_DUP OP_HASH160 <Cafe Public Key Hash> OP_EQUALVWEIFY OP_CHECKSIG
```

#### Podpisy cyfrowe
W bitcoin są to [[ECDSA]] czyli Eliptic Curve Digital Signature Algorithm

Siganture Hash Type (SIGHASH)
Flaga która jest zawarta w Podpisie cyfrowym mówi co podpisujemy, tzn. definiuje kto może korzystać z transakcji, np. kto może przekazać gdzie chce wysłać wyjścia transakcji

Konstruowanie transakcji odbywana się po za blockchain moża przyjąć że jest podpisywanie zapomocą SIGHASH jest podobne do umów, tzn. przygotowywanie transakcji to nie musi być stworzone przez jedną osobę.

#### Struktura [[Block]]
Rozmiar max. 1mb
```
Block size = 4 bytes rozmiar w byte
Block Header = 80 byte
Transaction Counter = 1-9 bytes (varint) - ilość transakcji
Transactions - tablica transakcji
```

Header:
```
Version 4bytes
Previous Block hash 32bytes 
Merkel Root 32bytes
Timestamp 4bytes
Difficullty Target 4bytes
Nonce 4bytes
```

Teprezanracja Target:

```
target = coeffictent * 2 ^ (8 * (expontent - 3))
where:
expontent - 1 byte
coeffictent = 3 btyes
```

Digital FingerPrint to SHA256(SHA256(Block Header))


Genesis block - jest to block pierwszy w blockchain i zachardkodowany w blockchain

### Merkle tree

Struktura dancych służąca szybkiemu weryfikowaniu dużych zbiorów danych

#### Bibliografia
- Mastering Bitcoin