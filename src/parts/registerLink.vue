<template>
    <div class="login-box--link">
        <input type="button"  @click="changeRegisterFlag" >Sign up</input>
    </div>
</template>
<script>
export default {
    methods: {
        changeRegisterFlag () {

            //this.$emit('부모 컴포넌트에서 리스닝할 이벤트 이름', 전달할 데이터)
            this.$emit('changeRegister', true);
            console.log("test");
        }
    }

    
}
</script>