<template>
  <div id="app">
    접속 기기 종류: {{ deviceInfo ? '모바일' : 'PC' }} <br>
  </div>
</template>

<script>
console.log(navigator.userAgent)
export default {
  name: 'App',
  data() {
    return {
      deviceInfo: '',
    }
  },
  created() {
    if (this.deviceInfo == true) {
      window.location.href = "https://google.com"
    }
  },
  methods: {
     isMobile() {
      const info = navigator.userAgent;
      var flag = false;

      if (info.indexOf("iPhone") > -1
        || info.indexOf("Android") > -1
        || info.indexOf("iPad") > -1
        || info.indexOf("iPod") > -1
      ) {
        flag = true;
      }
      this.deviceInfo = flag;
    },
  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
