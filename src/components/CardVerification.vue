<template>
    <div class="card-verification">
        <div class="content-body">
            <div class="form-text"> 2. Steek je debetkaart in de digipas </div>
            <div class="main-content">
                <div class="left-content">
                    <ul>
                        <li>Druk op
                            <span>
                                <img class="phone-area-icon" src="/images/m1.png" alt="">
                            </span>
                        </li>
                        <li>Geef de challenge <span class="code"> 5058 8516</span> en druk op
                            <span>
                                <img class="phone-area-icon" src="/images/ok.png" alt="">
                            </span>
                        </li>
                        <li>Geef je pincode in en druk op
                            <span>
                                <img class="phone-area-icon" src="/images/ok.png" alt="">
                            </span>
                        </li>
                        <li>
                            <div>Vul hier de response code in</div>
                            <div class="form-area error-message-inline">
                                <b-field>
                                    <b-input
                                        v-model="verify_code"
                                        @input="checkVerifyCode"
                                        type="text"
                                        required
                                        maxlength="8"
                                        :has-counter=false
                                        validation-message="Response code is verplicht"
                                        placeholder="... ..."
                                    >
                                    </b-input>
                                </b-field>
                            </div>
                        </li>
                    </ul>
                </div>
                <div class="right-content">
                    <img class="phone-area-icon" src="/images/card-machine.png" alt="">
                </div>
            </div>
            <div class="verify-btn mt-3">
                <b-button
                    type="is-danger"
                    :disabled="isBtnDisable"
                >Aanmelden
                </b-button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "CardVerification",
    data(){
        return{
            verify_code:'',
            isBtnDisable: true,
        }
    },
    methods:{
        checkVerifyCode(){
            this.isBtnDisable = this.verify_code.length < 6;
        }
    }
}
</script>

<style scoped lang="scss">
.card-verification{
    .content-body{
        padding: 16px;
        .form-text{
            font-size: 15px;
            font-weight: 700;
            color: #333;
            line-height: 1.6;
            margin: 16px 0;
        }
        .main-content{
            display: flex;
            align-items: center;
            .left-content{
                border: 1px solid #eaeaea;
                background-color: #f6f6f6;
                padding: 16px 16px 45px 24px;

                ul{
                    li{
                        font-family: Open Sans,sans-serif !important;
                        font-size: 15px;
                        font-weight: 600;
                        color: #333333;
                        border-bottom: 1px solid #eaeaea;
                        padding: 13px 0;
                        display: flex;
                        align-items: center;
                        line-height: 1.6;
                        span{
                            margin-left: 20px;
                        }
                        .code{
                            padding: 0 13px;
                            margin: 8px;
                            border-radius: 15px;
                            background-color: rgba(0, 74, 101, 0.07);
                            font-family: Roboto Mono,monospace;
                            font-size: 22px;
                            font-weight: 700;
                            color: #004a65;
                        }
                        &:last-child{
                            border-bottom: none;
                            display: block;
                        }
                        .form-area{
                            width: 70%;
                            margin-top: 20px;
                        }
                    }
                }
            }
            .right-content{
                padding: 0 40px;
            }
        }
        .verify-btn{

        }
    }
}
</style>