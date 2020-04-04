<template>
  <div id="todays-names">
    <h3>Today's date is</h3>
    <todays-date :date="nameDayToday.dates"></todays-date>
    <h3>and the names for today are</h3>
    <todays-names-table :countryCodes="countryCodes" :nameDayToday="nameDayToday"></todays-names-table>
  </div>
</template>

<script>
import TodaysDate from './TodaysDate.vue';
import TodaysNamesTable from './TodaysNamesTable.vue'

export default {
    name: 'names-for-today',
    props: ['nameDayToday', 'countryCodes'],
    components: {
      "todays-date": TodaysDate,
      "todays-names-table": TodaysNamesTable
    }
}
</script>

<style scoped>
  #todays-names {
    border: solid black 2px;
  }
</style>