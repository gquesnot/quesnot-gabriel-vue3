<script setup>


import { onMounted, ref } from "vue";
import Monster from "@/components/Monster.vue";

const props = defineProps(["monster_id"]);
let monster = ref([]);
onMounted(() => {
  fetch("https://metallo.ew.r.appspot.com/monsters/"+props.monster_id)
    .then((response) => response.json())
    .then((data) => {
      monster.value = data;
    });
});
</script>

<template>
<div class="flex flex-column my-4">
    <h2>{{monster._id}}</h2>
    <img style="width: 30%" :src="monster.image" :alt="monster.name" />
    <h2>  {{monster.name}}</h2>
    <p>{{monster.description}}</p>

</div>

</template>
