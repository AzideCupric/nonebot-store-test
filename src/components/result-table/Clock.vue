<script setup lang="ts">
import Zero from "vue-material-design-icons/CircleOutline.vue";
import Eight from "vue-material-design-icons/ClockTimeEightOutline.vue";
import Eleven from "vue-material-design-icons/ClockTimeElevenOutline.vue";
import Five from "vue-material-design-icons/ClockTimeFiveOutline.vue";
import Four from "vue-material-design-icons/ClockTimeFourOutline.vue";
import Nine from "vue-material-design-icons/ClockTimeNineOutline.vue";
import One from "vue-material-design-icons/ClockTimeOneOutline.vue";
import Seven from "vue-material-design-icons/ClockTimeSevenOutline.vue";
import Six from "vue-material-design-icons/ClockTimeSixOutline.vue";
import Ten from "vue-material-design-icons/ClockTimeTenOutline.vue";
import Three from "vue-material-design-icons/ClockTimeThreeOutline.vue";
import Twelve from "vue-material-design-icons/ClockTimeTwelveOutline.vue";
import Two from "vue-material-design-icons/ClockTimeTwoOutline.vue";

// like 2023-06-26T21:53:28.908452+08:00
defineProps<{ hour: number }>();
function getClockIcon(hour: number) {
  switch (hour) {
    case 1:
      return One;
    case 2:
      return Two;
    case 3:
      return Three;
    case 4:
      return Four;
    case 5:
      return Five;
    case 6:
      return Six;
    case 7:
      return Seven;
    case 8:
      return Eight;
    case 9:
      return Nine;
    case 10:
      return Ten;
    case 11:
      return Eleven;
    case 12:
      return Twelve;
    default:
      return Zero;
  }
}
</script>

<template>
  <component :is="getClockIcon(hour)" />
</template>
