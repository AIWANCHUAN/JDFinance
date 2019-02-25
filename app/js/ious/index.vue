<template lang="html">
    <div>
      <Heador/>
      <Slider/>
      <Welfare/>
      <Service/>
      <Footor/>
      <Nav-bar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue";
import Slider from "./islider.vue";
import Welfare from "./welfare.vue";
import Service from "./service.vue";
import Footor from "../public/footer.vue";
import NavBar from "../public/navbar.vue";
export default {
    components: {
        Heador,
        Slider,
        Welfare,
        Service,
        Footor,
        NavBar
    }
};
</script>
