<template>
    <div class="component">
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <p>User name: {{switchName()}}</p>
        <button @click="resetName">Reset Name</button>
    </div>
</template>

<script>
    export default {

            props: ['name'],

           methods:{
                switchName: function () {

                    return this.name.split("").reverse().join("");
                },

               resetName: function () {
                   this.name="Maheeb";
                   this.$emit('namewasReset', this.name);
               }


           }




    }


</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
