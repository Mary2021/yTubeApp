<template>
  <h1>catch all numbers</h1>
</template>

<script>
export default {
    valitate({params}){
    return /^\d+$/.test(params.id);
    }

}
</script>

<style>

</style>