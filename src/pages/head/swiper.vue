<template>
    <div class="swiper-container">
        <div class="swiper-wrapper">
            <div class="swiper-slide">slider1</div>
        </div>
    </div>
</template>

<script>
import Swiper from 'swiper'
import axios from 'axios'
export default {
    name: 'swiper',
    methods: {
        handleGetSucc (res) {
            console.log(res)
        },
        handleGetError (error) {
            console.log(error)
        }
    },
    mounted () {
        axios.post('/mobile/index.php?m=default&c=index&a=ajax_goods&type=best&u=0')
          .then(this.handleGetSucc.bind(this))
          .catch(this.handleGetError.bind(this))
    }
}
</script>

<style>

</style>
