<template>
    <header class="header">
      <img src="/Img/head.svg" alt="" class="header_img" />
      <div class="header_content">
        <p class="header_heading">Наш проект</p>
        <p class="header_text">Домой / Блог</p>
      </div>
    </header>
</template>

<script>
export default {
  name:"HeaderComponent",
};
</script>

<style>
.header{
    height: 356px;
    margin-top: 45px;
    position: relative;
    margin-bottom:200px;
}
    .header_img{
        width: 100%;
        height: 356px;
        overflow:hidden;
    }
    .header_content{
        position: absolute;
        width: 503px;
        height: 160px;
        border-radius: 50px 50px 0 0;
        background-color: #ffffff;
        top: 55.5%;
        left: 41.7%;
    }
    .header_heading{
        margin-top: 41px;
        font-size: 50px;
        margin-left: 85px;
        color:  #292F36 ;
        width: 347px;
        text-align: center;
    }
    .header_text{
        font-size: 22px;
        color: #4D5053;
        width: 162px;
        height: 66px;
        text-align: center;
        margin-left: 171px;
    }
</style>