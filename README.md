# zst-workshop

## Przygotowanie systemu

- Instalacja git

  `sudo apt upate`

  `sudo apt install git`

- Instalacja [Google Chrome](https://support.google.com/chrome/answer/95346?co=GENIE.Platform%3DDesktop&hl=en)

  - 'Pobierz Chrome' (64-bitowy .deb)
  - `cd ~/Downloads`
  - `sudo dpkg -i nazwa-pobranego-pliku.deb`

- Pobranie repozytorium

  `git clone https://github.com/lukaszkarbownik/zst-workshop.git`

## HTML

```html
<div id="my-id" class="my-class" data-id="13">
  <h1>tytuł</h1>
  <p class="text">paragraf z tekstem</p>
  <p>kolejny tekst z paragrafem</p>
</div>
<img class="image" src="http://zst.pila.pl/images/schoolLogoWhite.png" />
```

## CSS

```css
#my-id {
  color: red;
  padding: 30px;
  margin-left: 10px;
}

.my-class {
  background-color: red;
  color: blue;
  text-align: center;
}

.my class p.text {
  color: yellow;
  width: 30%;
  height: 200px;
}

.image {
  width: 30px;
  height: 30px;
}
```

## JavaScript

### Struktury danych

```javascript
// komentarz

var a; // pusta zmienna

var b = null; // zmienna z pustą wartością

var num = 3; // zmienna z liczbą 3

var text = 'tekst'; // zmienna ze stringiem 'tekst'

var list = ['element 1', 3, 'element 2'];

list[0]; // 'element 1'
list[2]; // 'element 2'

var post = {
  title: 'tytuł postu',
  content: 'treść postu',
}; // obiekt

post.title; // tytuł postu
post['title']; // tytuł postu

var listOfPosts = [{title: 'post 1'}, {title: 'post 2'}];
listOfPosts[0].title;
```

### Funkcje

```javascript
function add(num1, num2) {
  return num1 + num2;
}

add(3, 4); // 7

var list = [1, 2, 3];
list.pop(); // 3
console.log(list); // [1, 2]

var body = document.querySelector('body');
body.addEventListener('click', function(event) {
  console.log(event.target);
});

body.textContent; // zawartość tekstowa elementu
body.style; // style css elementu
body.style.color; // kolor tekstu elementu

var container = document.createElement('div');
body.appendChild(container);

var image = document.createElement('img');
image.src = 'http://zst.pila.pl/images/schoolLogoWhite.png';
container.appendChild(image);

var titleElement = document.createElement('p');
titleElement.textContent = 'tekst dodany do paragrafu';
container.appendChild(titleElement);
```

### Tablice

```javascript
var fruits = [];

fruits[1] = 'apple'; // przypisuje lub zastępuje element pod indexem 1

fruits.push('apple'); // dodaje element 'apple' do tablicy

fruits.slice(); // zwraca kopię tablicy
fruits.slice(1); // zwraca kopię tablicy zaczynając od 2 elementu
fruits.slice(1, 3); // zwraca elementy od 2 do 4
fruits.slice(-1); // zwraca ostatni element

fruits.splice(2, 1); // Usuwa jeden element rozpoczynając od indexu 2

fruits.indexOf('apple'); // Zwraca index elementu w tablicy lub -1, gdy element nie występuje w tablicy

var movie = 'Avengers: Infinity War';
movie.indexOf('War'); // 19

fruits.forEach(function(fruit) {
  // funkcja zostanie wywołana 1 raz dla każdego elementu listy
  console.log(fruit);
});

var a = [1, 2, 3];
a.length; // 3

var b = 'apple';
b.length; // 4
```

### Pola input

```javascript
var movieNameInput = document.querySelector('.name-input');
movieNameInput.value; // zwraca aktualną wartość pola movieNameInput
movieNameInput.value = ''; // zmienia wartość pola movieNameInput na pusty string
```

### Instrukcje warunkowe

```javascript
var value = true;

if (value) {
  console.log('test');
}

if (false) {
  console.log('test');
}

var a = 'abc';
if (a.length === 3) {
  console.log('string a is 3 characters long');
}
```

### Typy danych

```javascript
typeof 'abc'; // "string"
typeof 3; // "number"
typeof true; // "boolean"
typeof {}; // object
typeof []; // object

Number('1'); // 1
String(1); // "1"
```

### localStorage

```javascript
localStorage.setItem('klucz', 'wartosc'); // zapisuje wartość pod kluczem 'klucz'
localStorage.getItem('klucz', 'wartosc'); // zwraca wartość zapisaną pod kluczem 'klucz'
localStorage.removeItem('klucz'); // usuwa wartość zapisaną pod kluczem 'klucz'
```

### JSON

```javascript
JSON.stringify([1, 2, 3]); // "[1,2,3]"
JSON.parse('[1,2,3]'); // [1,2,3]
```

### Usuwanie elementów z drzewa DOM

```javascript
var movieListElement = document.querySelector('.movie-list');
movieListElement.removeChild(movieListElement.firstChild); // usuwa pierwszy element z elementu movieListElement

// Usunięcie wszystkich elementów
while (movieListElement.firstChild) {
  movieListElement.removeChild(movieListElement.firstChild);
}
```
