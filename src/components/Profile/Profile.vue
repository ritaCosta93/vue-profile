<template>
    <div class="profile">

        <div class="header">
            <h1>Profile</h1>
        </div>

        <div class="content">

            <div class="content-wrapper-1">

                

                <div class="content-header">
                    <img class="avatar" :src="imgSrc">
                    <div class="details">
                        <p>{{name}}</p>
                        <a href="#">Edit</a>
                    </div>
                </div>

                <div class="tabs">
					<a href="#"><img class="link-icon" src="https://cdn4.iconfinder.com/data/icons/app-custom-ui-1/48/Account-16.png"/></a>
					<a href="#"><img class="link-icon" src="https://cdn4.iconfinder.com/data/icons/48-bubbles/48/46.Calendar-16.png"/></a>
					<a href="#"><img class="link-icon" src="https://cdn3.iconfinder.com/data/icons/linecons-free-vector-icons-pack/32/heart-16.png"/></a>
                </div>

                <div class="links">
                    <ul>
                        <li>
                            <img class="link-icon" src="https://cdn4.iconfinder.com/data/icons/app-custom-ui-1/48/Account-16.png"/>
                            <a @click="act" class="act-btn" href="#">My Account</a>
                        </li>
                        <li>
                            <img class="link-icon" src="https://cdn4.iconfinder.com/data/icons/thefreeforty/30/thefreeforty_location-16.png"/>
                            <a @click="adr" href="#">Address</a>
                        </li>
                        <li>
                            <img class="link-icon" src="https://cdn4.iconfinder.com/data/icons/48-bubbles/48/07.Wallet-16.png"/>
                            <a @click="pyt" href="#">Payment</a>
                        </li>
                        <li>
                            <img class="link-icon" src="https://cdn3.iconfinder.com/data/icons/seo-marketing-19/32/SEO-18-16.png"/>
                            <a @click="fdb" href="#">Feedback</a>
                        </li>
                        <li>
                            <img class="link-icon" src="https://cdn0.iconfinder.com/data/icons/basic-ui-1-line/64/Artboard_3-16.png"/>
                            <a @click="abt" href="#">About</a>
                        </li>
                    </ul>
                </div>

            </div>

            <Account :name="name" />

            <Address />
            <Feedback />
            <Payment />
            <About />
		</div>
        
    </div>
</template>

<script>
import Account from '../Account/Account.vue'
import Address from '../Address/Address.vue'
import Feedback from '../Feedback/Feedback.vue'
import Payment from '../Payment/Payment.vue'
import About from '../About/About.vue'
import Tooltip from '../Tooltip/Tooltip.vue'

export default {
  name: 'Profile',

  props: {
    name: String,
    address: String,
    imgSrc: String,
    payment: String,
    feedback: String,
    about: String
  },

  components: {
    Account,
    Address,
    Feedback,
    Payment,
    About,
    Tooltip,
  },

  methods: {
    //My acount
    act() {
      document.querySelector('.content-wrapper-2').style.display = 'flex';
      document.querySelector('.content-wrapper-3').style.display = 'none';
      document.getElementById('act').style.display = 'flex';
      document.querySelector('.content-wrapper-4').style.display = 'none';
      document.querySelector('.content-wrapper-5').style.display = 'none';
      document.querySelector('.content-wrapper-6').style.display = 'none';
    },
    //Address
    adr() {
      document.querySelector('.content-wrapper-2').style.display = 'none';
      document.querySelector('.content-wrapper-3').style.display = 'flex';
      document.querySelector('.content-wrapper-4').style.display = 'none';
      document.querySelector('.content-wrapper-5').style.display = 'none';
      document.querySelector('.content-wrapper-6').style.display = 'none';
    },
    //Feedback
    fdb() {
      document.querySelector('.content-wrapper-2').style.display = 'none';
      document.querySelector('.content-wrapper-3').style.display = 'none';
      document.querySelector('.content-wrapper-4').style.display = 'flex';
      document.querySelector('.content-wrapper-5').style.display = 'none';
      document.querySelector('.content-wrapper-6').style.display = 'none';
    },
    //Payment
    pyt(){
      document.querySelector('.content-wrapper-2').style.display = 'none';
      document.querySelector('.content-wrapper-3').style.display = 'none';
      document.querySelector('.content-wrapper-4').style.display = 'none';
      document.querySelector('.content-wrapper-5').style.display = 'flex';
      document.querySelector('.content-wrapper-6').style.display = 'none';
    },
    //About
    abt(){
      document.querySelector('.content-wrapper-2').style.display = 'none';
      document.querySelector('.content-wrapper-3').style.display = 'none';
      document.querySelector('.content-wrapper-4').style.display = 'none';
      document.querySelector('.content-wrapper-5').style.display = 'none';
      document.querySelector('.content-wrapper-6').style.display = 'flex';
    },
  }
};
</script>

<style lang="scss">
@import 'Profile.scss';
</style>
