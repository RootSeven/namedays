<template>
<div>
    <h3>and the names for today are</h3>
    <table>
        <tr>
            <th>Country</th>
            <th>Names</th>
        </tr>
        <tr v-for="(names, country) in nameDayToday.namedays" :key="country" :value="names">
            <td>{{ country }}</td>
            <td>{{ names }}</td>
        </tr>
      </table>
</div>
</template>

<script>
export default {
    props: ['nameDayToday'],
    components: {
    }
}
</script>

<style>
    table {
        width: 100%;
    }
</style>