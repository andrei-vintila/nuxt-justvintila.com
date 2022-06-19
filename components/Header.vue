<template>
  <div class="flex justify-between max-w-2xl px-4 py-4 mx-auto sm:px-8">
    <!-- Navigation -->
    <div class="text-gray-700 dark:text-gray-200">
      <ContentNavigation v-slot="{ navigation }">
        <NuxtLink
          v-for="link of navigation"
          :key="link._path"
          :to="link._path"
          active-class="font-bold"
          class="mr-4"
        >
          {{ link.navTitle || link.title }}
        </NuxtLink>
      </ContentNavigation>
    </div>
    <!-- Social icons & Color Mode -->
    <div text="xl gray4" flex gap-3 class="text-gray-500 dark:text-gray-200 transition">
      <a href="https://twitter.com/Atinux" title="Twitter" class=" hover:text-gray-700 dark:hover:text-gray-300 i-carbon-logo-twitter" />
      <a href="https://github.com/Atinux/content-wind" title="GitHub" class=" hover:text-gray-700 dark:hover:text-gray-300 i-carbon-logo-github" />
      <ColorModeSwitch class="hover:text-gray-700 dark:hover:text-gray-300" />
    </div>
  </div>
</template>
