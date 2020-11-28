<template>
  <ul>
    <li :class="{active: acitiveOption === 'poor'}"><button type="button" @click="active('poor')">Poor</button></li>
    <li :class="{active: acitiveOption === 'average'}"><button type="button" @click="active('average')">Average</button></li>
    <li :class="{active: acitiveOption === 'great'}"><button type="button" @click="active('great')">Great</button></li>
  </ul>
</template>
<script>
  export default {
    data() {
      return {
        acitiveOption: null
      }
    },
    methods: {
      active(option) {
        this.acitiveOption = option;
        console.log(this.acitiveOption)
      },
    },
  }
</script>
<style scoped>
.active {
  border-color:tomato;
}
.acitive button {
  color: tomato;
}
ul {
  list-style: none;
  margin: 0.5rem 0;
  padding: 0;
  display: flex;
}
li {
  margin: 0 1rem;
  border: 1px solid #ccc;
  padding: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
}
button {
  font: inherit;
  border:none;
  outline: none;
  background-color: transparent;
  cursor: pointer;
}
</style>
