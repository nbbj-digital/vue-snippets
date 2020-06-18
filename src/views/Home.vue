<template>
  <div class="home">
    <HelloWorld class="spacing" msg="Vue Snippets"/>
    <h2>Custom V-Model</h2>
    <custom-v-model name="Chip Selection" v-model="customVModelData"/>
  </div>
</template>

<script>
export default {
  name: "Home",
  data: () => ({
    stuff: null,
    customVModelData: null,
  }),
  components: {
    HelloWorld: () => import("../components/HelloWorld.vue"),
    CustomVModel: () => import("../components/CustomVModel.vue"),
  }
};
</script>
<style scoped>
.spacing{
  padding-bottom: 30px;
}
</style>
