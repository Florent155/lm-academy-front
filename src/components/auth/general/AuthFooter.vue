<script setup>

</script>

<template>
     <div class="absolute bottom-0 left-0" style="margin-left: 25px; margin-bottom: 21px;">
     <div class="flex gap-3 text-[#0085DB]">
      <router-link :to="{name: 'PrivacyPolicy'}" active-class="border-b-textPrimary border-b-2">Privacy Policy</router-link>
            <span>|</span>
            <router-link :to="{name: 'TermsOfService'}" active-class="border-b-textPrimary border-b-2">Terms of service</router-link>
  </div>
</div>
</template>