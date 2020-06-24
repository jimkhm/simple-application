<template>
    <input type="button" class="login-box--btn" :value="buttonName">
</template>
<script>
export default {
    props: {
        buttonName: String    
    }
}
</script>