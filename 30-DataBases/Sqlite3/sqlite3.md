# Sqlite3
Sqlite3 jest bazą danych która znajduje się w jednym pliku. \
Pozwala to na łątwe przechowywanie i także zarządznie nią.
Nadaje się idealnie do minimalnych baz, lokalnych, przechowywania danych do przesłania ich dalej do np. serwera


## Możliwości
Przechowywanie dużej bazy w jedntm pliku, nawet po setki GB (Nie testowałem takich wartości nie było mi to potrzebne) 

### ASP.NET
Idealna baza lokalna do przechowywania 
 
## Ogranicznie
-- Brak pełnej obsługi wielowątkowości / wysokiej równoległości
SQLite działa świetnie w aplikacjach desktopowych i mobilnych, ale przy dużej liczbie jednoczesnych zapisów (np. setki użytkowników naraz) może być wąskim gardłem.
- Brak serwera
To baza plikowa – nie ma mechanizmów typowych dla serwerów baz danych (np. zarządzania użytkownikami, replikacji, wysokiej dostępności).
- Rozmiar pliku
Choć teoretycznie obsługuje setki GB, w praktyce przy bardzo dużych plikach mogą pojawić się problemy z wydajnością i backupami.
- Ograniczone typy danych
SQLite ma dynamiczne typowanie – nie wymusza ścisłych typów jak np. SQL Server czy PostgreSQL. To czasem ułatwia, ale może prowadzić do niespójności danych.
- Brak zaawansowanych funkcji
Nie znajdziesz tu pełnej obsługi procedur składowanych, rozbudowanych mechanizmów bezpieczeństwa czy replikacji.
- Zależność od systemu plików, podatność na uszkodzenia
Jeśli plik zostanie uszkodzony , cała baza może być zagrożona.
