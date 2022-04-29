<template>
  <div class="top">
    <a>캡스톤</a>
  </div>
  <div class="menu li " v-if="menu_stat">
    <div class="row row_margin">
      <div class="col-6">
        <button v-on:click="add" type="button" class="btn btn-outline-dark home_menu">{{ menu[0] }}</button>
      </div>
      <div class="col-6">
        <button type="button" class="btn btn-outline-dark btn-block home_menu">{{ menu[1] }}</button>
      </div>
    </div>
    <div class="row row_margin">
      <div class="col-6">
        <button type="button" class="btn btn-outline-dark home_menu">{{ menu[2] }}</button>
      </div>
      <div class="col-6">
        <button type="button" class="btn btn-outline-dark home_menu">{{ menu[3] }}</button>
      </div>
    </div>
  </div>
  <!-- <div class="menu li" v-if="menu_stat">
    <div class="row">
      <div class="col-sm-6 b">
        <button v-on:click="add" type="button"  class="btn btn-default">
            {{ menu[0] }}
        </button>
      </div>
      <div class="col-sm-6 b">
        <button type="button" class="menu">
          <div class="text">
            {{ menu[0] }}
          </div>
        </button>
      </div>
      <div class="col-sm-6 b">
        <button type="button" class="menu"> {{ menu[2] }} </button>
      </div>
      <div class="col-sm-6 b">
        <button type="button" class="menu"> {{ menu[3] }} </button>
      </div>
    </div>
  </div> -->
  <div>
    <!-- <h4 class="menu" v-for="작명 in menu" :key="작명"> {{ 작명 }} </h4> -->
  </div>
    <comparsion v-if="comparsion_appear" v-model="comparsion_apper"/>
  <div>
  </div>
</template>

<script>

import comparsion from './components/comparsion.vue'
export default {
  name: 'App',
  components: {
    comparsion,
  },
  data() {
    
    return {
      menu_stat:true,
      isStatusOn: false,
      menu : ['금융 상품 비교', '보이스 피싱 방지 어시스턴트',
      '뱅킹 앱 자원봉사자 대면 도우미', '자원봉사자 신청'],
      style : "color : blue",
      comparsion_appear:false
    }
  },

  methods: {
    toggleOnOff:function() {
      this.isStatusOn = !this.isStatusOn;
    },
    add: function(){
      this.menu_stat = false,
      this.comparsion_appear = true
    },
    pChangeName: function(name){
      console.log(name);
    },
    // add_backup: function(event){
    //   alert('hello' + this.name + '!')
    //   if (event) {
    //     alert(event.target.tagName)
    //   }
    // }
  },
}
</script>

<style>
button:focus { outline: none; }

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
}

.top {
  background: darkblue;
  padding: 15px;
  border-radius : 5px;
  color: white;
}

.home_menu {
  height: 40vh;
  width: 100%;
  font-size:5vh;
}

.row_margin {
  margin: 10px 10px 10px 10px;
}

/* .menu {
  margin:0 -px;
  display: flex;
  flex-wrap: wrap;
  height: 40vh;
  width:100%;
  float:inherit; 
  text-align: center;
} */

/* .text {
  width: 100%;
} */


/* .menu {
  margin-left: auto;
  margin-right: auto;
  width : 40%;
  height: 100%;
  text-align: center;
} */
</style>
