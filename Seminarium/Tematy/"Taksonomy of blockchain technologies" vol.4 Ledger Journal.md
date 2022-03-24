---
tags: [Seminarium,University]
---
[[Blockchain]] [[Ledger Journal]]

![[taksonomy_blockchain.png]]

[[140-Article Text-762-1-10-20190214.pdf]]

# Podział
## [[Consensus]]
### Topologia sieci
- zdecentralizowany
- hierarchiczny ( [[Consortium Blockchain]] ) - niektóre [[Node|nody]] są uprzywilejowane
- scentralizowany ( [[Private Blockchain]] )

### Niemutowalność konsensusu i błędoodporność
- [[Proof of Work]]
- [[Proof of Stake]]:
	- deterministyczne - [[Nxt]]
	- niedeterministyczne ( coin-age ) - [[Peercoin]]
	- [[DPoS]] - [[Tendermint]]
- [[Proof of Authority]] - najczęściej w [[Private Blockchain]] ponieważ są węzły które mogą podpisywać [[Block|bloki]] 
- [[Proof of Space]]/[[Proof of Capacity]]/[[Proof of Storage]] - 
- [[Proof of Burn]] -  [[Counterparty]]
- Hybrydowe - 

### Plotkowanie (gossiping)
- lokanie - Ripple, najczęściej konsensus jest osiągany lokalnie, [[Federated Consensus]]
- globalnie - większość [[Blockchain]]

### Konsensus Agreement
- Opóźnienie:
	- komunikacja synchroniczna - np. [[Bitcoin]], [[Block|bloki]] musi mieć timestamp z określonego przedziału
	- komunikacja asynchroniczna - [[Synereo]] 
- Finalność:
	- niedeterministyczne - [[Bitcoin]], [[Blockchain]] wkońcu się 
	- deterministyczne - [[Stellar]] [[Lamport Byzantine Fault Tolerance]]
## [[Transaction]]

### Struktura danych 
- [[Merkle Tree]]
- [[Patricia Merkle Tree]]
### Model transakcji
 - [[UTXO]] - model jak w [[Bitcoin]], transakcja to suma wszystkich nie wydanych tansakcji oraz wyjście to kolejne niewydane transakcje
 - [[Traditional Ledger]] - [[Stellar]] [[Ripple]]
### Server Storage
- Full [[Node]] Only
- Thin [[Node]] Capable - pozwala 
### [[Block]] Storage
- [[Transaction]]
- User Balance

### Ograniczenia Skalowalności
- liczba [[Transaction|transakcji]]
- liczba użytkowników - [[Ripple]] 
- liczba [[Node|nodów]]
- czas potwierdzenia
- możliwe wartości wzrostu (jako bazy danych):
	- niezależnie
	- liniowo
	- najwyżej kwadratowo
	- gorzej niż kwadratowo


## Native Currency 
### Native Asset
- Brak
- własna waluta
- Convertible Multiple Assets.

### Tokenisation
- brak - jak [[Bitcoin]]
- throught 3-rd party
- obecna - [[Smart Contract]]

### Zarządzanie dostawcami aktywów
- limitowane-deterministyczne -[[Bitcoin]]
- nielimitowane-deterministyczne - [[Dogecoin]]
- pre-mined

## Rozszerzalność
### Interoperacyjność
możliwość komunikacji ze światem
- niejawna (język skryptowy [[Turing-Complete]] )
- jawna - [[Bitcoin]] + [[Counterparty]]
- brak - [[Bitcoin]]

### Intraoperability
- niejawna (język skryptowy [[Turing-Complete]] )
- jawna - [[Bitcoin]] + [[Counterparty]]
- brak - [[Bitcoin]]

### Zarządzanie
- [[Open Source]]
- Technical
- Alliance

### Język skryptowy
- Turing Complete
- Generic Non-Turing Complete
- Application-Specific Non-Turing Complete
- Non-Turing Complete + External Data
-
## Bezpieczeństwo i Prywatność
### Data Encryption
- [[SHA-2]]
- ZK-SNARKS - The Zero-Knowledge—Succinct Non-interactive Argument of Knowledge
### Data Privacy
- Built-In Data Privacy - [[ZeroCash]] (kryptografia z wiedzą zerową) , [[Enigma]] , Corda
- Add-On Data Privacy
	- mieszanie [[Transaction|transakcji]] M-N w [[Block|blocku]]
	- ring signatures
	- stealth addresses - [[Monero]]
## Baza kodu
### Języki programowania
 - jeden
 - wiele

### Licencja
- [[Open Source]]
- Close Source

### Architektura
- Monolithic
- Polylithic
## Zarządzanie tożsamością
### Access and Control Layer
- [[Blockchain]] publiczne
- permissioned public [[Blockchain]] - Ripple
- permissioned private [[Blockchain]] - Monax

### Identity Layer
- KYC/AML - (Know-Your-Customer / Anti-Money-Laundering)
- Anonymous (pseudoanonimowe)
## Charging and Rewarding System
### Reward System
- Lump-Sum Reward
- Block + Security Reward

### Fee System
- Optional Fees
- Mandatory Fees
- No Fee

### Fee Structure
- Variable Fees - [[Bitcoin]]
- Fixed Fees - [[Enigma]]