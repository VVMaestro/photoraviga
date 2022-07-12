<template>
  <div>
    {{ hello }}
    {{ data.gem }}
    <v-btn @click="changeSmth">
      Изменить что то
    </v-btn>
  </div>
</template>

<script lang="ts" setup>
  const hello = ref('Hello World Photoraviga');
  const { data, refresh } = await useFetch('/api/gem');

  const changeSmth = () => {
    refresh();
  }
</script>
