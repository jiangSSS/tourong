<template>
    <div class="">
       <div>测试</div>
       <div class="social-share" style="margin-top:4rem"></div>
    </div>
</template>

<script>
    import 'social-share.js/dist/css/share.min.css'
    import 'social-share.js/dist/js/social-share.min.js'
    export default {
        data() {
            return {

            };
        },
        mounted() {
            var $config = {
                title: '234',
                description: '123',
                wechatQrcodeTitle: "微信扫一扫：分享", // 微信二维码提示文字
                wechatQrcodeHelper: '<p>微信里点“发现”，扫一下</p><p>二维码便可将本文分享至朋友圈。</p>',
            };
            // socialShare('.social-share-cs', $config);
        },

        methods: {


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