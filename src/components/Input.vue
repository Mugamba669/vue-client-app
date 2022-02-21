<template lang="html">
    <div>
        <input type="text" v-model="input" @onchange="checkInput" placeholder="Provide the url here"/>
    </div>
</template>
<script>
export default {
    name:'Input',
    data(){
        return{
            input:""
        }
    },
    methods:{
        checkInput(){
                this.$emit('checkNewInput',this.input);
        }
    }
}
</script>
<style lang="scss" scoped>
    div{
       
        input{
            width:200px;
            margin: 10px;
            outline: none;
            padding: 10px;
            border-radius: 5px;
            border: 1px solid #63ccdd;
            font: 200 18px Ubuntu,Arial;
            
        }
    }
</style>