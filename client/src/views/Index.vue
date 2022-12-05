<script>
import axios from 'axios'
import { onMounted, ref } from 'vue'
      export default{
        setup() {
            let data = ref([]);

            onMounted(() => {
                axios.get('http://localhost:3000/products')
                .then((result) => {
                    // console.log(result)
                    data.value = result.data
                }).catch((err) => {
                    console.log(err.response)
                });
            });

            return {
                data
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
            <div class="col-md-3 mt-4" v-for="datas in data">
                <div class="card shadow" style="width: 18rem;">
                    <!-- <img src="..." class="card-img-top" alt="..."> -->
                    <div class="card-body">
                      <h5 class="card-title">{{ datas.nama }}</h5>
                      <p class="card-text">Harga : Rp.{{ datas.harga }}</p>
                      <a href="#" class="btn btn-primary">Beli</a>
                    </div>
                  </div>
            </div>
        </div>
    </div>
</template>