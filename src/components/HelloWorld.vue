<template>
  <div class="container">
    <h1>{{ msg }}</h1>
    
    <div class="testDiv" ref="testDiv">This is our test div!!</div>

    <div class="propertiesContainer">
        <h3> Different css properties for border and background: </h3>

        <div class="bgContainer">
          <button ref="b1" v-on:click="b1">background</button>
          <button ref="b2" v-on:click="b2">background-color</button>
          <button ref="b3" v-on:click="b3">background-image</button>
          <button ref="b4" v-on:click="b4">background-position</button>
          <button ref="b6" v-on:click="b6">background-size</button>
          <button ref="b5" v-on:click="b5">background-repeat</button>
          <button ref="b7" v-on:click="b7">background-clip</button>
          <button ref="b8" v-on:click="b8">background-origin</button>
        </div>
        <div class="borderContainer">
          <button ref="b9" v-on:click="b9">border</button>
          <button ref="b10" v-on:click="b10">border-color</button>
          <button ref="b12" v-on:click="b12">border-style</button>
          <button ref="b13" v-on:click="b13">border-width</button>
          <button ref="b14" v-on:click="b14">border-radius</button>
          <button ref="b11" v-on:click="b11">border-image</button>
        </div>
        <div class="etc">
          <button ref="b15" v-on:click="b15">box-shadow</button> 
          <button ref="b16" v-on:click="b16">outline</button>
        </div>
    </div>
  </div>
</template>

<script>
import Image1 from '@/assets/bg1.jpg';
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    b1: function () {
      this.$refs.testDiv.style.background = "#efefef"; //combination
    },
    b2: function () {
      this.$refs.testDiv.style.backgroundColor = '#000'; //color code
    },
    b3: function () {
      this.$refs.testDiv.style.backgroundImage = 'url(' + Image1 + ')'; //image url
    },
    b4: function () {
      this.$refs.testDiv.style.backgroundPosition = 'center'; //top, left, bottom, right, center, X Y
    },
    b5: function () {
      this.$refs.testDiv.style.backgroundRepeat = 'no-repeat'; //repeat, no-repeat, repeat-x, repeat-y, space, round
    },
    b6: function () {
      this.$refs.testDiv.style.backgroundSize = '30%'; //"100px 50px"; "cover"; "contain"
    },
    b7: function () {
      this.$refs.testDiv.style.backgroundClip = 'border-box'; //padding-box, content-box //image or color
    },
    b8: function () {
      this.$refs.testDiv.style.backgroundOrigin = 'content-box'; //padding-box, content-box //only image
    },
    b9: function () {
      this.$refs.testDiv.style.border = '2px solid rgb(7, 71, 166)'; //combination
    },
    b10: function () {
      this.$refs.testDiv.style.borderColor = '#00ff00'; //color code
    },
    b11: function () {
      this.$refs.testDiv.style.borderImage = 'url(' + Image1 + ') 30 repeat'; //source width outset repeat
    },
    b12: function () {
      this.$refs.testDiv.style.borderStyle = 'dashed'; // none, hidden, dotted, dashed, solid, double, groove, ridge, inset, outset 
    },
    b13: function () {
      this.$refs.testDiv.style.borderWidth = '8px'; // T R B L, thin/medium/thick
    },
    b14: function () {
      this.$refs.testDiv.style.borderRadius = '10px 40px 40px 10px'; // TL TR BR BL
    },
    b15: function () {
      this.$refs.testDiv.style.boxShadow = '3px 10px #FFC107, olive -1em 0px 4em'; //none | color code, X, Y, glowWidth
    },
    b16: function () {
      this.$refs.testDiv.style.outline = '5px dotted green'; // width style color
      //An outline is a line that is drawn around elements, outside the borders, to make the element "stand out".
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .testDiv {
    margin: 10vh 20vw;
    padding: 20px 50px;
    height: 200px;
  }
  .bgContainer {
    padding: 0px 20px;
  }
  div.bgContainer button {
    margin: 10px;
    width: 20vw;
  }

  .borderContainer {
    padding: 30px 30px 10px;;
  }
  div.borderContainer button {
    margin: 8px;
    width: 12vw;
  }

 .etc {
    padding: 30px;
  }
  div.etc button {
    margin: 10px;
    width: 25vw;
  }
</style>
