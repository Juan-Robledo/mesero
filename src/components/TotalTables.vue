<template>
        <div :class='["tables", isSelected ? "selected" : ""]'>
            <h4>{{tableName}}</h4>
            <p>Import: {{amountFormatted}}</p>
        </div>
</template>

<script>
export default {
    name: 'TotalTables',
    props: {
        tableName: String,
        tableAmount: Number,
        isSelected: Boolean
    },
    computed: {
        amountFormatted(){
            return `$ ${this.tableAmount}`;
        }
    },
}
</script>

<style scoped>
    .tables{
        width: 150px;
        padding: 10px;
        margin: 10px;
        border: 2px solid #6d2be7;
        cursor: pointer;
    }
    .selected{
        background-color: #dddddd;
    }
</style>