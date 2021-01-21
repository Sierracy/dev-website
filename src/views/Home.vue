<template>
  <span>
    <home-hero></home-hero>
    <project-browser></project-browser>
    <contact></contact>
    
  </span>
</template>

<script>
import HomeHero from '@/components/HomeHero'
import ProjectBrowser from '@/components/ProjectBrowser'
import Contact from '@/components/Contact'

export default {
  name: 'home',
  components: {
    HomeHero, ProjectBrowser, Contact,
  }
}
</script>
