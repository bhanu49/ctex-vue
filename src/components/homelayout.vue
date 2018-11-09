<template>
  <div>
    <!-- <h1>{{ msg }}</h1> -->
    <!-- banner design  -->
    <div class="row">
      <div class="container-fluid">
        <div class="row">
          <div class="col-md-6">
            <div class="banner-title">
              <h1> Stepping stone for your future </h1>
              <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. </p>
              <button class="btn btn-default"> Find Courses </button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- body tiles for courses preview design -->
    <div class="container">
      <div class="row justify-content-center">
        <h5 class="underline"> Popular Courses</h5>
        <b-card-group deck>
          <b-card title="Title" img-src="http://www.creativeapplications.net/wp-content/uploads/2012/09/AmnonOwed-KinectPhysics-06-320x180.png"
            img-alt="Img" img-top>
            <p class="card-text">
              This is a wider card with supporting text below as a
              natural lead-in to additional content. This content
              is a little bit longer.
            </p>
            <div slot="footer">
              <small class="text-muted">
                <button class="btn  card-btn"> More </button>
              </small>
            </div>
          </b-card>
          <b-card title="Title" img-src="http://www.creativeapplications.net/wp-content/uploads/2012/09/AmnonOwed-KinectPhysics-06-320x180.png"
            img-alt="Img" img-top>
            <p class="card-text">
              This card has supporting text below as a natural lead-in
              to additional content.
            </p>
            <div slot="footer">
              <button class="btn  card-btn"> More </button>
            </div>
          </b-card>
          <b-card title="Title" img-src="http://www.creativeapplications.net/wp-content/uploads/2012/09/AmnonOwed-KinectPhysics-06-320x180.png"
            img-alt="Img" img-top>
            <p class="card-text">
              This is a wider card with supporting text below as a natural
              lead-in to additional content. This card has even longer content
              than the first to show that equal height action.
            </p>
            <div slot="footer">
              <button class="btn  card-btn"> More </button>
            </div>
          </b-card>
        </b-card-group>

        <div>
          <button class="btn viewall"> View all courses</button>
        </div>
      </div>
      <!-- uni logo design -->
      <div class="row uni-logos justify-content-center">
        <ul>
          <li>
            <div class="box">
              <img src="https://www.incimages.com/uploaded_files/image/970x450/getty_883231284_200013331818843182490_335833.jpg"
                alt="">
            </div>
          </li>
          <li>
            <div class="box">
              <img src="https://www.incimages.com/uploaded_files/image/970x450/getty_883231284_200013331818843182490_335833.jpg"
                alt="">
            </div>
          </li>
          <li>
            <div class="box">
              <img src="https://www.incimages.com/uploaded_files/image/970x450/getty_883231284_200013331818843182490_335833.jpg"
                alt="">
            </div>
          </li>
        </ul>
      </div>


      <!-- latest news -->
      <div class="row news justify-content-center">

        <h4 class="underline">Latest News</h4>

        <div class="row">
          <div class="col-md-6">
            <div class="news-container">
              <h4>{{dispTitle}}</h4>
              <h6>Subtitle</h6>
              <div class="img-cont">
                <img v-bind:src = "dispImg" alt="">
              </div>
                <p class="">
                  {{dispTxt}}
                </p>  
            </div>
        </div>
        <div class="col-md-6 news-list">
          <div v-for="(item, i) in news" class="news-item" v-on:click = "updateNews(i)">
              {{item.title}}
          </div>

        </div>
        </div>
      </div>
    </div> <!-- container div end -->
  </div> <!-- tepm div end -->
</template>

<script>
  export default {
    name: 'homelayout',
    props: {
      msg: String
    },
    data(){
      return{
        news:[
          {
            "title": "Gloman Academy",
            "text" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed fringilla diam a orci aliquam sodales.",
            "img"  : ""
          },
          {
            "title": "Some random stuff",
            "text" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed fringilla diam a orci aliquam sodales.",
            "img"  : "https://www.sdabocconi.it/sites/default/files/upload/dl.jpg"
          },
          {
            "title": "Some other random stuff",
            "text" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed fringilla diam a orci aliquam sodales.",
            "img"  : "https://xyleme.com/wp-content/uploads/2015/04/Image-Blog-Want-To-Know-What-Personalized-Learning-Looks-Like.png"
          },
          {
            "title": "Some other random stuff with differenrt image",
            "text" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed fringilla diam a orci aliquam sodales.",
            "img"  : "https://connect.mla.hcommons.org/files/2015/10/interdisciplinary.png"
          }
        ],
        dispTitle: "Blended Learning",
        dispTxt: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed fringilla diam a orci aliquam sodales. Vestibulum magna nisi, commodo ut urna eu, porta fermentum est. Nulla aliquet ac est id scelerisque. Fusce varius sollicitudin magna vel congue. Donec fringilla elit nisl, sit amet sagittis nunc auctor at.",
        dispImg: " https://cdn-images-1.medium.com/max/1600/1*nOmfBUSJI6V2G26EgKNpbQ.png"
      }
    },
    methods:{
      updateNews:function (i) { 
        this.dispTitle = this.news[i].title;
        this.dispTxt = this.news[i].text;
        this.dispImg = this.news[i].img;
       }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "../styles/mixins";

  h5 {
    margin-top: 20px;
    padding: 15px;
    margin-bottom: 20px;
  }

  .underline::before {
    content: ' ';
    display: block;
    border: 1px solid black;
    margin-bottom: 10px;
  }

  .container-fluid {
    width: 100%;
    height: 500px;
    background-image: url('../assets/banner.jpg');
    background-size: cover;
    background-position: center center;
    padding: 20px;

    .banner-title {
      text-align: left;
      padding: 10px;
      margin-top: 15%;
      margin-left: 30px;

      button {
        background-color: #456990;
        color: white;
        font-weight: bold;
      }
    }
  }

  .card-btn {
    background-color: #114B5F;
    color: white;
  }

  .viewall {
    background-color: #F45B69;
    color: white;
    margin: 20px;
  }

  .uni-logos {
    border-top: 1px solid rgba(11, 15, 34, 0.1);
    border-bottom: 1px solid rgba(11, 15, 34, 0.1);

    ul {
      list-style: none;

      li {
        float: left;
        margin: 20px;

        .box {
          width: 250px;
          height: 100px;

          img {
            display: block;
            object-fit: fill;
            width: 100%;
          }
        }
      }
    }
  }

  .news {
    margin-top: 20px;
    .news-container{
      text-align: left;
      margin-top: 20px;
    }
    .news-list{
      margin-top: 80px; 
      .news-item{
        padding: 20px;
        text-align: left;
        border-bottom: 1px solid rgba(11, 15, 34, 0.1);
          font-size: 18px;
          color: black;
          text-decoration: none;
      }
      .news-item:hover{
       color: #F45B69;
      }
    }
  }
  
  .img-cont{
    img {
            display: block;
            object-fit: fill;
            width: 100%;
            margin: 15px 0px 15px 0;
          }
  }
  
</style>