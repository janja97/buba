<template>
  <div>
    <NavbarBlack />
    <div class="my-5">
      <Filters />
    </div>
  </div>
</template>
<script>
import { ref } from '@vue/reactivity';
import NavbarBlack from '../components/NavbarBlack.vue'
import Filters from '../components/Filters.vue'

export default {
  name: 'AppFilters',
  
  components: {
    NavbarBlack,
    Filters,
 
  },
  mounted() {
    var checkbox = document.getElementById("menuToggle");
    if (checkbox.checked) {
      checkbox.checked = false;
    }
  }
};

</script>

<style setup>

</style>
  