<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div class="container">
    <div class="row">
      <div class="col-md-4">
        <p class="h3 fw-bold text-success">UserList</p>
        <p class="fst-italic">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure
          repudiandae modi dignissimos aliquam esse debitis ratione reiciendis
          aliquid! Commodi alias pariatur quisquam eos, velit adipisci quae
          ipsum nesciunt maiores quis.
        </p>
      </div>
      <div v-if="loading">
        <spinner />
      </div>

    <div v-if="errorMessage">
    <p class="fw-bold text-danger">{{errorMessage}}</p></div>

      <div class="row" v-if="!loading && users.length > 0">
        <div class="col">
          <table class="table table-hover table-striped text-center">
            <thead class="bg-success text-white">
              <tr>
                <th>Sno</th>
                <th>Name</th>
                <th>Email</th>
                <th>Company</th>
                <th>Website</th>
                <th>Location</th>
              </tr>
            </thead>

            <tbody>
              <tr v-for="user in users" :key="user.id">
                <td>{{ user.id }}</td>
                <td>{{ user.name }}</td>
                <td>{{ user.email }}</td>
                <td>{{ user.company.name }}</td>
                <td>{{ user.website }}</td>
                <td>{{ user.address.city }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { UserService } from "@/services/UserService";
import Spinner from "./Spinner.vue";
export default {
  components: { Spinner },
  // eslint-disable-next-line vue/multi-word-component-names
  name: "UserList",
  data: function () {
    return {
      loading: false,
      users: [],
      errorMessage: null,
    };
  },
  created: async function () {
    try {
      this.loading = true;
      let response = await UserService.getAllUsers();
      this.loading = false;
      this.users = response.data;
      console.log(response.data);
    } catch (error) {
      this.loading = false;
      this.errorMessage = error;
      console.log(error);
    }
  },
};
</script>

<style scoped></style>
