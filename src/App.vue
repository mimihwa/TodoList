<template>
    <nav class="navbar">
        <ul>
            <li><router-link :to="{name:'Home'}">HOME</router-link></li> <!-- name 링크 -->
            <li><router-link :to="{name: 'Todos'}">TODOS</router-link></li> <!-- path 링크 -->
        </ul>

    </nav>
    <router-view/>
</template>

<script>
   export default {

   }
</script>

<style>
    .navbar{border: 1px solid#ddd; width: 100%; padding: 20px;}
    .navbar ul{max-width: 1024px; width: 100%; list-style: none; display: flex; margin: 0 auto;}
    .navbar li a{text-decoration: none; padding: 10px 20px; font-weight: bold; color: #55b796;}
</style>