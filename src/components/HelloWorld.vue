<template>
  <div class="container">
    <header>
      <slot name="header"></slot>
    </header>
    <main>
      <slot></slot>
    </main>
    <footer>
      <slot name="footer"></slot>
    </footer>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  mounted(){
      this.$nextTick(function () {
          console.log("************",this)
     })
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
