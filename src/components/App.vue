<script>

 import {
   MDBTable,
   MDBBtn,
   MDBBadge
 } from 'mdb-vue-ui-kit';


 export default {
   components: {
     MDBTable,
     MDBBtn,
     MDBBadge
   },
 
 data(){
      return {
        // initial state
        dataprov : [
          {name: Max, age: 20},
          {name: Jan, age: 30},
          {name: Ana, age: 40}
        ]
      }}
    };
</script>


<template>
  <h1><b>Songbird</b></h1>
 <MDBTable class="align-middle mb-0 bg-white">
   <thead class="bg-light">
     <tr>
       <th>Name</th>
       <th>Address</th>
       <th>SuccessRate</th>
     </tr>
   </thead>
   <tbody>
     <tr >
       <td>
         <div class="d-flex align-items-center">
           <img src="https://mdbootstrap.com/img/new/avatars/8.jpg" alt="" style="width: 45px; height: 45px"
             class="rounded-circle" />
           <div class="ms-3">
             <p class="fw-bold mb-1">John Doe</p>
             <p class="text-muted mb-0">john.doe@gmail.com</p>
           </div>
         </div>
       </td>
       <td>
         <p class="fw-normal mb-1">Software engineer</p>
         <p class="text-muted mb-0">IT department</p>
       </td>
       <td>
         <MDBBadge badge="success" pill class="d-inline">Active</MDBBadge>
       </td>
     </tr>

   </tbody>
 </MDBTable>
</template>
<style scoped>
#app {
 font-family: Roboto, Helvetica, Arial, sans-serif;
}
</style>



