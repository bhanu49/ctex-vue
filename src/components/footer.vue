<template>
    <div>
        <!--footer starts from here-->
        <footer class="footer">
            <div class="container bottom_border">
                <div class="row">
                    <div class=" col-sm-4 col-md col-sm-4  col-12 col">
                        <h5 class="headin5_amrc col_white_amrc pt2">Find us</h5>
                        <!--headin5_amrc-->
                        <p class="mb10">Lorem Ipsum is simply dummy text of the printing and typesetting industry.
                            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s</p>
                        <p><i class="fa fa-phone"></i> +49- xxxxxxxxx </p>
                        <p><i class="fa fa fa-envelope"></i> info@example.com </p>
                    </div>

                    <div class=" col-sm-4 col-md  col-6 col">
                        <h5 class="headin5_amrc col_white_amrc pt2">Quick links</h5>
                        <!--headin5_amrc-->
                        <ul class="footer_ul_amrc">
                            <li><a href="">courses</a></li>
                            <li><a href="">blogs</a></li>
                            <li><a href="">dummy</a></li>
                            <li><a href="">dummy</a></li>
                            <li><a href="">dummy</a></li>
                            <li><a href="">Idummy</a></li>
                        </ul>
                        <!--footer_ul_amrc ends here-->
                    </div>


                    <div class=" col-sm-4 col-md  col-6 col">
                        <h5 class="headin5_amrc col_white_amrc pt2">Legal</h5>
                        <!--headin5_amrc-->
                        <ul class="footer_ul_amrc">
                            <li><a href="">courses</a></li>
                            <li><a href="">blogs</a></li>
                            <li><a href="">dummy</a></li>
                            <li><a href="">dummy</a></li>
                            <li><a href="">dummy</a></li>
                            <li><a href="">Idummy</a></li>
                        </ul>
                        <!--footer_ul_amrc ends here-->
                    </div>


                    <div class=" col-sm-4 col-md  col-12 col">
                        <h5 class="headin5_amrc col_white_amrc pt2">Follow us</h5>
                        <!--headin5_amrc ends here-->

                        <ul class="footer_ul2_amrc">
                            <li><a href="#"><i class="fab fa-twitter fleft padding-right"></i> </a>
                                <p>Lorem Ipsum is simply dummy text of the printing...<a href="#">facebook</a></p>
                            </li>
                            <li><a href="#"><i class="fab fa-twitter fleft padding-right"></i> </a>
                                <p>Lorem Ipsum is simply dummy text of the printing...<a href="#"> twitter</a></p>
                            </li>
                            <li><a href="#"><i class="fab fa-twitter fleft padding-right"></i> </a>
                                <p>Lorem Ipsum is simply dummy text of the printing...<a href="#">linkiden</a></p>
                            </li>
                        </ul>
                        <!--footer_ul2_amrc ends here-->
                    </div>
                </div>
            </div>


            <div class="container">
                <!-- <ul class="foote_bottom_ul_amrc">
                    <li><a href="">Home</a></li>
                    <li><a href="">About</a></li>
                    <li><a href="">Services</a></li>
                    <li><a href="">Pricing</a></li>
                    <li><a href="">Blog</a></li>
                    <li><a href="">Contact</a></li>
                </ul> -->
                <!--foote_bottom_ul_amrc ends here-->
                <p class="text-center copyr">Copyright @2018 | Designed With by @Bhanu</p>

                <ul class="social_footer_ul">
                    <li><a href=""> </a></li>
                    <li><a href=""> </a></li>
                    <li><a href=""> </a></li>
                    <li><a href=""> </a></li>
                </ul>
                <!--social_footer_ul ends here-->
            </div>

        </footer>

    </div>
</template>

<script>
    export default {

    }
</script>

<style lang="scss" scoped>
.copyr{
    margin-top: 10px;
}
footer {
  width: 100%;
  background-color: #456990;
  min-height: 250px;
  padding: 10px 0px 25px 0px;
  margin-top: 10%;
}
.pt2 {
  padding-top: 40px;
  margin-bottom: 20px;
  color: black;
}
footer p {
  font-size: 13px;
  color:white;
  padding-bottom: 0px;
  margin-bottom: 8px;
}

.mb10 {
  padding-bottom: 15px;
}
.footer_ul_amrc {
  margin: 0px;
  list-style-type: none;
  font-size: 14px;
  padding: 0px 0px 10px 0px;
  li {
    padding: 0px 0px 5px 0px;
    a {
      color: white;
      &:hover {
        color: #fff;
        text-decoration: none;
      }
    }
  }
}

.fleft {
  float: left;
}

.padding-right {
  padding-right: 10px;
}

.footer_ul2_amrc {
  margin: 0px;
  list-style-type: none;
  padding: 0px;
  li {
    p {
      display: table;
    }
    a:hover {
      text-decoration: none;
    }
    i {
      margin-top: 5px;
    }
  }
}

.bottom_border {
  border-bottom: 1px solid #323f45;
  padding-bottom: 20px;
}

.foote_bottom_ul_amrc {
  list-style-type: none;
  padding: 0px;
  display: table;
  margin-top: 10px;
  margin-right: auto;
  margin-bottom: 10px;
  margin-left: auto;
  li {
    display: inline;
    a {
      color: #999;
      margin: 0 12px;
    }
  }
}
.social_footer_ul {
  display: table;
  margin: 15px auto 0 auto;
  list-style-type: none;
  li {
    padding-left: 20px;
    padding-top: 10px;
    float: left;
    a {
      color: white;
      border: 1px solid white;
      padding: 8px;
      border-radius: 50%;
    }
    i {
      width: 20px;
      height: 20px;
      text-align: center;
    }
  }
}

</style>

