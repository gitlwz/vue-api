<template>
  <div class="home">
    <div>
      <h1 class="title">带有 slot-scope 特性的作用域插槽 自 2.6.0 起被废弃。</h1>
      <CurrentUser>
        <template slot-scope="slotProps">
          {{ slotProps }}
        </template>
        <span
          slot="main"
          slot-scope="slotProps"
        >
          {{ slotProps }}
        </span>
        <span
          slot="footer"
          slot-scope="slotProps"
        >
          {{ slotProps }}
        </span>
      </CurrentUser>
    </div>

    <div>
      <h1 class="title">作用域插槽 新语法</h1>
      <CurrentUser>
        <template v-slot:default="slotProps">
          {{ slotProps }}
        </template>
        <template v-slot:main="slotProps">
          {{ slotProps }}
        </template>
        <template v-slot:footer="slotProps">
          {{ slotProps }}
        </template>
      </CurrentUser>
    </div>

    <div>
      <h1 class="title">动态插槽名 新语法</h1>
      <CurrentUser>
        <template v-slot:[delIndex]="slotProps">
          {{ slotProps }}
        </template>
      </CurrentUser>
    </div>
    <button @click="click">修改插槽</button>
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
      index: 0
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
