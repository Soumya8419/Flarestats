<template>
  <meta
    name="viewport"
    content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0"
  />

  <div>
    <MDBTabs v-model="activeTabId1">
      <!-- Tabs navs -->
      <MDBTabNav pills   tabsClasses=" nav justify-content-center nav-fill ms-2 me-1">
        <MDBTabItem tabId="ex1-1" class="bg-primary text-white align-items-stretch" href="ex1-1">
          <img
            src="https://app.flareportal.com/wp-includes/images/media/songbird.svg"
            class="img-fluid rounded"
            style="width: 20px; height: 20px"
            alt="Songbird"
          />
          Songbird</MDBTabItem
        >
        <MDBTabItem tabId="ex1-2" class="bg-warning text-white align-items-stretch" href="ex1-2">
          <img
            src="https://app.flareportal.com/wp-includes/images/media/1flare.svg"
            class="img-fluid rounded"
            style="width: 20px; height: 20px"
            alt="Flare"
          />
          Flare</MDBTabItem
        >
        <MDBTabItem tabId="ex1-3" class="bg-success text-white align-items-stretch" href="ex1-3">
          <img
            src="https://flareportal.com/wp-content/uploads/2022/01/FlarePortal_PNG_300DPI_150px_150px.png.webp"
            class="img-fluid rounded"
            style="width: 20px; height: 20px"
            alt="Flareportal"
          />
          About</MDBTabItem
        >
      </MDBTabNav>
      <!-- Tabs navs -->
      <!-- Tabs content -->
      <MDBTabContent>
        <MDBTabPane tabId="ex1-1"  >

            <div class="d-flex justify-content-center">
              <span v-for="(item, index) in details" :key="index">
                <MDBBadge badge="dark" pill
                  >Reward Epoch: {{ item.sgbepoch }}</MDBBadge
                >
                <MDBBadge badge="info" pill>
                  Last Refresh: {{ timeSince(item.time) }} </MDBBadge
                ><MDBBadge></MDBBadge>
              </span>
            </div>

            <!-- <div class="items-container"> -->
            <MDBTable class="justify-content-center ms-2 me-3">
              <thead class="bg-primary text-white ms-2 me-3">
                <tr>
                  <th>Ranking</th>
                    <th>Name</th>
                    <th>Reward@</th>
                    <th>Fee(%)</th>
                </tr>
              </thead>
              <tbody>
                <tr  v-for="(person, index) in personssb" :key="index">
                  <!-- <tr v-for="person in persons" :key="person.chainId"> -->
                  <td>
                    <MDBBadge badge="success" pill class="d-inline">{{
                      index + 1
                    }}</MDBBadge>
                  </td>
                  <td>
                    <div class="align-items-left">
                      <img
                        :src="person.logoURI"
                        alt=""
                        style="width: 20px; height: 20px"
                        class="rounded-circle"
                      />

                      <p class="fw-bold mb-3">{{ person.name }}</p>
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
            <!-- </div> -->

        </MDBTabPane>
        <MDBTabPane tabId="ex1-2" >
          <div class="container">
            <div class="d-flex justify-content-center">
              <span v-for="(item, index) in details" :key="index">
                <MDBBadge badge="dark" pill
                  >Reward Epoch: {{ item.flrepoch }}</MDBBadge
                >
                <MDBBadge badge="info" pill>
                  Last Refresh: {{ timeSince(item.time) }} </MDBBadge
                ><MDBBadge></MDBBadge>
              </span>
            </div>
            <div class="items-container">
              <MDBTable class="align-left  mb-5 bg-white ms-2 me-1">
                <thead class="bg-warning text-white">
                  <tr>
                    <th>Rank</th>
                    <th>Name</th>
                    <th>Reward@</th>
                    <th>Fee(%)</th>
                  </tr>
                </thead>
                <tbody>
                  <tr  v-for="(person, index) in personsfl" :key="index">
                    <td>
                      <MDBBadge badge="success" pill class="d-inline">{{
                        index + 1
                      }}</MDBBadge>
                    </td>
                    <td>
                      <div class="align-items-left">
                        <img
                          :src="person.logoURI"
                          alt=""
                          style="width: 20px; height: 20px"
                          class="rounded-circle"
                        />
                        <p class="fw-bold mb-0">{{ person.name }}</p>
                      </div>
                    </td>
                    <td>
                      <MDBBadge badge="primary" pill class="d-inline">{{
                        person.rewardRate
                      }}</MDBBadge>
                    </td>
                    <td>
                      <div class="ms-0">
                        <p class="text-muted mb-0">{{ person.fee }}</p>
                      </div>
                    </td>
                  </tr>
                </tbody>
              </MDBTable>
            </div>
          </div>
        </MDBTabPane>
        <MDBTabPane tabId="ex1-3">
          <div class="container align-left  mb-5 bg-white  fs-6" >
            <p class="text-sm-start">
            </p>
              <span data-contrast="auto"><b>Flareportal</b></span
              ><span data-ccp-props="{}">&nbsp;</span>
              <div class="note note-success mb-3">
                <p> A lot of love and effort has gone in building this app.</p>
                <p> As we strive to better at scoring to be Top-20 FTSO, we will continue building more apps  
                    to bring our FTSO community together.</p> 
                    <p>  You can reach us on Twitter @ Flareportal </p> 
                      <p> We also have a Forum on our website at Flareportal where our community can post questions and answers.</p> 
                        <p> Reach out to the community at https://flareportal.com/forum/</p> 
              </div>
            <p><span data-ccp-props="{}">&nbsp;</span></p>
            <p>
              <span data-contrast="auto"><b>Flare Portal xApp</b></span
              ><span data-ccp-props="{}">&nbsp;</span>
                                   </p>
            <p>
              <span data-contrast="auto"
                >
                <div class="note note-success mb-3">
                This app provides <b>FTSO'</b>s listed and sorted decending on their <b>‘Reward Rate’</b>.
                <p></p>
                SGB / FLR holders can delegate their tokens to their own choice
                of Data Providers (TSO&rsquo;s also named FTSO&rsquo;s). By
                delegating your vote, your assets will stay in your
                possession.
                <p></p>
                The Flare Portal xApp provides key information to select on
                this delegation process. Data is updated as per (in the xApp) indicated interval / last
                updated information.</div></span>
            </p>
            <p>
              <span data-contrast="auto"><b>Reward Rate</b></span
              ><span data-ccp-props="{}">&nbsp;</span>
            </p>
            <p class="fs-6">
              <span data-contrast="auto"
                >
                <div class="note note-success mb-3">
                Ratio used to calculate how many tokens you will receive per
                100 delegated $WSGB / $WFLR. 
                <p></p>
                The Vote Power of a FTSO / Data Provider is the sum of its balance 
                Vote Power and all balance vote powers delegated to it by other accounts. 
                The calculation is based on the Current Vote Power of the 
                Data Provider (not the Active Vote Power).
                <p></p>
                The Active Vote Power of an account is its Vote Power at a specific block, 
                called the Vote Power Block, whereas the Current Vote Power is the Vote Power 
                is the sum of its balance Vote Power and all balance Vote Powers delegated to 
                it by other accounts prior to the Vote Power Block. The Current Vote Power is 
                therefore a more usefull indicator for the upcoming Reward Epoch, as if the Data
                Provider exceeds the Vote Power Cap it impacts the reward ratio. The Vote
                Power Cap lowers the maximum power a data provider can have in deciding 
                the median price of a signal.
                </div> </span
              >
            </p>
  
            <p>
              <span data-contrast="auto"><b>When do I start earning rewards?</b></span
              ><span data-ccp-props="{}">&nbsp;</span>
            </p>
            <p>
              <span data-contrast="auto"
                ><div class="note note-warning mb-3">A vote power block (snapshot) 
                is created (automatically and random time/date - around the beginning of
                the new epoch). Example for Songbird: Your vote power should be delegated to 
                a FTSO for the upcoming epoch before the above-mentioned snapshot and
                accruing rewards starts in regrards to Songbird Network after 08:41 UTC 
                on Saturday in regards to Songbird. The Reward Epoch cycle for Flare network
                is 3.5 days (twice a week).
                .</div></span
              >
            </p>
            <p>
              <span data-contrast="auto"><b>Support us</b></span
              ><span data-ccp-props="{}">&nbsp;</span>
            </p>
            <p class="fs-6">
              <span data-contrast="auto"
                >
                <div class="note note-primary mb-3">
                Support us by delegating your wrapped SGB / FLR to Flare Portal.
                <p></p>
                Delegation can be done via e.g. Bifrost Wallet.
                <p></p>
                In Bifrost Wallet you can wrap your SGB / FLR and delegate to a 
                Data Provider. You can search for Flare Portal.
                <p></p>
                Flare Portal SGB & FLR address:
                <p class="fs-6">0x9225db8B30A59D8Dd15448E2E5918BD160262b5D</p>
                <p></p>
                </div> </span
              >
          
              <span data-contrast="auto"><b>DISCLAIMER</b></span
              > 
            </p>
            <p>
              <span data-contrast="auto">Last updated February 2, 2023</span
              >
            </p>
            <p>
              <span data-contrast="auto"><b>xAPP and WEBSITE DISCLAIMER</b></span
              > 
            </p>
            <p>
              <span data-contrast="auto"
                ><div class="note note-warning mb-3">
                >The information provided by Flare Portal (FTSO) based in The
                Netherlands (&ldquo;we,&rdquo; &ldquo;us&rdquo;, or
                &ldquo;our&rdquo;) on https://flareporal.com (the
                &ldquo;Site&rdquo;) is for general informational purposes only.
                Use of the information is at your own risk as our technical
                process could fail updating the information. The information
                provided does not contain financial advice. Don't rely on the 
                information to make financial decisions. All information on
                the Site is provided in good faith, however we make no
                representation or warranty of any kind, express or implied,
                regarding the accuracy, adequacy, validity, reliability,
                availability or completeness of any information on the Site.
                UNDER NO CIRCUMSTANCE SHALL WE HAVE ANY LIABILITY TO YOU FOR ANY
                LOSS OR DAMAGE OF ANY KIND INCURRED AS A RESULT OF THE USE OF
                THE SITE OR RELIANCE ON ANY INFORMATION PROVIDED ON THE SITE.
                YOUR USE OF THE SITE AND YOUR RELIANCE ON ANY INFORMATION ON THE
                SITE IS SOLELY AT YOUR OWN RISK.
              </div></span>
            </p>
            <p>
              <span data-contrast="auto"><b>EXTERNAL LINKS DISCLAIMER</b></span
              >
            </p>
            <p>
              <span data-contrast="auto"
                ><div class="note note-warning mb-3">
                The xApp or Site may contain (or you may be sent through the
                Site) links to other websites or content belonging to or
                originating from third parties or links to websites and features
                in banners or other advertising. Such external links are not
                investigated, monitored, or checked for accuracy, adequacy,
                validity, reliability, availability or completeness by us. WE DO
                NOT WARRANT, ENDORSE, GUARANTEE, OR ASSUME RESPONSIBILITY FOR
                THE ACCURACY OR RELIABILITY OF ANY INFORMATION OFFERED BY
                THIRD-PARTY WEBSITES LINKED THROUGH THE SITE OR ANY WEBSITE OR
                FEATURE LINKED IN ANY BANNER OR OTHER ADVERTISING. WE WILL NOT
                BE A PARTY TO OR IN ANY WAY BE RESPONSIBLE FOR MONITORING ANY
                TRANSACTION BETWEEN YOU AND THIRD-PARTY PROVIDERS OF PRODUCTS OR
                SERVICES.
              </div></span>
            </p>
          </div>
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
              <p class="  mb-1">{{ person.name }}</p>
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
  </div>
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
      details: []
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
    fetch("https://flareportal.com/data/dpsb.json", {
      credentials: "same-origin",
    })
      .then((res) => res.json())
      .then((data) => (this.personssb = data))
      .catch((err) => console.log(err.message));
    console.log(this.persons);
    fetch("https://flareportal.com/data/dpfl.json", {
      credentials: "same-origin",
    })
      .then((res) => res.json())
      .then((data) => (this.personsfl = data))
      .catch((err) => console.log(err.message));
    console.log(this.persons);
    fetch(
      "https://flareportal.com/data/details.json",
      { cache: "no-store" },
      { credentials: "same-origin" }
    )
      .then((res) => res.json())
      .then((data) => (this.details = data))
      .catch((err) => console.log(err.message));
    console.log(this.persons);
  },
  methods: {
    timeSince(timestamp) {
      let current_time = new Date().getTime();
      let timestamp_time = new Date(timestamp).getTime();
      let diff = current_time - timestamp_time;
      let seconds = Math.floor(diff / 1000);
      let minutes = Math.floor(seconds / 60);
      let hours = Math.floor(minutes / 60);
      let days = Math.floor(hours / 24);

      return (
        days +
        "D " +
        (hours % 24) +
        "H " +
        (minutes % 60) +
        "M " +
        (seconds % 60) +
        "S ago"
      );
    },
  },
});
</script>
 
 
 <style>
