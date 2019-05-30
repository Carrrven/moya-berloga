<template>
  <div>
    <p>{{ message }}{{ now }}</p>
    <p>{{ msg }}</p>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      message: "Сейчас: ",
      msg: " Назови себя",
      now: new Date().toLocaleString()
    };
  },
  created() {
    setInterval(() => (this.now = new Date().toLocaleString()), 1000);
  }
};
</script>