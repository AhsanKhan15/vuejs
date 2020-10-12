<template>
<div>
    <!-- <h1>Hello from Home component </h1>
    <h2>{{data}}</h2>
        <h3>{{msg}}</h3>
        <button v-on:click ="hello('Ahsan')">Call hello function</button>
        <button v-on:click ='testing'>Call testing function</button>
<h1 v-if="show">Conditional Rendering</h1>
<h1 v-else>Conditional Rendering else block</h1>
        <button v-on:click ='display'>toggle element</button>  -->
<!-- <table border="1px">
    <tr>
        <td>Id</td>
        <td>Name</td>
        <td>Email</td>
    </tr>

     <tr v-for="user in users" :key="user.id">
        <td>{{user.id}}</td>
        <td>{{user.name}}</td>
        <td>{{user.email}}</td>
    </tr>
</table> -->
<h1>Home Component</h1>
<Users/>
<Products/>
</div>
</template>

<script>
 import Users from './Users'

 import Products from './Products'
export default {
    name:'Home',
    props:{
        data:String,
        msg:String
    },
    components:{
        Users,
        Products
    },
    methods:{
        hello(params){
            console.log("hello",params);
        },
        testing(){
            console.log("testing");
        },
        display(){
            this.show =!this.show
        }
    },
    data(){

    return {show:true,
    users:[
        {id:1,name:'peter',email:'gmail'},
        {id:2,name:'herry',email:'yah'},
        {id:3,name:'jerry',email:'del'},
        {id:4,name:'john',email:'alsjkd'},

    ]
    }
    }

}
</script>

<style scoped>
div{
    /* background-color: grey; */
    height: 500px;
}
</style>