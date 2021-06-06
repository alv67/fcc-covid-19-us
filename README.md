## fcc-covid-19-us

Seconda applicazione di esempio del video corso del canale Youtube di [freeCodeCamp.org](https://www.youtube.com/channel/UC8butISFwT-Wl7EV0hUK0BQ):

[Learn the Svelte JavaScript Framework - Full Course](https://www.youtube.com/watch?v=ujbE0mzX-CU)

---

# Annotazioni sullo sviluppo del progetto

Di seguito alcune annotazioni ritenute interessanti nello sviluppo di questo progetto

## Bulma : il framework CSS

In questo progetto ci si affida a BULMA (https://bulma.io) come framework CSS.

__Installazione__

Oltre al pacchetto `bulma` occorre anche installare il corrispondente plugin per rollup : `rollup-plugin-css-only`

```
npm install --save-dev bulma rollup-plugin-css-only
```

__Editing di rollup.config.js__

Per attivare l'utilizzo di Bulma occorre configurare opportunamente l'uso del plugin `css-only` aggiungendo al file `rollup.config.js` le seguenti linee:

```js
import css from 'rollup-plugin-css-only'; 
```
subito alla fine degli altri `import`.

Inoltre occorre aggiungere tra i `plugin` del `client`:

```js
css({ output: 'static/extra.css'}),
```

__Importare la librerie al fine di poterla utilizzare__

Alla fine occorre importare la libreria in modo che possa essere utilizzata nel codice del client.

Quindi aggiungere la seguente linea di codice al file `client.js`

```js
import 'bulma/css/bulma.min.css';
```

## moment.js : manipolazione di tempi e date

Per facilitare la gestione di dati temporali si utilizza la libreria [moment.js](https://momentjs.com).

```
npm install --save-dev moment
```

## chart.js : grafici e visualizzazione dati

Per la visualizzazione grafica di dati si utilizza la libreria [chart.js](https://www.chartjs.org)

```
npm install --save-dev chart.js
```

## axios.js : gestione asincrona di API su base HTTP

Per intercettare in modo asincrono le richieste e le risposte API/HTTP

In questo caso viene installato come pacchetto runtime e non dev quindi l'applicazione lo utilizzerà come dipendenza in runtime.

```
npm instal --save axios
```
