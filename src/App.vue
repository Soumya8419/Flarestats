<template>
  <MDBTabs v-model="activeTabId1">
    <!-- Tabs navs -->
    <MDBTabNav tabsClasses="mb-3">
      <MDBTabItem tabId="ex1-1" href="ex1-1"><h4>Songbird</h4></MDBTabItem>
      <MDBTabItem tabId="ex1-2" href="ex1-2"><h4>Flare</h4></MDBTabItem>
      <MDBTabItem tabId="ex1-3" href="ex1-2"><h4>About Us</h4></MDBTabItem>
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
              <th>Rank</th>
             <th>Name</th>
              <th>SuccessRate</th>
              <th>Fee</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(person, index) in personsfl" :key="index">
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
                    <p class="text-muted mb-0">{{ person.address }}</p>
                  </div>
                </div>
              </td>
              <td>
                                <MDBBadge badge="success" pill class="d-inline">{{
                  person.sucessRate
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
       <MDBTabPane tabId="ex1-3">
        <p> 

 

This app provides FTSO's listings sorted per best ‘Reward Rate’. 

 

SGB / FLR holders can delegate their tokens to their own choice of Data Providers (TSO’s also named FTSO’s). By delegating your vote, assets will stay in your possession. The Flare Portal xApp provides key information for your delegation process, the FTSO's listing is sorted per best ‘Reward Rate’ for Songbird and Flare Network as most used indicator. Data is updated as per (in the xApp) indicated interval / last updated information. 

 

Reward Rate 

Ratio used to calculate how many tokens you will receive per 100 delegated $WSGB / $WFLR. 

 

When do I start earning rewards? 

A vote power block (snapshot) is created each week (automatically and random time/date - around the beginning of the new epoch). Your vote power should be delegated to a FTSO for the upcoming epoch before the above-mentioned snapshot and accruing rewards starts after 08:41 UTC on Saturday. 

 

Support us 

Support us by Delegating your wrapped (WSGB / WFLR) to Flare Portal via e.g., Bifrost Wallet  

on your phone (Apple / Google), in Bifrost Wallet: Click the Add Provider tab toward the bottom of the screen. Select which provider you want to delegate to (you can select up to 2 providers). Choose the percentage of your $WSGB / $WFLR you wish to delegate to that specific provider. Click Continue then click Confirm and finally click Close. You are only delegating your Vote; the assets stay in your possession / wallet. 

 

Support us via delegating to Flare Portal 
You can copy the below Flare Portal SGB / FLR address or search for ‘Flare Portal’ in e.g. Bifrost Wallet. 

Afbeelding met tekst

Automatisch gegenereerde beschrijving 

Flare Portal SGB / FLR address: 

0x9225db8B30A59D8Dd15448E2E5918BD160262b5D 

 

Additional information – Flare Portal 

Forum 

FlareChat 

xApp webpage 

Songbird network Explorer 

Flare network Explorer 

 

For support questions, improvements or feature request 

Twitter 

https://flareportal.com 

info@flareportal.com 

 

DISCLAIMER 

 

Last updated December 29, 2022 

 

xAPP and WEBSITE DISCLAIMER 

 

The information provided by Flare Portal (FTSO) based in The Netherlands (“we,” “us”, or “our”) on https://flareporal.com (the “Site”) is for general informational purposes only. Use of the information is at your own risk as our technical process could fail updating the information. All information on the Site is provided in good faith, however we make no representation or warranty of any kind, express or implied, regarding the accuracy, adequacy, validity, reliability, availability or completeness of any information on the Site. UNDER NO CIRCUMSTANCE SHALL WE HAVE ANY LIABILITY TO YOU FOR ANY LOSS OR DAMAGE OF ANY KIND INCURRED AS A RESULT OF THE USE OF THE SITE OR RELIANCE ON ANY INFORMATION PROVIDED ON THE SITE. YOUR USE OF THE SITE AND YOUR RELIANCE ON ANY INFORMATION ON THE SITE IS SOLELY AT YOUR OWN RISK. 

 

EXTERNAL LINKS DISCLAIMER 

 

The xApp or Site may contain (or you may be sent through the Site) links to other websites or content belonging to or originating from third parties or links to websites and features in banners or other advertising. Such external links are not investigated, monitored, or checked for accuracy, adequacy, validity, reliability, availability or completeness by us. WE DO NOT WARRANT, ENDORSE, GUARANTEE, OR ASSUME RESPONSIBILITY FOR THE ACCURACY OR RELIABILITY OF ANY INFORMATION OFFERED BY THIRD-PARTY WEBSITES LINKED THROUGH THE SITE OR ANY WEBSITE OR FEATURE LINKED IN ANY BANNER OR OTHER ADVERTISING. WE WILL NOT BE A PARTY TO OR IN ANY WAY BE RESPONSIBLE FOR MONITORING ANY TRANSACTION BETWEEN YOU AND THIRD-PARTY PROVIDERS OF PRODUCTS OR SERVICES. 

        </p>
         </MDBTabPane>
    </MDBTabContent>
    <!-- Tabs content -->
  </MDBTabs>
  <!--  
 
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
                <MDBBadge badge="success" pill class="d-inline">{{
                  index
                }}</MDBBadge>
              </td>
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

