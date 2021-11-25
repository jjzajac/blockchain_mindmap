---
tags: [Consensus]
---


Najbardziej popularny mechanizm konsensusu istniejący między innymi w [[Bitcoin]] i [[Ethereum]]. ![[Ethereum#Zmiana mechanizmu konsensusu]] Mechanizm ten polega generowaniu nowych [[Block]], tak aby  po zastosowaniu [[Hash Function]] na [[Block]], początek hasha zawierał określoną liczbę zer. Tak więc jedyną metodą aby znaleść taki hash jest sprawdzenie każdej wartości które dodaje się do bloku nazywane `Nonce` w [[Bitcoin]].

Osoby które zajmują się generowaniem nowych [[Block|bloków]] potocznie nazywana się [[Miners|miners]].

Mechanizm ten pozwala zachować konsensu sieci ponieważ, można założyć że `1 CPU = 1 głos` przez co im więcej komputerów w sieci tym trudniej jest głosować w sposób `malicious`, jednak podlega to [[51% Attack]].

