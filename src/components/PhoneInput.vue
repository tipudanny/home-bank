<template>
    <div class="first-component">
        <div class="is-flex content-header">
            <img class="phone-area-icon" src="/images/phone-area-icon.svg" alt="">
            <div class="phone-text ml-4">
                <p class="sub-title">Aanmelden met</p>
                <p class="text-title">Debetkaart & digipas</p>
            </div>
        </div>
        <div class="content-body">
            <div class="form-text"> 1. Vul je kaartnummer in </div>
            <div class="form-area">
                <b-field>
                    <b-input
                        :value="input_value"
                        type="text"
                        required
                        validation-message="Kaartnummer is minstens 17 cijfers lang"
                    >
                    </b-input>
                </b-field>
            </div>
            <div class="checkbox-area">
                <b-field>
                    <b-checkbox type="is-success"> Bewaar mijn kaartnummer </b-checkbox>
                </b-field>
            </div>
        </div>
    </div>
</template>

<script>
import PhoneAreaIcon from "./icons/phoneAreaIcon";
export default {
    name: "PhoneInput",
    components: {PhoneAreaIcon},
    data(){
        return{
            input_value:'6703 5656 5656 5656 5'
        }
    }
}
</script>

<style scoped lang="scss">
.first-component{
    border-radius: 10px;
    box-shadow: 0 2px 24px 0 rgb(0 0 0 / 10%);
    border: 1px solid #eaeaea;
}
.content-header{
    padding: 16px;
    background-color: #f6f6f6;
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
}
.content-body{
    padding: 16px;
    .form-text{
        font-size: 15px;
        font-weight: 700;
        color: #333;
        line-height: 1.6;
        margin: 16px 0;
    }
    .form-area{
        margin-bottom: 16px;
    }
}
</style>