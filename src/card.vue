<template >
   <div>
      <table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <!-- <tr>
      <th scope="row">1</th>
      <td>{{ item.name }}</td>
      <td>{{ item.age }}</td>
    </tr> -->
 
  </tbody>
</table>
   </div>
</template>

<script>
export default {
    data(){
      return {
         data:[
            {name:"sajib",age:23},
            {name:"shaon",age:24},
            {name:"rakib",age:25},
            {name:"bg",age:26},
            {name:"ib",age:27},
      ]
      }
    },
    
    created:{
      // getData(){
      //    axios.get
      // }
    }
}
</script>
 
<style>

</style>