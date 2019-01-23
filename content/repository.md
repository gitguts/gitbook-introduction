# Tworzenie repozytorium

## Konfiguracja

Przed przystąpieniem do prac z naszym pierwszym repozytorium upewnijmy się, że klient git został poprawnie skonfigurowany. Konfiguracja ta może być wykonywana na poziomie:

* pojedynczego repozytorium
* globalnym

W celu weryfikacji globalnej nazwy naszego użytkownika ora jego adresu email należy w wierszu poleceń wykonać następujące komendy:

```bash
git config --global user.name
git config --global user.email
```

Jeżeli chcemy sprawdzić całą konfigurację wystarczy wydać następujące polecenie:

```bash
git config --global --list
```

Dokumentację polecenia **git config** możemy przejrzeć wydając polecenie:

```bash
git config --help
```

## Inicjalizacja repozytorium

Mając poprawnie skonfigurowanego klienta git możemy przystąpić do tworzenia repozytorium. W pierwszej kolejności musimy utworzyć katalog, w którym będziemy je przetrzymywać i przejść do niego:

```bash
mkdir repository
cd repository
```

Inicjalizacja pustego repozytorium wymaga od nas jedynie wprowadzenia następującej komendy:

```bash
git init
```

Jeśli chcemy sprawdzić jakie zmiany wykonała ta komenda możemy sprawdzić bieżącą zawartość katalogu:

```bash
ls -al
```

W celu sprawdzenia, czy repozytorium zostało poprawnie utworzone wywołajmy w wierszu poleceń poniższą komendę:

```bash
git status
```