<template>
  <div id="app">
    <waiter-registration @amount-saved='(event) => saveTableAmount(event)'></waiter-registration>
    <div class="tables__group">
          <total-tables v-for="(table, index) in tables" :key="index">{{table.name}}</total-tables>
    </div>
  </div>
</template>

<script>
import TotalTables from './components/TotalTables';
import WaiterRegistration from './components/WaiterRegistration';

export default {
  name: 'App',
  components: {
    TotalTables,
    WaiterRegistration
  },
  methods: {
    saveTableAmount(){
    }
  },
  data() {
    return {
        tables: [
          {
              name: 'Mesa 1',
              price: [],
          },
          {
              name: 'Mesa 2',
              price: [],
          },
          {
              name: 'Mesa 3',
              price: [],
          },
          {
              name: 'Mesa 4',
              price: [],
          },
          {
              name: 'Mesa 5',
              price: [],
          },
          {
              name: 'Mesa 6',
              price: [],
          },
          {
              name: 'Mesa 7',
              price: [],
          },
          {
              name: 'Mesa 8',
              price: [],
          },
          {
              name: 'Mesa 9',
              price: [],
          }
        ],
    }
  },
}
</script>

<style scoped>
  #app{
    width: 1120px;
    margin: 0 auto;
    display: flex;
    flex-flow: row wrap;
    padding: 20px;
    border: 2px solid #1becae;
  }
  .tables__group{
    width: 60%;
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
    }
</style>