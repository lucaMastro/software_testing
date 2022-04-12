# MIGLIORAMENTI

Motivare le scelte con le motivazione dei ragionamenti. Deve essere pensato come una specifica da seguire per i tester: il lettore (sviluppatore di casi di test) deve essere in grado di sviluppare un caso di test in codice a partire dal documento. Motivare anche la scelta dei parametri.

> **Nota**: non specificare un risultato atteso per un sottoinsieme dei parametri di input: se il metodo testato prevede 3 input, non posso dire che il risultato atteso sarà _success_ per un certo valore di un singolo parametro.

Nel caso specifico di un tipo di dato relativo a una `password` possiamo definire classi di equivalenza del tipo:

- _password vuota_
- `null`
- _password valida_: rispetta le specifiche, ad esempio una maiuscola, una minuscola, un numero\dots
- _password non valida_: non rispetta le specifiche sopra.
- _password corretta_: ad esempio, dato un login, è la password relativa all'utente con cui faccio il login.
- _password non corretta_: non rispetta la condizione sopra.

Prima dell'esecuzione del test case, può essere necessario fare una configurazione opportuna per coprire i vari casi: possono esserci situazione di _setup_ e _teardown_ per un caso di test.

## Risultato atteso

In alcuni casi non è facile stabilire cosa ci si aspetta da un caso di test: definire un risultato atteso significa definire una serie di condizioni che devono essere verificate. Quando il metodo ritorna potrei verificare che le informazioni contenute nell'oggetto ritornato siano le stesse specificate in fase di creazione. Per esempio, crearlo con alcuni parametri bisogna fare degli assert sui get di quei parametri.

> **Nota**: non usare i soli valori sul bordo, ma usare anche parametri intermedi.
