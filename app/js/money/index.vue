<template lang="html">
    <div>
      <Heador/>
      <Slider/>
      <AdvertiseA/>
      <Money/>
      <AdvertiseB/>
      <Finance/>
      <AdvertiseC/>
      <Footor cname="mfooter"/>
      <Nav-bar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue";
import Slider from "./mslider.vue";
import AdvertiseA from "./advertise_a.vue";
import Money from "./money.vue";
import AdvertiseB from "./advertise_b.vue";
import Finance from "./finance.vue";
import AdvertiseC from "./advertise_c.vue";
import Footor from "../public/footer.vue";
import NavBar from "../public/navbar.vue";
export default {
    components: {
        Heador,
        Slider,
        AdvertiseA,
        Money,
        AdvertiseB,
        Finance,
        AdvertiseC,
        Footor,
        NavBar
    }
};
</script>
<style lang="scss">
.mfooter {
    margin-top: 0 !important;
    ul {
        li {
            &:first-child {
                display: none;
            }
        }
    }
}
</style>