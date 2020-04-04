<template>
<div id="todays-date">
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
    #todays-date {
        background-color: pink;
    }
</style>