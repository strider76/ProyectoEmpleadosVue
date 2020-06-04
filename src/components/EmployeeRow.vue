<template>
  <tr>
    <td>{{this.name}}</td>
    <td>{{this.surname}}</td>
    <td>{{this.department}}</td>
  </tr>
</template>

<script>
export default {
  name: "EmployeeRow",
  props: {
    name: String,
    surname: String,
    department: String
  }
};
</script>

<style>
</style>