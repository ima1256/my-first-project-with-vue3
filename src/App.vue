<script setup>
import { ref, computed } from 'vue'

let i = ref(0);

let favoriteNumbers = ref([])

const increment = () => {
  console.log("Increase counter")
  i.value++;
  console.log("Counter")
}

const decrement = () => {
  i.value--;
}

const reset = () => {
  i.value = 0;
}

const addFavorite = computed(() => {
  favoriteNumbers.value.push(i.value);
})

const isFavorite = computed(() => {
  return favoriteNumbers.value.includes(i.value)
})

const classCounter = computed(() => {
  if (i.value < 0) return 'negative'
  else if (i.value > 0) return 'positive'
  return 'zero'
})

</script>

<template>
  <div class="container">

    <div class="btn-group">

      <button class="btn btn-success" @click.left="increment()">Increment</button>
      <button class="btn btn-primary" @click.middle="reset()">Reset</button>
      <button class="btn btn-primary" v-on:click.right.prevent="decrement()">Decrement</button>
      <button class="btn btn-success" :disabled="isFavorite" @click="addFavorite">Add to favorites</button>

    </div>

    <!-- <h2 v-if="i < 0" :style="colors['belowZero']"> {{ i }} </h2>
<h2 v-else-if="i > 0" :style="colors['aboveZero']"> {{ i }} </h2>
<h2 v-else> {{ i }} </h2> -->

    <h2 :class="classCounter">{{ i }}</h2>

    <h3 class="padding: 20px">Favorites</h3>
    <ul class="list-group">
      <li class="list-group-item" v-for="number in favoriteNumbers" :key="number">
        {{ number }}
      </li>
    </ul>

  </div>

  <!-- <h2 v-else>{{ i }}</h2> -->
</template>

<style>

.container {
  display: flex;
  flex-direction: column;
}

.zero {
  color: peru;
}

.negative {
  color: red;
}

.positive {
  color: green;
}
</style>