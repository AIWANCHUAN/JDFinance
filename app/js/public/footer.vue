<template>
    <Panel :class="$style.companyInfo" title="公司详情" :cname="cname">
        <ul :class="$style.content">
            <li>
                <router-link to="{name:home}">
                    <img
                        src="//img12.360buyimg.com/jrpmobile/jfs/t2842/350/3035567089/14791/5f6ff93d/577cf395N31e76288.png?width=1125&height=252"
                        alt
                    >
                </router-link>
            </li>
            <li>
                <div>
                    <router-link to="{name:home}">
                        <img
                            src="//img12.360buyimg.com/jrpmobile/jfs/t2971/333/1297567079/898/f2d2e00d/577dc28dNe5138337.png?width=108&height=108"
                            alt
                        >
                        <p>客户端</p>
                    </router-link>
                </div>
                <div>
                    <router-link to="{name:home}">
                        <img
                            src="//img12.360buyimg.com/jrpmobile/jfs/t2824/256/2966087355/831/188bfa25/577cf3dcN18aadbf2.png?width=108&height=108"
                            alt
                        >
                        <p>触屏版</p>
                    </router-link>
                </div>
                <div>
                    <router-link to="{name:home}">
                        <img
                            src="//img12.360buyimg.com/jrpmobile/jfs/t2920/282/1283157010/1040/23f1430b/577cf3e5N53f740b8.png?width=108&height=108"
                            alt
                        >
                        <p>电脑版</p>
                    </router-link>
                </div>
            </li>
            <li>Copyright © 2004-2017 京东JD.com 版权所有</li>
            <li>投资有风险，购买需谨慎</li>
            <li>京东金融平台服务协议</li>
            <li>京东金融隐私政策</li>
        </ul>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue";
export default {
    components: {
        Panel
    },
    props:{
        cname:{
            type:String,
            default:''
        }
    }
};
</script>

<style module lang='scss'>
@import "../../css/element.scss";
.companyInfo {
    @include panel;
    margin-bottom: 100px;
    > h4 {
        display: none;
    }
    .content {
        @include list;
        background: #f5f5f5;
        li {
            width: 100%;
            text-align: center;
            color: #999;
            font-size: 24px;
            img {
                width: 100%;
            }
            // 第二行
            &:nth-of-type(2) {
                @include list(row);
                height: 186px;
                & > div {
                    box-sizing: border-box;
                    padding-top: 20px;
                    width: 33.33%;
                    text-align: center;
                    a {
                        text-decoration: none;
                        img {
                            width: 90px;
                            height: 90px;
                        }
                        p {
                            font-size: 26px;
                            color: #999;
                            text-align: center;
                            margin-top: 12px;
                            overflow: hidden;
                            text-overflow: ellipsis;
                            white-space: nowrap;
                        }
                    }
                }
            }
            // 第三行和之后
            &:nth-of-type(n + 3) {
                padding: 24px 0;
                height: 38px;
                line-height: 38px;
                border-top: 1px solid #ddd;
            }
        }
    }
}
</style>