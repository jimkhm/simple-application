<template>
    <div class="login-box--textbox">
        <i class="fa fa-lock" aria-hidden="true"></i>
        <input type="password" :placeholder="placeHolderText">
    </div>
</template>
<script>
export default {
    props: {
        placeHolderText: {
            type: String,
            required: true
        }
    }
    
}
</script>