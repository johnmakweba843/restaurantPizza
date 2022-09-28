<template> 
 <header v-bind:class = "heading"> 
  <h2 v-bind:style = "{fontSize:size + 'px' , 
fontWeight:weis , textAlign:align ,  
textTransform:trans , fontStyle:sty}">{{name}}</h2>
 </header>
 <main v-bind:class = "man"> 
   <h2 v-bind:class = "mama">{{toggle ()}}</h2> 
   <button v-bind:class = "papa" v-on:click = "paras = 'the world of burger'">Change Now</button>
 </main>  
  <h2 v-bind:id = "bata">{{tog}}</h2>
 <form v-bind:class = "niggas" @submit.prevent = "submitForm"> 
  <input type = "text" id = "username" placeholder = "username" v-model.trim.lazy = "formValues.username" /> 
  <textarea placeholder="userinfo"  v-bind:style = "{marginTop:mag + 'px'}" v-bind:class = "baby" id="userinfo" v-model = "formValues.userinfo" cols="30" rows="10"></textarea> 
   <select v-bind:class = "kaka"  id="country" v-model = "formValues.country"> 
     <option value="">country</option> 
     <option value="arfghastian">Arfghastian</option> 
     <option value="america">America</option> 
     <option value="south america">South America</option> 
     <option value="tanzania">Tanzania</option>
   </select>   
   <input v-bind:class = "dada" type="checkbox"  id="remoteWork" v-model = "formValues.remoteWork" true-value = "yes" false-value = "no" /> 
   <label v-bind:class = "dudu" for="remoteWork">accept terms and conditions</label>
   <button v-bind:class = "lol" onclick = "alert('you are hacked')" v-on:click = "name = 'burgers'">submit</button>
   
 </form>
</template> 

<script>
export default {
  data(){ 
    return{ 
        name:'restaurant', 
        size:18, 
        weis:800, 
        sty:'italic', 
        align:'center', 
        trans:'uppercase', 
        heading:'active', 
        man:'men', 
        paras:'the World of Pizza', 
        mama:'mother', 
        papa:'baba', 
        bog:'SignUp', 
        niggas:'search-box', 
        bata:'duck', 
        mag:20,  
        baby:'boy', 
        kaka:'bro', 
        dada:'sister', 
        dudu:'nyunyu', 
        lol:'bos',
        formValues:{ 
              username:'', 
              userinfo:'', 
              country:'', 
              remoteWork:"no"
        }
    }
  }, 
  methods:{ 
    toggle(){ 
      return this.paras
    }, 
    submitForm(){ 
      console.log("Form Values" , this.formValues)
    }
  }, 
  computed:{ 
     tog(){ 
        return `${this.bog}`
     }
  }
}
</script> 

<style lang = "css"> 
  *{ 
    margin:0; 
    padding:0; 
    box-sizing:border-box;  
    font-family:'Poppin',sans-serif;
  } 

  .active{ 
      width:100%; 
      padding:10px 15px; 
      background-color:aquamarine; 
      box-shadow:2px 8px 4px rgba(200 , 10 , 0.5);
  } 

  .men{ 
      display:flex; 
      align-items:center; 
      justify-content:center; 
      flex-direction:column;
  } 

  .mother{ 
      font-size:18px;  
      letter-spacing:1.2px;
      font-weight:800; 
      font-style:italic; 
      text-transform:uppercase;  
      margin-top:20px;
  } 

  .baba{ 
      width:100%; 
      max-width:200px; 
      padding:10px 15px; 
      border:none; 
      background:rgb(162, 31, 195); 
      color:#000; 
      font-size:18px; 
      font-weight:800; 
      font-style:italic; 
      text-transform:uppercase; 
      border-radius:1rem; 
      cursor:pointer; 
      transition:0.3s ease-in-out; 
      box-shadow:2px 8px 4px rgba(200 , 10 , 0.5);
      margin-top:10px;
  } 

  .baba:hover{ 
      color:#000; 
      background:#fff; 
      border:3px solid orange;
  } 

  .search-box{ 
       display:flex; 
       align-items:center; 
       justify-content:center; 
       flex-direction:column;
  } 

  input{ 
    outline:none;
  } 

  input[type = "text"]{ 
      width:100%; 
      padding:10px 15px; 
      background:aquamarine; 
      color:#000; 
      font-size:18px; 
      font-weight:800;  
      margin-top:30px;
      font-style:italic; 
      border-radius:8px; 
      border:none; 
      margin-left:5px;
  } 

  input[type = "text"]::placeholder{ 
      color:#000; 
      font-size:18px; 
      font-weight:800; 
      font-style:italic;
  } 

  #duck{ 
      font-size:18px; 
      font-weight:800; 
      font-style:italic; 
      text-transform:uppercase;
      text-align:center; 
      margin-top:30px;
  } 

  .boy{ 
      border:1px solid black;
      color:#000; 
      font-size:18px; 
      font-weight:800; 
      padding-left:20px; 
      font-style:italic;  
    }  

    .boy::placeholder{ 
       color:#000; 
       font-size:18px; 
       font-weight:800; 
       text-transform:capitalize; 
       font-style:italic; 
       letter-spacing:1.2px; 
       padding-left:20px;
    }

  .bro{ 
     width:100%; 
     max-width:200px; 
     padding:10px 15px; 
     border-radius:8px; 
     background:rgb(89, 212, 68); 
     color:#000; 
     font-size:18px;  
     text-transform:capitalize;
     font-weight:800; 
     font-style:italic; 
     margin-top:20px;
  } 

  .sister{
      width:20px; 
      height:20px; 
      border:2px solid black; 
      margin:10px 0; 

  } 

  .nyunyu{ 
     font-size:18px; 
     font-weight:800; 
     font-style:italic; 
     text-transform:capitalize; 
     color:#000; 

  } 

  .bos{ 
      width:100%; 
      max-width:200px; 
      padding:10px 15px; 
      border:none; 
      border-radius:1rem; 
      background:rgb(208, 203, 56); 
      color:#000; 
      font-size:18px; 
      font-weight:800; 
      font-style:italic; 
      text-transform:uppercase; 
      margin-top:20px; 
      margin-bottom:30px;  
      cursor:pointer; 
      transition:0.3s ease; 
      box-shadow:2px 8px 4px rgba(200 , 10 , 0.5);
  } 

  .bos:hover{ 
      color:#000; 
      background:#fff; 
      border:3px solid red;
  }
</style>