# Bullying-and-Cyberbullying-Detection
![Bullying Image](https://user-images.githubusercontent.com/61507983/176214682-6902d68d-7040-45fe-9039-eb4f0635dd06.png)

## OBIETTIVI
1. <h3> Bullying e Cyberbullying Detection: </h3> Classificare e distinguere gli utenti attivi e passivi nel fenomeno di bullismo e cyberbullismo
2. <h3> Identificare la VideoActivity più discriminante: </h3> Identificare il video, tra i quattro proposti, in grado di discriminare meglio tra vittima e bullo
3. <h3> Individuare l’approccio migliore e il classificatore migliore: </h3> Determinare l’approccio migliore tra Shallow Learning e Deep Learning ed il conseguente classificatore migliore

## IMPLEMENTAZIONE
- Piattaforma utilizzata: Google Colaboratory
- GPU di Google utilizzata: Si
- Linguaggio di  programmazione utilizzato: Python
- Librerie utilizzate: Pandas, Scikit-Learn, Seaborn, Numpy
- Framework utlizzato: Tensorflow con Keras

### Dettagli Implementativi
- Sono stati implementati e utilizzati gli algoritmi messi a disposizione dal Machine Learning, tra cui: SVM, BernoulliNB, Random Forest, BayesianRidge, CNN, LSTM, BiLSTM
- In base alla *VideoActivity* d'interesse, è possibile spostarsi da un'attività ad un'altra modificando il valore della variabile denominata *word*
- Le *VideoActivity* sono:
  - Video1Activity, Domanda_Video1Activity;
  - Video2Activity, Domanda_Video2Activity;
  - Video3Activity, Domanda_Video3Activity;
  - Video4Activity, Domanda_Video4Activity.
- E' stata utilizzata la DCT - *Discrete Cosine Transform* per standardizzare il numero di campioni di ciascuna coordinata, in modo da alleggerire le varie computazioni
  - Il numero di trasformate applicato a ciascuna coordinata è pari a 1000, per un totale di 3000 campioni.

## SPERIMENTAZIONI
Sono state effettuate 4 macro-sperimentazioni, in ordine:
1. TEST 1
2. TEST 2
3. TEST UNIONE
   - UNIONE: Unione degli utenti del TEST 1 agli utenti del TEST 2
5. TEST UNIONE + BILANCIAMENTO
   - UNIONE + BILANCIAMENTO: Unione e successivo bilanciamento degli utenti, dalla classe maggioritaria eliminati alcuni utenti su base casuale

## DATASET
Per ogni sperimentazione è stato creato un dataset ad hoc. <br> Tutti i test fanno riferimento alle 3 classificazioni stabilite a priori:
1. Utenti a Rischio - Utenti Normali
2. Bullismo Bullo - Bullismo Vittimizzazione
3. Bullismo Totale - Vittimizzazione Totale

### Dataset TEST 1
|Utenti a Rischio - 1|Utenti Normali - 0|
|:---:|:---:|
|25|26|

|Bullismo Bullo - 1|Bullismo Vittimizzazione - 0|
|:---:|:---:|
|3|13|

|Bullismo Totale - 1|Vittimizzazione Totale - 0|
|:---:|:---:|
|4|14|

### Dataset TEST 2
|Utenti a Rischio - 1|Utenti Normali - 0|
|:---:|:---:|
|19|29|

|Bullismo Bullo - 1|Bullismo Vittimizzazione - 0|
|:---:|:---:|
|4|12|

|Bullismo Totale - 1|Vittimizzazione Totale - 0|
|:---:|:---:|
|5|14|


### Dataset TEST UNIONE
|Utenti a Rischio - 1|Utenti Normali - 0|
|:---:|:---:|
|44|55|

|Bullismo Bullo - 1|Bullismo Vittimizzazione - 0|
|:---:|:---:|
|7|25|

|Bullismo Totale - 1|Vittimizzazione Totale - 0|
|:---:|:---:|
|9|28|


### Dataset TEST UNIONE + BILANCIAMENTO
|Utenti a Rischio - 1|Utenti Normali - 0|
|:---:|:---:|
|44|44|

|Bullismo Bullo - 1|Bullismo Vittimizzazione - 0|
|:---:|:---:|
|7|7|

|Bullismo Totale - 1|Vittimizzazione Totale - 0|
|:---:|:---:|
|9|9|





