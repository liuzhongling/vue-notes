<template>
    <div class="across-page">
        <h3>vue-cli proxyTable接口跨域请求调试</h3>
        <div class="toutiao-btn" @click="searchToutiao">搜索今日头条</div>
    </div>
</template>

<script>
import axios from "axios"
export default {
    created() {
    },
    methods: {
        searchToutiao() {
            axios.get('/list/?tag=__all__&ac=wap&count=20&format=json_raw&as=A1650B64D201BC2&cp=5B42914BDCD27E1&min_behot_time=0&_signature=L6a3GQAAdOu-XX6t1tSwdC-mtw&i=')
                .then(res => {
                    console.log(res)
                })
                .catch(err => {
                    console.log(err)
                })
        }
    }
}
</script>

<style scoped>
    .across-page {
        margin: 0;
        padding: 10px;
        height: 100%;
        background-color: rgb(224, 230, 174);
    }

    .toutiao-btn {
        margin: 0 auto;
        margin-top: 20px;
        width: 200px;
        height: 40px;
        line-height: 40px;
        text-align: center;
        font-size: 16px;
        background-color: blueviolet;
        color: #fff;
    }
</style>
