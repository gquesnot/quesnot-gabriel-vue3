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
   <table>
       <thead>
       <tr>
           <th>#</th>
           <th>Name</th>
           <th>Category</th>
           <th>Actions</th>
        </tr>
       </thead>
        <tbody>
          <tr v-for="monster in monsters" :key="monster._id">
              <td class="px-2">{{monster._id}}</td>
              <td class="px-2">{{monster.name}}</td>
              <td class="px-2">{{monster.category}}</td>
              <td class="px-2"><a :href="'/monsters/'+monster._id">
                  <button class="btn-primary">Voir</button>
              </a></td>
          </tr>
        </tbody>
   </table>

</template>
