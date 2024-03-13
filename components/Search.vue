<script setup lang="ts">

const uri = "https://a9cd-89-188-176-187.ngrok-free.app/"
const data = await $fetch(uri + "getLocations", { 
    body: {location_id: 1},
    method: 'post'
})

const people = [
    { id: 1, label: 'Сосиска Cooper' },
    { id: 2, label: 'Сиси Mccoy' },
    { id: 3, label: 'Devon Webb' },
    { id: 4, label: 'Tom Cook' },
    { id: 5, label: 'Tanya Fox' },
    { id: 6, label: 'Hellen Schmidt' },
    { id: 7, label: 'Caroline Schultz' },
    { id: 8, label: 'Mason Heaney' },
    { id: 9, label: 'Claudie Smitham' },
    { id: 10, label: 'Emil Schaefer' },
    { id: 11, label: 'Сосиска Cooper' },
    { id: 12, label: 'Сиси Mccoy' },
    { id: 13, label: 'Devon Webb' },
    { id: 14, label: 'Tom Cook' },
    { id: 15, label: 'Tanya Fox' },
    { id: 16, label: 'Hellen Schmidt' },
    { id: 17, label: 'Caroline Schultz' },
    { id: 18, label: 'Mason Heaney' },
    { id: 19, label: 'Claudie Smitham' },
    { id: 20, label: 'Emil Schaefer' }
]

const selected = ref([data[3]])
const selected1 = ref([people[3]])
</script>

<template>
    <div class ="flex">
         <div class = "Box mr-[10px]">
        <UCommandPalette class="bg-[#EDEDED] rounded-[20px] h-[500px] " v-model="selected" nullable :autoselect="false"
            :groups="[{ key: 'data', commands: data }]" 
            :fuse="{ resultLimit: 100, fuseOptions: { threshold: 0.1 } }"
            placeholder="Быстрый поиск" />

         </div>
        <div class = "Box">
            <UCommandPalette class="bg-[#EDEDED] rounded-[20px] h-[500px] " v-model="selected1" nullable :autoselect="false"
                :groups="[{ key: 'people', commands: people }]"
                :fuse="{ resultLimit: 100, fuseOptions: { threshold: 0.1 } }"
                 placeholder="Быстрый поиск" />

        </div>
    </div>
</template>
<style>
.Box {
    width: 280px;
    height: 500px;
    background-color: #EDEDED;
    border-radius: 20px;
    margin-top: 15px;
}
.Row{
    display: flex;
    margin-left: 10px
}
</style>