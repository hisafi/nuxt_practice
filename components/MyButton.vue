<template>
  <a
    :class="{MyButton:true, left_arrow, right_arrow}"
    :style="{'background-color': back_color, color: fore_color}"
  >
    <slot>ボタン</slot>
  </a>
</template>

<script>
export default {
  props: {
    back_color: {
      type: String,
      default: "#00a656"
    },
    fore_color: {
      type: String,
      default: "#ffffff"
    },
    left_arrow: {
      type: Boolean,
      default: false
    },
    right_arrow: {
      type: Boolean,
      default: false
    }
  }
};
</script>

<style>
.MyButton {
  /* background-color: #00a656; */
  border-radius: 1.5em;
  box-shadow: 0 0.2em 0.5em rgba(0, 0, 0, 0.2);
  padding: 1em 2em;
  /* color: #ffffff; */
  font-weight: bold;
  text-decoration: none;
}
.MyButton.left_arrow {
  padding-left: 0;
}
.MyButton.left_arrow::before {
  content: "〈";
  padding-right: 1em;
}
.MyButton.right_arrow {
  padding-right: 0;
}
.MyButton.right_arrow::after {
  padding-left: 1em;
  content: "〉";
}
</style>