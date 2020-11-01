<template>
    <div>
        <h1>{{msg}}</h1>
        <button @click="emitEvent">Custom Event</button>
    </div>
</template>

<script>
export default {
    name: 'HolaMundo',
    props: {
        msg: String
    },
    methods: {
        emitEvent(){
            this.$emit('click-event', 'Datos enviado desde Hola Mundo')
        }
    },
}
</script>