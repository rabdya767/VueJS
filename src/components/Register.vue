<template>
  <div class="container">
    <div class="row">
      <div class="col-md-3">
        <!-- <pre>{{ this.user }}</pre> -->
        <div class="card shadow-lg">
          <div class="card-header bg-success text-white">
            <p class="h3">Register Here</p>
          </div>
          <div class="card-body bg-light">
            <form @submit.prevent="register()">
              <div class="mb-2">
                <input
                  v-model="user.name"
                  type="text"
                  class="form-control"
                  placeholder="Name"
                />
              </div>
              <div class="mb-2">
                <input
                  v-model="user.email"
                  type="text"
                  class="form-control"
                  placeholder="Email"
                />
              </div>
              <div class="mb-2">
                <input
                  v-model="user.password"
                  type="password"
                  class="form-control"
                  placeholder="Password"
                />
              </div>
              <div class="mb-2">
                <input type="submit" class="btn btn-success" value="Register" />
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Register",
  data: function () {
    return {
      user: {
        name: "",
        email: "",
        password: "",
      },
    };
  },
  methods: {
    register: function () {
      console.log(this.user);
    },
  },
};
</script>

<style scoped></style>
