<template>
  <div class="Test2">


  <Navbar/>

    <div id="summary">
      <div id="retailer-logo"><img alt="A beautiful cheesecake" class="logo-retailer" src="../assets/food1.jpeg"></div>
      <div class="left-part-summary">
        <div id="retailer-name"><h1>Retailer name</h1></div>
        <div id="retailer-descr">Has autem provincias, quas Orontes ambiens amnis imosque pedes Cassii montis illius celsi praetermeans funditur in Parthenium mare, Gnaeus Pompeius superato Tigrane regnis Armeniorum abstractas dicioni Romanae coniunxit.</div>
        <!--<div class="trustpilot-widget" data-locale="en-GB" data-template-id="539ad0ffdec7e10e686debd7" data-businessunit-id="592eadc50000ff0005a39280" data-style-height="350px" data-style-width="100%" data-theme="light" data-stars="1,2,3,4,5" data-schema-type="Organization"><a href="https://uk.trustpilot.com/review/howto.trustpilotdemo.com" target="_blank">Trustpilot</a></div>-->
        <div class="rate">
        <img alt="rate" class="star" src="../assets/star.svg">
        <img alt="rate" class="star" src="../assets/star.svg">
        <img alt="rate" class="star" src="../assets/star.svg">
        <img alt="rate" class="star" src="../assets/star.svg">
        <img alt="rate" class="star" src="../assets/star.svg">
        </div>
      </div>
    </div>
    <div id="suggested-categories">
      <div>
        <h2>Suggested Categories</h2>
      </div>
      <div class="align-categories">
        <div class="category-tile">
          <div><img alt="food category" class="food-category" src="../assets/food2.jpeg"></div>
          <div class="title-tile">Category</div>
        </div>
        <div class="category-tile">
        <div><img alt="food category" class="food-category" src="../assets/food3.jpeg"></div>
        <div class="title-tile">Category</div>
        </div>
        <div class="category-tile">
        <div><img alt="food category" class="food-category" src="../assets/food4.jpeg"></div>
          <div class="title-tile">Category</div>
        </div>
        <div class="category-tile">
        <div><img alt="food category" class="food-category" src="../assets/food5.jpeg"></div>
          <div class="title-tile">Category</div>
        </div>
        <div class="category-tile">
        <div><img alt="food category" class="food-category" src="../assets/food6.jpeg"></div>
          <div class="title-tile">Category</div>
        </div>
      </div>
    </div>
    <div id="top-brands">
      <div>
        <h2>Top Brands sold by Retailer Name</h2>
      </div>
      <div class="align-brand">
        <div class="brand-tile">
          <div><img alt="hilbert logo" class="brand-logo" src="../assets/hilbert-logo.jpg"></div>
        </div>
        <div class="brand-tile">
          <div><img alt="hilbert logo" class="brand-logo" src="../assets/hilbert-logo.jpg"></div>
        </div>
        <div class="brand-tile">
          <div><img alt="hilbert logo" class="brand-logo" src="../assets/hilbert-logo.jpg"></div>
        </div>
        <div class="brand-tile">
          <div><img alt="hilbert logo" class="brand-logo" src="../assets/hilbert-logo.jpg"></div>
        </div>
        <div class="brand-tile">
          <div><img alt="hilbert logo" class="brand-logo" src="../assets/hilbert-logo.jpg"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import Navbar from './Navbar.vue';

export default {
  name: 'app',
  components: {

    Navbar
    
  }
}

</script>

<style>


.Test2 {
    font-family: 'Montserrat', sans-serif;
    color: #393e43;
    margin: 10px;

}

.logo-retailer {
  margin-top: 50px;
  width: 550px;
  height: 400px;

}

#summary {
  display: flex;

}

#retailer-name {
  margin-top: 50px;
  font-size: 10px;
  font-weight: 500;

}

h2 {
  margin-top: 50px;
  font-size: 18px;
  font-weight: 700;

}

#retailer-descr {
  width: 1000px;
  margin-top: 30px;
  margin-bottom: 30px;
  color: #1e1e1e;
  font-size: 15px;
  font-family: "Helvetica", sans-serif;
  color: grey;
  

}

.left-part-summary {
  display: flex;
  flex-flow: column wrap;
  margin-left: 50px;

}

.food-category {
  width: 200px;
  height: 200px;
  border-radius: 10%;
  margin-bottom: 10px;

}

.align-categories, .align-brand {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
}

.title-tile {
  font-weight: 700;

}

.category-tile {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 30px;
}

.brand-tile {
  margin-top: 30px;
  margin-bottom: 50px;

}

.brand-logo {
  width: 200px;
  height: 200px;
}

.rate {
  display: flex;
}

.star {
  width: 20px;
  height: 20px;
}

@media screen and (max-width:1300px) {
#retailer-descr {
  width: 500px;

  }
}

@media screen and (max-width:1000px) {
  .logo-retailer {
    display: none;

}

  #summary {
    display: flex;
    align-content: center;
    flex-flow: column wrap;

}

#retailer-descr {
  width: 600px;

}

.left-part-summary {
  margin-left: 0;

}

.align-categories, .align-brand {
  justify-content: space-around;

  }
}

@media screen and (max-width:600px) {
  .logo-retailer {
    display: none;

}

#retailer-descr {
  width: 400px;

}

.align-categories, .align-brand {
  justify-content: space-around;
}

h2 {
  text-align: center;
  
  }
}  

</style>
