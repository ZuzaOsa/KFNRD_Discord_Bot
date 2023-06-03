# KFNRD_Discord_Bot
## Instalowanie potrzebnych rzeczy
```shell
sudo apt update
sudo apt upgrade
sudo snap install --classic node
sudo snap install --classic code
```
Pliki w JavaScript mają rozszerzenie .js. Stwórzcie sobie jakiś testowy folder, otwórzcie go w VSCode (File > Open Folder) a następnie stwórzcie w nim nowy plik z rozszerzeniem .js. VSCode powinien sam wykryć jeżeli nie macie zainstalowanego rozszerzenia do tego języka i w prawym dolnym rogu podpowiedzieć aby zainstalować (recommended extensions).

# Podstawy języka Javascript
W VSCode po zainstalowaniu node.js możemy łatwo uruchamiać programy klikając klawisz F5, przy pierwszej kompilacji pokaże nam się lista z której musimy wybrać opcję node.js i kliknąć Enter. Napiszmy podstawowy program w tym języku:

```js
console.log("Hello world!");
```
Po kliknęciu F5 powinno pojawić się na dole okienko z wypisanym tekstem Hello World!

Deklaracja zmiennej w JavaScript wygląda tak:
```js
//inicjalizujemy zmienną nazwa, ale ma ona niezadeklarowaną wartość (undefined)
let nazwa;
console.log(nazwa);
```
```js
//inicjalizujemy zmienną nazwa i przypisujemy jej wartość 3
let nazwa = 3;
console.log(nazwa);
```
```js
//inicjalizujemy zmienną nazwa i przypisujemy jej dany tekst
let nazwa = 'tekst';
console.log(nazwa);
```
Przy deklaracji w JavaScript nie definiujemy typu zmiennej, inaczej niż jak np. w C++ musimy zdefiniować int nazwa lub string nazwa. Aby w JavaScript deklarować jakiś tekst możemy używać zamiennie ' lub ". Jest to przydatne gdy chcemy mieć dany znak w tekście na przykład jeżeli chcemy zadeklarować tekst I'm a cat! taki kod nam się nie skompiluje (dlaczego?):
```js
let nazwa = 'I'm a cat!';
console.log(nazwa);
```
ale taki już tak (dlaczego?):
```js
let nazwa = "I'm a cat!";
console.log(nazwa);
```
JS ułatwia nam pisanie niektórych operacji arytmatycznych, możemy na przykład napisac:
```js
let a = 1;
let b = 2;
a += b; //zamiast a = a + b;
console.log(a);
a -= b; //zamiast a = a - b;
console.log(a);
//itd., inne operatory to między innymi * (mnożenie), / (odejmowanie), % (reszta z dzielenia), ** (podnoszenie do potęgi)
a++; //zamiast a += 1; lub a = a + 1;
console.log(a);
a--; //zamiast a -= 1; lub a = a - 1;
console.log(a);
```
## Smaczki JS:
Jakich wyników poniższych kodów się spodziewacie:
```js
// numeric string used with + gives string type
let wynik;

wynik = '3' + 2; 
console.log(wynik);

wynik = '3' + true; 
console.log(wynik);

wynik = '3' + undefined; 
console.log(wynik);
```

A w takim razie co wypisze taki kod:
```js
let wynik;

wynik = '4' - '4'; 
console.log(wynik);

wynik = '4' - 4;
console.log(wynik);

wynik = '4' * 2;
console.log(wynik);

wynik = '4' / 2;
console.log(wynik);
```
## Intrukcje warunkowe - zrób coś jeżeli coś jest spełnione
```js
let wynik = 1;
if (wynik > 1) {
    console.log("Większe od 1");
}
else if (wynik == 1) {
    console.log("Równe 1");
}
else {
    console.log("Mniejsze od 1");
}
```
Co się stanie gdy zmienicie wartość zmiennej wynik lub zmienicie warunki w if? Dozwolone operacje to ==, >=, <=, >, <, !=

## Pętle while i for
```js
//zadeklaruj i = 1, dopóki warunek (i mniejsze lub równe 5) jest spełniony wykonaj kod pętli, zwiększ i o 1
for (let i = 1; i <= 5; i++) {
    console.log(i);
} 
```
Zaimlementuj pętlę iterującą się zamiast od 1 do 5 to od 5 do 1. Zaimplementuj pętlę iterującą się po liczbach parzystych od 0 do 10.
```js
//dopóki warunek jest spełniony to wykonuj kod pętli
let i = 1;
while (i <= 5) {
    console.log(i);
    i++;
}
```
Uwaga częsty błąd popełniony nawet przez doświadczonych programistów i nagle dostajemy ekran pełen jedynek (lub crash VSCode, więc polecam nie odpalać u siebie):
```js
let i = 1;
while (i <= 5) {
    console.log(i);
}
```

## Funkcje
Często będziemy chcieli dany kawałek kodu wykorzystać wiele razy lub podzielić sobie kod na więcej bloków aby wygodniej nam się go czytało. Pomagają w tym funkcje czyli bloki kodu do których możemy się odwoływać. Mogą one zwracać coś lub nie:
```js
function add_and_write(a, b) {
    console.log(a + b)
}

function add_and_return(a, b) {
    return a + b;
}
add_and_write(1, 2);
console.log(add_and_return(1, 2));
```

Napisz funkcję która sprawdza czy dana liczba jest pierwsza i zwraca true jeżeli tak lub false w przeciwnym wypadku. Następnie użyj jej aby wypisać liczby pierwsze mniejsze od 100. Dla chętnych: Zastanów się czy Twój kod można jakoś ulepszyć, czyli sprawić aby wykonywał mniej operacji?

