# Zadania

## Zadanie 1

## Zadanie 2

## Zadanie 3

## Zadanie 4 – TOKEN CSRF

Token CSRF jest najbardziej popularnym zabezpieczeniem przed atakami CSRF. Polega on na dodawaniu ukrytego pola w formularzu zawierającego losowy ciąg znaków. Tak powiązany token z ciasteczkami sesji pozwala na skuteczną weryfikację zapytań po stronie serwera. Atakujący nie jest w stanie odgadnąć tokenu ustanowionego dla danej sesji, więc każde sfabrykowane zapytanie będzie odrzucane przez serwer.

### 4.1 Generowanie unikalnego tokenu

Aby zabezpieczenie działało poprawnie, należy wygenerować unikalny token przy ustanawianiu nowej sesji, na przykład podczas logowania się przez użytkownika. Warto przechowywać taki token w zmiennej $_SESSION.

Gdzieś w tym miejscu trzeba to zrobić (*np. plik login* .php)

**tutaj screen z podpowiedzia**

### 4.2 Przekazywanie tokenu CSRF klientowi

Następnie należy przekazać token CSRF klientowi. W zapytaniach POST używa się do tego pola input z parametrem hidden. Dzięki temu token będzie przesyłany za każdym razem, gdy używamy konkretnego formularza. Robimy to w formularzu w pliku tutaj *nazwa tego pliku co bedzie wjazd na niego*.php. 

Takie pole może wyglądać w ten sposób

**tutaj screen z podpowiedzia**


### 4.3 Walidacja tokenu CSRF

Ostatnim krokiem jest weryfikacja czy dla danego zapytania token jest poprawny (lub czy w ogóle istnieje). Tutaj znowu należy coś dodać do pliku tutaj *nazwa tego pliku co bedzie wjazd na niego*.php

Można to zrobić gdzieś w tym miejscu (wystarczy prosty if sprawdzający czy token jest prawidłowy lub czy w ogóle istnieje)

**tutaj screen z pokazaniem gdzie**

Tak zaimplementowany token zabezpiecza użytkownika przed atakami CSRF, można sprawdzić jego działanie przeprowadzając jeden z ataków z poprzednich zadań. Należy jednak pamiętać, że taki token musi być zawarty w każdym zapytaniu generowanym do serwera (np. w każdym formularzu). Dodatkowo aby takie zabezpieczenie miało sens, aplikacja musi być zabezpieczona przed atakami XSS tak aby nie dało się wykraść wartości tokenu.
