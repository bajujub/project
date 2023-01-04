<script>
export default{
  data() {
    return {
      counter: 0,
      btnid: ""
    }
  },
  methods: {
    con() {
      switch(this.counter){
        case 0:
        this.btnid = document.getElementById("btn1");
        this.counter = 1;
        break;
        case 1: 
        this.btnid = document.getElementById("btn2");
        this.counter = 2;
        break;
        case 2: 
        this.btnid = document.getElementById("btn3");
        this.counter = 3;
        break;
        case 3: 
        this.btnid = document.getElementById("btn4");
        this.counter = 4;
        break;
        case 4: 
        this.btnid = document.getElementById("btn5");
        this.counter = 5;
        break;
        case 5:
        window.open('success.html')
        break;
      }
    }
  }
}
</script>

<template>
  <div class="wrapper">

    <div class="content">

    <div class="components">
      <button type="button" @click="con()" id="btn1">Готово</button>
    </div>
    <div class="components" >
      <button type="button" @click="con()" v-show="counter >= 1" id="btn2">Готово</button>
    </div>
    <div class="components">
      <button type="button" @click="con()" v-show="counter >= 2" id="btn3">Готово</button>
    </div>
    <div class="components">
      <button type="button" @click="con()" v-show="counter >= 3" id="btn4">Готово</button>
    </div>
    <div class="components">
      <button type="button" @click="con()" v-show="counter >= 4" id="btn5">Готово</button>
    </div>

    </div>

    <div class="content">

    <div class="components">
      <button type="button" @click="con()" v-show="counter >= 5" id="btn6">Оформити замовлення</button>
    </div>
    <div class="components"></div>
    <div class="components"></div>
    <div class="components"></div>
    <div class="components"></div>

    </div>

  </div> 
</template>

<style scoped>

* {
  margin: 0;
  padding: 0;
}
.wrapper {
  width: 800px;
  height: 600px;
  background-color: black;
  padding: 1%;
  display: flex;
  border-radius: 50px;
}

.content {
  width: 50%;
  max-width: 50%;
  min-height: 100%;
  float: left;
}

.components {
  height: 20%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

button {
  height: 30%;
  width: 40%;
  border-radius: 5px;
  text-align: center;
  cursor: pointer;
}

</style>
