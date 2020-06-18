<template>
  <div class="center-flex" :style="layoutWidth">
  </div>
</template>

<script>
export default {
  name: "CssByProps",
  props: {
    width: {
      type: Number,
      default: 500
    },
    height: {
      type: Number,
      default: 50
    },
    minWidth: {
      type: Number,
      default: 100
    },
    maxWidth: {
      type: Number,
      default: 800
    },
    borderRadius: {
      type: Number,
      default: 25
    },
    color: {
      type: String,
      default: "black"
    }
  },
  computed: {
    layoutWidth() {
      return {
        width: `${this.width}px`,
        height: `${this.height}px`,
        border: `2px solid ${this.color}`,
        "min-width": `${this.minWidth}px`,
        "max-width": `${this.maxWidth}px`,
        "border-radius": `${this.borderRadius}px`
      };
    }
  }
};
</script>

<style scoped>
.center-flex {
  display: flex;
  margin: 0 auto;
  flex-direction: column;
}
</style>
