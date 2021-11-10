<template>
  <div class="home">
    <field-add />
    <list-task v-if="$store.state.tasks.length" />
    <no-task v-else />
  </div>
</template>

<script>
import FieldAdd from "../components/Todo/FieldAdd.vue";
import ListTask from "../components/Todo/ListTask.vue";
import NoTask from "../components/Todo/NoTask.vue";

export default {
  components: {
    "field-add": FieldAdd,
    "list-task": ListTask,
    "no-task": NoTask,
  },
};
</script>


