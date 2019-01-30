<template>
    <div class="">
        <a class="totop" id="totop" @click="goTop">
            <img src="../../static/app/img/backTop.png" alt="">
        </a>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                // toTopShow: true,
                // isTop: true,
                // timer: null
            };
        },
        mounted() {
            // this.goTop()
            // window.addEventListener('onscroll', function () {
            // })
            // var scrollTop = document.documentElement.scrollTop || window.pageYOffset || document.body.scrollTop;
            // console.log(scrollTop);
        },
        //   destroyed() {
        //     window.removeEventListener("scroll", this.scrollToTop);
        //   },
        methods: {
            goTop() {
                //   var scrollTop = 0;
                //   if (document.documentElement && document.documentElement.scrollTop) {
                //     scrollTop = document.documentElement.scrollTop;
                //   } else if (document.body) {
                //     scrollTop = document.body.scrollTop;
                //   }
                var scrollTop = document.documentElement.scrollTop || window.pageYOffset || document.body.scrollTop;
                console.log(scrollTop);
                this.scrollTop = 0
                //   console.log(scrollTop);
                //   console.log(document.documentElement.scrollTop);
                //   scrollTop = 0
                //   document.body.scrollTop = 0;
                //   let totop = document.getElementById("totop");
                //   let scrollTop =
                //     window.pageYOffset ||
                //     document.documentElement.scrollTop ||
                //     document.body.scrollTop;
                //   let browserHeight = window.outerHeight;
                //   if (scrollTop > browserHeight) {
                //     totop.style.display = "block";
                //   } else {
                //     totop.style.display = "none";
                //   }
            }
            // nexttick(){
            //     var scrollTop = document.documentElement.scrollTop || window.pageYOffset || document.body.scrollTop;
            //     console.log(scrollTop);
            // }
        }
    };
</script>
<style scoped lang="scss">
    .totop {
        position: fixed;
        left: 0.8rem;
        bottom: 1.5rem;
        cursor: pointer;
    }
</style>