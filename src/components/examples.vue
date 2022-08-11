<template>
  <div>
    <h1>firstname:{{firstname}}</h1>
    <h1>lastname:{{lastname}}</h1>
    <h1>{{details()}}</h1>
    <p>{{ foo }}</p>
    <button v-on:click="foo = 'baz'">Change it</button>
  </div>
</template>

<script>
export default {
    name: 'ExampleWord',
    data(){
    return{
        firstname: 'saikiran',
        lastname: '',
        foo: 'bar'
        }
    },
    beforeCreate(){
      console.log('beforeCreate');
    },
    created(){
      console.log('Created');
    },
    beforeMount(){
      console.log('beforeMount');
    },
    mounted(){
      console.log('Mounted');
    },
    beforeUpdate(){
      console.log('beforeUpdate');
    },
    updated(){
      console.log('updated');
    },
    beforeDestroy(){
      console.log('beforeDestroyed');
    },
    destroyed(){
      console.log('Destroyed');
    },
    methods:{
        details:function(){
            return 'My name is ' + this.firstname + ' ' + this.lastname
        }
    }
  };
</script>