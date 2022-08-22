<template>
  <div id="app">
    <div id="date">{{ date }}</div>
    <div id="time">{{ time }}</div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      timer: null,
      date: "--月--日",
      time: "--:--:--",
    };
  },
  computed: {},
  watch: {},
  mounted() {
    const timer = setInterval(() => {
      this.clock();
    }, 1000);
    this.$once("hook:beforeDestroy", () => {
      clearInterval(timer);
    });
  },
  methods: {
    clock() {
      const now = new Date();
      const month = `${now.getMonth() + 1}`;
      const day = `${now.getDate()}`;
      const hour = `${now.getHours()}`;
      const minute = `${now.getMinutes()}`;
      const second = `${now.getSeconds()}`;
      this.date = `${month.padStart(2, "0")}月${day.padStart(2, "0")}日`;
      this.time = `${hour.padStart(2, "0")}:${minute.padStart(2, "0")}:${second.padStart(2, "0")}`;
    },
  },
};
</script>
<style lang="scss" scoped>
#app {
  width: 100%;
  height: 100%;
  overflow: hidden;
}

#date {
  margin-top: 50px;
  text-align: center;
  font-size: 24vh;
  font-weight: bold;
  color: #e2ecfd;
}

#time {
  text-align: center;
  font-size: 48vh;
  font-weight: bold;
  line-height: 48vh;
  color: #e2ecfd;
}
</style>
