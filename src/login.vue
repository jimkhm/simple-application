<template>
    <div class="login-box">
        <h1 class="login-box--title">Login</h1>
        <namebox></namebox>
        <passwordbox></passwordbox>
        <buttons></buttons>
    </div>
</template>
<script>
import namebox from './parts/namebox'
import passwordbox from './parts/passwordbox'
import buttons from './parts/buttons'

export default {
    components: {namebox, passwordbox, buttons}
    
}
</script>