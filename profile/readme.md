# WE BE BALLIN'

# Jak to ma działać?

## Na czym polega realizacja projektu?
1. Dostajemy projekt do wykonania np. aplikacja ScreenTime dla Karwatki
2. Tworzymy repozytorium. Można to zrobić na dwa sposoby:
   - Repozytorium pojedyńcze:
     - `weballin-inc/Gerard-ScreenTime`
     - `weballin-inc/Gerard-PythonMath`
   - Repozytorium zbiorcze:
     - `weballin-inc/Gerard-UniProjects`
3. W `weballin-inc/Projects` tworzymy work item (_Issue_):
   - Title: `[Nazwa Projektu]` - `Nazwisko wykładowcy`
   - Description: _Dowolny_
   - Assignees: Osoby zaangażowane w projekt (kilka, jeśli to projekt grupowy)
   - Label: Zajęcia np. `Programowanie Obiektowe`
   - Issue type: `Uni-Project` (w przypadku podania `Task`, item ten nie pokaże sie na tablicy)
   - W szczegółach itemu > Projects ustaw Priority, Target Date i Start Date wedle uznania. 
     <img width="403" height="346" alt="image" src="https://github.com/user-attachments/assets/a759b9ee-39d6-45fe-95d8-ca61a66b80f7" />
     <img width="320" height="236" alt="image" src="https://github.com/user-attachments/assets/3652a506-7eb8-481e-8dff-10477a848e71" />
4. W czasie realizacji projektu aktualizuj work item na tablicy, umieszczając go w odpowiednich kolumnach:
   - **Chłodnia** - _Backlog_ dla wszystkich projektów zaplanowanych, gdzie sprawa nie jest pilna.
   - **Obrane** - _To Do_, gdzie znajdują się projekty do realizacji.
   - **Gotowanie** - _Work In Progress_, projekty które obecnie są rozwijane.
   - **Podawanie** - Kontener na wszystkie ukończone projekty, ale potrzebujące ostatnich szlifów przed oddaniem.
   - **Wydane** - Projekty wysłane do wykładowcy, oczekujące na ocenę.
   - **Zjedzone** - Projekty które zostały ocenione, sprawa zamknięta.
5. W przypadku zmiany repozytorium, można użyć akcji `Transfer Issue` aby przenieść work item do docelowego repo.
  
## Repozytoria
Repozytoria z projektami można utworzyć na dwa sposoby

### Repozytoria pojedyńcze
Zasada "jedno repo na każdy projekt".
- Nazwa repozytorium: `Imię-TytułProjektu` np. `Gerard-ScreenTime`
- Branch `master` jest finalną wersją rozwiązania projektowego.
- Work Itemy projektowe są przypisane do konkretnego repozytorium, do brancha `master`.

### Repozytoria zbiorcze
Zasada "wszystko w jednym miejscu, łatwo dostępne"
- Nazwa repozytorium: `Imię-UniProjects` np. `Gerard-UniProjects` (ogólna nazwa, nie musi być taka sama)
- Branch `master` służy jako zbiór wszystkich projektów, punkt startowy dla projektów powiązanych (gdyby się chciało rozwinąć jakiś konkretny)
- Osobne branche niosące nazwę projektu np. `ScreenTime`, które służą jako punkty wyjściowe dla `Releases`.
  - Release'y działają na zasadzie tagowania konkretnych commitów - więc w przypadku "dodania czegoś w wyniku sklerozy" trzeba będzie otagować najświeższego commita i utworzyć z nim release ponownie.
- Work Itemy projektowe są przypisane do konkretnego brancha.
- Finalne wersje rozwiązań mogą zostać przesłane jako source code z release'a, lub jako osobne repozytorium będące kopią brancha.

## Słowniczek 👍
- **Git**: System kontroli źródła: język githuba do kontrolowania wersji programów:
  - **Commit** to operacja zatwierdzenia zmian wprowadzonych w kodzie, aby zpushować commit do remote'a należy dołączyć komentarz do niego
  - **Push** to operacja przesłania wersji lokalnej (`local`) programu do zdalnego repozytorium (`remote`)
  - **Pull** to operacja ściągnięcia wersji programu ze zdalnego repozytorium na lokalną maszynę
  - **Branch** to odgałęzienie kodu od jego głównej wersji (`master`/`main`), służy utrzymaniu porządku gdy kilka nowych funkcji jest wprowadzanych jednocześnie (np. branch `button-fix`)
  - **Merge** to operacja zespolenia danego brancha z gałęzią główną (np. `button-fix` trafia do `master`, i staje się oficjalną częścią aplikacji)
  - **Pull Request** (**Nie mylić z Pull**) to deklaracja operacji merge, najczęściej wymagająca akceptacji przez osobę odpowiedzialną za repozytorium. (np. *Requesting merge `button-fix` to `master` branch*)
  - **Fork** to operacja sklonowania całego repozytorium na własny użytek, np. w celu odosobnionej pracy nad cudzym kodem.
  - **`.gitignore`** - Plik, który zawsze warto dodawać do swojego repo, bo pozwala uniknąć niepotrzebnego zaśmiecania commitów plikami konfiguracyjnymi twojego IDE
