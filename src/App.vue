<template>
  <div id="app">
    <waiter-registration
      :total='totalAmount'
      :inputs='totalInputs'
      :selectedTable='selectedTable'
      :tableInputs='selectedTable ? selectedTable.inputs.length : "???"'
      :tableTotal='tableAmount(selectedTable)'
      @amount-saved='(event) => saveTableAmount(event)'
      >
    </waiter-registration>
    <div class="tables__group">
          <total-tables v-for="(table, index) in tables"
          :key="`table-${index}`"
          :tableName='table.name'
          :tableAmount='tableAmount(table)'
          :isSelected="isSelectedTable(index)"
          @click="selectTable(index)">
          </total-tables>
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
    saveTableAmount(amount){
      const intAmount = parseInt(amount);
      const input = {amount: intAmount};
      this.selectedTable.inputs.push(input);
    },
    tableAmount(table){
      let result = 0;
      if(table){
        table.inputs.forEach(input => {
          result += input.amount;
        })
      }
      return result;
    },
    selectTable(idx){
      this.selectedTable = this.tables[idx];
    },
    isSelectedTable(idx){
      const selectedTableIndex = this.tables.indexOf(this.selectedTable)
      return idx === selectedTableIndex;
    }
  },
  computed: {
    totalAmount(){
      let result = 0;
      this.tables.forEach(table => {
        result += this.tableAmount(table)
      })
      return result;
    },
    totalInputs(){
      let result = 0;
      this.tables.forEach(table => {
        result += table.inputs.length;
      })
      return result;
    }
  },
  data() {
    return {
      selectedTable: null,
      tables: [
          {
              name: 'Mesa 1',
              inputs: [],
          },
          {
              name: 'Mesa 2',
              inputs: [],
          },
          {
              name: 'Mesa 3',
              inputs: [],
          },
          {
              name: 'Mesa 4',
              inputs: [],
          },
          {
              name: 'Mesa 5',
              inputs: [],
          },
          {
              name: 'Mesa 6',
              inputs: [],
          },
          {
              name: 'Mesa 7',
              inputs: [],
          },
          {
              name: 'Mesa 8',
              inputs: [],
          },
          {
              name: 'Mesa 9',
              inputs: [],
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