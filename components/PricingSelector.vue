<template>
  <div class="pricing-selector">
    <div :class="{ active: type == 0 }" class="item" @click="onClick(0)">
      <strong>Figma</strong> for design + prototyping
    </div>
    <div :class="{ active: type == 1 }" class="item" @click="onClick(1)">
      <strong>FigJam</strong> for whiteboarding
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      type: 0,
    };
  },
  methods: {
    onClick(type) {
      this.type = type;
      this.$emit("selectType", this.type);
    },
  },
};
</script>

<style scored>
.pricing-selector {
  border-radius: 8px;
  background-color: rgb(229, 229, 229);
  display: inline-flex;
  padding: 4px;
}

.item {
  font-size: 22px;
  background-color: rgb(229, 229, 229);
  color: rgba(0, 0, 0, 0.7);
  padding: 12px 14px;
  text-align: center;
  border-radius: 5px;
}
.active {
  background-color: rgb(255, 255, 255);
}
</style>
