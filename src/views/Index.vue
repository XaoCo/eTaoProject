<template>
    <div class="main">
        <div class="left">
            <Left></Left>
        </div>
        <div class="right">
            <div class="top">
                <img src="/img/title.jpg"/>
            </div>
            <div class="mainPage">
                <Right></Right>
            </div>
        </div>
    </div>
</template>

<script>
    import Left from '../components/Left.vue'
    import Right from '../components/Right.vue'
    export default {
        components: {
            Left,
            Right
        }
    }
</script>
<style>
    *{
        margin: 0;
        padding: 0;
    }
    .left{
        width: 150px;
        float: left;
        margin-left: 10px;
    }
    .right{
        width: 1200px;
        float: left;
        margin-left: 10px;

    }
    .main{
        width: 1400px;
        margin: 20px auto;
    }
    .top img{
        width: 1200px;
        height: 200px;
    }
    .left,.right{
        height: 1000px;
        background-color: #f3f4f5;
    }
</style>
