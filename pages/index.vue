<template>
  <div class="container">
    <div>
      <MyButton back_color="red" />
      <MyButton left_arrow />
      <MyButton back_color="red">スロットテスト</MyButton>
    </div>
  </div>
</template>

<script>
import MyButton from "@/components/MyButton.vue";
export default {
  components: {
    MyButton
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
