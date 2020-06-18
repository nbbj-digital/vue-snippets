<template>
  <div class="home">
    <div class="spacing">
      <HelloWorld msg="Vue Snippets"/>
    </div>

    <div class="spacing">
      <h2>Custom V-Model</h2>
      <custom-v-model name="Chip Selection" v-model="customVModelData"/>
    </div>

    <div class="spacing">
      <h2>CSS By Props</h2>
      <css-by-props color="orange"/>
    </div>

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
    CssByProps: () => import("../components/CssByProps.vue"),
  }
};
</script>
<style scoped>
.spacing {
  padding-bottom: 30px;
}
</style>
