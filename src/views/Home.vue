<template>
    <div class="home-page">
        <div class="columns is-mobile">
            <div class="column is-two-thirds left-area">
                <div class="left-content">
                    <div class="top-bar">
                        <logo-svg/>
                        <div class="right-menu">
                            <div class="is-flex">
                                <i-icon-svg class="svg-icon"/>
                                <div class="menu-text">Help</div>
                            </div>
                            <div class="is-flex">
                                <div class="menu-text"> Ga naar www.argenta.be </div>
                                <right-arrow-svg class="svg-icon"/>
                            </div>
                            <div class="is-flex">
                                <div class="menu-text"> NL </div>
                                <down-arrow-svg class="svg-icon"/>
                            </div>
                        </div>
                    </div>
                    <h1 class="title"> Aanmelden op internetbankieren </h1>
                    <div class="main-content">
                        <div>
                            <phone-input></phone-input>
                        </div>
                    </div>
                </div>
            </div>
            <div class="column right-area"></div>
        </div>
    </div>
</template>

<script>

import LogoSvg from "../components/icons/LogoSvg";
import IIconSvg from "../components/icons/iIconSvg";
import RightArrowSvg from "../components/icons/rightArrowSvg";
import DownArrowSvg from "../components/icons/downArrowSvg";
import PhoneInput from "../components/PhoneInput";
export default {
    name: 'Home',
    components: {PhoneInput, DownArrowSvg, RightArrowSvg, IIconSvg, LogoSvg},
}
</script>
<style scoped lang="scss">
.home-page{
    background-color: #fafafb !important;
    & > div {
        margin: 0;
        padding: 0;
        .left-area{
            width: 63.3% !important;
            padding: 28px 16px;
            .left-content{
                margin: 0 40px;
                .top-bar{
                    display: flex;
                    justify-content: space-between;
                    .right-menu{
                        display: flex;
                        align-items: center;
                        & > div{
                            border-right: 0.5px solid #eaeaea;
                            padding: 0 10px;
                            color: #00a160;
                            .svg-icon{
                                width: 14px;
                                margin: 0 5px;
                            }
                            .menu-text{
                                color: #00a160;
                                font-weight: 700;
                                font-size: 14px;
                            }
                            &:last-child{
                                font-weight: normal;
                                font-size: 12px;
                                border: none;
                                color: #AAAAAA !important;
                                .menu-text{
                                    font-size: 12px;
                                    font-weight: normal;
                                    color: #AAAAAA;
                                }
                                .svg-icon{
                                    width: 12px;
                                    margin: 2px 5px;
                                }
                            }
                        }
                    }
                }
                .title{
                    padding-bottom: 8px;
                    padding-top: 20px;
                    color: #333;
                }
                .main-content{

                }
            }
        }
        .right-area{
            background-image: url("../../public/images/homebankbg.jpeg");
            background-size: cover;
            height: 100vh;
        }
    }
    .d-flex{
        display: flex;
        align-items: center;
    }
}

</style>