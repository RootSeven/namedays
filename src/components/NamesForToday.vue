<template>
  <div id="todays-names">
    <todays-date :date="nameDayToday.dates"></todays-date>
    <todays-names-table :nameDayToday="nameDayToday"></todays-names-table>
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