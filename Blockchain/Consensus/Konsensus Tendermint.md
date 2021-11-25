## Konsensus Tendermint
 System procesów komunikujących się za pomocą widomości. Każdy proces ma jakiś voting power. Każdy proces jest połączony z peers'ami co tworzy sieć w której wszystkie procesy są ze sobą połączone w sieć niebezpośrednią tzn. ewentualnie połączone przez peers. 

#### Wiadomości w Tendermint 
- `Proposal` - sugeruje potencjalną wartość - `v` czyli blok transakcji
- `Prevote` - wiadomość podjęcia decyzji co do `Proposal` może być to z wartością zawarą w `Proposal`, lub `Nil` gdy niezgadzamy się z decyzją
- `Precommit` - próba akcepatcji [[Block|bloku]]. 


#### Tworzy to maszynę stanów
![[Tendermint_state_machine.png]]

