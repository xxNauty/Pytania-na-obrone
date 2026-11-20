# IPv4
- **długość**: 32 bity, podzielone na 4 równe oktety (8 bitów)
- **zapis dziesiętny**: cztery liczby od 0 do 255 oddzielone kropkami (np. `192.168.1.1`)
- **zapis binarny**: cztery razy po osiem cyfr 0 lub 1 (np. `11000000.10101000.00000001.00000001`)
#### Podział na dwie części
Adres IPv4 składa się z dwóch części, których podział określa maska podsieci
1. Część sieciowa (lewa strona adresu): identyfikuje konkretną sieć
2. Część hostowa (prawa strona adresu): identyfikuje konkretnego hosta w danej sieci
Przykład:
- adres IP: 192.168.1.1
- maska: 255.255.255.0
- część sieciowa: 192.168.1.xxx
- część hostowa: xxx.xxx.xxx.1
Tam gdzie w masce są 1 to należy do części sieciowej, tam gdzie są 0 do części hostowej
#### Historyczny podział adresów IP
| Nazwa klasy | Pierwszy oktet | Liczba oktetów dla sieci | Pierwszy adres IP | Ostatni adres IP | Liczba sieci                    | Maksymalna liczba adresów w sieci |
| ----------- | -------------- | ------------------------ | ----------------- | ---------------- | ------------------------------- | --------------------------------- |
| A           | 0xxxxxxx       | 1                        | 0.0.0.0           | 127.255.255.255  | 128 (7 bitów sieciowych)        | 16_777_216 (24 bity dla hostów)   |
| B           | 10xxxxxx       | 2                        | 128.0.0.0         | 191.255.255.255  | 16_384 (14 bitów sieciowych)    | 65_536 (16 bitów dla hostów)      |
| C           | 110xxxxx       | 3                        | 192.0.0.0         | 223.255.255.255  | 2_097_152 (21 bitów sieciowych) | 256 (8 bitów dla hostów)          |
| D           | 1110xxxx       |                          | 224.0.0.0         | 239.255.255.255  | ---                             | ---                               |
| E           | 1111xxxx       |                          | 240.0.0.0         | 255.255.255.255  | ---                             | ---                               |
Od roku 1997 podziała na klasy jest nieaktualny i nieużywany. Obecnie adresy IPv4 przydzielane są bez uwagi na klasę, według założeń CSDIR Classless Routing
#### Prywatne adresy IPv4
Istnieją trzy zakresy adresów IPv4, które mogą być przydzielone tylko w ramach sieci lokalnych:
1. 10.0.0.0 - 10.255.255.255 -> dla sieci prywatnych z dawnej klasy A (maska 255.0.0.0 lub /8)
2. 172.16.0.0 - 172.31.255.255 -> dla sieci prywatnych z dawnej klasy B (maska 255.240.0.0 lub /12)
3. 192.168.0.0 - 192.168.255.255 -> dla sieci prywatnych z dawnej klasy C (maska 255.255.0.0 lub /16)
# IPv6
- **długość**: 128 bitów
- **zapis**: osiem 16-bitowych bloków zapisanych w systemie szesnastkowym, oddzielonych od siebie dwukropkiem
- **skrócenie zapisu**: dozwolone jest pomijanie początkowych zer w bloku (zamiast `:0db8:`, można zapisać `:db8:`), oraz pominięcie jednego ciągu bloków składających się z samych zer. Pominięte bloki oznacza się podwójnym dwukropkiem. 
Poniższe adresy IPv6 są sobie równoważne:
- `2001:0db8:0000:0000:0000:0000:1428:57ab`
- `2001:0db8:0:0:0:0:1428:57ab`
- `2001:db8::1428:57ab`
#### Adresy specjalne
`::1/128` -> loopback, adres wskazujący na host lokalny