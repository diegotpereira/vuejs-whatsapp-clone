<template>
    <div class="barraLateralTopModule">
        <div class="barraLateral__cabecalho">
            <div class="barraLateral__perfil_foto">
                <img src="../assets/imagens/user1.jpg" alt="">
            </div>
            <div class="barraLateral__cabecalho_icones">
                <font-awesome-icon class="barraLateral__cabecalho_icone" icon="fa-solid fa-recycle"/>
                <font-awesome-icon class="barraLateral__cabecalho_icone" icon="fa-solid fa-message"/>
                <font-awesome-icon class="barraLateral__cabecalho_icone" icon="fa-solid fa-ellipsis-vertical"/>
            </div>
        </div>
        <div class="barraLateral__buscar">
            <div class="barraLateral__buscar_area">
                <font-awesome-icon class="barraLateral__buscar_icone" icon="fa-solid fa-magnifying-glass"/>
                <input type="text" name="" id="" placeholder="Pesquisar ou iniciar uma conversa">
            </div>
            <div class="barraLateral_buscar_filtro">
                <font-awesome-icon class="barraLateral__buscar_icone" icon="fa-solid fa-bars"/>
            </div>
        </div>
        <div class="barraLateral__arquivo">
            <div class="barraLateral__arquivo_icones">
                <font-awesome-icon class="barraLateral__arquivo_icone" icon="fa-solid fa-arrow-down"/>
            </div>
            <span>arquivado</span>
        </div>
    </div>
</template>
<script>
export default {
    name: 'CabecalhoBarraLateral'
}
</script>
<style>
@import '../assets/css/lateralBarra.css';
</style>