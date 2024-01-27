<script>
export default {
  name: 'app',
  data (){
    return {
      message: 'Dario',
      content: 'Prima creazione Vue',
      name: '',
      lastname:'',
    }    
  },

  methods: {
      testfunction(){
        console.log('THis i s a method [ a function inside an object ]');
      }
    }
}
</script>

<template>
  <header>
    <div>
      <input type="text" v-model="name">
    </div>
    <div>
      <input type="text" v-model="lastname">
    </div>
    <p> Ciao {{name}} {{lastname}}</p>
    <button @click="testfunction">Click me</button>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
