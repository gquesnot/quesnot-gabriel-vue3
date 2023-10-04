<script setup>
import {onMounted, ref} from "vue";
import Monster from "@/components/Monster.vue";

  let monsters = ref([])

  onMounted(() => {
       fetch("https://metallo.ew.r.appspot.com/monsters")
        .then(response => response.json())
        .then(data => {
          monsters.value = data
        })
  })

</script>



<template>
<h1>Monsters</h1>
<div >
    <Monster :monster="monster" v-for="monster in monsters"  :key="monster._id"/>
</div>
  
</template>
