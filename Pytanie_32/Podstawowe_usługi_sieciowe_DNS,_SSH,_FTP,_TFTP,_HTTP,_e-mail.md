## 1. DNS (Domain Name System)
System tłumaczący nazwy domenowe na adresy IP, dzięki czemu użytkownik nie musi zapamiętywać adresów serwerów.

**Jak działa:**
1. Użytkownik wpisuje adres domeny, np. `google.com`.
2. Komputer wysyła zapytanie do serwera DNS.
3. Serwer DNS odnajduje przypisany do domeny adres IP.
4. Komputer wykorzystuje otrzymany adres IP do nawiązania połączenia z serwerem.

- **Port:** 53 (UDP/TCP).
- **Zastosowanie:** odnajdywanie adresów IP na podstawie nazw domenowych.
## 2. SSH (Secure Shell)
Protokół umożliwiający bezpieczne, zdalne zarządzanie komputerami i serwerami za pomocą szyfrowanego połączenia.

**Jak działa:**
1. Klient SSH łączy się z serwerem.
2. Następuje uwierzytelnienie użytkownika, np. za pomocą hasła lub klucza kryptograficznego.
3. Nawiązywane jest szyfrowane połączenie.
4. Użytkownik może wykonywać polecenia na zdalnym komputerze tak, jakby pracował bezpośrednio na nim.

- **Port:** 22 (TCP).
- **Zastosowanie:** zdalne zarządzanie serwerami, przesyłanie plików (SFTP) i wykonywanie poleceń.
## 3. FTP (File Transfer Protocol)
Protokół służący do przesyłania plików pomiędzy klientem a serwerem.

**Jak działa:**
1. Klient nawiązuje połączenie z serwerem FTP.
2. Użytkownik uwierzytelnia się za pomocą loginu i hasła (jeśli serwer tego wymaga).
3. Klient może przeglądać katalogi oraz pobierać i wysyłać pliki.
4. Serwer realizuje otrzymane polecenia.

- **Port:** 21 (TCP) – połączenie sterujące; port 20 może być używany do przesyłania danych w trybie aktywnym.
- **Zastosowanie:** przesyłanie plików między komputerami.
- **Uwaga:** klasyczny FTP nie szyfruje transmisji, przez co dane i hasła mogą zostać przechwycone.
## 4. TFTP (Trivial File Transfer Protocol)
Uproszczona wersja protokołu FTP, przeznaczona do prostego przesyłania plików bez rozbudowanych mechanizmów uwierzytelniania.

**Jak działa:**
1. Klient wysyła żądanie pobrania lub wysłania pliku do serwera.
2. Serwer odpowiada i rozpoczyna transmisję.
3. Plik przesyłany jest w blokach danych, które są potwierdzane przez odbiorcę.
4. Po przesłaniu wszystkich bloków transmisja zostaje zakończona.

- **Port:** 69 (UDP) – port początkowego żądania.
- **Zastosowanie:** przesyłanie plików konfiguracyjnych, aktualizacji i obrazów systemów do urządzeń sieciowych, np. routerów.
## 5. HTTP (Hypertext Transfer Protocol)
Protokół komunikacyjny wykorzystywany do przesyłania stron internetowych i innych zasobów pomiędzy przeglądarką a serwerem WWW.

**Jak działa:**
1. Użytkownik wpisuje adres strony internetowej.
2. Przeglądarka wysyła żądanie HTTP do serwera.
3. Serwer przetwarza żądanie i odsyła odpowiedź, np. kod HTML, CSS, JavaScript lub obraz.
4. Przeglądarka interpretuje otrzymane dane i wyświetla stronę.

- **Port:** 80 (TCP) – standardowy HTTP; HTTP/3 wykorzystuje QUIC przez UDP.
- **Zastosowanie:** przeglądanie stron internetowych i komunikacja z aplikacjami internetowymi.
- **Uwaga:** HTTPS to zabezpieczona wersja HTTP wykorzystująca szyfrowanie TLS (standardowo port 443).
## 6. E-mail (poczta elektroniczna)
System umożliwiający wysyłanie i odbieranie wiadomości elektronicznych pomiędzy użytkownikami za pośrednictwem serwerów pocztowych.

**Jak działa:**
1. Nadawca tworzy wiadomość w programie pocztowym.
2. Wiadomość jest wysyłana na serwer pocztowy za pomocą protokołu SMTP.
3. Serwer nadawcy przekazuje wiadomość do serwera pocztowego odbiorcy.
4. Odbiorca pobiera lub synchronizuje wiadomość za pomocą protokołu POP3 albo IMAP.

**Najważniejsze protokoły pocztowe:**
- **SMTP (25, 587, 465 TCP)** – wysyłanie wiadomości i przekazywanie ich między serwerami.
- **POP3 (110, 995 TCP)** – pobieranie wiadomości z serwera na urządzenie.
- **IMAP (143, 993 TCP)** – synchronizacja wiadomości i folderów między serwerem a urządzeniami.
---
## Podsumowanie

| Protokół | Główne zastosowanie | Port |
|---|---|---|
| DNS | Tłumaczenie domen na adresy IP | 53 |
| SSH | Zdalne zarządzanie komputerem | 22 |
| FTP | Przesyłanie plików | 21 |
| TFTP | Proste przesyłanie plików | 69 |
| HTTP | Przesyłanie stron internetowych | 80 |
| SMTP | Wysyłanie poczty | 25 / 587 / 465 |
| POP3 | Pobieranie poczty | 110 / 995 |
| IMAP | Synchronizacja poczty | 143 / 993 |