<template>
     <item :order-list="orderList" :cancel="cancel"></item>
</template>
<script>
    import item from './item';
    import { mapGetters, mapActions } from 'vuex';
    import {http} from '../../assets/public';
    export default{
        name:'GH_DZFDD',
        components:{
            item:item,
        },
        mounted(){
            this.set_order_zj({type:'Y011',status:'2'});
        },
        computed:{
            ...mapGetters({
                orderList:'getDzfdd_zj'
            })
        },
        methods:{
            ...mapActions(['set_order_zj']),
            cancel(){

            }
        }
    }
</script>