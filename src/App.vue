<script setup>
import {ref} from 'vue';

      const inputText = ref("....")
      const selectedNationality = ref("us")
</script>
<template>
  <div>
   <h1>Let me know your nationality!</h1>
    <label for="inputText">Enter your name:</label>
    <input type="text" id="inputText" v-model="inputText" />
    <label for="nationality">Select your nationality:</label>
    <select id="nationality" v-model="selectedNationality">
      <option value="us">United States</option>
      <option value="fr">France</option>
      <option value="jp">Japan</option>
      <option value="cn">China</option>
      <option value="kr">South Korea</option>
    </select>

   
    <div v-if="selectedNationality === 'us'">
      <h2>Welcome, {{ inputText }}!</h2>
    </div>
    <div v-else-if="selectedNationality === 'fr'">
      <h2>Bonjour, {{ inputText }}!</h2>
    </div>
    <div v-else-if="selectedNationality === 'jp'">
      <h2>こんにちは、{{ inputText }}さん！</h2>
    </div>
    <div v-else-if="selectedNationality === 'cn'">
      <h2>你好，{{ inputText }}！</h2>
    </div>
     <div v-else-if="selectedNationality === 'kr'">
      <h2>Anyeonghaseyo，{{ inputText }}！</h2>
    </div>
    <div v-else>
      <h2>Hello, {{ inputText }}!</h2>
    </div>
  </div>

    
</template>


