<template>
  <div class="counter">
    <p :class="getData">{{ numberVariable }}</p>
    <div class="btns">
        <button class="decBtn" @click="numberVariable--">-</button>
        <button class="incBtn" @click="numberVariable++">+</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      redClass: "test",
      greenClass: "test2",
      numberVariable: 0,
      textValue: null,

      myArr: ["ZD banda", "baro lasha", "chemi venebi", "rasqvia bicho", 100],
    };
  },
  mounted() {
    this.clickFunction();
  },

  created() {
    console.log("created mode");
  },

  watch: {
    numberVariable: {
      immediate: true,
      handler: function () {
        console.log("var changed");
      },
    },
  },

  computed: {
    getData() {
      if (this.numberVariable < 0) {
        return this.redClass;
      } else if (this.numberVariable > 0) {
        return this.greenClass;
      } else {
        return;
      }
    },
  },

  methods: {
    clickFunction() {
      console.log(this.myArr);
    },
  },
};
</script>

<style scoped>
.counter{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.decBtn{
    background-color: red;
}

.incBtn{
    background-color: green;
}

.btns button{
    margin: 10px 10px 10px;
    padding: 10px 45px;
    font-size: 25px;
    font-weight: bold;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    color: white;

}

.counter p{
    font-size: 35px;
    font-weight: bold;
}

.test {
  color: red;
}

.test2 {
  color: green;
}

.box {
  width: 200px;
  height: 200px;
  background-color: red;
}

.dark {
  background-color: black;
}
</style>
