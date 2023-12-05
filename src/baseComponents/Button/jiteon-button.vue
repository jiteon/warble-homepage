<template>
  <div class="jiteon-button-box">
    <div class="btn">
      <a :class="{animation:useAnimation}" href="#">{{title}}</a>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "jiteon-button",
  props: {
    title: {
      type: String,
      default: "按钮"
    },
    backgroundColor: {
      type: String,
      default: "rgba(16,143,111,0.3)"
    },
    useAnimation: {
      type: Boolean,
      default: false
    }
  },
  setup() {}
};
</script>

<style lang="scss">
.jiteon-button-box {
  font-size: 15px;
  .btn {
    position: relative;
    min-width: 70px;
    height: 30px;
  }
  &:hover .animation {
    background: v-bind("backgroundColor");
  }
  a {
    position: relative;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background: rgba(255,255,255,0.05);
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    border-top: 1px solid rgba(255,255,255,0.1);
    border-radius: 5px;
    color: var(--color-text);
  }
}
</style>