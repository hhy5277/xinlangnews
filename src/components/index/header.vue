<template>
  <div class="header">
    <img src="../../assets/identify.png" @click="showInfo">
    <span>新浪新闻</span>
    <img src="../../assets/search.png" @click="toSearch">
  </div>
</template>

<script>
  export default{
      methods:{
        showInfo() {
            console.log(1)
          this.$store.commit('showSiderbar',true)
          this.$store.commit('showLogin',true)
        },
        toSearch() {
            this.$router.push("/search")
        }
      }
  }
</script>

<style scoped>
  .header{
    position: fixed;
    top: 0;
    width: 100%;
    height:1.2rem;
    background-color: #0994ec;
    display:flex;
    justify-content:space-between;
    align-items:center;
    color:#ffffff;
    font-size:.67rem;
    font-weight: 600;
    letter-spacing: 4px;
    z-index:100;
  }
  img {
    width: .67rem;
    height: .67rem;
    padding: .4rem;
  }
</style>















