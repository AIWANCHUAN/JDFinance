<template>
    <article>
        <!-- 轮播图 -->
        <Slider :items="items" :cname="$style.slider"></Slider>
        <!-- 第一行list工具 -->
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters1" :key="item.img">
                <router-link :to="{name:item.href}">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{item.title}}</h4>
                </router-link>
            </div>
        </section>
        <!-- 第二行list工具 -->
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters2" :key="item.img">
                <router-link :to="{name:item.href}">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{item.title}}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script>
import Slider from "../core/slider.vue";
export default {
    components: {
        Slider
    },
    data() {
        return {
            // slider数据
            items: [
                {
                    src:
                        "//img12.360buyimg.com/jrpmobile/jfs/t1/23987/10/6467/33251/5c51768aE67229997/72c6ddc1b71c0b11.png?width=750&height=400",
                    href: "home"
                },
                {
                    src:
                        "//img12.360buyimg.com/jrpmobile/jfs/t1/17773/3/6891/54795/5c653dcdE25124e00/6d2f5d6998a597b6.jpg?width=750&height=400",
                    href: "home"
                },
                {
                    src:
                        "//img12.360buyimg.com/jrpmobile/jfs/t1/26590/6/7266/149007/5c6a7ab7E5a201499/3949ded503668475.png?width=750&height=400",
                    href: "home"
                },
                {
                    src:
                        "//img12.360buyimg.com/jrpmobile/jfs/t1/19204/26/5600/48084/5c3ed8a5Ef3ff6d5e/8dce48f9e85e7939.jpg?width=750&height=400",
                    href: "home"
                }
            ],
            // 列表数据
            enters1: [
                {
                    img:
                        "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                    href: "download",
                    title: "优惠券"
                },
                {
                    img:
                        "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                    href: "home",
                    title: "领福利"
                },
                {
                    img:
                        "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
                    href: "home",
                    title: "抢钢镚"
                },
                {
                    img:
                        "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=132&height=132",
                    href: "home",
                    title: "白条提取"
                }
            ],
            enters2: [
                {
                    img:
                        "//img12.360buyimg.com/jrpmobile/jfs/t1/520/34/950/3686/5b9239e3Eaaf5465c/8d8c35badacfc114.png?width=132&height=132",
                    href: "home",
                    title: "工资理财"
                },
                {
                    img:
                        "//img12.360buyimg.com/jrpmobile/jfs/t1/1216/39/659/4516/5b923b1cE5943d1c6/dabaf8b842f57eb9.png?width=132&height=132",
                    href: "home",
                    title: "众筹"
                },
                {
                    img:
                        "//img12.360buyimg.com/jrpmobile/jfs/t1/3924/28/657/3552/5b9240dbE60256c31/78b52d5ab675f800.png?width=132&height=132",
                    href: "home",
                    title: "租房"
                },
                {
                    img:
                        "//img12.360buyimg.com/jrpmobile/jfs/t27088/243/2089650291/12365/2469f395/5bf677f9N795eec5e.png?width=132&height=132",
                    href: "home",
                    title: "车主服务"
                }
            ]
        };
    }
};
</script>
 
<style lang="scss" module>
@import "../../css/element.scss";
.slider {
    margin-top: 120px;
    img {
        width: 100%;
    }
}
.list {
    @include list(row, block);
    background: #fff;
    padding-top: 40px;
    padding-bottom: 20px;
    justify-content: space-around;
    a {
        text-decoration: none;
    }
    .item {
        text-align: center;
        img {
            display: inline-block;
            width: 90px;
            height: 90px;
        }
        h4 {
            font-size: 26px;
            margin-top: 12px;
            color: #666;
        }
    }
}
</style>