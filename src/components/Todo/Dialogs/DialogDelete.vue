<template>
  <v-row justify="center">
    <v-dialog value="true" persistent max-width="290">
      <v-card>
        <v-card-title class="headline"> ¿Borrar? </v-card-title>
        <v-card-text> ¿Seguro quires eliminar este item?</v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="green darken-1" text @click="$emit('close')">
            No
          </v-btn>
          <v-btn
            color="red darken-1"
            text
            @click="$store.dispatch('deleteTask', task.id)"
          >
            Sí
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
export default {
  props: ["task"],
  data() {
    return {
      dialog: false,
    };
  },
};
</script>

<style>
</style>