<template>
  <div class="home">
    <b-button @click="showCard = !showCard"> Toggle Jumpstart Card </b-button>

    <div class="jumpstart-div">
      <b-card
        title="Jumpstart"
        tag="article"
        style="max-width: 20rem"
        class="mb-2"
        v-if="showCard"
      >
        <b-card-text> Testing out bootstrap-vue components. </b-card-text>

        <div class="button-div">
          <b-button
            class="alert-button"
            @click="showDismissibleAlert = true"
            variant="info"
          >
            Activate Alert
          </b-button>
          <b-button variant="success" href="/new-route">Change Route</b-button>
        </div>
      </b-card>

      <b-alert variant="warning" v-model="showDismissibleAlert" dismissible>
        The Alert has been triggered
      </b-alert>
    </div>

    <router-view />
  </div>
</template>

<style>
.button-div {
  display: flex;
  justify-content: space-between;
}
.home {
  display: flex;
  align-items: center;
  flex-direction: column;
  margin-top: 20px;
}
.jumpstart-div {
  margin-top: 20px;
}
</style>

<script>
export default {
  data() {
    return {
      showCard: false,
      showDismissibleAlert: false,
    };
  },
};
</script>
