<template>
  <div>
    <ul class="list-group">
        <li class="list-group-item" v-for="(equipe, index) in equipes" :key="index">
            <EquipePronta :dados="equipe"/>
        </li>
    </ul>
  </div>
</template>

<script>
import EquipePronta from '@/components/EquipePronta'
import { mapState } from 'vuex';


export default {
    name: 'ListaEquipes',
    components: {
        EquipePronta
    },
    computed: {
        ...mapState(['equipes'])
    }
}
</script>

<style>

</style>