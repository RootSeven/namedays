<template>
  <div>
    <h1>Name Days</h1>
    <h2>What is a Name Day?</h2>
    <p>A name day is a day of the year associated with a certain given name, and these days are celebrated in some parts of Europe and Latin America. These names are related to saints in Roman Catholicism and Eastern Orthodox Christianity. The day is celebrated in much the same way as one's birthday.</p>

        <names-for-today :countryCodes="countryCodes" :nameDayToday="nameDayToday"></names-for-today>
  </div>
</template>

<script>
import NamesForToday from './components/NamesForToday.vue';

export default {
  name: "app",

  data() {
    return {
      nameDayToday: {},
      countryCodes: {
        at: "Austria",
        bg: "Bulgaria",
        hr: "Croatia",
        cz: "Czechia",
        dk: "Denmark",
        ee: "Estonia",
        fi: "Finland",
        fr: "France",
        de: "Germany",
        gr: "Greece",
        hu: "Hungary",
        it: "Italy",
        lv: "Latvia",
        lt: "Lithuania",
        pl: "Poland",
        ru: "Russian Federation",
        sk: "Slovakia",
        es: "Spain",
        se: "Sweden",
        us: "United States of America"
      }
    }
  },

  mounted() {
    fetch('https://api.abalin.net/today')
    .then( response => response.json() )
    .then( nameDayToday => this.nameDayToday = nameDayToday.data );
  },

  components: {
    "names-for-today": NamesForToday
  }
}

</script>

<style scoped>
  div {
    text-align: center;
  }
</style>