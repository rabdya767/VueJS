<template>
  <div class="container">
    <div class="row">
      <div class="col-md-5">
        <div class="card shadow-lg">
          <div class="card-body">
            <p class="h3 display-3">
              Hello <span class="fw-bold">{{ this.msg }}</span>
            </p>
            <button class="btn btn-success m-1" @click="greet('Good Morning')">
              Good Morning
            </button>
            <button
              class="btn btn-warning m-1"
              @click="this.greet('Good Afternoon')"
            >
              Good Afternoon
            </button>
            <button
              class="btn btn-danger m-1"
              @click="this.greet('Good Evening')"
            >
              Good Evening
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
  name: "Test",
  data: function () {
    return {
      msg: "",
    };
  },
  methods: {
    greet: function (value) {
      this.msg = value;
    },
  },
};
</script>

<style scoped></style>
