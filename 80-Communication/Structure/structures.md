# (PL) Struktury Projektowe
## MAUI 1
Za pomocą MAUI można spokojnie robić aplikacje, gry na każde urządzenie. MAUI posiada wiele wad ale umożliwai takei rozwiązanie.
- Blazor wizualia, UI, zadbanie o wygląd strony/aplikacji
- SQL ( Najlepiej chyba urzyć sqlite3 do małych baz z danymi, choć jest dobra nawet do dużej. Istnieje możliwość zakodowania takiej bazy i łączenia się przez aplkacje, bardzo użyteczne do zapisywaniu zmian przez wysłaniem na serwer.
-  



# Structures 
## Structure -> ASP.NET + Azure SQL + MAUI/Web Architecture
1. ** Client (MAUI/Web) **
- `HttpClient` or   Refit`  -> API endpoints.
- JWT/Azure AD B2C Authentication , build new authentication 

2. ** ASP.NET Core web API **
- Application logic
- Infrastructure logic -> query -> Azure SQL
- Controlles, REST endpoints

3. ** Azure SQL Database**
- Connection secured Key Vault Identity Manager
- Automatic backup

## Structure -> 
## Structure -> 
