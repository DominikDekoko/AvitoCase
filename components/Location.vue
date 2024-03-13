<script>

</script>

<template>
    <div class="flex justify-between">
        <section>
            <b>Выберите локацию</b>
            <div>
                <Search />
            </div>
        </section>
        <section>
            <b> Напишите ID пользователя</b>
            <div>
                <input placeholder="ID" class = "Vvod" />
            </div>
            <img src="/Instruction-image.svg" class="w-[500px] h-[500px]">
        </section>
    </div>
</template>

<style>
.Vvod {
    width: 500px;
    height: 50px;
    background-color: #EDEDED;
    margin-top: 10px;
    margin-bottom: -10px;
    border-radius: 20px;
    border-color:black;
    padding-right: 20px;
    padding-left: 20px;
}
</style>