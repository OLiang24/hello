<template>
  <div id="app">
    <img src="./assets/d11.png" alt="">
    <div>
      <slide />
    </div>

    <div class="container">
      <div class="btn btn-light" >
        <div class="row 12">
          <div class="col-10 ">
            <img src="./assets/a.jpg" alt width="70%" >
            <counter @cc="sum1"></counter>
          </div>
          <div class="col-2 ">
            <h3>
              Sum
              <ul>{{total1}}</ul>
            </h3>
          </div>
        </div>
      </div>
      <br />
      <br />
      <div class="btn btn-light">
        <div class="row 12">
          <div class="col-10 ">
            <img src="./assets/b.jpg" alt width="70%" >
            <counter @cc="sum2"></counter>
          </div>

          <div class="col-2 ">
            <h3>
              Sum
              <ul>{{total2}}</ul>
            </h3>
          </div>
        </div>
      </div>
      <br />
      <br />
      <div class="btn btn-light">
        <div class="row 12">
          <div class="col-10 ">
            <img src="./assets/c.png" alt width="70%" >
            <br />
            <counter @cc="sum3"></counter>
          </div>
          <div class="col-2 ">
            <h3>
              Sum
              <ul>{{total3}}</ul>
            </h3>
          </div>
        </div>
      </div>
      <br />
      <br />
    </div>
  </div>
</template>

<script>
import Counter from "./components/Counter.vue";
import slide from "./components/slide.vue";

export default {
  name: "App",
  components: {
    Counter,
    slide,
  },

  data: function () {
    return {
      total: 0,
      total1: 0, //ผลรวมทั้งหมด --> เอาไปแสดงผล {{}}
      total2: 0,
      total3: 0,
    };
  },

  methods: {
    // 3. คำนวนผลรวมทั้งหมดที่ส่งออกมาจาก emit
    // แล้วเก็บผลรวมไว้ที่ this.total
    sum(CounterValue) {
      this.total = CounterValue;
    },
    sum1(CounterValue) {
      this.total1 = CounterValue;
    },
    sum2(CounterValue) {
      this.total2 = CounterValue;
    },
    sum3(CounterValue) {
      this.total3 = CounterValue;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background-image: url(./assets/p.jpg);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #3886d4;
  margin-top: 60px;
}

</style>
