<script setup>
import {ref} from 'vue';


        // Singgle value menggunkan ref
        const count = ref(0);
        // non primitive menggunkan reactive
        // const counttt = reactive([]);

        function increase (){
            count.value++;
        }

        function decrease (){
            count.value--
        }


</script>








<!-- <script >

    export default{
        data(){
            return{
                count:1,
            }
        },
        methods:{
            increase(){
                this.count++;
            },
            decrease(){
                this.count--;
            }
        }
    }

</script> -->



<template>
       <main>
        <h1>Counter</h1>
        <span id="Value">{{ count }}</span>
        <div>
            <button  @click="decrease" id="decrease">-</button>
            <button  @click="increase">+</button>
        </div>
    </main>
</template>

<style scoped>

main {
    text-align: center;
    background-color: gray;
    padding: 20px;
    border-radius: 10px;
}

#Value{
    font-size: 54px;
}

button{
    margin: 0 5px;
    font-size: 16px;
    background-color: black;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 4px;
    cursor: pointer;
}



button:hover{
    background-color: aqua;
    color: black;
}

button:active{
    animation: pulse 0.5s linear;
}

@keyframes pulse {
    0%{
        transform: scale(1);
    }
    50%{
        transform: scale(1.1);
    }
    100%{
        transform: scale(1);
    }
}

</style>