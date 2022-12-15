<script>
   import dp from '../dp.json'
 import {
  MDBTabs,
    MDBTabNav,
    MDBTabContent,
    MDBTabItem,
    MDBTabPane,
   MDBTable,
   MDBBtn,
   MDBBadge
 } from 'mdb-vue-ui-kit';
 import { ref } from 'vue';

  const activeTabId1 = ref('ex1-1');

 export default {
   components: {
    MDBTabs,
      MDBTabNav,
      MDBTabContent,
      MDBTabItem,
      MDBTabPane,
     MDBTable,
     MDBBtn,
     MDBBadge
   },
   setup() {
      const activeTabId1 = ref('ex1-1');

      return {
        activeTabId1,
      };
    },
 data(){
      return {
        // initial state
        persons :  dp
      }}
    };
</script>


<template>
   <MDBTabs v-model="activeTabId1">
    <!-- Tabs navs -->
    <MDBTabNav tabsClasses="mb-3">
      <MDBTabItem tabId="ex1-1" href="ex1-1"><h4>Songbird</h4></MDBTabItem>
      <MDBTabItem tabId="ex1-2" href="ex1-2"><h4>Flare</h4></MDBTabItem>
    
    </MDBTabNav>
    <!-- Tabs navs -->
    <!-- Tabs content -->
    <MDBTabContent>
      <MDBTabPane tabId="ex1-1">
        <h8>  Disclaimer : to be finalised. All data refreshed hourly. </h8>
 <MDBTable class="align-middle mb-0 bg-white">
   <thead class="bg-light">
     <tr>
       <th>Name:Address</th>
       <th>Reward Rate</th>
       <th>Avialability,Voting Power,Fee</th>
     </tr>
   </thead>
   <tbody>
     <tr v-for='(person, index) in persons' :key="index">   
      <td>
        <div class="d-flex align-items-center">
           <img  :src= "person.logoURI"   alt="" style="width: 45px; height: 45px"
             class="rounded-circle" />
           <div class="ms-3">  
             <p class="fw-bold mb-1">{{ person.name }}</p>
             <p class="text-muted mb-0">{{ person.address }}</p>
             </div>
         </div>  
       </td>
       <td>  
           <MDBBadge badge="success" pill class="d-inline">{{ person.successRate}}</MDBBadge>
       </td>  
        <td>
          <div class="ms-3">  
            <p class="fw-bold mb-1">{{ person.availability }}</p>
             <p class="fw-bold mb-1">{{ person.currentVotePower }}</p>
             <p class="text-muted mb-0">{{ person.fee.fee }}</p>
             </div>
       </td>

     </tr>

   </tbody>
 </MDBTable>
      </MDBTabPane>
      <MDBTabPane tabId="ex1-2"> <h1><b>Songbird</b></h1>
 <MDBTable class="align-middle mb-0 bg-white">
   <thead class="bg-light">
     <tr>
       <th>Name:Address</th>
       <th>SuccessRate</th>
       <th>Avialability,Voting Power,Fee</th>
     </tr>
   </thead>
   <tbody>
     <tr v-for='(person, index) in persons' :key="index">   
      <td>
        <div class="d-flex align-items-center">
           <img  :src= "person.logoURI"   alt="" style="width: 45px; height: 45px"
             class="rounded-circle" />
           <div class="ms-3">  
             <p class="fw-bold mb-1">{{ person.name }}</p>
             <p class="text-muted mb-0">{{ person.address }}</p>
             </div>
         </div>  
       </td>
       <td>  
           <MDBBadge badge="success" pill class="d-inline">{{ person.successRate}}</MDBBadge>
       </td>  
        <td>
          <div class="ms-3">  
            <p class="fw-bold mb-1">{{ person.availability }}</p>
             <p class="fw-bold mb-1">{{ person.currentVotePower }}</p>
             <p class="text-muted mb-0">{{ person.fee.fee }}</p>
             </div>
       </td>

     </tr>

   </tbody>
 </MDBTable></MDBTabPane>
     
    </MDBTabContent>
    <!-- Tabs content -->
  </MDBTabs>
<!--  
 
  <h1><b>Songbird</b></h1>
 <MDBTable class="align-middle mb-0 bg-white">
   <thead class="bg-light">
     <tr>
       <th>Name:Address</th>
       <th>SuccessRate</th>
       <th>Avialability,Voting Power,Fee</th>
     </tr>
   </thead>
   <tbody>
     <tr v-for='(person, index) in persons' :key="index">   
      <td>
        <div class="d-flex align-items-center">
           <img  :src= "person.logoURI"   alt="" style="width: 45px; height: 45px"
             class="rounded-circle" />
           <div class="ms-3">  
             <p class="fw-bold mb-1">{{ person.name }}</p>
             <p class="text-muted mb-0">{{ person.address }}</p>
             </div>
         </div>  
       </td>
       <td>  
           <MDBBadge badge="success" pill class="d-inline">{{ person.successRate}}</MDBBadge>
       </td>  
        <td>
          <div class="ms-3">  
            <p class="fw-bold mb-1">{{ person.availability }}</p>
             <p class="fw-bold mb-1">{{ person.currentVotePower }}</p>
             <p class="text-muted mb-0">{{ person.fee.fee }}</p>
             </div>
       </td>

     </tr>

   </tbody>
 </MDBTable> -->


</template>
<style scoped>
#app {
 font-family: Roboto, Helvetica, Arial, sans-serif;
}
</style>



