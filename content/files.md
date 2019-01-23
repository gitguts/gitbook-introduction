# Operacje na plikach

Celem narzędzi typu SCM jest zarządzanie kodem, a więc plikami tekstowymi. Na samym początku utworzymy pusty plik tekstowy:

```bash
touch report.csv
```

Sprawdźmy jaką informację otrzymamy, gdy wywołamy polecenie status:

```bash
git status
```

## Budowa repozytoroim

Lokalne repozytorium git składa się z kilku części, między którymi zawartość naszego pliku będzie przenoszona.

##### ![](/assets/git_repository_structure.png)

Przepływ treści w naszym repozytorium (w dużym uproszczeniu) możemy przedstawić następująco:

##### ![](/assets/git_repository_file_flow.png)

## Index (staging area)

Nim zapiszemy wersję naszego dokumentu musimy "przenieść go" z przestrzeni roboczej (Workspace) do Indeksu (lub inaczej zwanego Staging Area). W tym celu wykonajmy polecenie:

```bash
git add report.csv
```

Index jest miejscem, gdzie przechowujemy zawartość naszych plików, nie same pliki. W celu zobrazowania tego zmodyfikujmy zawartość pliku **report.csv** i sprawdźmy w jakim stanie będzie nasze repozytorium:

```bash
git status
```

Aby zaktualizować plik **report.csv** w indeksie należy ponownie wykonać polecenie **git add**:

```bash
git add report
```

## Zapisywanie zmian

Po zakończonej pracy z naszym plikiem - przyszła pora na zapisanie go w repozytorium. W tym celu wykonajmy następujące polecenie (którego wynik za chwilę omówimy):

```bash
git commit -m "Initial report for 2019."
```

Aby upewnić się, że nasze zmiany zostały poprawnie zapisane sprawdźmy historię naszego repozytorium oraz jego aktualny status:

```bash
git log

git status
```