<template>
    <div class="content-wrapper-3" >
        <div class="adr-details" id="adr">
            <h3>My address</h3>
            <iframe
                width="600"
                height="450"
                frameborder="0" style="border:0"
                src="https://www.google.com/maps/embed/v1/place?key=AIzaSyB8jwFhJcdngjjtEsofxSae7qUHH7qZYt8&q=rua+cidade+tokushima,leiria,portugal&zoom=18&maptype=satellite" allowfullscreen>
            </iframe>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Address'
};
</script>

<style lang="scss">
@import 'Address.scss';
</style>
