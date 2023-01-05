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
        <h8> Disclaimer : to be finalised. All data refreshed hourly. </h8>
        <MDBTable class="align-middle mb-0 bg-white">
          <thead class="bg-light">
            <tr>
              <th>Rank</th>
              <th>Name</th>
              <th>Reward Rate</th>
              <th>Fee</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(person, index) in personssb" :key="index">
              
            <!-- <tr v-for="person in persons" :key="person.chainId"> -->
              <td>
                <MDBBadge badge="success" pill class="d-inline">{{
                  index
                }}</MDBBadge>
              </td>
              <td>
                <div class="d-flex align-items-center">
                  <img
                    :src="person.logoURI"
                    alt=""
                    style="width: 45px; height: 45px"
                    class="rounded-circle"
                  />
                  <div class="ms-3">
                    <p class="fw-bold mb-1">{{ person.name }}</p>
                  </div>
                </div>
              </td>
              <td>
                <MDBBadge badge="success" pill class="d-inline">{{
                  person.successRate
                }}</MDBBadge>
              </td>
              <td>
                <div class="ms-3">
                  <p class="text-muted mb-0">{{ person.fee.fee }}</p>
                </div>
              </td>
            </tr>
          </tbody>
        </MDBTable>
      </MDBTabPane>
      <MDBTabPane tabId="ex1-2">
        <h1><b>Songbird</b></h1>
        <MDBTable class="align-middle mb-0 bg-white">
          <thead class="bg-light">
            <tr>
              <th>Name</th>
              <th>SuccessRate</th>
              <th>Avialability,Voting Power,Fee</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(person, index) in personsfl" :key="index">
              <td>
                <div class="d-flex align-items-center">
                  <img
                    :src="person.logoURI"
                    alt=""
                    style="width: 45px; height: 45px"
                    class="rounded-circle"
                  />
                  <div class="ms-3">
                    <p class="fw-bold mb-1">{{ person.name }}</p>
                    <p class="text-muted mb-0">{{ person.address }}</p>
                  </div>
                </div>
              </td>
              <td>
                                <MDBBadge badge="success" pill class="d-inline">{{
                  person.successRate
                }}</MDBBadge>
              </td>
              <td>
                <div class="ms-3">
                  <p class="text-muted mb-0">{{ person.fee.fee }}</p> 
                </div>
              </td>
            </tr>
          </tbody>
        </MDBTable></MDBTabPane
      >
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
       <th>Fee</th>
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
             <p class="text-muted mb-0">{{ person.fee.fee }}</p>
             </div>
       </td>

     </tr>

   </tbody>
 </MDBTable> -->
</template>
<script>
// import dp from '../dp.json'
//import axios from "axios";

import {
  MDBTabs,
  MDBTabNav,
  MDBTabContent,
  MDBTabItem,
  MDBTabPane,
  MDBTable,
  MDBBtn,
  MDBBadge,
} from "mdb-vue-ui-kit";
import { ref } from "vue";
import { defineComponent } from "vue";
const activeTabId1 = ref("ex1-1");

export default defineComponent({
  components: {
    MDBTabs,
    MDBTabNav,
    MDBTabContent,
    MDBTabItem,
    MDBTabPane,
    MDBTable,
    MDBBtn,
    MDBBadge,
  },
  setup() {
    const activeTabId1 = ref("ex1-1");

    return {
      activeTabId1,
    };
  },
  data() {
    return {
      //   // initial state
      //   //persons: dp ,
      personssb: [],
      personsfl: [],
    };
  },
  // created: function () {
  //   axios
  //   .get("http://flareportal.com/data/dp.json")
  //   .then((result) => {
  //    this.persons = result.data;
  //   });
  //   async created() {
  //      try{
  //       const response = await axios.get("http://flareportal.com/data/dp.json");

  //         //const response = await fetch("http://flareportal.com/data/dp.json");
  //          this.persons = await response.data;
  //  //   data.forEach(film => console.log(film.title));
  //   } catch(err) {console.error(err.message)}
  //       // this.persons =  res.data.map((post) => {
  //       //   return {id: post.logoURI };
  //       // })
  //   }
  mounted() {
    fetch("https://flareportal.com/data/dpsb.json",{ credentials: 'same-origin',})
      .then((res) => res.json())
      .then((data) => (this.personssb = data))
      .catch((err) => console.log(err.message));
      console.log(this.persons)

    fetch("https://flareportal.com/data/dpfl.json",{ credentials: 'same-origin',})
      .then((res) => res.json())
      .then((data) => (this.personsfl = data))
      .catch((err) => console.log(err.message));
      console.log(this.persons)
  },  
});
</script>



<style scoped>
#app {
  font-family: Roboto, Helvetica, Arial, sans-serif;
}
</style>



