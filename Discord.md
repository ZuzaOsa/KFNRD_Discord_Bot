Skoro umiemy już trochę JavaScript czas przejść do pisania własnych prostych botów. Najpierw jednak musimy go stworzyć.
## Setup
Stwórzcie nowy folder w którym stworzycie swój projekt, a następnie przejdzcie do niego w konsoli (cd nazwa_folderu). Juz gdy jesteście w tym folderze uruchomcie poniższe komendy:
```shell
npm init -y
npm install discord.js
```
Teraz jak już mamy folder na bota musimy stworzyć go rzeczywiście na Discordzie. W tym celu musimy stworzyc sobie konto na platformie Discord i uruchomić na nim 2FA(2 Factor Authentication). Discord tak sprawia aby konta z których tworzone są boty były bezpieczniejsze. Gdybyśmy pisali bota który jest dodany do jakiegoś dużego serwera i ktoś wykradłby nasze hasło to mógłby wgrać swój kod bota i np. usunąć wszystkie wiadomości, wszystkie osoby z danego serwera itp. Po tym kroku możemy wejść w [Discord Developer Portal](https://discord.com/developers/applications).

## Tworzenie i ustawienia bota
Gdy jesteśmy już na tej stronie mamy opcję stworzenia New Application. Musimu nadać naszemu botowi nazwę, a następnie trafiamy na stronę dalszej konfiguracji. Możemy dodać zdjęcie profilowe i opis naszego bota. 