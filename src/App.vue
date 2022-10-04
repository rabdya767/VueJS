<template>
  <div class="container mt-3">
    <div class="grid">
      <div class="row">
        <div class="col">
          <p class="h3 text-success fw-bold">App Component</p>
          <p class="fst-italic">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptate
            laudantium magnam modi. Dignissimos, accusamus illum impedit, quae
            provident ea vel et expedita sequi iste omnis molestias voluptatem
            adipisci obcaecati rerum.
          </p>
        </div>
      </div>
    </div>
    <!-- <Counter />  -->
    <!-- <Customer name="RABDYA SANTHOSH" age="21" designation="Software Engineer" /> -->
    <!-- <Employee /> -->
    <!-- <Greeting /> -->
    <!-- <Register /> -->
    <!-- <Spinner /> -->
    <UserList />
  </div>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import Customer from "./components/Customer";
import Employee from "./components/Employee";
import Counter from "./components/Counter";
import Greeting from "./components/Greeting";
import Register from "./components/Register";
import UserList from "./components/UserList";
import Spinner from "./components/Spinner";
export default {
  // eslint-disable-next-line vue/no-unused-components
  components: {Customer,Employee,Counter,Greeting,Register,UserList,Spinner,
  },
};
</script>

<style>
@import "./styles.css";
</style>
