<template>
  <div>
    <p
      :class="{ selectedStyle: selected, noselect: true }"
      @click="toggleSelect"
    >
      {{ name }}
    </p>
  </div>
</template>

<script>
export default {
  name: "CustomVModel",
  props: {
    name: String
  },
  data: () => ({
    selected: false
  }),
  watch: {
    // The emitted event has to be named "input" in order for the parent component
    // to be able to consume this data through the v-model API
    selected(val) {
      this.$emit("input", { id: this.name, status: val });
    }
  },
  methods: {
    toggleSelect() {
      this.selected = !this.selected;
    }
  }
};
</script>

<style scoped lang="scss">
p {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: rgb(0, 192, 222);
  background-color: white;
  display: inline-block;
  padding: 5px;
  margin-left: 3px;
  margin-right: 3px;
  box-sizing: border-box;
  border-radius: 25px;
  border: 2px solid rgb(0, 192, 222);
  transition: border 0.1s ease-in, background-color 0.3s ease-in-out,
  color 0.3s ease-in-out;
}
p:hover {
  background-color: rgb(0, 192, 222);
  color: white;
}
.selectedStyle {
  background-color: rgb(0, 192, 222);
  color: white;
}

.noselect {
  -webkit-user-select: none; /* Safari */
  -moz-user-select: none; /* Firefox */
  -ms-user-select: none; /* IE10+/Edge */
  user-select: none; /* Standard */
}
</style>
