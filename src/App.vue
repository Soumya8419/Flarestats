<template>
  <MDBTabs v-model="activeTabId1" >
    <!-- Tabs navs -->
    <MDBTabNav tabsClasses="mb-3">
      <MDBTabItem tabId="ex1-1" href="ex1-1">Songbird</MDBTabItem>
      <MDBTabItem tabId="ex1-2" href="ex1-2">Flare</MDBTabItem>
      <MDBTabItem tabId="ex1-3" href="ex1-2">About Us</MDBTabItem>
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
              <th>Fee(%)</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(person, index) in personssb" :key="index">
              
            <!-- <tr v-for="person in persons" :key="person.chainId"> -->
              <td>
                <MDBBadge badge="success" pill class="d-inline">{{
                  index + 1
                }}</MDBBadge>
              </td>
              <td>
                <div class="d-flex align-items-left">
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
                <MDBBadge badge="primary" pill class="d-inline">{{
                  person.rewardRate
                }}</MDBBadge>
              </td>
              <td>
                <div class="ms-3">
                  <p class="text-muted mb-0">{{ person.fee }}</p>
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
              <th>Fee(%)</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(person, index) in personsfl" :key="index">
                          <td>
                <MDBBadge badge="success" pill class="d-inline">{{
                  index + 1
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
                  person.rewardRate
                }}</MDBBadge>
              </td>
              <td>
                <div class="ms-3">
                  <p class="text-muted mb-0">{{ person.fee }}</p> 
                </div>
              </td>
            </tr>
          </tbody>
        </MDBTable>
        </MDBTabPane>
       <MDBTabPane tabId="ex1-3">
        <p> 

