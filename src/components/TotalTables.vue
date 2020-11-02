<template>
    <div class="total-tables">
        <div class="tables" v-for="(tables, index) in totalTables" :key="index">
            <h4>Mesa: {{tables.number}}</h4>
            <input type="number" v-model.number="tables.price" placeholder="Amount">
            <button @click="tables.acountTable = tables.acountTable + tables.price">Add</button>
            <p>Import: ${{tables.acountTable}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TotalTables',
    data() {
        return {
            totalTables: [{
                number: 1,
                price: '',
                acountTable: 0
            },
            {
                number: 2,
                price: '',
                acountTable: 0
            },
            {
                number: 3,
                price: '',
                acountTable: 0
            },
            {
                number: 4,
                price: '',
                acountTable: 0
            },
            {
                number: 5,
                price: '',
                acountTable: 0
            },
            {
                number: 6,
                price: '',
                acountTable: 0
            },
            {
                number: 7,
                price: '',
                acountTable: 0
            },
            {
                number: 8,
                price: '',
                acountTable: 0
            },
            {
                number: 9,
                price: '',
                acountTable: 0
            }
            ],
        }
    },
    methods: {
    },
    computed: {
    },
}
</script>

<style scoped>
    .total-tables{
        width: 60%;
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        align-items: center;
    }
    .tables{
        width: 150px;
        padding: 10px;
        margin: 10px;
        border: 2px solid #6d2be7;
    }
    .tables input{
        width: 80%;
        padding: 3px;
        margin: 3px;
    }
    .tables button{
        width: 50%;
        border: none;
        background-color: #6d2be7;
        color: #1becae;
        padding: 3px 10px;
        margin: 3px 10px;
    }
</style>