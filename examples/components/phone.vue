<template>
  <div class="phone">
    <iframe
      class="demo-page"
      :src="'//elemefe.github.io/mint-ui/#' + (routePath === '/loadmore' ? '/pull-down' : (routePath === '/repositories' || routePath === '/quickstart' ? '' : routePath))"
      frameborder="0">
    </iframe>
  </div>
</template>

<script>
export default {
  name: 'phone',

  computed: {
    routePath() {
      return this.$route.path.replace(/^\/(zh-cn|en)2?/, '');
    }
  }
};
</script>

<style lang="sass" scoped>
  .phone {
  	position: fixed;
    top: 7em;
    margin: 20px 20px 0 20px;
    background-image: url('../assets/images/phone.png');
    background-repeat: no-repeat;
    background-size: 100%;
    height: 100%;
    padding: 100px 16px;
    box-sizing: border-box;
    width: 340px;
  }

  .demo-page {
  	width:100%;
  	height:530px;
  	background-color: #fff;
  }
</style>
