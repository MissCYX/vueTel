<template>
  <div>
    <div ref="nomal" class="wai" @mouseenter="mouseenter"  @mouseleave="mouseleave">
      <div class="contain">
        <div class="number">222</div>
        <div class="detail">333</div>
      </div>
    </div>
  </div>
</template>
<script>
import console from 'console'

export default{
  data (){
    return {
      show: false
    }
  },
  methods: {
    mouseenter(){
      // this.show = true
      console.log('8')
      this.$refs.nomal.querySelector(".contain").className = "contain fadeOut"
    },
    mouseleave() {
      this.$refs.nomal.querySelector(".contain").className = "contain fadeIn"
      // this.$refs.nomal.querySelector(".detail").classList.add('fadeOut')
    }
  }
} 
</script>
<style lang="scss" scoped>
.wai{
  width: 200px;
  height: 200px;
  overflow: hidden;
  .contain{
    width: 100%;
    height: 400px;
  }
  .number{
    width: 100%;
    height: 200px;
    // transition: height 0.3s;
    background-color: #ccc;
  }
  .detail{
    width: 100%;
    height:200px;
    // transition: height 0.3s;
    background-color: red;
  }
  .fadeOut{
    transform: translateY(-200px);
    transition: 0.3s;
  }
  .fadeIn{
    transform: translateY(0px);
    transition: 0.3s;
  }
}

</style>