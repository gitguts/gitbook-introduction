# Zdalne repozytoria

Praca w zespole oznacza konieczność dzielenia się naszymi dokonaniami z innymi. W tym celu najlepszym sposobem jest skorzystanie z konceptu zdalnych repozytoriów w systemie kontroli wersji git.

##### ![](/assets/git_remote_repository.png)

Na powyższym rysunku przedstawiona jest sytuacja, gdy połączeni jesteśmy z jednym zdalnym repozytorium. W systemie git możliwe jest łączenie lokalnego repozytorium z dowolną ilością zdalnych repozytoriów:

##### ![](/assets/git_multiple_remote_repositories.png)

## Łączenie z repozytorium

Po utworzeniu rezpozytorium w serwisie GitHub należy je połączyć z naszym lokalnym repozytorium w następujący sposób:

```bash
git remote add origin <REPOSITORY_URL>
```

W celu opublikowania dotychczasowych zmian w repozytorium wykonujemy następujące polecenie:

```bash
git push -u origin <BRANCH>
```

## Pobieranie zmian z repozytorium

W trakcie naszej pracy, nasi koledzy i koleżanki z zespołu dokonują swoich kontrybucji i publikują je w zdalnym repozytorium. Aby móc pobrać ich zmiany należy wykonać następujące polecenie:

```bash
git pull
```