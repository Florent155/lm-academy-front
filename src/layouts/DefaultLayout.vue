<script setup>
import HeaderDefault from '../components/default/general/HeaderDefault.vue';
import FooterDefalult from '../components/default/general/FooterDefalult.vue';
</script>


<template>
<main class="px-4">
<!--header-->
<HeaderDefault/>


<!--content-->
 <div class="wrapper min-h-[80vh]"> 
<router-view />
</div>
<!--end content-->

<!--footer-->
<FooterDefalult/>
<!--end footer-->

</main>
</template>