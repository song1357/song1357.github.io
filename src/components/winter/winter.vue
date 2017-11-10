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

    <section class="banner">
        <img src="../../assets/trees-winter.jpg" alt="" class="img-fluid" >
    </section>

    <section class="parallaxScrolling">
        <div class="header">
            <h2>Hello Winter</h2>
            <p>In this example we have turned off parallax scrolling for mobile devices.
                It works as expected on all desktop screens sizes.
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur debitis ea eligendi in obcaecati optio
                quas quod sint. Consequatur, dicta.
            </p>
        </div>

        <div class="parallax"></div>
        <div class="parallax-text" style="height:200px;font-size:16px">
            This div is just here to enable scrolling.
            Tip: Try to remove the background-attachment property to remove the scrolling effect.
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. A animi dolor facere qui ratione voluptatem.
        </div>

        <div class="parallax2"></div>
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
    .btnOpen:hover:after {
        color: darken($theme-primary, .1);
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
      color: fade-out(white, .3);
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
    height: 350px;
    img {
        height: 100%;
        width: 100%;
    }
}

//Parallax Scrolling section
    .parallaxScrolling {
        height: 400px;
        .header {
            h2 {
                text-align: center;
                padding-top: 20px;
            }
            p {
                margin-bottom: 20px;
                margin-top: 10px;
                padding-left: 20px;
                padding-right: 20px;
                text-align: justify;
            }
        }
        .parallax {
            height: 100%;
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
            background-image: url('../../assets/people-winter.jpg');
          
        }
        .parallax-text {
            background-color: #282e34;
            color: rgba(255,255,255,.8);
            text-align: justify;
            padding-top: 60px;
            padding-left: 50px;
            padding-right: 50px;
            padding-bottom: 30px;
        }
        .parallax2 {
            height: 100%;
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
            background-image: url('../../assets/winter.jpg');

        }
    }

</style>