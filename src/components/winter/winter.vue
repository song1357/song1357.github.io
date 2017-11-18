<template>
<div class="">
    <nav class="navbar navbar-expand-lg navbar-light fixed-top" id="mainNav">
        <div class="container">
            <router-link to="/"><a class="navbar-brand js-scroll-trigger">Winter is coming</a></router-link>
            <div class="button">
                <a href="#" @click="isActive = !isActive"  :key="first" :class="{ btnOpen: !isActive, btnClose: isActive }"></a>
            </div>
            <div :class="{ overlay: isActive}" v-show="isActive">
                <div class="wrap">
                    <ul class="wrap-nav">
                        <li>
                            <a href="#">About</a>
                            <ul>
                                <li><a href="#">About Company</a></li>
                                <li><a href="#">Designers</a></li>
                                <li><a href="#">Developers</a></li>
                                <li><a href="#">Pets</a></li>
                            </ul>
                        </li>
                        <li>
                            <a href="#">Services</a>
                            <ul>
                                <li><a href="#">Web Design</a></li>
                                <li><a href="#">Development</a></li>
                                <li><a href="#">Apps</a></li>
                                <li><a href="#">Graphic design</a></li>
                                <li><a href="#">Branding</a></li>
                            </ul>
                        </li>
                        <li>
                            <a href="#">Work</a>
                            <ul>
                                <li><a href="#">Web</a></li>
                                <li><a href="#">Graphic</a></li>
                                <li><a href="#">Apps</a></li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </nav>
<!-- banner -->
    <section class="banner">
        <h1>Hello World</h1>
    </section>
        
<!-- parallaxScrolling -->
    <section class="parallaxScrolling">
        <div class="header">
            <h2>Hello Winter</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. At fugit, vero. Esse eum facere ipsa ipsam
                molestiae officia praesentium ullam veniam? Aliquam autem doloremque in maiores officia possimus quos
                reprehenderit?
            </p>
        </div>
        <div class="parallax">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Expedita cumque odio voluptatibus doloribus dolores molestiae, eos eius. Itaque, fuga, maiores?</p>
        </div>
    </section>

    <!-- timeline -->
    <section id=timeline>
        <div class="dark-overlay">
            <div class="timeline">
          <div class="container left">
              <div class="content">
              <h2>2017</h2>
              <p>Lorem ipsum dolor sit amet, quo ei simul congue exerci, ad nec admodum perfecto mnesarchum, vim ea mazim fierent detracto. Ea quis iuvaret expetendis his, te elit voluptua dignissim per, habeo iusto primis ea eam.</p>
              </div>
          </div>
          <div class="container right">
            <div class="content">
              <h2>2016</h2>
              <p>Lorem ipsum dolor sit amet, quo ei simul congue exerci, ad nec admodum perfecto mnesarchum, vim ea mazim fierent detracto. Ea quis iuvaret expetendis his, te elit voluptua dignissim per, habeo iusto primis ea eam.</p>
            </div>
          </div>
          <div class="container left">
            <div class="content">
              <h2>2015</h2>
              <p>Lorem ipsum dolor sit amet, quo ei simul congue exerci, ad nec admodum perfecto mnesarchum, vim ea mazim fierent detracto. Ea quis iuvaret expetendis his, te elit voluptua dignissim per, habeo iusto primis ea eam.</p>
            </div>
          </div>
          <div class="container right">
            <div class="content">
              <h2>2012</h2>
              <p>Lorem ipsum dolor sit amet, quo ei simul congue exerci, ad nec admodum perfecto mnesarchum, vim ea mazim fierent detracto. Ea quis iuvaret expetendis his, te elit voluptua dignissim per, habeo iusto primis ea eam.</p>
            </div>
          </div>
        </div>
        </div>
        
    </section>
</div>
</template>

<script>
    export default {
        data() {
            return {
              isActive: false,
              msg: 'Hello'
          }
        }
    }
</script>

<style lang="scss" scoped>

