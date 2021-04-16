<template>
  <div>
    <div class="header">
      <h1>My Website</h1>
      <p>{{subtitle}}</p>
    </div>

    <div class="topnav">
      <a href="#" @click="goTo('home')">Home</a>
      <a href="#" @click="goTo('otraPagina')">OTRA PAGINA</a>
      <a href="#" style="float:right">aaaa</a>
    </div>

    <home v-show="visiblePage=='home'"></home>
    <otra-pagina v-show="visiblePage=='otraPagina'"></otra-pagina>

    <div class="footer">
      <h2>Footer</h2>
    </div>
</div>
</template>

<script>
import Home from "./components/Home.vue"
import OtraPagina from "./components/OtraPagina.vue"

export default {
  name: 'App',
  data: function() {
    return {
      visiblePage: 'home',
      subtitle: 'A la grande le puse cuca'
    }
  },
  components: {
    Home, OtraPagina
  },
  methods: {
    goTo(pag) {
      this.visiblePage=pag;
    }
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}

body {
  font-family: Arial;
  padding: 10px;
  background: #f1f1f1;
}

/* Header/Blog Title */
.header {
  padding: 30px;
  text-align: center;
  background: white;
}

.header h1 {
  font-size: 50px;
}

/* Style the top navigation bar */
.topnav {
  overflow: hidden;
  background-color: #333;
}

/* Style the topnav links */
.topnav a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

/* Change color on hover */
.topnav a:hover {
  background-color: #ddd;
  color: black;
}

/* Create two unequal columns that floats next to each other */
/* Left column */
.leftcolumn {   
  float: left;
  width: 75%;
}

/* Right column */
.rightcolumn {
  float: left;
  width: 25%;
  background-color: #f1f1f1;
  padding-left: 20px;
}

/* Fake image */
.fakeimg {
  background-color: #aaa;
  width: 100%;
  padding: 20px;
}

/* Add a card effect for articles */
.card {
  background-color: white;
  padding: 20px;
  margin-top: 20px;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

/* Footer */
.footer {
  padding: 20px;
  text-align: center;
  background: #ddd;
  margin-top: 20px;
}

/* Responsive layout - when the screen is less than 800px wide, make the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 800px) {
  .leftcolumn, .rightcolumn {   
    width: 100%;
    padding: 0;
  }
}

/* Responsive layout - when the screen is less than 400px wide, make the navigation links stack on top of each other instead of next to each other */
@media screen and (max-width: 400px) {
  .topnav a {
    float: none;
    width: 100%;
  }
}
</style>
