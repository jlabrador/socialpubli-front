<script setup lang="ts">
import DataTable from 'datatables.net-vue3';
import DataTablesCore from 'datatables.net';

DataTable.use(DataTablesCore);

const columns = [
  { data: 'name' },
  { data: 'height' },
  { data: 'mass' },
  { data: 'hair_color' },
  { data: 'skin_color' },
  { data: 'eye_color' },
];
</script>

<template>
  <div>
    <h1>Prueba técnica SocialPubli</h1>
    <h2>Listado de personajes de Star Wars</h2>

    <DataTable
        :columns="columns"
        ajax="http://api.socialpubli.local:8888/api/people"
        class="display"
        width="100%"
    >
      <thead>
      <tr>
        <th>Name</th>
        <th>Height</th>
        <th>Mass</th>
        <th>Hair color</th>
        <th>Skin Color</th>
        <th>Eye Color</th>
      </tr>
      </thead>
      <tfoot>
      <tr>
        <th>Name</th>
        <th>Position</th>
        <th>Office</th>
        <th>Extn.</th>
        <th>Start date</th>
        <th>Salary</th>
      </tr>
      </tfoot>
    </DataTable>
  </div>
</template>

<style>
@import 'datatables.net-dt';
</style>
