<template>
  <div>
    <h1>firstname:{{firstname}}</h1>
    <h1>lastname:{{lastname}}</h1>
    <h1>{{details()}}</h1>
    <p>{{ foo }}</p>
    <button v-on:click="foo = 'baz'">Change it</button>
    <p v-html="raw"></p>
    <p>{{raw}}</p>
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
    raw: '<h1>hello saikiran</h1>'
    }
  },
  methods:{
    details:function() {
        return this.firstname + " " + this.lastname;
    }
  }
}
</script>