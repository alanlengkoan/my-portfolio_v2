<template>
  <main>
    <section id="home" class="flex items-center p-4">
      <div class="container mx-auto px-3">
        <div class="py-4 text-center">
          <!-- begin:: introduce myself -->
          <img class="py-2 px-2 mx-auto rounded-full" src="./../assets/img/profil.jpg" alt="Profile" width="200" height="auto">
          <h1 class="font-bold text-3xl">
            Yo, I'm Alan Saputra Lengkoan a
          </h1>
          <h1 class="font-bold text-2xl py-2">
            <VueWriter :array="['Web Developer', 'Mobile App Developer']" :typeSpeed="50" />
          </h1>
          <p class="py-2">
            Follower of Jesus | Code Addict | Tech Enthusiast | Plus Ultra!
          </p>
          <div class="py-2 flex items-center justify-center">
            <div class="grid gap-4 grid-cols-2 sm:grid-cols-3 md:grid-cols-6 lg:grid-cols-6">
              <a v-for="row in contact" :key="row.icon" :href="row.href" target="_blank" :aria-label="row.name"
                class="text-2xl rounded-full outline p-2 mx-2 hover:bg-background-secondary hover:outline-copy-secondary hover:text-copy-primary">
                <font-awesome-icon :icon="row.icon" />
              </a>
            </div>
          </div>
          <!-- end:: introduce myself -->
        </div>
      </div>
    </section>
  </main>
</template>

<script setup>
  const contact = [
    {
      name: 'instagram',
      icon: 'fa-brands fa-instagram',
      href: 'https://www.instagram.com/alanlengkoan',
    },
    {
      name: 'twitter',
      icon: 'fa-brands fa-twitter',
      href: 'https://twitter.com/LengkoanAlan',
    },
    {
      name: 'facebook',
      icon: 'fa-brands fa-facebook',
      href: 'https://web.facebook.com/alanlengkoan',
    },
    {
      name: 'github',
      icon: 'fa-brands fa-github',
      href: 'https://www.github.com/alanlengkoan',
    },
    {
      name: 'linkedin',
      icon: 'fa-brands fa-linkedin',
      href: 'https://www.linkedin.com/in/alanlengkoan',
    },
    {
      name: 'discord',
      icon: 'fa-brands fa-discord',
      href: 'https://discordapp.com/users/3628',
    },
  ]
</script>

<script>
import VueWriter from 'vue-writer'

export default {
  components: { VueWriter }
}
</script>

<style>
  #home {
    min-height: 100vh;
  }
</style>