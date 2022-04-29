<template>
    <!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>CSS Class App</title>

  </head>
  <body>
    <header>CSS Class App</header>
    <div class="container css--class--app">
      <div class="card text-center">
        <ul v-for="color in colorList" :key="color"  class="css--palette text-center row">
          <li @click="changeColor(color)" :style="color"></li>
        </ul>
        <div class="result-box" :style="ChangeItem()"></div>
      </div>
    </div>
  </body>
</html>

</template>
<script>
export default {
    data() {
        return {
            colorList: [
                
                {'background-color': 'red'},
                {'background-color': 'green'},
                {'background-color': 'blue'}
                
            ],
            selectedColor:{'background-color': 'green'}
         
      
        }
    },
    methods: {
        changeColor(color){
          this.selectedColor=color;
          return  this.ChangeItem(color);
          
        },
        ChangeItem(){
            return this.selectedColor;
        }

    }
}
</script>
<style >
@import '../assets/style.css';
</style>
