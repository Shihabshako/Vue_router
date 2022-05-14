<template>
 <div class="text-center space-y-4">
      <h2 class="text-xl font-bold">Job Details</h2>
      <p>The job id is {{ id }} </p>
  </div>
</template>

<script>
import { ref } from 'vue'
import { useRoute } from 'vue-router'
export default {
    props : ['id'],
    setup(props){
        // const route = useRoute()
        // const id = ref(route.params.id)

        const id = ref(props.id)
        
        return {
            id
        }
    }
}
</script>

<style>

</style>