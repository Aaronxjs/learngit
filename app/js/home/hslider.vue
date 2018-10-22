<template>
    <article>
        <Slider :items="items" :cname="$style.slider"/>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{name: item.href}">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{item.title}}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>
<script>
import Slider from "../core/slider.vue"
export default {
    components: {
        Slider
    },
    data(){
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t1/2790/15/6365/41512/5ba22351E6a312896/91ede54780a0ef37.jpg?width=750&height=320"
            },{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t1/4093/36/6284/46179/5ba222d4Ef6991e80/fcd0a90a6863602f.jpg?width=750&height=320"
            }],
            enters: [{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                title: "优惠劵"
            },{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                title: "领福利"
            },{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
                title: "抢钢蹦"
            },{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
                title: "白条提额"
            },{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t1/520/34/950/3686/5b9239e3Eaaf5465c/8d8c35badacfc114.png?width=90&height=90",
                title: "工资理财"
            },{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t1/1216/39/659/4516/5b923b1cE5943d1c6/dabaf8b842f57eb9.png?width=90&height=90",
                title: "众筹"
            },{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t1/3924/28/657/3552/5b9240dbE60256c31/78b52d5ab675f800.png?width=90&height=90",
                title: "租房"
            },{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t1/479/25/929/9198/5b9243aaE826fc97b/37ef0a7cdfd24238.png?width=120&height=120",
                title: "电影票"
            }]
        }
    }
}
</script>
<style lang="scss" module>
    @import "../../css/element.css";
    .slider{
        margin-top: 120px;
    }
    .list{
        @include list(row);
        background: #fff;
        padding-top: 120px;
        padding-bottom: 20px;
        justify-content: space-around;
        a{
            text-decoration: none;
        }
        .item{
            text-align: center;
            img{
                display: inline-block;
                width: 90px;
                height: 90px;
            }
            h4{
                font-size: 26px;
                margin-top: 12px;
                color: #666;
            }
        }
    }
</style>
