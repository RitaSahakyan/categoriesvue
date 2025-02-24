<template>
    <div class="categories container">
        <button class="categories-item" @click="$emit('category-selected', 'Ванная комната')">Ванная комната</button>
        <button class="categories-item" @click="$emit('category-selected', 'Спальня')">Спальня</button>
        <button class="categories-item" @click="$emit('category-selected', 'Кухня')">Кухня</button>
        <button class="categories-item" @click="$emit('category-selected', 'Гостиная')">Гостиная</button>
    </div>
</template>

<script>
    export default{
        name: "CategoriesComponent"
    }
</script>

<style>
    .categories{
        display:flex;
        justify-content:center;
        align-items:center;
        background-color: #fff;
        border:1px solid #CDA274;
        border-radius:30px;
        width:880px;
        height:75px;
        margin-left:106.5px;
        margin-bottom:61px;
    }
    .categories-item{
        width:220px;
        height:75px;
        border:none;
        border-radius:30px;
        color: #292F36;
        font-size:18px;
        align-items:center;
        text-align:center;
        display:flex;
        justify-content:center;
        cursor: pointer;
        background-color: #fff;
    }
    .categories-item:hover{
        background-color:#CDA274;
        color:#fff;
    }

</style>