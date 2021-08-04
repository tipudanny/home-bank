<template>
    <div class="is-flex infos ">
        <div class="copyright-area">© 2021 Argenta</div>
        <div class="is-flex">
            <div class="is-flex">
                <div class="info-text">Juridische informatie</div>
                <right-arrow-simple class="svg-icon"></right-arrow-simple>
            </div>
            <div class="is-flex">
                <div class="info-text">Privacy</div>
                <right-arrow-simple class="svg-icon"></right-arrow-simple>
            </div>
            <div class="is-flex">
                <div class="info-text">Cookiebeleid</div>
                <right-arrow-simple class="svg-icon"></right-arrow-simple>
            </div>
            <div class="is-flex">
                <div class="info-text">Tarieven</div>
                <right-arrow-simple class="svg-icon"></right-arrow-simple>
            </div>
            <div class="is-flex">
                <div class="info-text">homebank 1.6.1</div>
            </div>
        </div>
    </div>
</template>

<script>
import RightArrowSimple from "./icons/RightArrowSimple";
export default {
    name: "FooterComponent",
    components: {RightArrowSimple}
}
</script>

<style scoped lang="scss">

.infos{
    margin-top: 8px;
    padding: 10px 35px;
    align-items: center;
    justify-content: space-between;

    .copyright-area{
        font-size: 12px;
        font-weight: 700;
        color: #333;
    }
    .svg-icon{
        width: 7px;
        margin: -3px 5px;
    }
    .info-text{
        color: #666;;
        font-size: 12px;
        padding: 0 5px;
    }
}
</style>