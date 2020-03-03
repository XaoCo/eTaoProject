<template>
    <div>
        <div class="title">热门推荐</div>
        <ul class="menu">
            <li @click="menu1">耳机</li>
            <li @click="menu2">手机</li>
            <li>服饰</li>
            <li>手表</li>
            <li>书籍</li>
            <li>玩具</li>
            <li>小家电</li>
            <li>学习用品</li>
            <li>办公用品</li>
            <li>旅游必备</li>
            <li>游戏卡通</li>
            <li>游戏卡通</li>
            <li>游戏卡通</li>
            <li>游戏卡通</li>
            <li>游戏卡通</li>
            <li>游戏卡通</li>
            <li>游戏卡通</li>
            <li>游戏卡通</li>
            <li>游戏卡通</li>
        </ul>
    </div>
</template>

<script>
    import Msg from './msg.js'
    export default {
        methods:{
            menu1:function () {
                Msg.$emit("val",111)
            },
            menu2:function () {
                Msg.$emit("val",222)
            }
        }
    }
</script>
<style>
    .title {
        width: 150px;
        color: red;
        background-color: white;
    }

    .menu li{
        list-style: none;
        height: 50px;
        line-height: 50px;
        margin-bottom: 2px;
        background-color: white;
        cursor: pointer;
    }
</style>
