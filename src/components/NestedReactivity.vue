<template>
  <div>
    <p><b>Animal Type: </b>{{ animal.type }}</p>
    <div id="numbers-container">
      <p v-for="(word, i) in sentence" :key="`word-${word}-${i}`">{{ word }}</p>
    </div>
    <button @click="updateData">Reactively Update Data</button>
  </div>
</template>

<script>
export default {
  name: "NestedReactivity",
  data: () => ({
    animal: {},
    sentence: ["is", "is", "a", "sentence."]
  }),
  // Vue cannot detect a reactive change using these two lines
  mounted() {
    // Vue cannot detect the change in object of an item in an array
    this.numbers[0] = 1;
    // Vue cannot detect addition of property not predefined when instantiated in data
    this.animal.type = "Dog";
  },
  methods: {
    // The proper way to update the data is using Vue.set
    updateData() {
      // Set an object property specifying the property and value
      this.$set(this.animal, "type", "Dog");
      // Update item at index in array
      this.$set(this.sentence, 0, "This");
    }
  }
};
</script>

<style scoped>
#numbers-container {
  display: inline-flex;
  flex-direction: row;
}
p {
  margin: 2px;
}
</style>