//mixins

        @mixin sans-serif-font() {
            font-family: 'Open Sans', 'Helvetica Neue', Arial, sans-serif;
            }
        @mixin transition-all() {
            -webkit-transition: all 0.2s;
            -moz-transition: all 0.2s;
            transition: all 0.2s;
            }
        @mixin background-cover() {
            -webkit-background-size: cover;
            -moz-background-size: cover;
            -o-background-size: cover;
            background-size: cover;
            }

//variables

        $theme-primary: #F05F40;
        $gray-base: #000 !default;
        $gray-darker: lighten($gray-base, 13.5%) !default;

//global
body, html {
    height: 100%;
}

//navbar
#mainNav {
  position: absolute;
  border-color: fade-out($gray-darker, .95);
  background-color: transparent;
  @include sans-serif-font;
  @include transition-all;
  .navbar-brand {
    font-weight: 700;
    color: fade-out($color: white, $amount: .3);
    @include sans-serif-font;
    &:focus,
    &:hover {
      color: darken($theme-primary, .1);

    }
  }

    //style open and close button
    .button {
        display:inline;
        position: absolute;
        right: 50px;
        top: 6px;
        z-index: 999;
        font-size: 30px;
        a {
            text-decoration: none;
        }
    }
    .btnOpen:after {
        color: fade-out($color: white, $amount: .3);
        content: "\f0c9";
        font-family: "FontAwesome";
        transition: all .2s linear 0s;
        -moz-transition:all .2s linear 0s;
        -webkit-transition:all .2s linear 0s;
        -o-transition:all .2s linear 0s;
    }
    .btnOpen {
        // color: fade-out($color: white, $amount: .3);
        &:active:after {
            color: darken($theme-primary, .1);
        }
    }
    .btnClose:after {
        color:fade-out($color: white, $amount: .3);
        content:"\f00d";
        font-family:"FontAwesome";
        transition:all .2s linear 0s;
        -moz-transition:all .2s linear 0s;
        -webkit-transition:all .2s linear 0s;
        -o-transition:all .2s linear 0s;
    }
    .btnClose:hover:after {
        color: darken($theme-primary, .1);
    }

    //overlay
    .overlay {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: #333;
        overflow: auto;
        z-index: 99;
    }
    .wrap {
        position: relative;
        color: #e9e9e9;
        text-align: center;
        max-width: 90%;
        margin: 0 auto;
        ul.wrap-nav {
            text-transform: capitalize;
            padding: 130px 0px 20px;
            margin-bottom: 10px;
            li {
                font-size: 20px;
                display: inline-block;
                vertical-align: top;
                width: 24%;
                position: relative;
                a {
                    color:#34B484;
                    display:block;
                    padding:8px 0;
                    text-decoration:none;
                    transition:all .2s linear 0s;
                    -moz-transition:all .2s linear 0s;
                    -webkit-transition:all .2s linear 0s;
                    -o-transition:all .2s linear 0s;
                    &:hover {
                        color:#f0f0f0;
                    }
                }
            }
            ul {
                padding: 20px 0;
                li {
                    display: block;
                    font-size: 13px;
                    width: 100%;
                    color: #e9e9e9;
                    a {
                        color: #f0f0f0;
                        &:hover {
                            color: #34B484;
                        }
                    }
                }
            }
        }
    }


  @media (min-width: 992px) {
    border-color: fade-out(white, .7);
    background-color: transparent;
    .navbar-brand {
      color: fade-out(white, .3);;
      &:focus,
      &:hover {
        color: darken($theme-primary, .1);
      }
    }
    .wrap {
        ul.wrap-nav {
            li {
                font-size: 46px;
            }
            ul {
                li {
                    font-size: 20px;
                }
            }
        }
    }
  }
}

//banner
.banner {
    h1 {
        text-align: center;
        color: fade-out($color: white, $amount: .2);
        padding-top: 200px;
        padding-bottom: 30px;
      
    }
    position: relative;
    height: 450px;
    background: url('../../assets/trees-winter.jpg') center center no-repeat;
    background-size: cover;
    -webkit-background-size: cover;
    -moz-background-size: cover;
}

