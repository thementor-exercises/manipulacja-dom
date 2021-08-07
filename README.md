# manipulacja-dom

Document Object Model:
- Document - dokument czyli struktura i zawartość strony web
- Object - bo "window.document" jest zmienną wbudowaną reprezentującą obiekt "document"
- Model - chodzi tu o strukturę. W tym wypadku strukturę "drzewa"

Często mówi się o drzewie dom, albo o strukturze drzewa dom. Chodzi o nic innego jak o zawartość dokumentu. Może to być jego część, bądź trzon czy całość np.

<!DOCTYPE html>
<html>
  <head></head>
  <body></body>
</html>

jest standardową strukturą drzewa dom w stronach internetowych.

!DOCTYPE - to typ dokumentu. W tym wypadku html
html - to znacznik otwierający html
head - to nagłówek w którym znajduje się dodatkowa zawartość jak skrypty czy stylesheets (css), ale też fonty i metadane (keywords, title, subtitle itd. używane w silnikach wyszukiwarek typu google).
body - to zawartość strony do której można się dostać poprzez właściwość (property) obiektu "document"

document.body, bądź window.document.body

## DOM - to interfejs API do zarządzania strukturą dokumentu

czyli struktura DOM / struktura dokumentu, czy drzewo DOM / dokumentu to inne pojęcia jak sam DOM. DOM często służy jako zamiennik dla dokumentu jednak to nie to samo. DOM to API, dokument to obiekt.

stwórzmy za pomocą API element html "div", najczęściej używany element o właściwościach "blokowych".

var div = document.createElement("div");
console.log(div); // <div></div>

stworzony element posiada swoje API którego możemy użyć do zarządzania tym elementem.

Zadanie:
Odpal komendę "npm install", a następnie postaw serwer za pomocą "npm start".

Bazą będzie tego co jest w pliku index.html. Stwórz w pliku scripts.js skrypt który będzie tworzyć za pomocą API DOM x elementów div wewnątrz elementu div o id "printer". X jest podane w atrybucie "data-count" w elemencie o id "printer". Niech każdy stworzony element div zawiera numer indexu (1:x) jako tekst (textContent).