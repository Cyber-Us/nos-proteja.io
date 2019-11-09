<template>
  <section class="container-search">
    <div class="container">
      <h1>Verificar o status do site</h1>
      <h2>Trabalhando por uma Web mais segura</h2>
      <input
        class="search"
        type="text"
        placeholder="Pesquisar por URL"
        aria-labelledby="check-site-status"
      />
    </div>
    <footer>
      <div class="container result">Informações do site</div>
    </footer>
  </section>
</template>

<script>
export default {
  name: "Search"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container-search {
  align-items: center;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  justify-content: center;
  width: 100%;
  position: sticky;
  top: 3.75rem;
  padding: 15vh 0 0 0;
}
.container-search .container {
  width: 976px;
  margin: auto;
  color: white;
  font-family: sans-serif;
  font-style: normal;
  font-weight: 900;
  text-align: left;
}
.container-search .container h1 {
  font-size: 68px;
  line-height: 1;
  font-weight: 700;
  letter-spacing: -0.01em;
  text-align: left;
  margin: 10px 0;
  font-family: monospace;
}
.container-search .container h2 {
  font-weight: 100;
  font-size: 2em;
  font-family: monospace;
}
.container-search .container .search {
  display: block;
  width: 60%;
  height: 3.25rem;
  padding: 0 12px;
  font-size: 2rem;
  font-weight: 500;
  letter-spacing: 0.025em;
  color: #2c353a;
  background-color: #ffcc4f;
  border: 1px solid #ffcc4f;
  border-radius: 6px;
  -webkit-transition: all 0.2s ease;
  transition: all 0.2s ease;
  outline: none;
  font-family: monospace;
}

.container-search footer {
  background-color: #fff;
  -webkit-transition: all 0.3s ease;
  transition: all 0.3s ease;
  width: 0;
  height: 0;
  margin: auto;
  margin: 15vh 0 0 0;
}
.container-search footer .container {
  color: #2c353a;
  font-family: monospace;
  font-size: 1.2rem;
  font-weight: 500;
  padding: 20px 0;
}
.container-search footer.result {
  width: 100%;
  height: 2px;
}
.container-search footer.result.active {
  min-height: 300px;
}
</style>
