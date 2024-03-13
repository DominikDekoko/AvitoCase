<script setup lang="ts">

var loca: string = "Москва";
var cat: string = "Смартфоны";
var cena: string = "39000";

console.log(loca, cat, cena)
</script>

<template>
    <b>Найденная позиция:</b>
    <div class="Boxbot">
        <section class = "verse">
            <b class = "mb-[15px]">Локация: {{ loca }}</b>
            <b class = "mb-[15px]">категория: {{ cat }}</b>
            <b>Текущая стоимость для пользователя:</b>
            <b class = "textstyle"> {{ cena }} руб.</b>
        </section>
        <section class = "verse">
            <b>ID Локации</b>
            <b>ID Микрокатегории</b>
            <b>ID Пользователя</b>
            <b>ID Матрицы</b>
            <b>Скидка пользователя</b>
            <b class = " textstyle"> 100 руб</b>
        </section>
    </div>

</template>

<style>
.Boxbot {
    margin-top: 10px;
    width: auto;
    height: 200px;
    padding:10px;
    padding-left: 30px;
    padding-right: 30px;
    background-color: #EDEDED;
    border-radius: 20px;
    justify-content: space-between;
    display: flex;
}


.verse {
    display: flex;
    margin-bottom: 10px;
    white-space: pre-line;
    word-wrap: break-word;
    flex-direction: column;
}
.textstyle{
    font-size: 36pt;
    font-weight: 600;
}
</style>