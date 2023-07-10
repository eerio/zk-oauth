# zk-oauth
pomysl jest taki:  
logowanie sie do serwisow przez np. konto Google jest bardzo wygodne  
ale do Google trzeba sie zalogowac haslem  
haslo trzeba pamietac, ale sie go nie pamieta  
fajny pomysl to:  
niech haslo bedzie konkatenacją odpowiedzi na pytania kontrolne  
odpowiedzi na pytania kontrolne znamy my + pewna mała i bliska nam grupa ludzi  

np.: jak się nazywa kolega który wpadł do rzeki na wycieczke w podstawówce (ten w siwych włosach)? pierwsza litera z dużej, reszta małe, zachowując znaki spoza ascii

to jest coś czego się nie zapomina, a nawet jeśli byśmy stracili pamięć  
(np. w wypadku), to dana grupa ludzi *będzie* to pamiętać.  

problemy są 2:  
* po pierwsze, entropia takich odpowiedzi nie jest najwyższa; do ułożenia jednego hasła będziemy potrzebować 6-7 takich sekretów  
* po drugie, nie chcemy żeby nam te sekrety wyciekły, bo mamy ich w życiu ograniczoną liczbę + są dużo bardziej prywatne niż zwykłe hasło  

rozwiązanie to Zero-Knowledge proof of Knowledge.  
robimy ZK proof na znajomość sekretu. są od tego protokoły których nie rozumiem: zk-SNARKs.  
pomysł jest taki, by postawić serwis webowy, który będzie nas autentykować przez OAuth 2.0,  
ale tylko po pomyślnym przeprowadzeniu dowodu *znajomości* sekretu.  

najlepiej by było jakby to wszystko działało na blockchainie (Ethereum albo ZCash?) żeby te operacje były transparentne, dobrze zaimplementowane i weryfikowalne itp.
