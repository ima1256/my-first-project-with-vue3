  <!-- <h1>Hello Vue JS and {{ name.toUpperCase() }}</h1>
  <h2 :style="styleColor">I am blue</h2>
  <h2 :style="`color: ${colorsArray[2]}`">I am peru</h2>
  <h2> {{ activo ? 'I am active' : 'I am inactive' }}</h2>
  <h2 v-if="activ == 0">I am active 2</h2>
  <h2 v-else-if="activo"></h2>
  <h2 v-else> I am pollaco</h2>
  <h3> {{ obj }}</h3> -->


  <!-- <ul>
    <li v-for="(fruit, index) in fruits" :key="fruit.id">
     {{ fruit.id }} - {{ fruit.name }}
    </li>
  </ul> -->
<!-- 
  Fruits with greater or equal stock to 20:
  <ul>
    <template v-for="(fruit, index) in fruits" :key="fruit.id">
      <li v-if="fruit.stock >= 20">
          {{ fruit.id }} - {{ fruit.name }}
      </li>
    </template>
  </ul> -->

  <!-- <ul>
    <li v-for="(value, property, index) in fruitObject" :key="value">
      {{ property }} : {{ value }}
    </li>
  </ul>

const name = "Dynamic Web"
const styleColor = "color: blue; font-size: 50px"
const colorsArray = ["blue", "red", "peru"]
const obj = {
  colors: colorsArray
}
const active = 0

const fruits = [{
  id: 1,
  name: "pear",
  stock: 20
},
{
  id: 2,
  name: "apple",
  stock: 10
},
{
  id: 3,
  name: "orange",
  stock: 40
}]

const fruitObject = {
  id: 1,
  name: "pear",
  description: "disgusting fruit",
  price: "2$"
}

const handleClick = (message) => {

  if (message == "Left Click") increment();
  console.log(message);
}

-->