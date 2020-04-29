<template>
    <div class="page">
        <el-button
            :disabled="isDisabled"
            @click="saveCli">
            {{buttonName}}
        </el-button>
    </div>
</template>
<script>
export default {
    data(){
        return {
            isDisabled:false,
            second:null,
            buttonName:'按钮'
        }
    },
    methods:{
        saveCli(){
            const _this=this
            _this.isDisabled = true;
            const interval = window.setInterval(function() {
              _this.buttonName = "(" + _this.second + "秒)后重新发送";
              --_this.second;
              if (_this.second < 0) {
                _this.buttonName = "重新发送";
                _this.second = 60;
                _this.isDisabled = false;
                window.clearInterval(interval);
              }
            }, 1000)
        }
    }
}
</script>
<style lang="scss" scoped>

</style>

