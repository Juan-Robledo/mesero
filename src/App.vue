<template>
  <div id="app">
    <waiter-registration></waiter-registration>
    <total-tables></total-tables>
  </div>
</template>

<script>
import TotalTables from './components/TotalTables'
import WaiterRegistration from './components/WaiterRegistration'

export default {
  name: 'App',
  components: {
    TotalTables,
    WaiterRegistration
  }
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
</style>