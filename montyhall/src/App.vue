<template>
  <div id="app">
    <h1>Problema de Monty Hall</h1>
    <div class="form">
      <div v-if="!started">
        <label for="portsAmount">Quantas portas?</label>
        <input type="text" id="portsAmount" size="3" v-model.number="portsAmount">
      </div>
      <div v-if="!started">
        <label for="selectedPort">Qual a porta premiada?</label>
        <input type="text" id="selectedPort" size="3" v-model.number="selectedPort">
      </div>
      <button v-if="!started" @click="started = true">Iniciar</button>
      <button v-if="started" @click="restart">Reiniciar</button>
    </div>

    <div class="doors" v-if="started">
      <div v-for="i in portsAmount" :key="i">
        <DoorSurprise :hasGiftBox="i === selectedPort" :number="i" />
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import DoorSurprise from './components/DoorSurprise.vue';

export default {
  components: { DoorSurprise },
  setup() {
    const started = ref(false);
    const portsAmount = ref(3);
    const selectedPort = ref(null);

    const restart = () => {
      started.value = false;
      portsAmount.value = 3;
      selectedPort.value = null;
    };

    return { started, portsAmount, selectedPort, restart };
  }
};
</script>

<style>
  * {
    box-sizing: border-box;
    font-family: sans-serif;
  }

  body {
    color: #FFF;
    background: lightblue;
  }

  #app {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  #app h1 {
    border: 1px solid #000;
    background-color: #0004;
    padding: 20px;
    margin-bottom: 60px;
  }

  .form {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom: 40px;
  }

  .form, .form input, .form button {
    margin-bottom: 10px;
    font-size: 2rem;
  }

  .doors {
    align-self: stretch;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
  }
</style>
