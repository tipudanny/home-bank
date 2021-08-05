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
                <input
                    class="custom-input-class"
                    v-model="input_value"
                    @input="checkCardNumber"
                    type="text"
                    required
                    maxlength="17"
                    placeholder=" . . . .   . . . .   . . . .   . . . . ."
                >
                </input>
                <div v-if="isError" class="error-message-show">Kaartnummer is minstens 17 cijfers lang</div>
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
            input_value:'',
            isError:false,
        }
    },
    methods:{
        checkCardNumber() {
            if (this.input_value.length === 17 ){
                this.isError = false;
                this.$emit('checkInputCardNumber', true)
            } else this.isError = true;
        }
    },
    watch: {
        input_value() {
            let realValue = this.input_value.replace(/[^\d-]/g,'')
            this.input_value = realValue
        }
    }
}
</script>

<style scoped lang="scss">
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
        .custom-input-class{
            height: 50px;
            width: 50%;
        }
        .error-message-show{
            color: #eb1700;
            font-size: 14px;
            font-weight: 500;
            margin-top: 10px;
        }
    }
}
</style>