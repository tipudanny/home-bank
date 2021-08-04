<template>
    <div class="is-flex">
        <img class="phone-area-icon" src="/images/phone-area-icon.svg" alt="">
        <div class="phone-text ml-4">
            <p class="sub-title">Aanmelden met</p>
            <p class="text-title">Debetkaart & digipas</p>
        </div>
    </div>
</template>

<script>
import PhoneAreaIcon from "./icons/phoneAreaIcon";
export default {
    name: "PhoneInput",
    components: {PhoneAreaIcon}
}
</script>

<style scoped lang="scss">
.phone-area-icon{
    height: 48px;
    max-width: 48px;
}
.phone-text{
    .sub-title{
        color: #004a65;
        line-height: 24px;
        font-size: 15px;
    }
    .text-title{
        line-height: 24px;
        font-size: 15px;
        color: #004a65;
        font-weight: 700;
    }
}
</style>