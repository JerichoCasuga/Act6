<template>
  <breeze-authenticated-layout>
    <template #header>
      <h2 class="font-semibold text-xl text-gray-800 leading-tight">
        Dashboard
      </h2>
    </template>

    <div class="py-12">
      <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
        <div class="bg-white overflow-hidden shadow-sm sm:rounded-lg">
          <div class="p-6 bg-white border-b border-gray-200">
            <table class="rounded-t-lg m-5 w-5/6 mx-auto bg-gray-200 text-gray-800">
  <tr class="text-left border-b-2 border-gray-300">
    <th class="px-4 py-3">ID</th>
    <th class="px-4 py-3">Stock Category ID</th>
    <th class="px-4 py-3">Description</th>
    <th class="px-4 py-3">UOM</th>
    <th class="px-4 py-3">Barcode</th>
    <th class="px-4 py-3">Discontinued</th>
    <th class="px-4 py-3">Date Created</th>
  </tr>

  <tr v-for="item in stocks" class="bg-gray-100 border-b border-gray-200">
    <td class="px-4 py-3">{{ item.id }}</td>
    <td class="px-4 py-3">{{ item.stock_category_id }}</td>
    <td class="px-4 py-3">{{ item.description }}</td>
    <td class="px-4 py-3">{{ item.uom }}</td>
    <td class="px-4 py-3">{{ item.barcode }}</td>
    <td class="px-4 py-3">{{ item.discontinued }}</td>
    <td class="px-4 py-3">{{ item.photo_path }}</td>
    <td class="px-4 py-3">{{ item.created_at }}</td>
  </tr>


</table>

          </div>
        </div>
      </div>
    </div>
  </breeze-authenticated-layout>
</template>

<script>

import BreezeAuthenticatedLayout from "@/Layouts/Authenticated.vue";

export default {

    props:{
        stocks: Array,


    },

    components:{
        BreezeAuthenticatedLayout,
    },

};
</script>
