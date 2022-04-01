<template>
  <div class="calculator">
    <img v-bind:src="'https://upload.wikimedia.org/wikipedia/commons/thumb/b/b9/Fibonacci_Spiral.svg/300px-Fibonacci_Spiral.svg.png'">

    <h2 class="title">
      Fibonacci Calculator
    </h2>

    <label for="input">
      <input
        class="input is-normal"
        placeholder="Input"
        type="text"
        id="input"
        v-bind:value="inputValue"
        v-on:input="inputChangeHandler"
      >

      <input
        class="input is-normal"
        readonly
        placeholder="Result"
        type="text"
        v-bind:value="fibonacci"
      >
    </label>

    <button
      class="button is-success is-medium"
      v-on:click="fibonacci = calculateFibonacci(inputValue)"
    >
      Calculate
    </button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      inputValue: '',
      fibonacci: ''
    }
  },
  components: {
  },
  methods: {
    inputChangeHandler (event) {
      this.inputValue = event.target.value
    },
    calculateFibonacci (num) {
      return (
        num <= 1
          ? num
          : this.calculateFibonacci(num - 1) + this.calculateFibonacci(num - 2)
      )
    }
  }
}
</script>

<style>
.calculator {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 100vh;
}

img {
  margin: 50px 0;
  object-fit: contain;
  width: 200px;
  border-radius: 2px;
}

.input {
  display: block;
  margin: 20px 0;
  width: 80vw;
}

.button {
  position: absolute;
  bottom: 25vh;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
