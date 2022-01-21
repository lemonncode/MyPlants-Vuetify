<template>
  <div class="home">
    <field-add />
    <list-task v-if="$store.state.tasks.length" />
    <no-task v-else />
    <button-done-sorting v-if="$store.state.sorting" />
  </div>
</template>

<script>
import FieldAdd from "../components/Todo/FieldAdd.vue";
import ListTask from "../components/Todo/ListTask.vue";
import NoTask from "../components/Todo/NoTask.vue";
import ButtonDoneSorting from "../components/Todo/ButtonDoneSorting.vue";

export default {
  components: {
    "field-add": FieldAdd,
    "list-task": ListTask,
    "no-task": NoTask,
    "button-done-sorting": ButtonDoneSorting,
  },
};
</script>


