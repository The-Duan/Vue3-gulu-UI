<demo>
基本
</demo>

<template>
  <Switch v-model:value="bool" />
</template>

<script lang="ts">
import {
  ref
} from 'vue';
import {Switch} from "../../lib/index";
export default {
  components: {
    Switch
  },
  setup() {
    const bool = ref(false);
    return {
      bool
    }
  }
}
</script>
