<template>
  <div>
      <h3>Today's date is</h3>
      <h2>{{ nameDayToday.dates.day }}/{{ nameDayToday.dates.month }}</h2>
      <h3>and the names for today are</h3>
      <h2 v-for="(name, country) in nameDayToday.namedays" :value="name" :key="country">{{ country }}: {{ name }}</h2>

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