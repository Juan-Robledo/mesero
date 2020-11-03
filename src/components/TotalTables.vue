<template>
        <div class="tables">
            <h4>Mesa: {{name}}</h4>
            <p>Import: $ {{price}}</p>
        </div>
</template>

<script>
export default {
    name: 'TotalTables',
    props: {
        name: String,
        price: Number
    }
}
</script>

<style scoped>
    .tables{
        width: 150px;
        padding: 10px;
        margin: 10px;
        border: 2px solid #6d2be7;
    }
</style>