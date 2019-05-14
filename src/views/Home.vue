<template>
  <div class="home">
    <div>
      <h1 class="title">带有 slot 特性的具名插槽 自 2.6.0 起被废弃。</h1>
      <HelloWorld>
        <template slot="header">
          <h1>header</h1>
        </template>

        <p>mian1</p>
        <p>mian2</p>

        <template slot="footer">
          <p>footer</p>
        </template>
      </HelloWorld>
    </div>

    <div>
      <h1 class="title">具名插槽 新语法</h1>
      <HelloWorld>
        <template v-slot:header>
          <h1>header</h1>
        </template>

        <p>mian1</p>
        <p>mian2</p>

        <template v-slot:footer>
          <p>footer</p>
        </template>
      </HelloWorld>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>
