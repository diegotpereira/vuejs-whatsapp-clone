<template>
    <div class="mensagem">
        <span></span>
    </div>
</template>
<script>
export default {
    name: 'CorpoMensagem'
}
</script>
<style>
.mensagem {
    font-size: 14px;
    box-shadow: rgba(0, 0, 0, 0.13) 0px 1px 0.5px 0px;
    background: #202C33;
    margin: 5px 100px;
    padding: 5px 10px;
    border-radius: 5px;
    width: fit-content;
    color: white;
}
.mensagem.enviar {
    background: #005C48;
    align-self: flex-end;
    color: white;
}
.mensagem span {
    margin-left: 25px;
    font-size: 11px;
    color: rgb(201, 201, 201);
}
</style>