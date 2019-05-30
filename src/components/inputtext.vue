<template>
  <div>
    <input type="text" v-model="message">
    <h4>{{ error }}</h4>
  </div>
</template>
<script>
export default {
  props: {
    value: {
      type: String,
      default: ""
    }
  },
  computed: {
    listeners() {
      return {
        // Pass all component listeners directly to input
        ...this.$listeners,
        // Override input listener to work with v-model
        input: event => this.$emit("input", event.target.value)
      };
    }
  },
  data() {
    return {
      message: "",
      error: "",
      msg: "",
      names: [
        "Susel",
        "Сусел",
        "Сергей",
        "Кум",
        "Бабак",
        "susel",
        "сусел",
        "сергей",
        "кум",
        "бабак"
      ],
      name: ""
    };
  },
  watch: {
    message: function() {
      for (var name of this.names) {
        this.msg = name;
        if (this.message === name) {
          let tname = name;
          return (this.error = "Пошли бухать " + tname);
        } else {
          this.error = "Не знаю таких";
        }
      }
    }
  }
};
</script>

