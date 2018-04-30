<template>
<div id="app">
  <v-app>
    <v-content>
      <HelloWorld msg="Welcome to Your Vue.js App" />
      <br>
      <br>
      <img width="200" src="https://cdn.pixabay.com/photo/2017/05/12/15/16/hexagon-2307350_960_720.png">

      <div align="center">
        <v-container>

          <br>
          <br>

          <v-text-field style="width: 40%;" @keypress.enter="todo" id="myInput" name="input-2" label="Add Note's">
          </v-text-field>


          <v-btn href="/" type="button" name="button">Clear</v-btn>

          <v-container>

            <ol style="width: 30%;" id="myUL">

            </ol>
          </v-container>

        </v-container>
      </div>
    </v-content>
  </v-app>
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  methods: {
    todo: function() {
      var li = document.createElement("li");
      var inputValue = document.getElementById("myInput").value;
      var t = document.createTextNode(inputValue);
      li.appendChild(t);
      if (inputValue === '') {
        alert("You must write something!");
      } else {
        document.getElementById("myUL").appendChild(li);
      }
      document.getElementById("myInput").value = "";

      var span = document.createElement("SPAN");
      var txt = document.createTextNode("\u00D7");
      span.className = "close";
      span.appendChild(txt);
      li.appendChild(span);

      for (i = 0; i < close.length; i++) {
        close[i].onclick = function() {
          var div = this.parentElement;
          div.style.display = "none";
        }
      }
    }
  },
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  text-align: center;


}

#myInput {
  font-size: 24px;
}

li {
  font-size: 25px;
}
</style>
