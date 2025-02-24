<template>
    <div class="pagination container">
        <button class="pagination-btn">01</button>
        <button class="pagination-btn">02</button>
        <button class="pagination-btn">03</button>
        <button class="pagination-btn">
            <img :src="arrowIcon" alt="" class="blog_articles-arrow" />
        </button>
    </div>
</template>

<script>
export default {
  name:"PaginationComponent",
  data(){
    return {
        arrowIcon:require('@/assets/arrow.png')
    }
  }
};
</script>

<style>
    .pagination{
    display: flex;
    margin-left: 466.5px;
    gap: 20px;
    height: 52px;
    width: 268px;
    margin-bottom: 200px;
    margin-top: 50px;}
    .pagination-btn{
        width: 52px;
        height: 52px;
        background-color: #FFFFFF;
        border-radius: 50%;
        border: 1px solid #CDA274;
        text-align: center;
        font-size: 16px;
        color: #292F36;
        font-weight: 500;
        line-height: 150%;
        align-items: center;
        }
        .pagination-btn:first-child{
            background-color: #F4F0EC;
            border: none;
        }
</style>