//parallax Scrolling section
    .parallaxScrolling {
        height: 800px;
        .header {
            h2 {
                text-align: center;
                padding-top: 60px;
            }
            p {
                margin-bottom: 18px;
                margin-top: 10px;
                padding-left: 20px;
                padding-right: 20px;
                text-align: justify;
                padding-bottom: 58px;
            }
        }
        .parallax {
            p {
                font-size: 30px;
                padding-top: 29%;
                padding-left: 20%;
                padding-right: 20%;
                text-align: center;
            }
            height: 100%;
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
            background-image: url('../../assets/people-winter.jpg');
          
        }
        .parallax-text {
            height: 150px;
            font-size:16px;
            background-color: #282e34;
            color: rgba(255,255,255,.8);
            text-align: justify;
            padding-top: 60px;
            padding-left: 50px;
            padding-right: 50px;
            padding-bottom: 30px;
        }
        @media(max-width: 575px) {
            .parallax {
                background-attachment: scroll;
                background: url('../../assets/portfolio3.jpg') center center no-repeat;
                background-size: cover;
                height: 70%;
    
            }
            .parallax-text {
                height: 220px;
                color: rgba(255,255,255,.8);
                text-align: justify;
                padding-top: 26px;
                padding-left: 50px;
                padding-right: 50px;
                padding-bottom: 35px;
            }
        }
        @media(max-width: 1000px) and (min-width: 575px) {
            .parallax-text {
                height: 120px;
                color: rgba(255,255,255,.8);
                text-align: justify;
                padding-top: 26px;
                padding-left: 50px;
                padding-right: 50px;
                padding-bottom: 5px;
            }
        }
    }

// timeline
section#timeline {
    box-sizing:border-box; 
    background: url("../../assets/winter.jpg") no-repeat;
    background-size: cover;
    background-attachment: fixed;
    margin-bottom: 0;
    .dark-overlay {
        background-color: rgba(0, 0, 0, 0.2);
    }
    // The actual timeline (the verticle ruler)
    .timeline {
        position: relative;
        max-width: 1200px;
        margin: 0 auto;
        &::after {
            content: '';
            position: absolute;
            width: 6px;
            background-color: white;
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -3px;
        }
    }
    // Containter around content
    .container {
         padding: 10px 40px;
         position: relative;
         background-color: inherit;
         width: 50%;
         z-index: 100;
         &::after {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            right: -17px;
            background-color: white;
            border: 4px solid #FF9F55;
            top: 15px;
            border-radius: 50%;
            z-index: 1;
         }
    }
    // Place the container to the left and right
    .left {
        left: -25.4%;
    }
    .right {
        left: 25.4%;
    }
    /* Add arrows to the left container (pointing right) */
    .left::before {
        content: " ";
        height: 0;
        position: absolute;
        top: 22px;
        width: 0;
        z-index: 1;
        right: 30px;
        border: medium solid white;
        border-width: 10px 0 10px 11px;
        border-color: transparent transparent transparent white;
    }
    /* Add arrows to the right container (pointing left) */
    .right::before {
        content: " ";
        height: 0;
        position: absolute;
        top: 22px;
        width: 0;
        z-index: 1;
        left: 30px;
        border: medium solid white;
        border-width: 10px 11px 10px 0;
        border-color: transparent white transparent transparent;
    }
    /* Fix the circle for containers on the right side */
    .right::after {
        left: -16px;
    }

    /* The actual content */
    .content {
        padding: 20px 30px;
        background-color: white;
        position: relative;
        border-radius: 6px;
    }
    /* Media queries - Responsive timeline on screens less than 600px wide */
    @media all and (max-width: 600px) {
      /* Place the timelime to the left */
      .timeline::after {
        left: 3%;
      }
      
      /* Full-width containers */
      .container {
        width: 100%;
        padding-left: 70px;
        padding-right: 25px;
      }
       /* Make sure that all arrows are pointing leftwards */
      .container::before {
        left: 60px;
        border: medium solid white;
        border-width: 10px 11px 10px 0;
        border-color: transparent white transparent transparent;
      }

      /* Make sure all circles are at the same spot */
      .left::after, .right::after {
        left: 0%;
      }
      
      /* Make all right containers behave like the left ones */
      .right {
        left: 0%;
      }

      /* Make all left containers behave like the left ones */
      .left {
        left: 0%;
      }

    }
}



</style>