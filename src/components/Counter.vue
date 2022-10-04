
<template>
  <div class="container">
    <div class="row">
      <div class="col-md-4">
        <div class="card shadow-lg">
          <div class="card-body">
            <p class="h3 display-3">{{ count }}</p>
            <button class="btn btn-success m-1" @click="this.increment()">
              Increment
            </button>
            <button class="btn btn-warning m-1" @click="this.decrement()">
              Decrement
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Counter",
  data: function () {
    return {
      count: 0,
    };
  },
  methods: {
    increment: function () {
      this.count += 1;
    },
    decrement: function () {
      if (this.count < 1) {
        this.count = 0;
      } else {
        this.count -= 1;
      }
    },
  },
};
</script>

<style scoped></style>
