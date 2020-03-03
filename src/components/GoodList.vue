<template>
    <div name="show">
        <ul class="goodList">
            <li v-for="good in list">
                <img v-bind:src="good.img"/>
                <p>{{good.goodName}}</p>

            </li>
        </ul>

    </div>
</template>

<style>
    .goodList li {
        list-style: none;
        float: left;
        width: 20%;
        color: red;
        font-size: 20px;
        margin-top: 1px;
    }

    .goodList li img {
        width: 98%;
    }
</style>
<script>
    export default {
        name: "show",
        data() {
            var obj = this;
            var url = "";
            if (obj.goodId == 1) {
                url = "json/ej.json"
            } else if (obj.goodId == 2) {
                url = "json/sj.json"
            } else (obj.goodId == 0)
            {
                url = "json/sj.json"
            }
            this.$http.get(url).then(function (res) {
                obj.list = res.data;
            })
            return {
                list: []
            }

        },
        props: {
            goodId: Number
        },
        watch: {
            goodId() {
                var obj = this;
                var url = "";
                if (obj.goodId == 1) {
                    url = "json/ej.json"
                } else if (obj.goodId == 2) {
                    url = "json/sj.json"
                }
                this.$http.get(url).then(function (res) {
                    obj.list = res.data;
                })
                return {
                    list: []
                }

            }
        }
    }
</script>
