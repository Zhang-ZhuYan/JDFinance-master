<template>
    <article class="swiper">
        <slider :items="items"></slider>
        <section class="list">
            <div v-for="item of menus" :key="item.src" class="menu">
                <router-link :to="{name:item.href}">
                    <img :src="item.img" alt="">
                    <h4>{{item.title}}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>
<script>
import Slider from '../core/slider'
export default {
    data(){
        return {
            items: [
                {
                    href: 'a',
                    src: 'https://img10.360buyimg.com/mcmktadmin/jfs/t1/89860/1/8810/125315/5e09563cEd2c84b46/c66fc96833d63902.png?width=686&height=396'
                },{
                    href: 'b',
                    src: 'https://img10.360buyimg.com/mcmktadmin/jfs/t1/85115/40/8400/21554/5e0495c0E47a5e70b/eed48c90d936c097.png?width=686&height=396'
                },{
                    href: 'c',
                    src: 'https://img10.360buyimg.com/mcmktadmin/jfs/t1/100494/11/8497/152655/5e04968aE21f44b84/6b8a59041d046373.png?width=686&height=396'
                },{
                    href: 'd',
                    src: 'https://img10.360buyimg.com/mcmktadmin/jfs/t1/90724/4/8439/197686/5e04b83fE76bb7593/f7677ac08035774d.jpg?width=686&height=396'
                }
            ],
            menus: [
                {
                    href: 'https://m.jr.jd.com/mjractivity/rn/couponCenter/index.html?RN=couponCenter&from=wtmzhan&sid=',
                    img: 'https://img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132',
                    title: '优惠券'
                },{
                    href: 'https://m.jr.jd.com/spe/qyy/hzq/index.html?usertype=1176&mz&sid=',
                    img: 'https://img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132',
                    title: '抢钢镚'
                },{
                    href: 'https://m.jr.jd.com/spe/qyy/hzq/index.html?usertype=1176&mz&sid=',
                    img: 'https://img12.360buyimg.com/jrpmobile/jfs/t1/520/34/950/3686/5b9239e3Eaaf5465c/8d8c35badacfc114.png?width=90&height=90',
                    title: '工资理财'
                },{
                    href: 'https://m.jr.jd.com/ck/dingqicunkuan/record.html?sid=',
                    img: 'https://img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135',
                    title: '白条提额'
                }
            ]
        }
    },
    components: {
        Slider
    }
}
</script>
<style lang="scss">
@import '../../css/element.scss';
.swiper{
    margin-top: 120px;
    padding: 20px;
    .list{
        @include list(row);
        justify-content: space-between;
        .menu{
            a{
                text-decoration: none;
            }
            a>img{
                width: 90px;
                height: 90px;
            }
            a>h4{
                margin: 5px 0;
                padding: 0;
                font-size: 26px;
                font-weight: normal;
                color: #000000;
            }
        }
    }
}

</style>