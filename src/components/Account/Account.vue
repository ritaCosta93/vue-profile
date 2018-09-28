<template>
    <div class="content-wrapper-2" id="wp-2">
        <div class="act-details" id="act">
            <h3>My account</h3>

            <span>Name: {{name}}</span>
            <span>Address: {{address}}</span>
            <span>Payment: {{payment}}</span>
            <span>Feedback: {{feedback}}</span>
            <span>About: {{about}}</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Account',
  props: {
    name: String,
    address: String,
    payment: String,
    feedback: String,
    about: String
  }
};
</script>

<style lang="scss">
@import 'Account.scss';
</style>
