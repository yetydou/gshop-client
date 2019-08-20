<template>
  <div>
   <router-view></router-view>
   <FooterGuide v-show="$route.meta.showFooter"></FooterGuide>
  </div>
</template>

<script>
import {mapActions} from 'vuex'//调用action映射函数
import FooterGuide from './components/FooterGuide/FooterGuide'


export default {
  // name: 'app',
  components:{
      FooterGuide
  },
  mounted () {  // 例子
     //this.$store.dispatch('getAddress')
     this.getAddress()
  },
  methods:{
     ...mapActions(['getAddress'])
  }

}
</script>

<style lang="stylus" rel="stylesheet/stylus">

</style>
