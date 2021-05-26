<template>
  <div class="main">
    <div>
      <h1>
        bienvenid@ a mi jardín digital
      </h1>
      <p>
        Aquí hay notas, ideas, artículos, recomendaciones, libros. Un jardín que siempre esta creciendo.  
      </p>
      <!-- <button><nuxt-link to="/books">books</nuxt-link></button>
      <button><nuxt-link to="/recommendations">recomendaciones</nuxt-link></button>
      <button><nuxt-link to="/internetstuff">internet stuff</nuxt-link></button>
      <button><nuxt-link to="/about">about</nuxt-link></button> -->
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.main {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

button {
  background-color: #0a0a23;
  border: 1px solid #f4f4f4;
  color: #f4f4f4;
  padding: 5px 10px;
  border-radius: 10px;
  cursor: pointer;
}

button:hover {
  opacity: 0.5;
}

</style>
