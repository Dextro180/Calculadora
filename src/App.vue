<script>
export default {
  data() {
    return {
      valor1: null,
      valor2: null,
      nameSoft: "Calculadora",
      label1: "Valor 1",
      label2: "Valor 2",
      resultado: 0

    };
  },
  methods: {
    Postsumar() {
      this.resultado = parseInt(this.valor1) + parseInt(this.valor2);
    },
    Postrestar() {
      this.resultado = parseInt(this.valor1) - parseInt(this.valor2);
    },
    Postdividir() {
      this.resultado = parseInt(this.valor1) / parseInt(this.valor2);
    },
    postmultiplicar() {
      this.resultado = parseInt(this.valor1) * parseInt(this.valor2);
    }

  }



}

</script>

<template>
  <div>

    <h2>{{ nameSoft }}</h2>
    <label>{{ label1 }}</label> <input type="text" v-model="valor1" placeholder="Diga valor 1" /> <br>
    <label>{{ label2 }}</label> <input type="text" v-model="valor2" placeholder="Diga valor 2" /> <br>
    <button @click="Postsumar"> Sumar</button>
    <button @click="Postrestar">Restar</button>
    <button @click="postmultiplicar">Multiplicar</button>
    <button @click="Postdividir">Dividir</button>
    <span v-if="valor1 > 0 && valor2 > 0"> El resultado de {{ valor1 }} mas {{ valor2 }} es igual a {{ resultado
      }}</span>
  </div>
</template>

<style scoped>
div {
  color: white;
  text-align: center;
  position: relative;
  padding-top: 250px;
  font-size: large  
}
button{
  color: black;
  font-size: large;
}
input{
  font-size: large;
}
</style>