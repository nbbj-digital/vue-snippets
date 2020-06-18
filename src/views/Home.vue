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
      <css-by-props color="deepskyblue"/>
    </div>

    <div class="spacing">
      <h2>Manipulating Props From Child</h2>
      <manipulating-props :dataset="dataset"/>
    </div>

  </div>
</template>

<script>
export default {
  name: "Home",
  data: () => ({
    customVModelData: null,
    dataset: {
      duration: 10,
      type: "working"
    }
  }),
  components: {
    HelloWorld: () => import("../components/HelloWorld.vue"),
    CustomVModel: () => import("../components/CustomVModel.vue"),
    CssByProps: () => import("../components/CssByProps.vue"),
    ManipulatingProps: () => import("../components/ManipulatingProps.vue"),
  }
};
</script>
<style scoped>
.spacing {
  padding-bottom: 20px;
}
</style>
