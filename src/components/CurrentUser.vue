<template>
  <div>
    <header>
      <slot v-bind:user="user">
      </slot>
    </header>
    <main>
      <slot name="main"  v-bind:user="user">
      </slot>
    </main>
    <footer>
      <slot name="footer" v-bind:user="user" v-bind:text="text"></slot>
    </footer>
  </div>

</template>

<script>
export default {
  name: "CurrentUser",
  data() {
    return {
      user: {
        firstName: "firstName",
        lastName: "lastName"
      },
      text:{
          name:"name",
          age:"age"
      }
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
