Bridge to mechanika polegająca na pzesyłaniu [[Cryptocurrency|cryptowalut]] bądż [[Token|tokenów]] czy [[NFT]]. Zależy nam aby wartość aktywów które przerzucamy między [[Blockchain|chainami]] była taka sama. Najczęściej opiera się o mechanikę [[Lock-and-Mint-Burn-and-Release]]. 
*Przykład*
Tak więc z [[Blockchain|chain A]] chcemy przesłać [[Cryptocurrency|walutę]] do [[Blockchain|chain B]]. Tak więc do [[Bridge]] wysyłąmy fundusze z [[Blockchain|chain A]], [[Bridge]] [[Lock-and-Mint-Burn-and-Release#Lock|blokuje]] je i [[Lock-and-Mint-Burn-and-Release#Mint|mintuje]] na [[Blockchain|chain B]].
*Dygresja*
Tutaj trzeba się zatrzymać aby powiedzieć jak jest to realizowane. Ponieważ najczęściej posługujemy się [[Wrapper Token]], tzn tworzymy na naszym [[Blockchain|chainie]] [[Token|token]] który reprezentuje inny [[Token|token]]  czy [[Cryptocurrency|walutę]]. Trzeba też wspomnieć o tym że [[Wrapper Token]] ma być równoważny [[Token]]. Czyli np. istnieje `tBTC` czyli [[Wrapper Token]] [[Cryptocurrency]] [[Bitcoin]] który istnieje na [[Blockchain|chainie]] [[Ethereum]]. Mechanika [[Lock-and-Mint-Burn-and-Release]] zapewnia że [[Token|token]] jak i jego [[Wrapper Token]] będą tyle samo warte. 
*Koniec dygresji*
Jeśli chcemy dostać nasze [[Lock-and-Mint-Burn-and-Release#Lock|zablokowane]] [[Token|tokenów]] to musimy [[Lock-and-Mint-Burn-and-Release#Burn|zpalić]] [[Wrapper Token]], aby bridge mógł oddać nam [[Token|token]] z [[Blockchain|chain a]].
*Koniec Przykladu*
Tak więc Bridge umożliwia nam 


### Eksperyment myślowy 
identity jako nawiązanie do bridge
bridge jako punkt granbiczny który zmienia dokumenty