<template >
    <div>
      <div class="container w-50">
        <div class="card">
          <div class="card-body">
            <div class="card-title">
              <div class="d-flex justify-content-between">
            <div>
            <select  v-model="surahNumber" @change="getSpecificSura()" class="form-select" aria-label="Default select example">
              <option selected value="" disabled>Select Ayah</option>
              <option v-for="(surah,index) in suras" :key="index"  :value="surah.number">{{ surah.name }}-{{ surah.englishName }}</option>
            </select>
          </div>
            <div>
              Hello
            </div>
            <div>
              <select class="form-select" aria-label="Default select example">
                <option>Select Ayah</option>
                <option v-for="(surah,index) in suras" :key="index" value="1"> </option>
              </select>
            </div>
          </div>
          </div>

          <p v-for="ayah in ayahs">
            {{ ayah.text }}
          </p>
          
          </div>
        </div>
        
      </div>
     
    </div>
 </template>
 
 <script>
 import axios from "axios"
 export default {
     data(){
       return {
           ayahs:[],
           suras:[],
           currentSura:[],
           surahNumber:'',
       }
     },
     mounted() {
        axios.get('http://api.alquran.cloud/v1/surah')
        .then((res)=>{
          this.suras = res.data.data
        })
     },
     methods:{
       getSpecificSura(){
        axios.get('http://api.alquran.cloud/v1/surah/'+this.surahNumber)
        .then((res)=>{
            // console.log(res.data.data.ayahs);
            this.ayahs = res.data.data.ayahs
        })
       }
     }
     
 }
 </script>
  
 <style>
 
 </style>