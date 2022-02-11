<template>
  <div class="row">
    <div class="col-8">
      <h3>Nested draggable</h3>
      <p>There is an error here. el-button and el-switch cannot drag each other</p>
      <nested-draggable :tasks="list" />
    </div>
  </div>
</template>

<script>
import nestedDraggable from "./components/nested.vue";
export default {
  name: "nested-example",
  display: "Nested",
  order: 15,
  components: {
    nestedDraggable
  },
  data() {
    return {
      list: [
        {
          name: "el-scrollbar",
          tasks: [
            {
              name: "el-button",
              tasks: []
            }, {
              name: "el-switch",
              tasks: []
            }
          ]
        }
      ]
    };
  }
};
</script>
<style scoped></style>
