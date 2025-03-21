<template>
  <!--ketu shenohet kodi i html-->

  <p>{{ message }}</p>
  <p class="text-green-200">
Florent
  </p>
</template>


<script setup>
import {ref} from "vue";
const message = ref("Florent");

setTimeout(() => {
  message.value = "hello!"
}, 5000);
</script>
 
<style>

p{
  color:red;
}

</style>
