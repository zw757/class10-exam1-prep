<script setup>
//import the component from child
import Display from './components/Display.vue'
//import reactive variable: Use ref() when the value can change while the user is using the app
import { ref } from 'vue'
//set initial value of ref
const DisplayValue = ref(0)

//press event functionality: add value to the display value
function press(value) {
  DisplayValue.value += value
}

//clear event functionality: clear the displayValue
function clear() {
  DisplayValue.value = ''
}
</script>

<template>
  <main class="min-h-screen flex items-center justify-center p-4">
    <div class="card bg-base-100 shadow-xl w-full max-w-xs">
      <div class="card-body gap-4">

        <!-- set tailwind css styling and the value prop of the Display component -->
        <Display class="input input-lg w-full text-right font-mono text-xl" :value="DisplayValue" />

        <div class="grid grid-cols-4 gap-2">
          <button class="btn btn-accent" @click="clear">C</button>
          <button class="btn btn-neutral" @click="press('±')">±</button>
          <button class="btn btn-neutral" @click="press('%')">%</button>
          <button class="btn btn-secondary" @click="press('÷')">÷</button>

          <button class="btn" @click="press('7')">7</button>
          <button class="btn" @click="press('8')">8</button>
          <button class="btn" @click="press('9')">9</button>
          <button class="btn btn-secondary" @click="press('×')">×</button>

          <button class="btn" @click="press('4')">4</button>
          <button class="btn" @click="press('5')">5</button>
          <button class="btn" @click="press('6')">6</button>
          <button class="btn btn-secondary" @click="press('−')">−</button>

          <button class="btn" @click="press('1')">1</button>
          <button class="btn" @click="press('2')">2</button>
          <button class="btn" @click="press('3')">3</button>
          <button class="btn btn-secondary" @click="press('+')">+</button>

          <button class="btn col-span-2" @click="press('0')">0</button>
          <button class="btn" @click="press('.')">.</button>
          <button class="btn btn-primary" @click="press('=')">=</button>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped></style>
