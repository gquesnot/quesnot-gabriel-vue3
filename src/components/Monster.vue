<script setup>

const props = defineProps(["monster"]);

</script>

<template>

  <div style="display:flex;flex-direction:column;margin-top:20px">
  <img :src="monster.image" :alt="monster.name" />
  <h3>{{monster.name}}</h3>
    <a :href="'/monsters/'+monster._id">
        <button class="btn-primary">Voir</button>
    </a>
  </div>
</template>