<p><span data-contrast="auto">INFO</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">This app provides FTSO's listings </span><strong><span data-contrast="auto">sorted per</span></strong> <strong><span data-contrast="auto">best &lsquo;Reward Rate&rsquo;</span></strong><span data-contrast="auto">.</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">SGB / FLR holders can delegate their tokens to their own choice of Data Providers (TSO&rsquo;s also named FTSO&rsquo;s). By delegating your vote, assets will stay in your </span><span data-contrast="auto"><span data-ccp-charstyle="hrcahc" data-ccp-charstyle-defn="{&quot;ObjectId&quot;:&quot;c68bee1c-d300-49ba-bd20-00e1ba2b6f0f|12&quot;,&quot;ClassId&quot;:1073872969,&quot;Properties&quot;:[469775450,&quot;hrcahc&quot;,201340122,&quot;1&quot;,134233614,&quot;true&quot;,469778129,&quot;hrcahc&quot;,335572020,&quot;1&quot;,469778324,&quot;Default Paragraph Font&quot;]}">possession</span></span><span data-contrast="auto">. The </span><a href="https://flareportal.com/"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Flare Portal</span></span></a><span data-contrast="auto"> xApp provides key information for your delegation process, the FTSO's listing is sorted </span><strong><span data-contrast="auto">per best &lsquo;Reward Rate&rsquo;</span></strong><span data-contrast="auto"> for Songbird and Flare Network as most used indicator. Data is updated as per (in the xApp) indicated interval / last updated information.</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">Reward Rate</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">Ratio used to calculate how many tokens you will receive per 100 delegated </span><span data-contrast="auto"><span data-ccp-charstyle="hgkelc" data-ccp-charstyle-defn="{&quot;ObjectId&quot;:&quot;c68bee1c-d300-49ba-bd20-00e1ba2b6f0f|9&quot;,&quot;ClassId&quot;:1073872969,&quot;Properties&quot;:[469775450,&quot;hgkelc&quot;,201340122,&quot;1&quot;,134233614,&quot;true&quot;,469778129,&quot;hgkelc&quot;,335572020,&quot;1&quot;,469778324,&quot;Default Paragraph Font&quot;]}">$WSGB / $WFLR</span></span><span data-contrast="auto">.</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">When do I start earning rewards?</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">A vote power block (snapshot) is created each week (automatically and random time/date - around the beginning of the new epoch). Your vote power should be delegated to a FTSO for the upcoming epoch before the above-mentioned snapshot and accruing rewards starts after 08:41 UTC on Saturday.</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">Support us</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">Support us by Delegating your wrapped (WSGB / WFLR) to </span><a href="https://flareportal.com/"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Flare Portal</span></span></a><span data-contrast="auto"> via e.g., </span><a href="https://bifrostwallet.com/"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Bif</span><span data-ccp-charstyle="Hyperlink">ros</span><span data-ccp-charstyle="Hyperlink">t Wallet</span></span></a><span data-contrast="auto">&nbsp;</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">on your phone (</span><a href="https://apps.apple.com/us/app/bifrost-wallet/id1577198351AOvVaw0vFVmXT5NE1txYW9tooYL0"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Apple</span></span></a><span data-contrast="auto"> / </span><a href="https://play.google.com/store/apps/details?id=com.bifrostwallet.app"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Google</span></span></a><span data-contrast="auto">), in Bifrost Wallet: </span><span data-contrast="auto"><span data-ccp-charstyle="hgkelc">Click the Add Provider tab toward the bottom of the screen. Select which provider you want to delegate to (you can select up to 2 providers). Choose the percentage of your $WSGB </span><span data-ccp-charstyle="hgkelc">/ </span><span data-ccp-charstyle="hgkelc">$W</span><span data-ccp-charstyle="hgkelc">FLR</span><span data-ccp-charstyle="hgkelc"> you wish to delegate to that specific provider. Click Continue then click Confirm and finally click Close</span><span data-ccp-charstyle="hgkelc">. You are only delegating your Vote; the assets stay in your </span><span data-ccp-charstyle="hrcahc">possession</span><span data-ccp-charstyle="hgkelc"> / wallet.</span></span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><strong><span data-contrast="auto">Support us via delegating to </span></strong><a href="https://flareportal.com/"><strong><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Flare Portal</span></span></strong></a>&nbsp;<br /><span data-contrast="auto">You can copy the below Flare Portal </span><a href="http://0x9225db8b30a59d8dd15448e2e5918bd160262b5d/"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">SGB </span><span data-ccp-charstyle="Hyperlink">/ FLR </span><span data-ccp-charstyle="Hyperlink">address</span></span></a><span data-contrast="auto"> or search for &lsquo;Flare Portal&rsquo; in e.g. </span><a href="https://bifrostwallet.com/"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Bif</span><span data-ccp-charstyle="Hyperlink">ros</span><span data-ccp-charstyle="Hyperlink">t Wallet</span></span></a><span data-contrast="auto">.</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">Flare Portal SGB / FLR address:</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">0x9225db8B30A59D8Dd15448E2E5918BD160262b5D</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">Additional information &ndash; Flare Portal</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><a href="https://flareportal.com/community/"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Forum</span></span></a><span data-ccp-props="{}">&nbsp;</span></p>
<p><a href="https://flareportal.com/flarechat/"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">FlareChat</span></span></a><span data-ccp-props="{}">&nbsp;</span></p>
<p><a href="http://app.flareportal.com/"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">xApp</span><span data-ccp-charstyle="Hyperlink"> webpage</span></span></a><span data-ccp-props="{}">&nbsp;</span></p>
<p><a href="https://songbird-explorer.flare.network/address/0x9225db8B30A59D8Dd15448E2E5918BD160262b5D"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Songbird network Explorer</span></span></a><span data-ccp-props="{}">&nbsp;</span></p>
<p><a href="https://flare-explorer.flare.network/address/0x9225db8B30A59D8Dd15448E2E5918BD160262b5D"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Flare network Explorer</span></span></a><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">For support questions, improvements or feature request</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><a href="https://twitter.com/flareportal"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">Twitter</span></span></a><span data-ccp-props="{}">&nbsp;</span></p>
<p><a href="https://flareportal.com/"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">https://flareportal.com</span></span></a><span data-ccp-props="{}">&nbsp;</span></p>
<p><a href="mailto:info@flareportal.com"><span data-contrast="none"><span data-ccp-charstyle="Hyperlink">info@flareportal.com</span></span></a><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">DISCLAIMER</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">Last updated December 29, 2022</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">xAPP and WEBSITE DISCLAIMER</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">The information provided by Flare Portal (FTSO) based in The Netherlands (&ldquo;we,&rdquo; &ldquo;us&rdquo;, or &ldquo;our&rdquo;) on https://flareporal.com (the &ldquo;Site&rdquo;) is for general informational purposes only. Use of the information is at your own risk as our technical process could fail updating the information. All information on the Site is provided in good faith, however we make no representation or warranty of any kind, express or implied, regarding the accuracy, adequacy, validity, reliability, availability or completeness of any information on the Site. UNDER NO CIRCUMSTANCE SHALL WE HAVE ANY LIABILITY TO YOU FOR ANY LOSS OR DAMAGE OF ANY KIND INCURRED AS A RESULT OF THE USE OF THE SITE OR RELIANCE ON ANY INFORMATION PROVIDED ON THE SITE. YOUR USE OF THE SITE AND YOUR RELIANCE ON ANY INFORMATION ON THE SITE IS SOLELY AT YOUR OWN RISK.</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">EXTERNAL LINKS DISCLAIMER</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-contrast="auto">The xApp or Site may contain (or you may be sent through the Site) links to other websites or content belonging to or originating from third parties or links to websites and features in banners or other advertising. Such external links are not investigated, monitored, or checked for accuracy, adequacy, validity, reliability, availability or completeness by us. WE DO NOT WARRANT, ENDORSE, GUARANTEE, OR ASSUME RESPONSIBILITY FOR THE ACCURACY OR RELIABILITY OF ANY INFORMATION OFFERED BY THIRD-PARTY WEBSITES LINKED THROUGH THE SITE OR ANY WEBSITE OR FEATURE LINKED IN ANY BANNER OR OTHER ADVERTISING. WE WILL NOT BE A PARTY TO OR IN ANY WAY BE RESPONSIBLE FOR MONITORING ANY TRANSACTION BETWEEN YOU AND THIRD-PARTY PROVIDERS OF PRODUCTS OR SERVICES.</span><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
<p><span data-ccp-props="{}">&nbsp;</span></p>
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
                  index + 1
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
           <MDBBadge badge="primary" pill class="d-inline">{{ person.successRate}}</MDBBadge>
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

