<template>
    <Panel title="理财专享" :class="$style.advertiseA">
        <section :class="$style.content">
            <img
                src="//img12.360buyimg.com/jrpmobile/jfs/t10876/23/2566835181/40527/d7d27c08/59f97d68Ne53fda5b.png?width=1080&height=240"
                alt
            >
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
.advertiseA {
    @include panel;
    > h4 {
        display: none;
    }
    .content {
        img {
            width: 100%;
            display: block;
        }
    }
}
</style>