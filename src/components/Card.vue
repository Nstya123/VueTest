<template>
  <div class="card">
    <div class="card" style="width: 18rem;">
      <img v-if="check" v-bind:src="foto" class="card-img-top" alt="...">
        <div class="card-body">
          <p class="card-text">{{msg}}</p>
          <p> {{descr}}</p>
          <button v-on:click="remonde" type="button" class="btn btn-primary">{{msgBtn}}</button>
        </div>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: 'Card',
  props: {
    msg: String,
    foto: String,
    descr: String
  },
  methods:{
    remonde(){
       if(this.check != true){
          this.msgBtn = "Спрятать",
          this.check = !this.check
       }else{
          this.msgBtn = "Показать",
          this.check = !this.check
       }
    }
  },
  data(){
    return{
      msgBtn: "Спрятать",
      check: true
    }
  }  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
