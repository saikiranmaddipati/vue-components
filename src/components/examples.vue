<template>
  <div>
    <h1>firstname:{{firstname}}</h1>
    <h1>lastname:{{lastname}}</h1>
    <h1>{{details()}}</h1>
    <p>{{ foo }}</p>
    <button v-on:click="foo = 'baz'">Change it</button>
    <p v-html="raw"></p>
    <p>{{raw}}</p>
    <h1>Methods</h1>
    <button v-on:click="a++">Add to A</button>
    <button v-on:click="b++">Add to B</button>
    <p>Age + A = {{ addToAcomputed }}</p>
    <p>Age + B = {{ addToBcomputed }}</p>
  </div>
</template>

<script>
export default {
    name: 'ExampleWord',
    data(){
    return{
        firstname: 'saikiran',
        lastname: 'maddipati',
        foo: 'bar',
        raw: '<h1>hello saikiran</h1>',
        counterComputed: 0,
        counterMethod: 0,
        a: 0,
        b: 0,
        age: 20
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
    computed: {
        addToAcomputed: function(){
            console.log('addToAcomputed');
            return this.a + this.age;
        },
        addToBcomputed: function(){
            console.log('addToBcomputed');
            return this.b + this.age;
        }
    }
}
</script>