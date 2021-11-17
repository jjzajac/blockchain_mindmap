#### Eksperyment myślowy
Chcemy groadzić wiedę, w jakiejś bazie, oczywiście pominąć chcemy zcentralizowane bazy ponieważ premiuje ono jakieś osoby. Nie chcemy też usuwać nic z bazy ponieważ, błędna informacja też jest wartościową informacją. Czyli baza inkrementalna. Tak więc baza będzie składać się z kawałków informacji odzielonych czasem. Tak więc poźniejsze informacje mogą zależeć od przeszłych informacji. Więc musimy mieć jakąś chronologię. Tak więc każdy nowy [[Block|block]] będzie najlepiej zależeć od poprzedniego [[Block|bloku]]. Musimy w jakiś jednozanaczny sposób wyznaczć indeksy bloków. Takim rozwiązaniem jest [[Hash Function| funkcja hashująca]]. Tak więc każdy [[Block|block]] *będzie* mieć jednoznaczną interpretację. Tak więc podsumowując ten moment to mamy [[Block|bloki]] które mają jeden rodzic który też jest [[Block|blokiem]],  Tak więc w ogólności mamy drzewo nieograniczonej arności, ale pojawia się problem ponieważ chcemy mieć [[Single Source of Truth|jedną wersję prawdy]], czyli chcemy aby to był łańcuch jakiś. Więc musimy faworyzować tylko jedną ścieżkę w drzewie, aby drzewo się nie rozgalęziało.Tak więc musimy jakoś ograniczyć możliwość tworzenia nowych [[Block|block]]. Tak więc musimy wymyślić jakiś mechanizm utrudniający, [[Consensus|mechanizm konsensusu]]. Jedną metodą która przedstawi dowód że wykonaliśmy pracę, tak aby pokazać że to nasz [[Block|block]] ma być dodamy do naszej bazy. Będziemy potrzemy takiej procedury która jest [[NP|problemem  NP]]. czyli trudno wykonać obliczenia [[NP|w czasie NP]], oraz łatwo sprawdzić że wykonaliśmy obliczenia [[P| w czasie P]]. Tak więc możemy wprowadzić [[Hash Function|funkcje hashujące]], szczególnie [[Cryptographic Hash Function]]. To są funkcję które są funkcjami jedno kierunkowymi\* które
```
h: 2^* -> 2^k
```
oraz rzadko pordukują takie same wyniki.

Tak więc musimy założyć sobie używanie takiej funkcji [[Cryptographic Hash Function]] możemy zrobić zagadkę którą trzeba rozwiązać aby udowodnić wykonaną pracę. Czyli wprowadzliliśmy [[Proof of Work]]. 

#### Kryptografia asynchroniczna

##### Uproszczone RSA

```
p,q - liczby pierwsze
p*q = n
fi(n)=(p-1)(q-1)
d*e = 1 mod fi(n)

pubKey - (e,n)
privKey - (d,n)

szyforwanie:
m - message
pubKey - (e,n)
privKey - (d,n)
szyfrowanie - m^e = c mod n ; gdzie c to zaszyfrowany tekst
tak więc deszyfrowanie - c^d = m mod n ;
dowód:
	m^(e*d) = m * m ^ (fi(n)) = m bo małe twierdzenia fermata
	
pokazanie że jest to trudne:
problem jest to że faktoryzacja n jest trudna => więc wyliczenie d z e,n jest trudne

faktoryzacja n jest łatwa <= wyliczenie d jest trudne

```

Bibliografia:
RSA paper, MIler paper (dowodzi że )