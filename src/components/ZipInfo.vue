<template>
  <ion-card v-if="info">
    <ion-card-header>
      <ion-card-subtitle>{{info["post code"]}}</ion-card-subtitle>
      <ion-card-title>{{info["places"][0]['place name']}}</ion-card-title>
      <ion-card-content>
        <ion-list>
          <ion-label>
            <strong>State:</strong>
            {{info["places"][0]['state']}} ({{info["places"][0]['state abbreviation']}})
          </ion-label>
        </ion-list>
      </ion-card-content>
    </ion-card-header>
  </ion-card>
</template>

<script>
export default {
  name: "ZipInfo",
  props: ["info"]
};
</script>


