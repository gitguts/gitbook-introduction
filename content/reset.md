# Cofanie zmian

Przed opublikowaniem naszych zmian poza lokalne repozytorium, jeżeli popełniliśmy błąd przy tworzeniu commitu(ów) jesteśmy w stanie zmodyfikować historię naszego repozytorium.

##### ![](/assets/git_reset_modes.png)

## Wykonywanie resetu

Do cofania zmian w repozytorium służy polecenie **reset**, którego możemy użyć w jednym z trzech trybów:

```bash
git reset --soft HEAD~<n>
git reset --soft <sha>

git reset --hard HEAD~<n>
git reset --hard <sha>

git reset --mixed HEAD~<n>
git reset --mixed <sha>
```

## Cofanie commitu

Jeżeli chcemy cofnąć zmiany dokonane w commicie lecz nie jest on najnowszym w historii (lub jeżeli chcemy by pozostał on w historii) możemy dokonać tego za pomocą polecenia:

```bash
git revert <COMMIT_SHA>
```

## Cofanie zmian w pliku

Jeżeli w naszej przestrzeni roboczej (Workspace) dokonaliśmy zmian, z których chcemy się wycofać możemy to uczynić wywołując polecenie **checkout**:

```bash
git checkout -- <FILE>
```

## Cofanie zmian z indeksu

W przypadku, gdy przez pomyłkę dodaliśmy plik do indeksu i chcemy go stamtąd usunąć lecz pozostawić na dysku (w naszej przestrzeni roboczej) wystarczy, że wykonamy polecenie **reset** w odpowiedni sposób:

```bash
git reset HEAD <FILE>
```