<template>
  <div class="ConfDevices bg-light py-5">
    <div class="container">
      <h1>{{ $t('header-device') }}</h1>
      <p>{{ $t('lead-device') }}</p>
    </div>
  </div>
  <div class="container-fluid">
    <div class="row">
      <div class="col-12">

      </div>
      <div class="col-12">
        <table class="table table-striped table-hover shadow">
          <thead>
            <tr>
              <th scope="col">index</th>
              <th scope="col">First</th>
              <th scope="col">Last</th>
              <th scope="col">Handle</th>
              <th scope="col">Handle</th>
              <th scope="col">Handle</th>
              <th scope="col">Handle</th>
              <th scope="col">Handle</th>
              <th scope="col">Handle</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">1</th>
              <td>Mark</td>
              <td>Otto</td>
              <td>@mdo</td>
            </tr>
            <tr>
              <th scope="row">2</th>
              <td>Jacob</td>
              <td>Thornton</td>
              <td>@fat</td>
            </tr>
            <tr>
              <th scope="row">3</th>
              <td colspan="2">Larry the Bird</td>
              <td>@twitter</td>
            </tr>
          </tbody>

        </table>
      </div>
    </div>
  </div>

  <!-- TEST TABLE START-->

  <div class="container text-center  mt-5 mb-5">
    <h1 class="mt-5 fw-bolder text-success "> Student's Database </h1>
    <div class="table-responsive my-5">

      <!-- The table component -->
      <Table :fields='fields' :studentData="studentData"></Table>
    </div>

  </div>
</template>

<script>
// Importing the table component
import Table from '../../components/SegwTable.vue'
export default {
  name: 'App',
  components: {
    Table
  },
  setup() {
    //An array of values for the data
    const studentData = [
      { ID: "01", Name: "Abiola Esther", Course: "Computer Science", Gender: "Female", Age: "17" },
      { ID: "02", Name: "Robert V. Kratz", Course: "Philosophy", Gender: "Male", Age: '19' },
      { ID: "03", Name: "Kristen Anderson", Course: "Economics", Gender: "Female", Age: '20' },
      { ID: "04", Name: "Adam Simon", Course: "Food science", Gender: "Male", Age: '21' },
      { ID: "05", Name: "Daisy Katherine", Course: "Business studies", Gender: "Female", Age: '22' },
    ]
    const fields = [
      'ID', 'Name', 'Course', 'Gender', 'Age'
    ]
    return { studentData, fields }
  },
}
</script>

<!-- TEST TABLE END-->
