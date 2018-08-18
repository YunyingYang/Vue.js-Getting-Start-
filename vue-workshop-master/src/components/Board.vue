<template >
    <div class="board">
        <div class="board-score">Current score is: {{ score }}</div>
        <div class="board-miss">Miss number is: {{ miss }}</div>
    </div>
</template>

<script>
export default {
    props:[
        'score',
        'miss'
    ]
}
</script>

<style>

</style>
