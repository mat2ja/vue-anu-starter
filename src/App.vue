<script lang="ts" setup>
const drawerStore = useDrawerStore()
</script>

<template>
  <ADrawer
    v-model="drawerStore.isDrawerShown"
    title="Drawer title"
    subtitle="Chocolate cake tiramisu donut"
  >
    <template #default>
      <div class="a-card-body">
        <ABtn
          variant="light"
          class="text-sm"
          @click="drawerStore.close"
        >
          Close
        </ABtn>
      </div>
    </template>
  </ADrawer>

  <main
    container mx-auto p="x-4 y-12" min-h-screen
    text="center base-700 dark:base-200" font-sans
    space-y-6
  >
    <RouterView />
    <TheFooter />
  </main>
</template>

<style lang="postcss">
body {
  @apply bg-base-100 dark:bg-base-900 transition-colors duration-400 caret-primary;
}

::selection {
  @apply bg-primary/15 dark:bg-primary/20;
}
</style>
