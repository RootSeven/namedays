<template>
<div>
    <table>
        <tr>
            <th>Country</th>
            <th>Names</th>
        </tr>
        <tr v-for="(names, country) in nameDayToday.namedays" :key="country" :value="names" v-if="names!=='n/a'">
            <td>{{ countryCodes[country] }}</td>
            <td>{{ names }}</td>
        </tr>
      </table>
</div>
</template>

<script>
export default {
    props: ['nameDayToday', 'countryCodes'],
    components: {
    }
}
</script>

<style>
    table {
        width: 100%;
    }
</style>