@import url("https://use.typekit.net/iqo4nny.css");
/* @import url('https://fonts.googleapis.com/css?family=Ubuntu+Mono'); */
@import url("https://fonts.googleapis.com/css2?family=Ubuntu+Mono:wght@400;700&display=swap");
/* GLOBAL STYLES */
.failed-start {
  align-items: center;
}
.btn {
  font-size: 0.8rem;
  padding: 0.5rem 1rem;
  font-family: proxima-nova, sans-serif;
  font-weight: 800;
  border-radius: 5rem;
}
.btn svg {
  margin-right: 0.2rem;
}
.btn.btn-primary {
  background: var(--var-blue);
  border-color: var(--var-blue);
  color: var(--var-white);
}
.btn.btn-secondary {
  background: var(--var-grey);
  border-color: var(--var-grey);
  color: var(--var-white);
}
.btn.btn-light {
  background: var(--var-light);
  border-color: var(--var-light);
  color: var(--var-black);
}
.mono {
  font-family: "Ubuntu Mono" !important;
}
.push {
  margin-left: auto !important;
}
.h-100 {
  height: 100%;
}
.margin-0 {
  margin: 0 !important;
}
#app {
  font-family: proxima-nova, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100vh;
  overflow-y: auto;
  overflow-x: hidden;
}
html,
body {
  height: 100%;
  width: 100%;
  margin: 0;
}
#view {
  height: 100vh;
  padding: 0 1rem;
  overflow-y: hidden;
  overflow-x: hidden;
  display: flex;
  flex-direction: column;
  touch-action: none;
  /* border: 1px solid blue; */
}
.swal2-container.swal2-backdrop-show,
.swal2-container.swal2-noanimation {
  background: rgba(255, 255, 255, 0.4) !important;
}
.swal2-popup {
  box-shadow: 2px 2px 11px rgba(0, 0, 0, 0.3) !important;
  border-radius: 10px !important;
}
.row {
  display: flex;
  flex-direction: row;
  width: 100%;
  margin: 5px 0;
  align-items: center;
}
.column {
  display: flex;
  flex-direction: column;
  width: 100%;
}
fieldset {
  display: flex;
  align-items: center;
  margin-inline-start: 0;
  margin-inline-end: 0;
  padding-block-start: 0;
  padding-inline-start: 0;
  padding-inline-end: 0;
  padding-block-end: 0;
  min-inline-size: min-content;
  border-width: 0;
  border-style: none;
  border-color: rgba(255, 255, 255, 0);
  border-image: none;
}
</style>

