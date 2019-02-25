<template>
    <Panel :class="$style.daily" title="每日签到">
        <section :class="$style.content">
            <img
                src="//img12.360buyimg.com/jrpmobile/jfs/t3184/283/6032981290/37056/fa30c674/589bd5a2Nabdbbbd9.jpg?width=376&height=160"
                alt
            >
            <img
                src="//img12.360buyimg.com/jrpmobile/jfs/t3298/196/6130416421/33755/a0536d3e/589bd5d4Nf32e7adc.jpg?width=374&height=160"
                alt
            >
            <p>不抢白不抢</p>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue";
export default {
    components: {
        Panel
    }
};
</script>

<style module lang="scss">
@import "../../css/element.scss";
.daily {
    @include panel;
    .content {
        @include list(row);
        position: relative;
        img {
            width: 320px;
        }
        p {
            position: absolute;
            top: -112px;
            right: 20px;
            height: 112px;
            line-height: 112px;
            font-size: 24px;
            color: #999;
        }
    }
}
</style>
