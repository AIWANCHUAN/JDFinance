<template>
    <Panel :class="$style.life" title="生活服务">
        <ul :class="$style.content">
            <li :class="$style.item">
                <router-link to="{'name':home}">
                    <img
                        src="//img12.360buyimg.com/jrpmobile/jfs/t4375/104/1184122472/3976/89741da4/58be8a6eNf10193d0.png?width=135&height=135"
                        alt
                    >
                    <p>惠加油</p>
                </router-link>
            </li>
            <li :class="$style.item">
                <router-link to="{'name':home}">
                    <img
                        src="//img12.360buyimg.com/jrpmobile/jfs/t4747/185/1901740991/5892/1383fb93/58f57851N17ee6993.jpg?width=132&height=132"
                        alt
                    >
                    <p>小白信用</p>
                    <p>全新升级</p>
                </router-link>
            </li>
            <li :class="$style.item">
                <router-link to="{'name':home}">
                    <img
                        src="//img12.360buyimg.com/jrpmobile/jfs/t3241/234/8044685271/3713/7b29f77f/58be89c8Nb9d41295.png?width=135&height=135"
                        alt
                    >
                    <p>信用卡还款</p>
                </router-link>
            </li>
            <li :class="$style.item">
                <router-link to="{'name':home}">
                    <img
                        src="//img12.360buyimg.com/jrpmobile/jfs/t3172/259/7993557249/4351/fd082707/58be8a81Nd7716a06.png?width=135&height=135"
                        alt
                    >
                    <p>卡转让</p>
                </router-link>
            </li>
            <li :class="$style.item">
                <router-link to="{'name':home}">
                    <img
                        src="//img12.360buyimg.com/jrpmobile/jfs/t3085/320/8107659086/4344/cdbba2dd/58be8acfNdadcaf00.png?width=135&height=135"
                        alt
                    >
                    <p>定期还款</p>
                </router-link>
            </li>
        </ul>
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
.life {
    @include panel;
    .content {
        @include list(row);
        padding-bottom: 40px;
        .item {
            width: 20%;
            box-sizing: border-box;
            text-align: center;
            a {
                text-decoration: none;
                img {
                    width: 90px;
                    height: 90px;
                }
                p {
                    font-size: 26px;
                    color: #666;
                    text-overflow: ellipsis;
                    overflow: hidden;
                    white-space: nowrap;
                    margin: 12px 0;
                    &:nth-of-type(2) {
                        color: #ff801a;
                    }
                }
            }
        }
    }
}
</style>