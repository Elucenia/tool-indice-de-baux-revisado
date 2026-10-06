<!-- ELUCENIA technical documentation · indice-de-baux-revisado · it · no clinical/professional/rights approval -->

# Indice di Baux rivisto

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/indice-de-baux-revisado)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Età

`idade`

anni · intervallo: 0–110

### Superficie corporea ustionata

`scq`

% · intervallo: 0–100

### Lesione da inalazione?

`inalacao`

- `0` — No
- `1` — Sì

## Edizione del metodo

Baux rivisto/Osler 2010: età+superficie+17 lesione inalatoria; modello logistico originale

## Formula documentata

Baux rivisto = età (anni) + superficie ustionata (%) + 17 × lesione inalatoria (1=sì, 0=no).

Nel modello Osler (39888 ustionati del registro USA), età e superficie pesavano quasi uguale; l’inalazione equivaleva a 17 anni o 17% di superficie. La probabilità di morte è la trasformazione logistica del punteggio.

## Limiti e popolazione

Il Baux rivisto somma età, percentuale di superficie ustionata e 17 per la lesione da inalazione. Il totale grezzo non è una percentuale di mortalità: la probabilità richiede la trasformazione logistica della versione. Il modello semplificato ha avuto prestazioni inferiori al modello più complesso nell’articolo e richiede interpretazione nella popolazione clinica appropriata.

## Riferimenti

- [Osler T, Glance LG, Hosmer DW. Simplified estimates of the probability of death after burn injuries: extending and updating the Baux score. J Trauma, 2010.](https://doi.org/10.1097/TA.0b013e3181c453b3)

- [Dokter J et al. External validation of the revised Baux score for the prediction of mortality in patients with acute burn injury. J Trauma Acute Care Surg, 2014.](https://doi.org/10.1097/TA.0000000000000124)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Risultati documentati

Le informazioni seguenti conservano gli output del metodo per esempi sintetici. Non costituiscono una validazione clinica indipendente.

### 1

Maggiore è il punteggio, maggiore è la mortalità prevista; la lesione da inalazione equivale a 17 anni (o 17% della SCQ)

| Dettagli del risultato | |
| --- | --- |
| Baux classico (età + SCQ) | 70 |
| Lesione da inalazione | +17 |

Il punteggio di Baux classico è stato creato come stima della mortalità in %; con il trattamento attuale, questa lettura sovrastima il rischio.


### 2

Maggiore è il punteggio, maggiore è la mortalità prevista; la lesione da inalazione equivale a 17 anni (o 17% della SCQ)

| Dettagli del risultato | |
| --- | --- |
| Baux classico (età + SCQ) | 110 |
| Lesione da inalazione | no |

Il punteggio di Baux classico è stato creato come stima della mortalità in %; con il trattamento attuale, questa lettura sovrastima il rischio.


### 3

Maggiore è il punteggio, maggiore è la mortalità prevista; la lesione da inalazione equivale a 17 anni (o 17% della SCQ)

| Dettagli del risultato | |
| --- | --- |
| Baux classico (età + SCQ) | 38 |
| Lesione da inalazione | no |

Il punteggio di Baux classico è stato creato come stima della mortalità in %; con il trattamento attuale, questa lettura sovrastima il rischio.

