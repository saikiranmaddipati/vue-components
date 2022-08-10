<template>
  <div>
    <h1>firstname:{{firstname}}</h1>
    <h1>lastname:{{lastname}}</h1>
    <h1>{{details()}}</h1>
  </div>
</template>

<script>
export default {
    name: 'ExampleWord',
    data(){
    return{
        firstname: 'saikiran',
        lastname: 'maddipati'
        }
    },
    methods:{
        details:function(){
            return 'My name is ' + this.firstname + ' ' + this.lastname
        }
    }
  };
</script>