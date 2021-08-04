<template>
    <div class="info-component">
        <div class="message-area">
            <div class="title">
                Ga nooit in op ongewone e-mails of sms'en!
            </div>
            <div class="sub-title">
                Fraudeurs sturen vaak e-mails uit onder het mom van een vernieuwing van uw debetkaart of digipas. Ga daar nooit op in. Ze verwijzen naar websites die niet van Argenta zijn. Argenta zal ook nooit vragen om je kaartnummer via de telefoon door te geven omdat je zogezegd een nieuwe debetkaart of digipas krijgt.
            </div>
            <div class="title"> Krijg je toch verdachte boodschappen? </div>
            <div class="sub-title">
                Heb je al codes doorgegeven via de telefoon? Of is er al geld van je rekening gehaald? Neem dan
                <a href="tel:032855333">meteen contact op via het nummer 03/285 53 33</a>
                (voor slachtoffers van phishing 24/7 bereikbaar).
                <div class="line-break"></div>
                Heb je een verdacht bericht gekregen? Meld het via <a href="mailto:phishing@argenta.be">phishing@argenta.be</a>.
            </div>
            <div class="footer-title is-flex">
                <div class="is-flex">
                    <router-link to="" class="menu-text"> Tips voor veilig internetbankieren </router-link>
                    <right-arrow-svg class="svg-icon"/>
                </div>
                <div class="is-flex">
                    <router-link to="" class="menu-text"> Lees onze tips om phishing te voorkomen </router-link>
                    <right-arrow-svg class="svg-icon"/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import RightArrowSvg from "./icons/rightArrowSvg";
export default {
    name: "InfoComponent",
    components: {RightArrowSvg}
}
</script>

<style scoped lang="scss">
.info-component{
    background-color: #fef6f5;
    .message-area{
        border: 1px solid #eb1700;
        padding: 16px;
        font-size: 15px;

        .title{
            color: #eb1700;
            padding: 10px 0;
            font-size: 1.17em;
            font-weight: 700;
            margin: 0;
        }
        .sub-title{
            color: #666;
            font-size: .8rem;
            padding: 4px 0;
            margin: 0;
            a{
                color: #00a160;
                font-weight: 600;
                border-bottom: 1px solid;
                white-space: pre-line;
            }
            .line-break{
                margin-top: 8px;
            }
        }
        .footer-title{
            margin-top: 20px;
            & > div{
                align-items: center;
                position: relative;
                min-height: 35px;
                min-width: 33%;
                margin-right: 35px;
                .svg-icon{
                    width: 14px;
                    padding-top: 4px;
                    position: absolute;
                    right: 0;
                }
                .menu-text{
                    color: #00a160;
                    font-weight: 700;
                    font-size: 14px;
                    margin-right: 20px;
                }
                &:hover{
                    .menu-text{
                        border-bottom: 1px solid;
                    }
                    .svg-icon{
                        right: -10px;
                    }
                }
            }
        }
    }
}
</style>