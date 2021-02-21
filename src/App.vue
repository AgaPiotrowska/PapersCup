<template>
  <div id="app">
      <header class="header">
          <div class="container">
              <h1><strong>Paper</strong> Cups</h1>
              <h3>Best paper cups ever!</h3>
              <p>Solid white so they match anything, these <strong>paper hot cups </strong> are perfect for hot beverages.<br/>
                 </p>
              <Button/>
              <PaperCupPicture/>
          </div>
      </header>
      <section class="pageSection">
          <div class="container">
              <div class="sectionTitle">
                  <h1>Paper Cup</h1>
                  <h2>HQ Materials</h2>
              </div>
              <p>
                  Lorem ipsum dolor sit amet, <a href="#">consectetur</a> adipiscing
                  elit. Aliquam cursus quam neque, nec auctor ligula commodo ac. Sed
                  maximus mi id hendrerit pellentesque. Quisque porttitor, risus sed
                  volutpat tincidunt, odio nisi laoreet purus, sit amet ornare nisi
                  ligula ac odio. Sed feugiat aliquam est, non ultricies libero.
                  Interdum et malesuada fames ac ante ipsum primis in faucibus. Proin
                  quis congue tortor. In ante massa, auctor et diam sit amet, commodo
                  ornare libero. Fusce suscipit sem neque, at convallis dui cursus non.
                  Curabitur cursus tempor rutrum
              </p>
          </div>
      </section>
      <section class="column">
          <div class="left">
              <PaperCupPicture/>
          </div>
          <div class="right">
              <h2><strong>See what's included</strong></h2>
                      <ul>
                          <li v-for="item in items" :key="item">{{item}}</li>
                      </ul>
              <Button/>
          </div>
      </section>
      <section class="requirements">
          <h2>Requirements</h2>
          <p>Adobe Photoshop CS4+</p>
          <img src="assets/ps.png" alt="Adobe Photoshop" width="200" height="200">
      </section>
      <section class="features">
          <h2>Features</h2>
          <p>We are here for you</p>
          <div class="demos">
              <div class="demos-inner">
                  <div class="item" v-for="feature in features" :key="feature.header">
                      <div class="demo1" width="100%"> {{ feature.icon }}
                          <h4>{{ feature.header }}</h4>
                          <div class="item-text">
                              {{ feature.text }}
                          </div>
                      </div>
                 </div>
              </div>
          </div>
      </section>
      <div class="do-you">
          <h5>Do you like PAPER CUP?</h5>
          <div class="btn-black"><Button/></div>
      </div>
      <section class="form">
          <h2>Contact me</h2>
          <p>For any questions fill in the form below & we will get back to you ASAP!</p>
          <form class="form-data">
              <div class="input1"><input type="text" placeholder="Your name"></div>
              <div class="input2"><input type="email" placeholder="Your email"></div>
              <div class="input3"><textarea type="text" placeholder="Your message"></textarea></div>
              <div class="btn-full-width btn-black"><a href="#" class="btn"><span>Send message</span></a></div>
          </form>
      </section>
      <section class="final">
          <h5>Copyright 2020</h5>
          <div class="icons">
              <div class="icon"><img src="assets/facebook.png" alt="facebook" width="25px"></div>
              <div class="icon"><img src="assets/youtube.png" alt="youtube" width="25px"></div>
              <div class="icon"><img src="assets/twitter.png" alt="twitter" width="25px"></div>
          </div>
      </section>
  </div>
</template>

<script>
import Button from './components/Button.vue'
import PaperCupPicture from "./components/PaperCupPicture";
import Demo1 from './assets/demo1.jpg';
import Demo2 from './assets/demo2.jpg';
import Demo3 from './assets/demo3.jpg';

export default {
  name: 'App',
  components: {
      PaperCupPicture,
   Button
  },
    data() {
      return {
          items: [
              "Changeable lid color",
              "Changeable cup color",
              "Changeable cap label via smart object",
              "On/Off shadows",
              "On/Off specular",
              "Changeable background",
              "High resolution 3000 x 1875px",
          ],

          features: [
              { icon: 'Demo1', header: "Organized layers", text: "Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit."},
              {icon: 'Demo2', header: "Smart objects", text: "Suspendisse id justo auctor, hendrerit velit nec, consectetur libero."},
              {icon: 'Demo3', header: "Transparent bg", text: "Morbi fringilla malesuada purus quis sodales. Nunc hendrerit placerat pharetra. Ut id est orci."},
          ],
          Demo1,
          Demo2,
          Demo3,
        }
    }
}
</script>

<style>
$font-stack: Helvetica, sans-serif;
$primary-color: #2a3030;

body {
    font: 100% $font-stack;
    color: $primary-color;
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}

a {
    color: #fc3;
}

a:hover {
    text-decoration: underline;
}

