<template>
  <div class="home">
      <table>
          <tr>
              <td>123</td>
          </tr>
           <tr>
              <td>123</td>
              <td is="CurrentUser">2222222</td>
              <td is="CurrentUser">123</td>
          </tr>
    </table>
  </div>
</template>

<script>
// @ is an alias to /src
import CurrentUser from "@/components/CurrentUser.vue";

export default {
  name: "about",
  components: {
    CurrentUser
  },
  data() {
    return {
      index: 0,
      name:"CurrentUser"
    };
  },
  computed: {
    delIndex() {
      switch (this.index % 3) {
        case 0:
          return "default";
        case 1:
          return "main";
        case 2:
          return "footer";
        default:
          return "default";
          break;
      }
    }
  },
  methods: {
    click() {
      this.index = this.index + 1;
    }
  }
};
</script>
