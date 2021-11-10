<template>
  <h1>catch all</h1>
</template>

<script>
export default {
    valitate({params}){
    return /^[a-zA-Z]+$/.test(params.name);
    }

}
</script>

<style>

</style>