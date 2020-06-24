<template>
    <div class="login-box--textbox">
        <i class="fa fa-user" aria-hidden="true"></i>
        <input type="text" v-bind:placeholder="placeHolderText"  />    
    </div>    
</template>
<script>
export default {
    props: ['placeHolderText']
    
}
</script>