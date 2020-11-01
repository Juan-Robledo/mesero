<template>
    <div class="total-tables">
        <div class="tables" v-for="(tables, index) in totalTables" :key="index">
            <p>Mesa: {{tables.number}}</p>
            <input type="number" v-model="tables.price" placeholder="Amount">
            <button @click="add">Add</button>
            <p>Import: ${{tables.price}}</p>
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
                price: ''
            },
            {
                number: 2,
                price: ''
            },
            {
                number: 3,
                price: ''
            },
            {
                number: 4,
                price: ''
            },
            {
                number: 5,
                price: ''
            },
            {
                number: 6,
                price: ''
            },
            {
                number: 7,
                price: ''
            },
            {
                number: 8,
                price: ''
            },
            {
                number: 9,
                price: ''
            }
            ],
            total: 0
        }
    },
    methods: {
        add(){
            this.totalTables.price += this.totalTables.price;
        }
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