<template>
  <div class="top">
    <a>어플리케이션 이름</a>
  </div>
  <div class="container-fluid">
    <div class="row">
      <div class="col-sm-6 b">
        <button type="button" class="menu"> {{ menu[0] }} </button>
      </div>
      <div class="col-sm-6 b">
        <button type="button" class="menu"> {{ menu[1] }} </button>
      </div>
      <div class="col-sm-6 b">
        <button type="button" class="menu"> {{ menu[2] }} </button>
      </div>
      <div class="col-sm-6 b">
        <button type="button" class="menu"> {{ menu[3] }} </button>
      </div>
    </div>
  </div>
  <div>
    <!-- <h4 class="menu" v-for="작명 in menu" :key="작명"> {{ 작명 }} </h4> -->
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      menu : ['금융 상품 비교', '보이스 피싱 방지 어시스턴트',
      '뱅킹 앱 자원봉사자 대면 도우미', '자원봉사자 신청'],
      style : "color : blue",
    }
  },
  components: {
  }
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

.top {
  background: darkblue;
  padding: 15px;
  border-radius : 5px;
}
.top a {
  color : white;
  padding: 10px;
}

.menu {
  margin-left: auto;
  margin-right: auto;
  width : 40%;
  height: 100%;
  background: #363636;
  border: #2c3e50 100px;
  text-align: center;
}
</style>
