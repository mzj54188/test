<template>
    <div class="page">
        <img src="../../public/img/timg.jpg" alt="">
    </div>
</template>
<script>
export default {
    data(){
        return{}
    },
    methods:{
    }
}
</script>
<style lang="scss" scoped>
.page{
    width: 300px;
    height: 300px;
    border: #000 solid 1px;
    margin: 50px auto;
    overflow: hidden;
    & img{
        cursor: crosshair;
        transition: all 0.6s ease 0s;
    }
    & img:hover{
        transform: scale(1.4);
    }
}
</style>

