<template>
  <div class="root">
    <div class="intro" v-if="inIntroAnimation">
      <h1 class="display-3">
        <span class="intro-fade-1">Welcome to{{ ' ' }}</span>
        <span class="intro-fade-2">Façade</span>
        <span class="intro-fade-1">.com</span>
      </h1>
    </div>
    <b-container class="content" v-else>
      <div class="header">
        <h1 class="display-4 logo">Façade</h1>
        <h4 class="lead">
          We make sure you
          <i>always</i> like what you see.
        </h4>
      </div>

      <b-row class="cards">
        <b-col>
          <Card
            v-b-modal.modal-1
            title="Pupper"
            price="$6.99"
            img="https://cdn.notonthehighstreet.com/system/product_images/images/002/369/953/original_cockapoo-dog-on-phone-case.jpg"
          />
        </b-col>
        <b-col>
          <Card
            v-b-modal.modal-1
            title="Cat"
            price="$6.99"
            img="https://cdn.shopify.com/s/files/1/0394/6125/products/CCS-PA-0380_600x.jpg?v=1502099808"
            text="test info about item"
          />
        </b-col>
        <b-col>
          <Card
            v-b-modal.modal-1
            title="Javascript"
            price="$6.99"
            img="https://res.cloudinary.com/teepublic/image/private/s--rKABDHIx--/c_crop,x_10,y_10/c_fit,w_416/c_crop,g_north_west,h_1100,w_554,x_-69,y_-318/l_upload:v1452885561:production:blanks:gawvl5gka1pqwssxidw5/fl_layer_apply,g_north_west,x_-430,y_-395/b_rgb:000000/c_limit,f_jpg,h_630,q_90,w_630/v1548577527/production/designs/4089096_0.jpg"
            text="test info about item"
          />
        </b-col>
        <b-col @click="ageToast">
          <Card
            v-b-modal.modal-1
            title="Minecraft"
            price="$6.99"
            img="https://www.geekalerts.com/u/Minecraft-iPhone-Case.jpg"
          />
        </b-col>

        <b-col @click="genderToast">
          <Card
            v-b-modal.modal-1
            title="Basketball"
            price="$6.99"
            img="https://rlv.zcache.com/mens_basketball_iphone_x_case_w_custom_monogram-radd2cb0db15b4eb792767b1f876557d6_exgw3_540.jpg?rlvnet=1"
          />
        </b-col>

        <b-col @click="raceToast">
          <Card
            v-b-modal.modal-1
            title="Country Roads"
            price="$6.99"
            img="https://images.lookhuman.com/render/standard/0880459023820208/iphonexssn-whi-z1-t-country-roads.jpg"
          />
        </b-col>

        <b-col @click="raceToast">
          <Card
            v-b-modal.modal-1
            title="Tupac"
            price="$8.99"
            img="https://i.pinimg.com/originals/3c/15/02/3c1502394ede6c6aae5c924d13fecf41.jpg"
          />
        </b-col>

        <b-col @click="ageToast">
          <Card
            v-b-modal.modal-1
            title="Fortnite"
            price="$11.99"
            img="https://res.cloudinary.com/teepublic/image/private/s--yhpW2bdp--/c_crop,x_10,y_10/c_fit,w_504/c_crop,g_north_west,h_1100,w_554,x_-27,y_-248/l_upload:v1452885561:production:blanks:gawvl5gka1pqwssxidw5/fl_layer_apply,g_north_west,x_-388,y_-325/b_rgb:000000/c_limit,f_jpg,h_630,q_90,w_630/v1523875183/production/designs/2595294_0.jpg"
          />
        </b-col>

        <b-col @click="genderToast">
          <Card
            v-b-modal.modal-1
            title="Kawaii"
            price="$11.99"
            img="http://demandware.edgesuite.net/sits_pod37/dw/image/v2/BBTK_PRD/on/demandware.static/-/Sites-master-catalog/default/dwb4dd77a2/images/hi-res/25808_1.jpg?sw=2000&sh=2000&sm=fit"
          />
        </b-col>

        <b-col @click="genderToast">
          <Card
            v-b-modal.modal-1
            title="Dodgers"
            price="$11.99"
            img="http://ebayus.channeleffect.com/ImageHosting/viewImage?CompanyId=24583&FilePath=Images/1721"
          />
        </b-col>
        <b-col @click="genderToast">
          <Card
            v-b-modal.modal-1
            title="Heart"
            price="$11.99"
            img="https://res.cloudinary.com/teepublic/image/private/s--sDYpjjg3--/c_crop,x_10,y_10/c_fit,w_377/c_crop,g_north_west,h_1100,w_554,x_-80,y_-248/l_upload:v1452885561:production:blanks:gawvl5gka1pqwssxidw5/fl_layer_apply,g_north_west,x_-441,y_-325/b_rgb:eae0c7/c_limit,f_jpg,h_630,q_90,w_630/v1515059890/production/designs/2253166_1.jpg"
          />
        </b-col>

        <b-col @click="raceToast">
          <Card
            v-b-modal.modal-1
            title="Wolf"
            price="$11.99"
            img="https://res.cloudinary.com/dcwbn0hrw/image/upload/v1476457329/er3mz0hne9wtwxwfqtjh.jpg"
          />
        </b-col>
      </b-row>
      <div class="footer">
        <b-button size="md" squared variant="outline-dark">
          <p class="lead m-0" @click="() => {this.$emit('continue')}">Ok, I'm done exploring.</p>
        </b-button>
      </div>
      <div
        class="alert alert-secondary alert-dismissible fade show fixed-bottom m-0 cookies"
        v-show="showCookieAlert"
      >
        <b-row>
          <b-col sm="8">
            <small>
              We use cookies and other technologies to collect data about your
              browser, device and location. We share this data with advertising,
              social media and analytics partners to help us understand how the site
              is used and to
              <strike>
                personalize our content and the advertising you see on this and other
                sites
              </strike>make more money.
            </small>
          </b-col>
          <b-col class="d-flex justify-content-end pt-3">
            <b-button variant="light" squared @click="closeCookieAlert">
              <span aria-hidden="false">Do not sell my personal information</span>
            </b-button>

            <b-button variant="success" squared @click="closeCookieAlert">
              <span aria-hidden="false">Accept cookies</span>
            </b-button>
          </b-col>
        </b-row>
      </div>
      <b-modal id="modal-1" title="Info Pane" hide-footer>
        <p class="modal-text">
          This is a popup window to show you more information on what you just clicked.
          <br />
          <small
            class="aside"
          >But while you're getting more information about the product, websites are collecting more data on you.</small>
        </p>

        <p class="modal-text">
          Using simple statistical heuristics, we reccomend products you might enjoy!
          <br />
          <small class="aside">
            This is fine, until you add
            <b>P</b>ersonally
            <b>I</b>dentifiable
            <b>I</b>nformation into the mix. PII includes things like your name, email, address, phone number, etc. Organizations called
            <b>Data Brokers</b> buy and sell PII to individuals and corporations around the world.
          </small>
        </p>

        <b-form>
          <b-form-group
            id="input-group-1"
            label="Email address:"
            label-for="input-1"
            description="Using your email as a unique identifier, we can simply look you up and buy your information!"
          >
            <b-form-input id="input-1" type="email" required placeholder="Enter email"></b-form-input>
          </b-form-group>

          <b-form-group
            id="input-group-2"
            label="Your Name:"
            label-for="input-2"
            description="Your name isn't as important to us as other information, but we can still use it to find and buy your information!"
          >
            <b-form-input id="input-2" required placeholder="Enter name"></b-form-input>
          </b-form-group>

          <b-form-group
            id="input-group-3"
            label="Phone No."
            label-for="input-3"
            description="Phone numbers are extremely lucrative, from robocalls to scams to ordinary advertisement, plus we can use it to identify and buy even more information about you! We even sell the phone number you use for Two Factor Authentication."
          >
            <b-form-input id="input-2" required placeholder="Enter Phone No."></b-form-input>
          </b-form-group>
        </b-form>

        <b>Get a 5% discount, share with your friends!</b>
        <br />

        <b-button squared size="sm" variant="outline-dark" @click="contactsToast" class="mt-3">
          <p class="m-0">Scan Contacts</p>
        </b-button>
      </b-modal>
    </b-container>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "SiteHome",
  components: {
    Card
  },
  data() {
    return {
      inIntroAnimation: true,
      showCookieAlert: true
    };
  },
  methods: {
    ageToast() {
      this.makeToast(
        "Guessing your age",
        `There are strong incentives to group users by age, and reccomendation systems are already very good at guessing your age. Although there are protections for minors from data collection, enforcement is not widespread. `
      );
    },
    genderToast() {
      this.makeToast(
        "Guessing your gender",
        `Reccomendation software is already very adept at "gendering" the content you consume, and subsequently labelling you with "male" or "female"`
      );
    },
    raceToast() {
      this.makeToast(
        "Guessing your race/ethnicity",
        `The racial bias of the content you select is almost definitely tracked as you browse advertisements. Reccomendation systems make very strong assumptions about your race and ethnicity.`
      );
    },
    contactsToast() {
      this.makeToast(
        "Scanning and selling your connections pt.2",
        `Big Data makes
the argument that because these contacts are "owned" by you, companies are
allowed to collect the data that you provide on your friends - even if your
friends never consented. `
      );

      this.makeToast(
        "Scanning and selling your connections pt.1",
        `Frighteningly, web and mobile apps are beginning to use connections on your
device (through your phone contacts, Facebook friends, etc.) to gather critical
information about your connections - linking names with phone numbers and
addresses.


        In other words, your discount comes from selling the personal information of
your friends and family.

        `
      );
    },
    closeCookieAlert() {
      this.showCookieAlert = false;
      this.makeToast(
        "A few bad Cookies spoil the bunch",
        `Cookies are the main tool used to track you on the web. Not all cookies are bad! But on most major shopping/news websites, the purpose of cookies is to tag you with information that can be sold to and used by advertisers.
        This kind of cookie based tracking isn't usually *malicious*, however.
        `
      );
    },
    makeToast(title, message) {
      this.$bvToast.toast(message, {
        title: title,
        noAutoHide: true
      });
    },
    loadContent() {
      this.inIntroAnimation = false;
      setTimeout(() => {
        this.makeToast(
          "Tutorial",
          `Look out for messages up here, this is where you can learn more about how your data is being collected.`
        );
      }, 3000);
    }
  },
  mounted() {
    // this.makeToast(
    //   `Look out for messages up here, this is where you can learn more about how your data is being collected.`
    // );
    clearTimeout();
    setTimeout(this.loadContent, 9000);
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.root {
  width: 100%;
  height: 100%;
  min-height: 100vh;
}

.modal-text {
}
.aside {
  color: gray;
  font-style: italic;
}

.content {
  min-height: 100vh;
  opacity: 0;
  animation-name: fade;
  animation-duration: 2s;
  animation-fill-mode: both;
}

.cookies {
  opacity: 0;
  animation-name: fade;
  animation-duration: 1s;
  animation-delay: 2s;

  animation-fill-mode: both;
}
.logo {
  margin-left: -0.1em;
}
.header {
  margin-bottom: 3em;
}
.footer {
  margin-bottom: 3em;
  margin-top: 3em;
  display: flex;
  justify-content: center;
  width: 100%;
}
.intro {
  width: 100%;
  min-height: 100vh;

  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
}
.cards {
  opacity: 0;
  animation-name: fade;
  animation-duration: 2s;
  animation-delay: 1s;
  animation-fill-mode: both;
}

.intro-fade-1 {
  opacity: 0;
  animation-name: fade-intro;
  animation-duration: 6s;
  animation-delay: 1s;

  animation-fill-mode: both;
}

.intro-fade-2 {
  opacity: 0;
  animation-name: fade-intro;
  animation-delay: 1s;

  animation-duration: 8s;
  animation-fill-mode: both;
}
@keyframes fade-intro {
  0% {
    opacity: 0;
  }
  25% {
    opacity: 1;
  }

  50% {
    opacity: 1;
  }
  90% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}

@keyframes fade {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
