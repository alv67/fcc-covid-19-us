<script>
  export let cases;
  export let deaths;
  export let recovered;
  export let ventilator;
  export let hospitalized;
  export let icu;
  export let tested;
  export let updated;
</script>

<style>
  .columns {
    border: solid 1px black;
  }
</style>


<div class="section">
  <div class="container">
    <div class="columns">
      <h2 class="is-3 column">Casi: {cases}</h2>
      <h2 class="is-3 column">Decessi: {deaths}</h2>
      <h2 class="is-3 column">Ricoverati: {recovered}</h2>
      <h2 class="is-3 column">Aggiornato al: {updated}</h2>
    </div>
  </div>
</div>
<div class="section">
  <div class="container">
    <div class="columns">
      <h2 class="is-3 column">Testati: {tested}</h2>
      <h2 class="is-3 column">Ospedalizzati: {hospitalized}</h2>
      <h2 class="is-3 column">Terapia Intensiva: {icu}</h2>
      <h2 class="is-3 column">Ossigeno: {ventilator}</h2>
    </div>
  </div>
</div>