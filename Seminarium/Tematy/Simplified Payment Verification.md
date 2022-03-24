---
tags: [Seminarium,University]
---

[[Node]] w [[Bitcoin]]:
- Wallet,
-  Miner - tworzy nowe [[Block]]
-  Full Blockchain - umożliwa weryfikację samodzielnie transakcji
-  Network Routing Node - potrzebujemy relay [[Node]] 

W [[Node]] występują tymczasowe bazy:
- mempool - niepotweirdzone czekające [[Transaction]], początkowo puste
- orphan pool - transakcje odnoszą się to nieznaych transakcji, początkowo puste
- UTXO pool - niewydane transakcje, 

##### Compact Block
streszczenie pod odbiorcę
- 80-bajtów nagłówek
- skrócony indetyfikator transakcji (podówjny SHA-256) (anty-DoS)
- wysyłamy tansakcje które nie były w jego mempool

###### Oszczędzanie miejsca 
Purned Node:
walidacja całego blok, ale zapamiętujemy tylko niewydane transakcje (+ 288 całych ze względu na osieracane)

##### SPV:
pobieramy tylko nagłówki bloków nie transakcje - bloki Merkle
walidacja zależna od innych node'ów

###### Bloom filters
wysyłane żądanie dotyczny innych niż tylko nas intersują transakcji