<template>
  <div class="black-bg" v-if="modal_stat">
    <div class="white-bg">
      <h4>은행을 선택해주세요</h4>
      <li v-for="item in banks" v-bind:key="item">
        <div class="form-check">
          <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault">
          <label class="form-check-label" for="flexCheckDefault">
            {{ item }}
          </label>
        </div>
      </li>
      <div class="row"><button @click="modal_stat = false" class="btn btn-outline-dark">확인</button></div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      modal_stat : true,
      banks : ["우리은행", "1은행", "2은행", "3은행", "4은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행", "카카오은행"],
      popup_stat:{},
    }
  },
  methods: {
    popup_close:function() {
      this.modal_stat = false
      this.$emit("modal_from_child",false)
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  margin: 0;
}
div {
  box-sizing:border-box;
}
.black-bg {
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed; padding:20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px; padding:20px;
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
</style>
