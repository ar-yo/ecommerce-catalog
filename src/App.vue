<template>
  <ProdukKatalog/>
</template>

<script>
import ProdukKatalog from './components/ProdukKatalog.vue'
export default {
  name: 'App',
  components: {
    ProdukKatalog
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.background-wanita{
  position: absolute;
  width: 100%;
  height: 408px;
  left: 0px;
  top: 0px;
  background: #FDE2FF;
}

.background-pria{
  position: absolute;
  width: 100%;
  height: 408px;
  left: 0px;
  top: 0px;
  background: #D6E6FF;;
}

.background-unavailable{
  position: absolute;
  width: 100%;
  height: 408px;
  left: 0px;
  top: 0px;
  background: #D8D7D7;
;
}

.card{
  position: absolute;
  width: 1034px;
  height: 490px;
  left: 12%;
  top: 80px;
  margin-left: 25px;
  background: #FFFFFF;
  box-shadow: 0px 4px 4px rgba(58, 58, 58, 0.74);
  border-radius: 10px;

}

.product-title{
  width: 548px;
  height: 68px;
  left: 400px;
  text-align:left ;
}

.product-title-wanita{
  position: absolute;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 34px;
  text-align:left ;
  font: #720060;
}

.product-title-pria{
  position: absolute;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 34px;
  text-align:left ;
  color:  #002772;
}

.product-title-unavailable{
 display: none;
}

.card{
  position: absolute;
  width: 1034px;
  height: 480px;
  left: 147px;
  background: #FFFFFF;
  box-shadow: 0px 4px 4px rgba(104, 104, 104, 0.26);
  border-radius: 10px;
}

.product-img{
  margin-right: 640px;
  margin-top: 40px;
}

.img-detail{
  width: 280px;
}

.product-title{
  position: absolute;
  width: 548px;
  height: 68px;
  left: 400px;
  top: 12px;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 34px;
  color: #720060;
}

.product-category{
  position: absolute;
  left: 400px;
  top: 120px;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  color: #3F3F3F;
}

.product-rating{
  position: absolute;
  width: 45px;
  height: 22px;
  left: 730px;
  top: 120px;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  color: #3F3F3F;
}

.wanita-rating{
  position: absolute;
  width: 45px;
  height: 22px;
  right: -120px;
  top: 0px;

}

.pria-rating{
  position: absolute;
  width: 45px;
  height: 22px;
  right: -120px;
  top: 0px;
}

.wanita-rating-1{
  position: absolute;
  width: 18px;
  height: 18px;
  left: -330px;
  top: 120px;
  background: #720060;
  border-radius: 10px;
}

.wanita-rating-2{
  position: absolute;
  width: 18px;
  height: 18px;
  left: -310px;
  top: 120px;
  background: #720060;
  border-radius: 10px;
}

.wanita-rating-3{
  position: absolute;
  width: 18px;
  height: 18px;
  left: -290px;
  top: 120px;
  background: #720060;
  border-radius: 10px;
}

.wanita-rating-4{
  box-sizing: border-box;
  position: absolute;
  width: 18px;
  height: 18px;
  left: -270px;
  top: 120px;
  background: #FFFFFF;
  border: 1px solid #720060;
  border-radius: 10px;
}

.wanita-rating-5{
  box-sizing: border-box;
  position: absolute;
  width: 18px;
  height: 18px;
  left: -250px;
  top: 120px;
  background: #FFFFFF;
  border: 1px solid #720060;
  border-radius: 10px;
}


.pria-rating-1{
  position: absolute;
  width: 18px;
  height: 18px;
  left: -330px;
  top: 120px;
  background: #002772;
  border-radius: 10px;
}

.pria-rating-2{
  position: absolute;
  width: 18px;
  height: 18px;
  left: -310px;
  top: 120px;
  background: #002772;
  border-radius: 10px;
}

.pria-rating-3{
  position: absolute;
  width: 18px;
  height: 18px;
  left: -290px;
  top: 120px;
  background: #002772;
  border-radius: 10px;
}

.pria-rating-4{
  box-sizing: border-box;
  position: absolute;
  width: 18px;
  height: 18px;
  left: -270px;
  top: 120px;
  background: #FFFFFF;
  border: 1px solid #002772;
  border-radius: 10px;
}

.pria-rating-5{
  box-sizing: border-box;
  position: absolute;
  width: 18px;
  height: 18px;
  left: -250px;
  top: 120px;
  background: #FFFFFF;
  border: 1px solid #002772;
  border-radius: 10px;
}

.product-description{
  position: absolute;
  width: 517px; 
  right: -56px;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  text-align:left ;
  line-height: 24px;
  margin-top: 3px;
  color: #1E1E1E;
  top:80px;
  left:200px;
}


.price-wanita{
  position: absolute;
  width: 97px;
  left: 398px;
  top: 360px;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 34px;
  /* identical to box height */
  color: #720060;
  }

  .price-pria{
  position: absolute;
  width: 97px;
  left: 398px;
  top: 360px;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 34px;
  /* identical to box height */
  color: #002772;
  }

.button-wanita-buy{
  box-sizing: border-box;
  position: absolute;
  width: 259px;
  height: 42px;
  left: 346px;
  top: 405px;
  margin-left:54px;
  color: #FFFFFF;
  background: #720060;;
  border: 3px solid #720060;
  font-family: 'Inter';
  font-size: 20px;
  border-radius: 4px;
  }

  .button-pria-buy{
  box-sizing: border-box;
  position: absolute;
  width: 259px;
  height: 42px;
  left: 346px;
  top: 405px;
  margin-left:54px;
  color: #FFFFFF;
  background: #002772;;
  border: 3px solid #002772;
  font-family: 'Inter';
  font-size: 20px;
  border-radius: 4px;
  }

  .button-wanita-next{
  box-sizing: border-box;
  position: absolute;
  width: 259px;
  height: 42px;
  left: 670px;
  top: 405px;
  background: #FFFFFF;
  border: 3px solid #720060;
  font-family: 'Inter';
  font-size: 20px;
  color:#720060;
  border-radius: 4px;
  }
  
  .button-pria-next{
  box-sizing: border-box;
  position: absolute;
  width: 259px;
  height: 42px;
  left: 670px;
  top: 405px;
  background: #FFFFFF;
  border: 3px solid #002772;
  font-family: 'Inter';
  font-size: 20px;
  color:#002772;
  border-radius: 4px;
  }

  .button-unavailable{
  box-sizing: border-box;
  position: absolute;
  width: 465px;
  height: 42px;
  left: 282px;
  top: 265px;
  font-family: 'Inter';
  font-size: 20px;
  background: #FFFFFF;
  border: 3px solid #000000;
  border-radius: 4px;
  }
  
.line-top{
  margin-top:70px;
  margin-left: 200px;
  width: 530px;
}

.line-buttom{
  margin-top: 190px;
  width: 530px;
  margin-left: 200px;
}

.img-unavailable{
  position: absolute;
  background-image: url('./assets/bg.svg');
  font-family: 'Inter';
  margin-left: 6%;
  width: 95%;
  height: 90%;
}

.text-unavailable{
  position: absolute;
  width: 332px;
  height: 24px;
  left: 348px;
  top: 210px;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #000000;

}

.button-sad{
  box-sizing: border-box;
  position: absolute;
  width: 465px;
  height: 42px;
  left: 280px;
  top: 260px;
  text-align: center;
  background: #FFFFFF;
  border: 3px solid #000000;
  font-family: 'Inter';
  font-size: 20px;
  color:#000000;
  border-radius: 4px;
}

</style>

