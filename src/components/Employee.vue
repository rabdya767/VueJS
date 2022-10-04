<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <p class="h3">Employee</p>
        <ul class="list-group">
          <li class="list-group-item">Name : {{ this.employee.name }}</li>
          <li class="list-group-item">Age : {{ this.employee.age }}</li>
          <li class="list-group-item">
            Designation : {{ this.employee.designation }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Employee",
  data: function () {
    return {
      //state
      employee: {
        name: "rabdya santhosh",
        age: 21,
        designation: "Software Engineer",
      },
    };
  },
  props: {},
};
</script>

<style scoped></style>
