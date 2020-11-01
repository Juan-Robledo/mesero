<template>
    <div class="waiter">
        <h2>Mesero</h2>
        <div class="box">
            <h3>Total acumulado</h3>
            <p>$</p>
            <h3>Cantidad de cargas</h3>
            <p>#</p>
        </div>
        <div class="box">
            <h3>Mesa seleccionada</h3>
            <p>#</p>
            <h3>Cantidad de cargas</h3>
            <p>#</p>
            <h3>Total acumulado</h3>
            <p>$</p>
        </div>
        <div class="import">
            <input type="text" placeholder="Import">
            <button>Ok</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'WaiterRegistration'
}
</script>

<style scoped>
    .waiter{
        width: 38%;
        color: #288cdd;
        border: 2px solid #7628dd;
        margin: 3px;
        display: flex;
        flex-flow: column nowrap;
        justify-content: center;
        align-items: center;
    }
    h2{
        text-align: center;
    }
    .box{
        width: 80%;
        border: 2px solid #1becae;
        margin: 3%;
        padding: 3%;
    }
    .import{
        width: 80%;
        height: 60px;
        margin: 10px;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    .import input{
        width: 90%;
        height: 50%;
        font-size: 1.3rem;
    }
    .import button{
        font-size: 1.3rem;
        width: 20%;
        height: 100%;
        margin: 0 15px;
        border: none;
        border-radius: 50%;
        background-color:  #288cdd;
        color: #ffffff;
    }
</style>