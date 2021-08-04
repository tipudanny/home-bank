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
                                <router-link to="" class="menu-text">Help</router-link>
                            </div>
                            <div class="is-flex move-icon">
                                <router-link to="" class="menu-text"> Ga naar www.argenta.be </router-link>
                                <right-arrow-svg class="svg-icon"/>
                            </div>
                            <div class="is-flex" @click="openDialog">
                                <div class="menu-text"> NL </div>
                                <down-arrow-svg :class="isDialog?'rotate-icon':'revert-rotation'" class="svg-icon"/>
                                <div v-if="isDialog" class="open-dialog">
                                    <ul>
                                        <li class="active">NL -Nederlands</li>
                                        <li>FR -Français</li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                    <h1 class="title"> Aanmelden op internetbankieren </h1>
                    <div class="main-content">
                        <phone-input></phone-input>
                        <div class="divider"></div>
                        <info-component></info-component>
                        <footer-component></footer-component>
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
import InfoComponent from "../components/InfoComponent";
import FooterComponent from "../components/FooterComponent";
import UpArrowSvg from "../components/icons/upArrowSvg";
export default {
    name: 'Home',
    components: {UpArrowSvg, FooterComponent, InfoComponent, PhoneInput, DownArrowSvg, RightArrowSvg, IIconSvg, LogoSvg},
    data(){
        return{
            isDialog:false,
        }
    },
    methods:{
        openDialog(){
            this.isDialog = !this.isDialog
        }
    }
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
            padding-bottom: 10px;
            .left-content{
                margin: 0 40px;
                .top-bar{
                    display: flex;
                    justify-content: space-between;
                    .right-menu{
                        display: flex;
                        align-items: center;
                        .move-icon{
                            position: relative;
                            padding-right: 20px;
                            margin-top: -3px;
                            .menu-text{
                                margin-right: 15px;
                            }
                            .svg-icon{
                                position: absolute;
                                right: 10px;
                            }
                            &:hover{
                                .svg-icon{
                                    right: 0;
                                }
                            }
                        }
                        & > div{
                            border-right: 0.5px solid #eaeaea;
                            padding: 0 10px;
                            color: #00a160;
                            position: relative;
                            .svg-icon{
                                width: 14px;
                                margin: 0 5px;
                            }
                            .rotate-icon{
                                transform: rotate(180deg);
                                transition: transform .4s;
                            }
                            .revert-rotation{
                                transition: transform .4s;
                            }
                            .menu-text{
                                color: #00a160;
                                font-weight: 700;
                                font-size: 14px;
                                &:hover{
                                    border-bottom: 1px solid;
                                }
                            }
                            .open-dialog{
                                position: absolute;
                                right: 0;
                                top: 35px;
                                background: #FFFFFF;
                                border: 1px solid #004a65;
                                ul{
                                    font-size: 15px;
                                    min-width: 160px;
                                    padding: 15px;
                                    li{
                                        padding: 10px;
                                        min-height: 45px;
                                        &:hover{
                                            border-bottom: 1px solid;
                                        }
                                    }
                                    .active{
                                        color: #004a65;
                                    }
                                }
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
                                    &:hover{
                                        border-bottom: none;
                                    }
                                }
                                .svg-icon{
                                    width: 12px;
                                    margin: 2px 5px;
                                }
                                &:hover{
                                    cursor: pointer;
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
                    .divider{
                        border-bottom: 1px solid #eaeaea;
                        margin: 24px 0;
                    }

                }
            }
        }
        .right-area{
            background-image: url("../../public/images/homebankbg.jpeg");
            background-size: cover;
            height: 100vh;
            position: sticky;
            top: 0;
        }
    }
    .d-flex{
        display: flex;
        align-items: center;
    }
}

</style>