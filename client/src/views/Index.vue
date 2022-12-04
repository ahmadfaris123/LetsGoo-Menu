<script>
import json from '../assets/db.json'
      export default{
          data(){
              return{
                  myJson: json
              }
          }
      }
</script>

<template>
    <div class="container">
        <!-- Desktop -->
        <div class="d-none d-md-block">
            <div class="row">
                <div class="col-md-6">
                    <h2>Kini Memilih menu menjadi lebih mudah</h2><h3><strong>Coba Sekarang Juga</strong></h3>
                </div>
                <div class="col-md-6">
                    <img src="../assets/images/Hero.svg" width="50%"/>
                </div>
            </div>
        </div>

        <!-- Mobile -->
        <div class="d-sm-block d-md-none">
            <div class="row">
                <div class="col-md-6">
                    <img src="../assets/images/Hero.svg" width="50%"/>
                </div>
                <div class="col-md-6">
                    <h2>Kini Memilih menu menjadi lebih mudah</h2><h3><strong>Coba Sekarang Juga</strong></h3>
                </div>
            </div>
        </div>

        <div class="row mt-4">
            <h3>Products</h3>
            <div class="col-md-4">
                <div v-for="data in myJson">{{data}}</div>
            </div>
        </div>
    </div>
</template>