---
layout: 'home'
lang: 'es-ES'
title: 'Début'
hero:
  name: 'Drop Commander'
  text: 'Site de fans de l’univers.'
  tagline: 'Fait par des fans, pour des fans.'
features:
  - title: 'Dropfleet Commander V1.3.1'
    link: './dfc/'
    details: 'Mise à jour des règles de Dropfleet Commander.'
    icon:
      light: '/moon-landing.png'
      dark: '/moon-landing.dark.png'
      width: '100px'
      height: '100px'
  - title: 'Dropzone Commander V2.2.0'
    link: './dzc/'
    details: 'Mise à jour des règles de Dropzone Commander.'
    icon:
      light: '/orbit.png'
      dark: '/orbit.dark.png'
      width: '100px'
      height: '100px'
---
<script lang="ts" setup>
import { onMounted } from 'vue'
import { useData } from 'vitepress'
const { frontmatter } = useData()

onMounted(() => {
  let expires = new Date()
  expires.setFullYear(expires.getFullYear()+1)
  document.cookie = `nf_lang=${frontmatter.value.lang}; expires=${expires.toUTCString()}; path=/`
})
</script>
