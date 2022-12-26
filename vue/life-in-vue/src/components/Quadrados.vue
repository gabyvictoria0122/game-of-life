<template>
  <div>
    <h1>Gaby's Game of Life</h1>
    <hr style="margin-top: 0px; color: #d3d6da" />
    <div class="container-tabuleiro">
        <div class="tabuleiro">
            <div id="l1c1" class=" quadrado"></div>
            <div id="l1c2" class=" quadrado"></div>
            <div id="l1c3" class=" quadrado"></div>
            <div id="l1c4" class=" quadrado"></div>
            <div id="l1c5" class=" quadrado"></div>
        </div>

        <div class="tabuleiro">
            <div id="l2c1" class=" quadrado"></div>
            <div id="l2c2" class=" quadrado"></div>
            <div id="l2c3" class=" quadrado"></div>
            <div id="l2c4" class=" quadrado"></div>
            <div id="l2c5" class=" quadrado"></div>
        </div>
        <div class="tabuleiro">
            <div id="l3c1" class=" quadrado"></div>
            <div id="l3c2" class=" purple"></div>
            <div id="l3c3" class=" purple"></div>
            <div id="l3c4" class=" purple"></div>
            <div id="l3c5" class=" quadrado"></div>
        </div>
        <div class="tabuleiro">
            <div id="l4c1" class=" quadrado"></div>
            <div id="l4c2" class=" quadrado"></div>
            <div id="l4c3" class=" quadrado"></div>
            <div id="l4c4" class=" quadrado"></div>
            <div id="l4c5" class=" quadrado"></div>
        </div>
        <div class="tabuleiro">
            <div id="l5c1" class=" quadrado"></div>
            <div id="l5c2" class=" quadrado"></div>
            <div id="l5c3" class=" quadrado"></div>
            <div id="l5c4" class=" quadrado"></div>
            <div id="l5c5" class=" quadrado"></div>
        </div>
        <div class="tabuleiro">
            <div id="l6c1" class=" quadrado"></div>
            <div id="l6c2" class=" quadrado"></div>
            <div id="l6c3" class=" quadrado"></div>
            <div id="l6c4" class=" quadrado"></div>
            <div id="l6c5" class=" quadrado"></div>
        </div>
    </div>
    <button @click="test()"> Play </button>
  </div>
</template>

<script>
export default {
  name: 'QuadradosLife',
  methods: {
    test() {
      let clas = document.getElementsByClassName('purple');
      let fica = [...clas] 
      console.log("vamo ve", fica[0].id)
      for (let l = 1; l <= 6; l++){
        for(let c = 1; c <= 5; c++){
          let idTemp = `l${l}c${c}`
          let quanVizi = 0 
          
          for(let i = 0; i < fica.length; i++){
            if (fica[i].id == `l${l-1}c${c-1}`){
              quanVizi++; 
            }
            
            if (fica[i].id == `l${l-1}c${c}`){
              quanVizi++ 
            }
            
            if (fica[i].id == `l${l-1}c${c+1}`){
              quanVizi++ 
            }
            
            if (fica[i].id == `l${l}c${c+1}`){
              quanVizi++ 
            }
            
            if (fica[i].id == `l${l}c${c-1}`){
              quanVizi++ 
            }
            
            if (fica[i].id == `l${l+1}c${c-1}`){
              quanVizi++ 
            }
            
            if (fica[i].id == `l${l+1}c${c}`){
              quanVizi++ 
            }
            
            if (fica[i].id == `l${l+1}c${c+1}`){
              quanVizi++ 
            }
          } 
          
          if(document.getElementById(idTemp).classList == "quadrado" ){
            if(quanVizi === 3){
               document.getElementById(idTemp).classList.replace("quadrado", "purple")
            }
          } else if (quanVizi < 2 || quanVizi > 3) {
                document.getElementById(idTemp).classList.replace("purple", "quadrado")
          }
          
        }            
      }
    }
  }
  // } else if (2 <= quanVizi <= 3 ) {
  //   document.getElementById(idTemp).classList.add("purple")
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.quadrado {
  border: 2px solid #d3d6da;
  width: 38px;
  height: 38px;
  display: inline-block;
  margin: 0;
}

.purple {
  background-color: purple;
  border: 2px solid #d3d6da;
  width: 38px;
  height: 38px;
  display: inline-block;
  margin: 0;
}
</style>
