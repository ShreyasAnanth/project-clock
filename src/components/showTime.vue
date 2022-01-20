<template>
  <div>
    <h4>Current Time</h4>
    <div>
      {{ exactTime }}
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      exactTime: 'Loading Time...',
    };
  },
  mounted() {
    this.showTime();
  },
  methods: {
    showTime() {
      setInterval(() => {
        const now = new Date();
        this.exactTime = now;
      }, 1000);
    },
  },
};
</script>

