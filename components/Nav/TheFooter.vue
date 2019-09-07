<template>
  <footer>
    <div class="container">
      <div>
        Piara © 2019
      </div>
      <a
        href="mailto:piara@app.com"
        target="_top"
      >
        Piara@app.com
      </a>
    </div>

  </footer>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
footer {
  background-color: #96a1b5;
  height: 60px;
  width: 100%;
  color: white;

  .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 100%;
    a {
      color: white;
    }
  }
}
</style>