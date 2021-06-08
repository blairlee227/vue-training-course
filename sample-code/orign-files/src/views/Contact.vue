<template>
  <div id="contact">
    <!-- Header component -->
    <Header :pageTitle="pageTitle" />
    <div class="container">
      <button class="default-btn">Add</button>
      <!-- Please create a Table component and complete CRUD operations. -->
      <table class="table" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <th>No.</th>
            <th>Name</th>
            <th>Phone</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>A</td>
            <td>0912345678</td>
            <td>
              <button class="edit-btn">Edit</button>
              <button class="delete-btn">
                Delete
              </button>
            </td>
          </tr>
          <tr>
            <td>2</td>
            <td>B</td>
            <td>0912345679</td>
            <td>
              <button class="edit-btn">Edit</button>
              <button class="delete-btn">
                Delete
              </button>
            </td>
          </tr>
        </tbody>
      </table>
      <p>共 2 筆</p>
    </div>
    <!-- Model component -->
    <Model :title="model.title" v-if="model.show">
      <label>Name</label>
      <input />
      <label>Phone</label>
      <input />
      <button class="default-btn float-right">
        Save
      </button>
    </Model>
  </div>
</template>
<script>
import Header from "@/components/Header.vue";
import Model from "@/components/Model.vue";

export default {
  name: "Contact",
  components: { Header, Model },
  data() {
    return {
      pageTitle: "Contacts.",
      model: {
        title: "",
        show: false,
      },
    };
  },
};
</script>
