# Logowanie

Istnieje wiele sposobów na formatowanie historii repozytorium. Najczęściej wykorzystywane to:

```bash
git log -<n>
git log -p
git log --stat
git log --graph
git log --oneline
git log --pretty=oneline|raw|short|full|fuller|format=“”
```

Sprawdzenie zmian wprowadzanych w pliku:

```bash
git log <FILE>

git log -1 <FILE>
```

Sprawdzenie zmian z wybranego commitu:

```bash
git show <SHA1>
```