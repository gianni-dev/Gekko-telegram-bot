# Gekko-telegram-bot

## GUIDA COMPLETA BOT TELEGRAM PER GEKKO BOT(ANCHE PER NEWBIE)



**Il bot permette di riceve in live segnali di buy o sell a seguito della strategia usata.**

**Interfaccia a riga di comando (CLI) di Gekko Come utilizzare il bot di Telegram per interrogare prezzi e guadagni**

L'interfaccia a riga di comando di Gekko è  adatta per l'esecuzione di strategie di trading o backtest aventi una grande quantità di dati: consuma basse risorse  ed è veloce. **l'unico svantaggio della CLI è che non è in grado di generare grafici di trading, ed è più difficile da monitorare in tempo reale, quindi puoi usare i plugin di Gekko per compensare questo.** Il bot di Telegram può interrogare direttamente il prezzo corrente e le entrate di negoziazione del robot creato da Telegram. 

INIZIO GUIDA:

![enter image description here](https://3.bp.blogspot.com/-oB8dPwDbibg/Wnr1mBcLVEI/AAAAAAAACLQ/uNBdy0Dt-jEfglMJ6efpVAypJj2rVHzGwCLcBGAs/s1600/2018-02-07_204810.jpg)

_Per prima cosa devi accedere al tuo account Telegram, quindi_ **_utilizzare /_** [_newbot_](https://telegram.me/BotFather) **_con BotFather per richiedere un nuovo robot,_** _quindi ti chiederà il nome e l'account del robot. Dopo aver risposto a tutte le domande, verrà generato un token Bot. 
Riempilo in config.js. (SI RIFERISCE AL FILE “sample-config.js” da RINOMINARE IN “config.js” NELLA DIRECTORY PRINCIPALE DI GEKKO)_


![enter image description here](https://4.bp.blogspot.com/-nABjBTUuMi0/Wnr2exE45SI/AAAAAAAACLY/BqNy2h6e7yY4AcT7vIUFCPlANW2NgQGLwCLcBGAs/s1600/2018-02-07_205146.jpg)

    config.telegrambot = {  
    enabled: true,  
    emitUpdates: true,  
    token: ' **Your Bot Token** ',  
    botName: ' **Your Bot Username** '  
    }

_Quindi inserisci il codice sopra in config.js nella cartella Gekko,_ **_cambia il token nel token Bot che hai appena ottenuto e botName(DA AGGIUNGERE MANUALMENTE poiché NON è PRESENTE) è il nome utente bot che hai appena ottenuto._**

  
![enter image description here](https://3.bp.blogspot.com/-ZQD-DeNRvbk/Wnr4YgSuHVI/AAAAAAAACLo/x5agGzwFDnME_JZS2G1reE2bVt1PNybVACLcBGAs/s1600/2018-02-07_210009.jpg)

    cd gekko
    npm install moment  
    npm install lodash  
    npm install node-telegram-bot-api

_Prima di eseguire Gekko, è necessario installare questi tre pacchetti: Telegrambot.js avrà bisogno di questi tre pacchetti per abilitarlo normalmente. Ricordarsi di CD nella directory Gekko prima dell'installazione._

ADESSO PER AVVIARE IN LIVE CON ANNESSO TELEGRAM BOT **NON BISOGNA ESEGUIRE** “`node gekko --ui` “ma “`node gekko --config config.js`”

DOPO AVER ESEGUITO DA TERMINALE:

    cd gekko
    node gekko --config config.js

  
SI AVRà UNA SCHERMATA COME QUESTA

![enter image description here](https://4.bp.blogspot.com/-fQq0RCmfJlY/Wnr4pkaegdI/AAAAAAAACLs/5QkqMYD1wTAok2UoqVxD7TsgSxwrg1c6ACLcBGAs/s1600/2018-02-07_210118.jpg)

_Quindi DA TELEGRAM avviare il bot eseguendo /start o /help per vedere tutti i comandi disponibili._

![enter image description here](https://3.bp.blogspot.com/-CYhRe2gCCKk/Wnr5nuNsA7I/AAAAAAAACL4/ZsgcSuckcR00SMzUHXRjrJRrwgcmYrbtQCLcBGAs/s1600/2018-02-07_200722.jpg)

_Quindi puoi trovare il tuo Telegram Bot su_ [_http://t.me/tuoBotUsername_](http://t.me/%E4%BD%A0%E7%9A%84BotUsername)

 _Al momento, ci sono solo due istruzioni:_ **_/price_** _e_ **_/advice_** _per interrogare il prezzo corrente e la consulenza fornita dalla strategia._

  
  
**Al momento 1 Telegram Bot può essere collegato solo a 1 Gekko** , il che significa che se apri due Gekko, devi associare due diversi Telegram Bot. 

PER INVIARE IN LIVE A Più PERSONE LE NOTIFICHE SUI SEGNALI DI BUY O SELL SI Può CREARE UN GRUPPO TELEGRAM ED INSERIRE IL BOT CREATO PRECENDETEMENTE NEL GRUPPO.


*This is a complete version of this guide (credit: [https://click-earn-btc.blogspot.com/2018/02/gekko-command-line-cli-telegram-bot.html](https://click-earn-btc.blogspot.com/2018/02/gekko-command-line-cli-telegram-bot.html))*
