<template>
  <v-card ref="popup" max-width="370" width="370" class="ol-popup mx-auto">
    <v-toolbar :color="$appConfig.app.color.primary" flat height="50" dark>
      <v-toolbar-title>{{ title ? title : '' }}</v-toolbar-title>
      <v-spacer></v-spacer>
      <slot name="close"></slot>
    </v-toolbar>
    <v-card-text style="max-height: 350px" class="pb-0 pr-0">
      <slot name="body"></slot>
    </v-card-text>

    <v-divider class="mt-2"></v-divider>
    <v-card-actions class="pt-0 mt-1">
      <slot name="actions"></slot>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  name: 'overlay-popup',
  props: {
    title: {type: String, required: false},
  },
};
</script>
