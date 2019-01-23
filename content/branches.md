# Operacje na gałęziach (branches)

Zarówno w programowaniu jak i w księgowości spotykamy się bardzo często z sytuacją, w której potrzebujemy wypróbować (przetestować) inną wersję projektu (naszych plików). Do tego typu operacji idealnie nadaje się mechanizm operacji na gałęziach (czyli tzw. branchach).

Do wypisania listy gałęzi w naszym lokalnym repozytorium posłużymy się następującym poleceniem:

```bash
git branch
```

## Tworzenie nowej gałęzi

Jeśli chcemy stworzyć nową gałąź potrzebujemy wywołać polecenie **branch** z dodatkowym argumentem będącym nazwą tworzonej gałęzi:

```bash
git branch refactoring
```

W celu przełączenia naszego repozytorium na nowo utworzoną gałęź wystarczy wpisać w wierszu poleceń:

```bash
git checkout refactoring
```

W systemie kontroli wersji git istnieje wiele sposobów na osiągnięcie jednego celu. Przykładowo jeśli chcemy stworzyć nową gałąź i w jednym poleceniu się na nią przełączyć - powyższe dwa polecenia (**branch** i **checkout**) możemy zastąpić jednym:

```bash
git checkout -b refactoring
```

## Dokonywanie zmian w nowej gałęzi

Będąc na branchu refactoring stwórzmy nowy plik z dowolną zawartością:

```bash
echo 'Example content for new file.' > example.txt
```

Zapiszmy nowy plik, uznając pracę nad nim za chwilowo zakończoną:

```bash
git add example.txt
git commit -m "Example.txt file."
```