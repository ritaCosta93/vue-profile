<template>
    <div class="content-wrapper-5" id="pyt" >


        <ul class="payment__list">
            <Tooltip />
            <li class="__item"><a   class="__link link1" href="#"><img class="__img" src="https://cdn4.iconfinder.com/data/icons/payment-method/160/payment_method_card_visa-32.png"/></a></li>
            <li class="__item"><a   class="__link link2" href="#"><img class="__img" src="https://cdn4.iconfinder.com/data/icons/payment-method/160/payment_method_master_card-32.png"/></a></li>
            <li class="__item"><a   class="__link link3" href="#"><img class="__img" src="https://cdn4.iconfinder.com/data/icons/payment-method/160/payment_method_paypal-32.png"/></a></li>
            <li class="__item"><a   class="__link link4" href="#"><img class="__img" src="https://cdn4.iconfinder.com/data/icons/payment-method/160/payment_method_skrill-32.png"/></a></li>
        </ul>
    </div>
</template>

<script>
import Tooltip from '../Tooltip/Tooltip.vue'

export default {
  name: 'Payment',

  components:{
      Tooltip
  }

};

</script>

<style lang="scss">
@import 'Payment.scss';
</style>
