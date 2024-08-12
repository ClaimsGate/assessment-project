<script lang="ts">
import Vue from "vue";
import TextComponent from "./text.vue";

export default Vue.extend({
  name: "ClaimComponent",
  components: {
    TextComponent,
  },
  props: {
    claim: {
      type: Object,
    },
  },
});
</script>

<template>
  <section>
    <TextComponent
      type="h1"
      :text="`Claim created for ${claim.userData.firstName} ${claim.userData.lastName}`"
      class="mb-3"
    />
    <p>Status: {{ claim.status }}</p>
    <p>IP Address: {{ claim.creationIpAddress }}</p>
    <p>Raw Data: {{ claim.data }}</p>
  </section>
</template>
