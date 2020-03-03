<template>
    <div>
        <div v-if="kk==111">
            <GoodList :goodId="1"></GoodList>
        </div>
        <div v-else-if="kk==222">
            <GoodList :goodId="2"></GoodList>
        </div>
        <div v-else>
            <GoodList :goodId="0"></GoodList>
        </div>
    </div>
</template>
<script>
    import Msg from './msg.js'
    import GoodList from './GoodList.vue'

    export default {
        data() {
            return {
                kk: 12
            }
        },
        mounted: function () {
            var _this = this
            Msg.$on("val", function (s) {
                _this.kk = s
            })
        },
        components: {
            GoodList
        }
    }
</script>
