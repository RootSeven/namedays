<template>
  <div>
    <todays-date :date="nameDayToday.dates"></todays-date>
      <h3>and the names for today are</h3>
      <table>
        <tr>
          <th>Country</th>
          <th>Names</th>
        </tr>
        <tr>
          <td>Germany</td>
          <td>Dorothy</td>
        </tr>
      </table>
      <!-- <h2 v-for="(name, country) in nameDayToday.namedays" :value="name" :key="country">{{ countryCodes[country.toString()] }}: {{ name }}</h2> -->
  </div>
</template>

<script>
import TodaysDate from './TodaysDate.vue';

export default {
    name: 'names-for-today',
    props: ['nameDayToday', 'countryCodes'],
    components: {
      "todays-date": TodaysDate
    }
}
</script>

<style scoped>
  table {
    width: 100%;
  }
</style>