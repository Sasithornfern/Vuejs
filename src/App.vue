<template>
  <div id="app">
    <div class="container">
      <h2 align="center">Work Shop #1 Limit Message</h2>
      <hr>

      <div class="input-group">
        <div class="input-group-prepend">
        <!-- กำหนดให้จำนวนสูงสุดลบกับจำนวนข้อมูลที่คีย์เข้ามา-->
          <span class="input-group-text" v-text="max-message.length"></span>
        </div>

          <!--กำหนดให้พิมพ์ได้สูงสุดเท่ากับตัวแปร max-->
          <input type="text" class="form-control" v-model="message" :maxlength="max">
      </div>
    </div>
  </div>
</template>

<script>


export default {
  name: 'App',
  data() {
    return{
      message: '',
      max:20
    }
  }
  
}
</script>

<style scoped>
  *{
    margin:0;
    padding: 0;
    box-sizing: border-box;
  }

  .container{
  max-width:960px;
  margin: 0 auto;
  width:100%;
  }

  .container h2{
    margin:15px;
    color: gray;
  }

  .input-group{
    margin-top:15px;
  }

  .input-group-text{
    padding:10px;
  }
</style>
