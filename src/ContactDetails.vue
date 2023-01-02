<template>
  <div>
    <h1>Contact details</h1>
    <p>Name <strong>{{ name }}</strong></p>
    <p>Adress <strong>{{ address }}</strong></p>
  </div>
</template>

<script>
export default {
    props:['name', 'address']

}
</script>

