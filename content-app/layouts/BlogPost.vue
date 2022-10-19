<script setup>
 const { next } = useContent()
</script>
<template>
   <div class="container">
    <div class="content">
      <slot />
    </div> 
    <div v-if="next" class="next-link">
      <div>Read next post</div>
      <NuxtLink :to="next._path">
           {{ next.title }}
      </NuxtLink>
      <p>{{ next.description }}</p>
    </div>
  </div>
</template>

<style scoped>
 .container {
    max-width: 580px;
    margin: 0 auto;
  }
 .content {
    padding: 1rem;
    margin-bottom: 10px;
 }
 .next-link {
    margin-top: 16px;
    text-align: center;
 }
 .next-link a {
    color: black;    
    font-weight: 900;
    font-size: 1.2rem;
 }
 .next-link p {
    margin: 4px;
    color: #686868;
 }
 
</style>

