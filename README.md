Typescript è un linguaggio di programmazione, sviluppato da Microsoft, pubblicato per la prima volta nell'ottobre 2012 e giunto alla versione 4.7.4. 
Si tratta di un linguaggio basato su JavaScript, al quale aggiunge alcune funzionalità. Il primo grande vantaggio è quello di essere compatibile con quest'ultimo, ovvero tutto il codice JS è anche codice TS. 
TS introduce una tipizzazione statica a JS, permettendo di specificare quale tipologia di valore una variabile può ricevere quando essa viene dichiarata in fase di sviluppo.

Così come SCSS e CSS, TS non può essere direttamente letto dal browser, e quindi esso deve prima passare attraverso un compilatore che lo traduca in JS. Dopo aver installato TS digitando il comando npm i -g typescript, occorre inizializzare con tsc --init, e poi il comando tsc <nome-del-file> per creare un JS che crei il file che sarà letto dal browser. Eseguire dunque tsc <nome-del-file> -w, che ricompila il JS a ogni salvataggio.

Per Type Inference si intende la capacità di TS di intuire automaticamente il tipo di variabile che si è assegnato senza richiedere necessariamente una dichiarazione esplicita. Pertanto, let num = 5 sarà automaticamente di tipo number.

Il tipo any è proprio di una variabile al quale non è stato dichiarato che valore "aspettarsi", e TS non esegue controlli su di essa. In questo senso, una dichiarazione del genere è uguale alla variabile di JS puro, e quindi è sconsigliato usarla nel contesto di TS perché più facilmente soggetta ad errori, non essendo segnalati.

Il tipo Union appartiene a una variabile che accetta solo una serie di tipi di valori specificati. Si imposta usando "|" per unire i tipi desiderati. Ad esempio, let unionVar: number | string; può avere valori che siano numeri o stringhe.

Il tipo Turple è proprio di un array di elementi nel quale ogni elemento deve aspettarsi valori di un tipo specifico. DIifferentemente da un array generico, dove tutti gli elementi hanno valori uguali, Turple consente di specificare per ognuno un certo valore.

Le interfacce in TS, definite da "interface", consentono di dichiarare una serie di proprietà specifiche che un certo oggetto deve possedere. Pertanto,  da "interface Utente {
  nome: string;
  età: number;
}" deriveranno oggetti che devono avere necessariamente le proprietà specificate.

In TS, i types permettono di definire determinati dati da associare a determinate variabili, e permette di creare anche tipi personalizzati, che servono a dichiarare una certa struttura in un modo ben specifico e univoco, contribuendo a prevenire errori. Quando si tratta di definire tipi complessi, che comprendano Union e simili, usare i Types è preferibile, poiché forniscono una maggiore flessibilità. Quando invece l'attenzione deve essere posta maggiormente alla struttura dell'oggetto che si deve creare, le interfaces sono lo strumento da preferire. 

I Generics permettono di scrivere del codice che può lavorare con diversi tipi di dati in un contesto statico, non vincolandosi a un tipo specifico ma mutando dinamicamente. Essi si definiscono usando il tipo generico <T> (La presenza di T tra le parentesi angolare è una convenzione). In questo esempio: "function unaFunzione<T>(array: T[], indice: number): T {
  return array[indice];
}" la presenza di <T> consente alla funzione di specificare un tipo di dato al momento dell'invocazione, e tale tipo può variare ogni volta.
