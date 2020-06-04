<template>
  <div id="app">
    <div class="container align-middle text-center table-responsive" style="padding-top: 5%;">
      <h1>Mi lista de Empleados</h1>

      <table class="table table-bordered table-striped">
        <caption>Lista de Empleados</caption>

        <thead>
          <tr>
            <th scope="col">Nombre</th>
            <th scope="col">Apellidos</th>
            <th scope="col">Departamento</th>
          </tr>
        </thead>

        <tbody>
          <template v-for="(employee, index) in this.employeeList">
            <EmployeeRow
              :name="employee.name"
              :surname="employee.surname"
              :department="employee.department"
              :key="index"
            />
          </template>
        </tbody>
        
      </table>
    </div>
  </div>
</template>


<script>
import EmployeeRow from "@/components/EmployeeRow.vue";

export default {
  name: "App",
  components: {
    EmployeeRow
  },
  data: function() {
    return {
      employeeList: [
        { name: "Juan", surname: "García", department: "Diseño/UX" },
        { name: "Antonio", surname: "Pérez", department: "QA" },
        { name: "José Miguel", surname: "Pazos", department: "Back-End" }
      ]
    };
  }
};
</script>

<style>
</style>
