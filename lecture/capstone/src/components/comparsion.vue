<template>
  <popup
  v-if="modal_stat"
  />
  <div class="row wrapper">
    <div class="col-3">
      <button type='button' @click="home" class="btn btn-outline-dark full">뒤로가기</button>
    </div>
    <div class="col-6">
      <input class="full" v-model="message" placeholder="검색어를 입력해주세요.">
    </div>
    <div class="col-3">
      <button v-on:click="counter += 1" class="btn btn-outline-dark full" >검색</button>
    </div>
  </div>
  <div class="row wrapper">
      <div class="col-6">
        <button class="btn btn-outline-dark btn-block full">금리순</button>
      </div>
      <div class="col-6">
        <button @click="popup_on" class="btn btn-outline-dark btn-block full">은행 선택</button>
      </div>
  </div>
  <div class="row wrapper">
    <div class="col-4">
      <button v-on:click="deposit" class="btn btn-outline-dark btn-block full">예금</button>
    </div>
    <div class="col-4">
      <button v-on:click="savings" class="btn btn-outline-dark full">적금</button>
    </div>
    <div class="col-4">
      <button @click="CMA" class="btn btn-outline-dark full">CMA</button>
    </div>
  </div>
  <div class="card card_wrapper" v-if="modal_stat == false" @modal_from_child="change_modal_stat">
    <div class="card-header">
      {{ info[0].name }}
    </div>
    <!-- <img src="images/card-image.png" alt="" /> -->
    <div class="card-body">
      <!-- <h5 class="card-title">Lorem</h5> -->
    <p class="card-text">{{ info[0].본문 }}</p>
    </div>
  </div>
</template>

<script>
import popup from './popup.vue'

export default {
  name:"UserList",
  components: {
    popup,
  },
  data() {
    return {
      modal_stat : false,
      info:[
        {
          name:"주식회사 카카오 뱅크",
          본문:"본문내용",
        },
        {
          name:"우리은행",
          본문:"본문내용",
        },
        {
          name:"우리은행3",
          본문:"본문내용3",
        },
        {
          name:"우리은행4",
          본문:"본문내용4",
        },
      ],
      popup_stat:false,
    }
  },
  props: {
    msg: String
  },
  methods: {
    popup_on:function() {
      this.modal_stat = true
    },
    change_modal_stat:function() {
      this.modal_stat = false
    },
    CMA:function() {
      this.modal_stat = false
    }
  },
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrapper {
  margin: 5px 5px 5px 5px;
}
.card_wrapper{
  margin: 10px 15px 5px 15px;
}

.full {
  width: 100%;
}
.com_out {
  border-width: 1px;
  border-style: none;
  border-block: black;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

div {
  display: flex;
  float:inherit; 
}
</style>
