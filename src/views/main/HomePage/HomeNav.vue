<template>
    <div class="index-left-block">
        <h2>全部产品</h2>
        <div v-for="(product, index) in productList" :key="index">
            <h3>{{ product.title }}</h3>
            <ul>
                <li v-for="(item, index) in product.list" :key="index">
                    <a :href="item.url">{{ item.name }}</a>
                    <span class="hot-tag" v-if="item.hot">HOT</span>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            productList: [
                {
                    title: "手机",
                    list: [
                        {
                            id: 1,
                            name: "荣耀",
                            url: "",
                            hot: true,
                        },
                        {
                            id: 2,
                            name: "华为",
                            url: "",
                            hot: false,
                        },
                        {
                            id: 3,
                            name: "vivo",
                            url: "",
                            hot: false,
                        },
                    ],
                },
                {
                    title: "书籍",
                    list: [
                        {
                            id: 1,
                            name: "红楼梦",
                            url: "",
                            hot: false,
                        },
                        {
                            id: 2,
                            name: "水浒传",
                            url: "",
                            hot: true,
                        },
                        {
                            id: 3,
                            name: "西游记",
                            url: "",
                            hot: false,
                        },
                        {
                            id: 4,
                            name: "三国演义",
                            url: "",
                            hot: false,
                        },
                        {
                            id: 5,
                            name: "昆虫记",
                            url: "",
                            hot: false,
                        },
                        {
                            id: 6,
                            name: "乡愁",
                            url: "",
                            hot: false,
                        },
                    ],
                },
                {
                    title: "相机",
                    list: [
                        {
                            id: 1,
                            name: "佳能",
                            url: "",
                            hot: true,
                        },
                        {
                            id: 2,
                            name: "徕卡",
                            url: "",
                            hot: false,
                        },
                        {
                            id: 3,
                            name: "索尼",
                            url: "",
                            hot: false,
                        },
                    ],
                },
            ],
        };
    },
};
</script>

<style scoped lang="less">
.index-left-block {
    margin: 15px;
    background: #fff;
    box-shadow: 0 0 1px #ddd;
}
.index-left-block .hr {
    margin-bottom: 20px;
    height: 1px;
    width: 100%;
    background: #ddd;
}
.index-left-block h2 {
    background: #63afe1;
    color: #fff;
    padding: 10px 15px;
    margin-bottom: 20px;
}
.index-left-block h3 {
    padding: 0 15px 5px 15px;
    font-weight: bold;
    color: #222;
}
.index-left-block ul {
    padding: 10px 15px;
}
.index-left-block li {
    padding: 5px;
    a {
        color: #222;
    }
}
.hot-tag {
    background: red;
    color: #fff;
}
</style>