<template>
	<body>
		<div class="nui-wrapper">
      <div class='popup-thing'>
        <h1 id="header">Tuner Chip</h1>
        <div>
            <span id="boost">Boost</span>
            <input type="range" min="1" max="5" value="3" id="boost-slider"/>
        </div>

        <div>
            <span id="acceleration">Acceleration</span>
            <input type="range" min="1" max="5" value="3" id="acc-slider"/>
        </div>

        <div>
            <span id="gear">Gear</span>
            <input type="range" min="1" max="5" value="3" id="g-slider"/>
        </div>

        <div>
            <span id="breaks">Breaking</span>
            <input type="range" min="1" max="5" value="3" id="b-slider"/>
        </div>

        <div>
            <span id="dtrain">Drivetrain</span>
            <input type="range" min="1" max="5" value="3" id="d-slider"/>
        </div>

        <div class = 'button1'>
          <button id = 'save'>Set</button>
        </div>

        <div class = 'button2'>
          <button id = 'reset'>Reset</button>
        </div>
        
      </div>
      
    </div>
	</body>
</template>

<script>
//import Nui from "./utils/Nui";
//import testData from "./utils/testData"
//import NavBar from "./components/NavBar.vue";
//import { mapState, mapActions } from "vuex";
export default {
  name: "app",

  window
  

  

};

window.addEventListener('message', function(event) {
    var item = event.data;
    if (item.showUI) {
        $('.app').show();
    } else {
        $('.app').hide();
    }
});


  
</script>

<style>
.nui-wrapper {
  text-align: center;
  height: 90%;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 30px;
}

pre {
  counter-reset:line-numbering;
  background:#60210993;
  padding:12px 0px 14px 0;
  line-height:140%;
}

.popup-thing {
  background: #1c3554;
  border-radius: 10px;
  box-shadow: #1a1a1b;
  width: 300px;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: -20px;
}

h1 {

  display: block;
  margin-bottom: 345px;

}

#boost-slider {
  display: block;
  position: absolute;
  width: 195px;
  font-size: bold;
  align-items: center;
  margin-left: -42px;
  margin-top: -90px;
}

#acc-slider {
  display: block;
  position: absolute;
  width: 195px;
  font-size: bold;
  align-items: center;
  margin-left: -42px;
  margin-top: -48px;
}


#g-slider {
  display: block;
  position: absolute;
  width: 195px;
  font-size: bold;
  align-items: center;
  margin-left: -42px;
  margin-top: -5px;
}

#b-slider {
  display: block;
  position: absolute;
  width: 195px;
  font-size: bold;
  align-items: center;
  margin-left: -42px;
  margin-top: 40px;
}


#d-slider {
  display: block;
  position: absolute;
  width: 195px;
  font-size: bold;
  align-items: center;
  margin-left: -42px;
  margin-top: 80px;
}


#header {
  position: absolute;

  text-align: center;
  color: #ffffff;
  margin-left: 10px;
}

#header:hover {
  

  
  color: #1a8c5e;
  
}

#boost {
  position: absolute;

  display: block;
  color: #ffffff;
  font-size: bold;
  margin-left: 37px;
  margin-top: -120px;
}


#acceleration {
  position: absolute;

  display: block;
  color: #ffffff;
  font-size: bold;
  margin-left: 16px;
  margin-top: -73px;
}

#gear {
  position: absolute;

  display: block;
  color: #ffffff;
  font-size: bold;
  margin-left: 40px;
  margin-top: -27px;
}

#breaks {
  position: absolute;

  display: block;
  color: #ffffff;
  font-size: bold;
  margin-left: 27px;
  margin-top: 16px;
}


#dtrain {
  position: absolute;

  display: block;
  color: #ffffff;
  font-size: bold;
  margin-left:25px;
  margin-top: 60px;
}










#save {
  position: relative;
  margin-bottom: -301px;
  margin-left: -35px;
  background-color: #1c3554;
  border-style: inset;
  border: none;
  text-align: center;

}

#save:hover {
  transition: 10ms;
  background-color: #0e7441;
  color: #1a1a1b;
}

#reset:hover {
  transition: 10ms;
  background-color: #0e7441;
  color: #1a1a1b;
}

#reset {
  position: relative;
  margin-bottom: -1px;
  margin-left: 19px;
  background-color: #1c3554;
  border-style: inset;
  border: none;
  text-align: center;

}

#save, #reset {
  margin-left: 10px;
}





#save {
  position: relative;
  background-color: #4c72af;
  border: none;
  font-size: 18px;
  color: #FFFFFF;
  width: 18;
  text-align: center;
  transition-duration: 0.4s;
  text-decoration: none;
  overflow: hidden;
  cursor: pointer;
  box-shadow: #1a1a1b;
}


#reset {
  position: relative;
  background-color: #4c72af;
  border: none;
  font-size: 18px;
  color: #FFFFFF;
  width: 18;
  text-align: center;
  transition-duration: 0.4s;
  text-decoration: none;
  overflow: hidden;
  cursor: pointer;
  box-shadow: #1a1a1b;
}







.button1 {
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 30px;
}


.button2 {
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: -300px;
}



input :hover {
  background-color: #0e7441;
}


@media screen and (-webkit-min-device-pixel-ratio:0) {
    input[type='range'] {
      overflow: hidden;
      width: 20px;
      height: 8px;
      -webkit-appearance: none;
      background-color: #2f9b5c;
    }
    
    input[type='range']::-webkit-slider-runnable-track {
      height: 10px;
      -webkit-appearance: none;
      color: #13bba4;
      margin-top: -1px;
    }
    
    input[type='range']::-webkit-slider-thumb {
      width: 10px;
      -webkit-appearance: none;
      height: 10px;
      cursor: ew-resize;
      background: #42f103;
      box-shadow: -80px 0 0 80px #43e5f7;
    }

}












</style>
