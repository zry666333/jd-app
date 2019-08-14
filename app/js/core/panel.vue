<template>
    <section :class="[panelClass,cname]">
        <h4>-{{title}}-</h4>
        <slot/>
    </section>
</template>

<script>
    export default {
        name: "panel",
        props:{
          cname:{
              type:String,
              default:''
          },
          title:String,
          default:''
        },
        data(){
            return {
                panelClass:'panel'
            }
        }
    }
</script>

<style scoped>
@import "../../css/element.scss";
    .panel{
        @include panel;
    }
</style>
