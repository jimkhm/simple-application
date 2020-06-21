<template>
    <div class="login-box">
        <h1 class="login-box--title">Login</h1>
        <namebox></namebox>
        <namebox v-if="registerPageFlag"></namebox>
        <passwordbox></passwordbox>
        <passwordbox v-if="registerPageFlag"></passwordbox>
        <buttons></buttons>
        <register-link @changeRegister="registerPageFlag=$event"></register-link>
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
            registerPageFlag: false
        }
    },

    methods: {
        changeRegisterFlag() {
            this.registerLink = true;
        }
    }
    
}
</script>