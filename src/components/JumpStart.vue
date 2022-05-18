<template>
  <div>
    <b-card
      title="Jumpstart"
      tag="article"
      style="max-width: 20rem"
      class="mb-2"
    >
      <b-card-text> Testing out bootstrap-vue components. </b-card-text>

      <b-button @click="showDismissibleAlert = true" variant="info">
        Activate Alert</b-button
      >
      <b-button variant="success" href="#">Change Route</b-button>
    </b-card>

    <b-alert variant="warning" v-model="showDismissibleAlert" dismissible>
      The Alert has been triggered
    </b-alert>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showDismissibleAlert: false,
    };
  },
};
</script>
