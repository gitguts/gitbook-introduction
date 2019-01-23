# Łączenie gałęzi

Pracując nad dwoma wersjami projektu przychodzi taki czas, że chcemy je ze sobą skonsolidować. Nie ma potrzeby ręcznego przenoszenia (kopiowania) zmian z jednej gałęzi i odtwarzania ich na drugiej.

Proces łączenia dwóch gałęzi historii w jedną jest następujący:

* przełączamy się na branch, na który chcemy nanieść zmiany
* wykonujemy polecenie łączenia (**merge**)
* rozwiązujemy konflikty (jeśli takowe powstały)

## Łączenie bez konfliktów

Jeżeli chcemy nanieść zmiany z gałęzi **refactoring** na gałąź **master** musimy wykonać następujące polecenia w terminalu:

```bash
git checkout master

git merge refactoring
```

Łączenie to odbyło się bez konfliktów. Sprawdźmy jak wygląda obecnie historia naszego repozytorium:

```bash
git log
```

W celu przedstawienia historii w bardziej graficzny sposób wystarczy zmodyfikować powyższe polecenie:

```bash
git log --graph
```

## Łączenie z konfliktami

Aby zademonstrować proces rozwiązywania konfliktów w naszym repozytorium utwórzmy nowy branch:

```bash
git checkout -b conflicts
```

Zmodyfikujmy zawartość pliku example.txt zamieniając tekst w nim zawarty na dowolny inny. Zapisujemy zmiany na naszej gałęzi:

```bash
git add example.txt

git commit -m "Changes from conflicts"
```

Przełączmy się teraz na branch master i dokonajmy analogicznej modyfikacji w pliku example.txt (lecz z inną treścią):

```bash
git add example.txt

git commit -m "Changes from master"
```

Jeżeli będąc na branchu master zechcemy nałożyć zmiany z gałęzi **conflicts** - operacja zostanie przerwana ze względu na zainstniałe konflikty:

```bash
git merge conflicts
```

Sprawdźmy w jakim stanie po przerwaniu operacji łączenia znajduje się nasze repozytorium:

```bash
git status
```

Aby dokończyć operację łączenia należy otworzyć plik **example.txt** i ręcznie rozwiązać konflikty. W celu dokończenia procesu wykonujemy następujące polecenia:

```bash
git add example.txt

git commit
```

Polecenie **commit** wywołujemy bez dodatkowych argumentów - dzięki temu treść commitu łączącego nasze gałęzie (rozwiązującego zainstniałe konflikty) jest automatycznie dla nas przygotowana. Zobaczmy jak po rozwiązaniu konfliktów wygląda nasze repozytorium:

```bash
git log --graph
```

## Usuwanie gałęzi

Po zakończonej pracy na gałęzi conflicts możemy zechcieć ją usunąć. Aby tego dokonać wystarczy wywołać polecenie:

```bash
git branch -D conflicts
```
