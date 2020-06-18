<template>
  <div>
    <label>
      Input
      <!--we set the v-model to the "two-way bound" dynamic property we've created-->
      <input type="text" v-model="duration"/>
    </label>
  </div>
</template>

<script>
export default {
  name: "ManipulatingProps",
  // the dataset object will be passed down from the parent component, but we will
  // make changes to it here and save it back to the parent
  props: {
    dataset: {
      type: Object,
      required: true
    }
  },
  computed: {
    duration: {
      get() {
        return this.dataset.duration;
      },
      // define a custom setter to handle "how" you want the data to be saved back
      // to the original object passed as a prop
      set(val) {
        this.dataset.duration = +val;
      }
    },
  }
};
</script>

<style scoped>
</style>
