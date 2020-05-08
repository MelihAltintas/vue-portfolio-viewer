<template>
<div class="portfolio-item-wrapper" @mouseenter="mouseEnter" @mouseleave="mouseLeave" :style="wrapperStyle">
    <a target="_blank" :href="href">
        <div class="portfolio-item long" :class="size" :style="style"></div>
    </a>
</div>
</template>

<script>
export default {
    name: 'PortfolioItem',
    props: {
        img: String,
        href: String,
        borderColor: {
            type: String,
            default: "#e74c3c"
        }
    },
    data() {
        return {
            wrapperStyle: ''
        }
    },
    methods: {
        mouseEnter() {
            this.wrapperStyle = `background-color:${this.borderColor};border-color:${this.borderColor}`;
        },
        mouseLeave() {
            this.wrapperStyle = "";
        }
    },
    computed: {
        style: function () {
            let style = "background-image:url(" + this.img + ");";
            return style;
        },
    }
}
</script>

<style scoped>
.portfolio-item-wrapper {

    border: 1px solid #fff;
    background-color: #fff;
    padding: 3px;
    position: relative;
    margin-right: 1px;
    transition: all 0.4s;
    -webkit-transition: all 0.4s;
    -webkit-box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
}

.portfolio-item {

    position: relative;
    background-position: top center;
    background-repeat: no-repeat;
    background-size: 100% auto;
    margin: 0 auto;
    height: 230px;
    -webkit-transition: background-position 1s linear 0s;
    -moz-transition: background-position 1s linear 0s;
    -o-transition: background-position 1s linear 0s;
    transition: background-position 1s linear 0s;
}

.portfolio-item-wrapper:hover {
    -webkit-box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4),
        0 -4px 12px rgba(0, 0, 0, 0.4);
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4),
        0 -4px 12px rgba(0, 0, 0, 0.4);
}

@media (max-width: 991px) {

    .portfolio-item-wrapper .portfolio-item {
        height: 600px;
    }
}

@media (max-width: 767px) {

    .portfolio-item-wrapper .portfolio-item {
        height: 500px;
    }
}

@media (max-width: 543px) {
    .portfolio-item-wrapper .portfolio-item {
        height: 300px;
    }
}

.portfolio-item-wrapper:hover {
    -webkit-transition: background-position .7s linear 0s;
    transition: background-position .7s linear 0s;
}

.long {
    -webkit-transition: background-position 4s linear 0s;
    transition: background-position 4s linear 0s;
}

.portfolio-item-wrapper:hover .portfolio-item {
    background-position: center bottom;
}
</style>
