<template lang="">
  <div id="app">

    <div id="loader" class="center"></div>

    <div class="container">
      <div class="container-bg">
        <span class="background-wanita" v-if="nextwanita"></span>
        <span class="background-pria" v-if="nextpria" ></span>
        <span class="background-unavailable" v-if="nextAnavailable"></span>
      </div>

      <div class="card">
        <div class="product-img">
          <img class="img-detail wanita" v-if="nextwanita"  :src="products.image" alt="baju" >
          <img class="img-detail pria" v-if="nextpria" :src="products.image" alt="baju">
          <p class="img-unavailable" v-if="nextAnavailable"></p>
          <p class="text-unavailable" v-if="nextAnavailable">This product is unavailable to show</p>
        </div>

        <div class="product-title">
          <p class="product-title-wanita" v-if="nextwanita">{{products.title}}</p>
          <p class="product-title-pria" v-if="nextpria">{{ products.title}}</p>
          <p class="product-title-unavailable" v-if="nextAnavailable"></p>
        </div>

        <div class="product-category" >
          <span v-if="nextwanita">{{products.category}}</span>
          <span v-if="nextpria">{{products.category}}</span>
          <span v-if="nextAnavailable"></span>
        </div>

        <div class="product-rating">
          <span v-if="nextwanita" >{{products.rating.rate}}/5</span>
          <span v-if="nextpria" >{{products.rating.rate}}/5</span>
        </div>

        <div class="wanita-rating" v-if="nextwanita">
          <span class="wanita-rating-1" ></span>
          <span class="wanita-rating-2" ></span>
          <span class="wanita-rating-3" ></span>
          <span class="wanita-rating-4" ></span>
          <span class="wanita-rating-5" ></span>
        </div>

        <div class="pria-rating" v-if="nextpria">
          <span class="pria-rating-1" ></span>
          <span class="pria-rating-2" ></span>
          <span class="pria-rating-3" ></span>
          <span class="pria-rating-4" ></span>
          <span class="pria-rating-5" ></span>
        </div>

        <div class="product-description">
          <hr class="line-top" v-if="nextwanita">
          <hr class="line-top" v-if="nextpria">
          <p  class="product-description" v-if="nextwanita">{{products.description}}</p>
          <p  class="product-description" v-if="nextpria">{{products.description}}</p>
          <p class="product-description" v-if="nextAnavailable"></p>
          <hr class="line-buttom" v-if="nextwanita">
          <hr class="line-buttom" v-if="nextpria">
        </div>

        <div class="product-price">
          <span class="price-wanita" v-if="nextwanita">${{products.price}}</span>
          <span class="price-pria" v-if="nextpria">${{products.price}}</span>
        </div>

        <div class="button">
          <button class="button-wanita-buy" v-if="nextwanita">Buy Now</button>
          <button class="button-pria-buy" v-if="nextpria">Buy Now</button>
          <button class="button-wanita-next" v-if="nextwanita" v-on:click="wanita">Next Product</button>
          <button class="button-pria-next" v-if="nextpria" v-on:click="pria">Next Product</button>
          <button class="button-unavailable" v-if="nextAnavailable" v-on:click="unavailable">Next Product</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data () {
    return {
      nextwanita: true,
      nextpria:false,
			nextAnavailable: false,
      products: '',
    }
  },
  
  beforeCreate() {
    let api = "https://fakestoreapi.com/products/16"
    fetch (api)
    .then((result) => result.json())
    .then((data) => (this.products = data))
},

  methods: {  

    async wanita(){
      const api = await fetch ('https://fakestoreapi.com/products/4');
      const response = await api.json()
      const data = response 
      console.log(this.products = data);

      this.nextAnavailable = false;
      this.nextwanita = false;
      this.nextpria = true;
    },

    async pria(){
      const api = await fetch ('https://fakestoreapi.com/products/16');
      const response = await api.json()
      const data = response 
      console.log(this.products = data);

      this.nextAnavailable = true;
      this.nextwanita = false;
      this.nextpria = false;
    },

    unavailable(){
      this.nextpria = false;
      this.nextwanita = true;
      this.nextAnavailable = false;
      
    }
  }
}
</script>




