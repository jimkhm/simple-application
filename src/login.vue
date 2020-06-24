<template>
    <div class="login-box">
        <h1 v-if="!registerPageFlag" class="login-box--title">Login</h1>
        <h1 v-if="registerPageFlag" class="login-box--title">Register</h1>
        <namebox :placeHolderText="email" />
        <namebox v-if="registerPageFlag" 
            :placeHolderText="emailCheck" />
        <passwordbox :placeHolderText="passowrdBox" />
        <passwordbox v-if="registerPageFlag" 
            :placeHolderText="passwordCheckBox"/>
        <buttons v-if="!registerPageFlag" 
            :buttonName="signInButton"/>
        <buttons v-if="registerPageFlag" 
            :buttonName="registerButton"/>
        <register-link  v-if="!registerPageFlag" 
            @changeRegister="registerPageFlag=$event"/>
        <!-- @리스닝할 자식 컴포넌트의 이벤트 이름 ="동작" 여기서는 자식 컴포넌트에서 전달받은 데이터($event)를  registerPageFlag에 넣어주고 있다-->
    </div>
</template>
<script>
import namebox from './parts/namebox'
import passwordbox from './parts/passwordbox'
import buttons from './parts/buttons'
import registerLink from './parts/registerLink'

export default {
    components: {namebox, passwordbox, buttons, registerLink},

    data() {
        return {
            registerPageFlag: false,
            email: 'email',
            emailCheck: 'email check',
            signInButton: 'Sign in',
            signUpButton: 'Sign up',
            registerButton: 'register',
            passowrdBox: 'password',
            passwordCheckBox: 'password check'
        }
    },

    methods: {
    }
    
}
</script>