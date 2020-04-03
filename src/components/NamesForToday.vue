<template>
  <div>
      <h3>Today's date is</h3>
      <h2>{{ nameDayToday.data.dates.day }}/{{ nameDayToday.data.dates.month }}</h2>
      <h3>and the names for today are</h3>
      <h2 v-for="(value, key) in nameDayToday.data.namedays">{{ value }}</h2>

  </div>
</template>

<script>
export default {
    name: 'names-for-today',
    props: ['nameDayToday']

}
</script>

<style scoped>

</style>