.header {
    height: 800px;
    padding-top: 70px;
    background: #fc3;
}

#mainHeader h1 {
    font-size: 70px;
    font-weight: 300;
}

#mainHeader h3 {
    margin: 10px 0 20px 0;
    font-size: 30px;
    font-weight: 600;
}

#mainHeader p {
    margin-bottom: 40px;
}

.btn {
    display: inline-block;
    height: 48px;
    line-height: 48px;
    padding: 0 35px;
    font-size: 14px;
    color: #000;
    background: #fff;
    border-radius: 4px;
    box-shadow: 0 4px 0 #e0e0e0;
    text-transform: uppercase;
    font-weight: 700;
}

.btn:hover {
    text-decoration: none;
    background: #ebebeb;
}

.btn span {
    font-size: 1.25em;
    padding-right: 5px;
}

.container {
    width: 800px;
    margin: 0 auto;
    text-align: center;
    margin-bottom: 60px;
}

.sectionTitle h1 {
    font-size: 38px;
    font-weight: 400;
    text-transform: uppercase;
}

.sectionTitle h2 {
    font-size: 21px;
    line-height: 28px;
    font-weight: 300;
    margin-bottom: 60px;
}

.pageSection {
    margin: 60px 0;
}

.column {
    display: flex;
}

.left {
    background-color: #63d0ee;
    width: 50%;
    padding: 30px;
}

.right {
    background-color: #fc3;
    background-size: cover;
    padding: 60px;
    width: 50%;
}

.right h2 {
    margin-bottom: 20px;
    font-size: 18px;
}

ul {
    padding-bottom: 20px;
}

.requirements {
    background-color: #e1e4e4;
    background-size: cover;
    padding: 60px 0px;
    text-align: center;
}

.requirements h2 {
    text-transform: uppercase;
    font-size: 38px;
    font-weight: 400;
}

.requirements p {
    font-size: 21px;
    font-weight: 300;
}

.requirements img {
    margin-top: 60px;
}

.features {
    background-color: white;
    background-size: cover;
    padding: 60px 0;
    text-align: center;
}

.features h2 {
    text-transform: uppercase;
    font-size: 38px;
    font-weight: 400;
}

.features p {
    font-size: 21px;
    font-weight: 300;
    padding-bottom: 60px;
}

.demos {
    display: flex;
    justify-content: center;
}

.demos-inner {
    padding: 0 40px 15px 40px;
    display: flex;
    justify-content: center;
    width: 800px;
    overflow: hidden;
}

.demo1, .demo2, .demo3 {
    border-radius: 50%;
    border: 5px solid #fc3;
}

.demos .demos-inner .item {
    margin-left: 80px;
    overflow-x: hidden;
    flex: 1 0 0;
}

.demos .demos-inner .item:first-child {
    margin-left: 0;
}

.demos-inner h4 {
    text-transform: uppercase;
    padding-top: 15px;
}

.do-you {
    background-color: black;
    color: white;
    padding: 60px 0;
    display: flex;
    justify-content: center;
}

.do-you h5 {
    padding-right: 40px;
    font-size: 26px;
}

.btn-black .btn {
    background-color: #fc3;
    color: black;
    box-shadow: 0 4px 0 #dfae08;
}

.form {
    padding: 60px 0 60px 0;
    background-color: white;
    background-size: cover;
    text-align: center;
    display: flex;
    align-items: center;
    flex-direction: column;
}

.form h2 {
    text-transform: uppercase;
    font-size: 38px;
    font-weight: 400;
}

.form p {
    font-size: 21px;
    font-weight: 300;
    margin-bottom: 60px;
}

.form-data {
    display: flex;
    width: 800px;
    padding: 0 10px;
    flex-wrap: wrap;
}

.input1, .input2 {
    display: flex;
    justify-content: center;
    line-height: 30px;
    flex: 1 0 0;
}

.input1 input, .input2 input {
    width: 100%;
}

.input2 {
    margin-left: 20px;
}

.input3 {
    width: 100%;
    margin: 10px 0;
}

.input3 textarea {
    width: 100%;
}

input, textarea {
    padding: 10px 7px;
    border-radius: 4px;
}

textarea {
    resize: vertical;
    min-height: 150px;
}

.input4 {
    display: inline-block;
    height: 48px;
    line-height: 48px;
    padding: 0 35px;
    font-size: 14px;
    border-radius: 4px;
    font-weight: 700;
    background-color: #fc3;
    color: black;
    box-shadow: 0 4px 0 #dfae08;
}

.btn-full-width, .btn-full-width a {
    width: 100%;
}

.icon1, .icon2 {
    width: 50%
}

.final {
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 40px 0;
    background-color: #2a3030;
    text-align: center;
}

.final h5 {
    color: white;
    padding-bottom: 25px;
}

.icons {
    width: 200px;
    display: flex;
    justify-content: space-between;
}




</style>
