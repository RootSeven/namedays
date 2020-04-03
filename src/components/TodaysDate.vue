<template>
<div>
    <h3>Today's date is</h3>
    <h2>{{ date.day }} {{ numberToMonth[date.month - 1 ] }}</h2>
</div>
</template>

<script>
export default {
props: ['date'],
data() {
    return {
        numberToMonth:[
            "January",
            "February",
            "March",
            "April",
            "May",
            "June",
            "July",
            "August",
            "September",
            "October",
            "November",
            "December"
        ]
    }
}
}
</script>

<style>

</style>