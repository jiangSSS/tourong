<template>
    <div>
        <div class="header clearfix">
            <div class="search fll">
                <div class="fll select">
                    <div class="leftHeader">
                        <select class="radioItem" v-model="type" placeholder="请选择">
                            <option value="1">找资金</option>
                            <option value="2">找项目</option>
                            <option value="3">找资讯</option>
                            <option value="4">找活动</option>
                        </select>
                    </div>
                </div>
                <input type="text" placeholder="请输入内容" v-model="title" class="input_search" />
                <i class="iconfont icon-sousuo1" @click="search"></i>
            </div>
            <div class="fll cancel" @click="$router.push('/')">取消</div>
        </div>
        <!-- <ul class="searchSelect">
            <li><img src="../../../static/app/img/apply.jpg">111111</li>
            <li><img src="../../../static/app/img/apply.jpg">222222</li>
            <li><img src="../../../static/app/img/apply.jpg">333322</li>
            <li><img src="../../../static/app/img/apply.jpg">444442</li>
            <li><img src="../../../static/app/img/apply.jpg">555552</li>
            <li><img src="../../../static/app/img/apply.jpg">666666</li>
        </ul> -->
    </div>
</template>

<script>
    export default {
        data() {
            return {
                isShow: false,
                searchList: ["项目", "资金", "资讯"],
                type: '1',
                title: ""
            }
        },
        methods: {
            search() {
                console.log("111")
                if (this.type == '1') {
                    this.$router.push({ name: "searchMoney", query: { title: this.title } })
                } else if (this.type == '2') {
                    this.$router.push({ name: "searchProject", query: { title: this.title } })
                } else if (this.type == '3') {
                    this.$router.push({ name: "searchNews", query: { title: this.title } })
                } else if (this.type == '4') {
                    this.$router.push({ name: "searchActivity", query: { title: this.title } })
                }
            },
        }
    }
</script>
<style scoped lang="scss">
    .select {
        width: 1.5rem;
    }

    .search {
        margin: 0.2rem;
        background: #f3f5f7;
    }
    .icon-sousuo1 {
        line-height: 2;
        margin-right: 0.2rem;
    }

    .input_search {
        border: 0;
        color: rgb(153, 153, 153);
        width: 4rem;
        border-radius: 4px;
        font-family: "PingFang";
        line-height: 2.103;
        padding: 0 0.2rem;
        background: #f3f5f7;
    }

    .input_search:focus {
        outline: none;
    }

    .input_search::-webkit-input-placeholder {
        padding-left: 0.3rem;
    }

    .cancel {
        line-height: 3.5;
        margin: 0 0.2rem;
    }

    .type {
        /* background: #f3f5f7 */
    }

    .radioItem {
        display: block;
        margin: 0 0.1rem;
        border: 0;
        background: #f3f5f7;
        margin-top: 0.1rem;
    }

    .radioItem:focus {
        border: 0;
    }

    .sbuTitle {
        /* background: #f3f5f7 */
    }
</style>