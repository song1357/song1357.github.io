<template>
    <div>
            <!--Navigation-->
            <nav class="navbar navbar-expand-sm navbar-dark  fixed-top" id="mainNav">
                <div class="container">
                    <a href="#page-top" class="navbar-brand js-scroll-trigger">Resume</a>
                    <button class="navbar-toggler navbar-toggler-right"
                            type="button"
                            data-toggle="collapse"
                            data-target="#navbarResponsive"
                            aria-controls="navbarResponsive"
                            aria-expanded="false"
                            aria-label="Toggle navigation">
                        <i class="fa fa-bars"></i>
                    </button>
                    <div class="collapse navbar-collapse" id="navbarResponsive">
                        <ul class="navbar-nav ml-auto">
                            <li class="nav-item">
                                <a class="nav-link js-scroll-trigger" href="#portfolio">Portfolio</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link js-scroll-trigger" href="#about">About</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link js-scroll-trigger" href="#about">Skills</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link js-scroll-trigger" href="#about">Education</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link js-scroll-trigger" href="#contact">Contact</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </nav>


            <!--Header-->
            <header id="masthead">
                <div>
                    <div class="wrap-banner">
                        <div class="main-title">
                            <img class="img-fluid rounded-circle mx-auto d-block" src="../assets/img-me.jpg" alt="">
                            <div class="intro-text">
                                <span class="name">Web Front-end Developer </span>
                            </div>
                        </div>
                        <vue-particles
                                color="#ffffff"
                                :particleOpacity="0.7"
                                linesColor="#ffffff"
                                :particlesNumber="80"
                                shapeType="circle"
                                :particleSize="5"
                                :linesWidth="2"
                                :lineLinked="true"
                                :lineOpacity="0.4"
                                :linesDistance="150"
                                :moveSpeed="3"
                                :hoverEffect="true"
                                hoverMode="grab"
                                :clickEffect="true"
                                clickMode="push"
                        >
                        </vue-particles>
                    </div>
                </div>
            </header>
        <!--Portfolio Grid Section-->
        <section id="portfolio">
            <div class="container">
                <div class="text-center">
                    <h2 class="heading">Portfolio</h2>
                </div>
                <div class="row">
                    <div class="col-sm-4 col-xs-8 portfolio-item">
                        <a class="portfolio-link" href="#portfolioModal1" data-toggle="modal">
                            <div class="caption">
                                <div class="caption-content">
                                    <i class="fa fa-search-plus fa-3x"></i>
                                </div>
                            </div>
                            <img class="img-fluid img-centered img" src="../assets/portfolio1.jpg" alt="">
                        </a>
                    </div>
                    <div class="col-sm-4 col-xs-8 portfolio-item">
                        <a class="portfolio-link" data-toggle="modal" href="#portfolioModal2">
                            <div class="caption">
                                <div class="caption-content">
                                    <i class="fa fa-search-plus fa-3x"></i>
                                </div>
                            </div>
                            <img class="img-fluid img-centered img" src="../assets/portfolio2.jpg" alt="">
                        </a>
                    </div>
                    <div class="col-sm-4 col-xs-8 portfolio-item">
                        <a class="portfolio-link" data-toggle="modal" href="#portfolioModal3">
                            <div class="caption">
                                <div class="caption-content">
                                    <i class="fa fa-search-plus fa-3x"></i>
                                </div>
                            </div>
                            <img class="img-fluid img-centered img" src="../assets/portfolio3.jpg" alt="">
                        </a>
                    </div>
                </div>
            </div>

        </section>

        <!--About Me-->
        <section class="success" id="about">
            <div class="container">
                <div class="text-center">
                    <h2 class="heading">About Me</h2>
                </div>
                <div class="row">
                    <div class="col-md-4 ml-auto">
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa, suscipit.</p>
                    </div>
                    <div class="col-md-4 mr-auto">
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa, suscipit.</p>
                    </div>
                </div>
            </div>
        </section>

        <!--Skills-->
        <section id="skills">
            <div class="">
                <div class="text-center">
                    <h2 class="heading">Skills</h2>
                </div>
                <ul>
                    <li>CET6(English)</li>
                    <li>Javascript</li>
                    <li>HTML</li>
                    <li>CSS</li>
                    <li>Bootstrap</li>
                    <li>Jquery</li>
                    <li>Sass</li>
                    <li>Vue</li>
                    <li>ES6</li>
                    <li>Nodejs</li>
                    <li>Express</li>
                    <li>MongoDB</li>
                    <li>Gulp</li>
                    <li>Git</li>
                    <li>科学上网</li>
                </ul>
            </div>
        </section>

        <!--Education-->
        <section class="success" id="education">
            <div class="container">
                <div class="text-center">
                    <h2 class="heading">Education</h2>
                </div>
                <!--Education-block-->
                <div class="education-block">
                    <div class="row">
                        <div class="mr-auto">
                            <h3>University of Qingdao</h3>
                            <h4 style="font-size: large">Bachelor of Management</h4>
                        </div>
                        <div class="ml-auto align-self-center">
                            <span>2012-2016</span>
                        </div>
                    </div>
                </div>

                <!--Education-block-->
                <div class="education-block2">
                    <div class="row">
                        <div>
                            <h3>Self-Learning</h3>
                        </div>
                        <div class="ml-auto">
                            <span class="education-date">2016-Forever</span>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!--Contact-->
        <section id="contact">
            <div class="container">
                <h2 class="heading">Contact Me</h2>
                <div class="row">
                    <form action="" class="mx-auto" id="contactForm" novalidate>
                        <div class="control-group">
                            <label style="margin-bottom: 20px;">YangSong</label>
                        </div>
                        <div class="control-group">
                            <label>Email: song23560@gmail.com</label>
                        </div>
                        <div class="control-group">
                            <label>Phone Number: 15610017612</label>
                        </div>
                    </form>
                </div>
            </div>
        </section>

        <!--Scroll to Top Button(Only visible on small and extra small screen sizes)-->
        <div class="scroll-top d-lg-none">
            <a href="#page-top" class="btn btn-primary js-scroll-trigger">
                <i class="fa fa-chevron-up"></i>
            </a>
        </div>
        <!--Portfolio Modals-->
        <div class="portfolio-modal modal fade" id="portfolioModal1" tabindex="-1" role="dialog" aria-hidden="true">
            <div class="modal-dialog" role="document">
                <div class="modal-content">
                    <div class="close-modal" data-dismiss="modal">
                        <div class="lr">
                            <div class="rl"></div>
                        </div>
                    </div>
                    <div class="container">
                        <div class="row">
                            <div class="col-lg-8 mx-auto">
                                <div class="modal-body">
                                    <h2 class="text-center">Project Title</h2>
                                    <hr class="start-primary">
                                    <img class="img-fluid img-centered" src="../assets/portfolio1.jpg" alt="">
                                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus cum deleniti
                                        dolore doloribus esse in, incidunt iure minus, mollitia nobis nulla provident
                                        quae quam quod repellat, repudiandae tempore velit. Debitis?</p>
                                    <button class="btn btn-success" type="button" data-dismiss="modal">
                                        <i class="fa fa-times"></i>
                                        close
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="portfolio-modal modal fade" id="portfolioModal2" tabindex="-1" role="dialog" aria-hidden="true">
            <div class="modal-dialog" role="document">
                <div class="modal-content">
                    <div class="close-modal" data-dismiss="modal">
                        <div class="lr">
                            <div class="rl"></div>
                        </div>
                    </div>
                    <div class="container">
                        <div class="row">
                            <div class="col-lg-8 mx-auto">
                                <div class="modal-body">
                                    <h2>Project Title</h2>
                                    <hr class="start-primary">
                                    <img class="img-fluid img-centered" src="../assets/portfolio1.jpg" alt="">
                                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus cum deleniti
                                        dolore doloribus esse in, incidunt iure minus, mollitia nobis nulla provident
                                        quae quam quod repellat, repudiandae tempore velit. Debitis?</p>
                                    <button class="btn btn-success" type="button" data-dismiss="modal">
                                        <i class="fa fa-times"></i>
                                        close
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="portfolio-modal modal fade" id="portfolioModal3" tabindex="-1" role="dialog" aria-hidden="true">
            <div class="modal-dialog" role="document">
                <div class="modal-content">
                    <div class="close-modal" data-dismiss="modal">
                        <div class="lr">
                            <div class="rl"></div>
                        </div>
                    </div>
                    <div class="container">
                        <div class="row">
                            <div class="col-lg-8 mx-auto">
                                <div class="modal-body">
                                    <h2>Project Title</h2>
                                    <hr class="start-primary">
                                    <img class="img-fluid img-centered" src="../assets/portfolio1.jpg" alt="">
                                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus cum deleniti
                                        dolore doloribus esse in, incidunt iure minus, mollitia nobis nulla provident
                                        quae quam quod repellat, repudiandae tempore velit. Debitis?</p>
                                    <button class="btn btn-success" type="button" data-dismiss="modal">
                                        <i class="fa fa-times"></i>
                                        close
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
</script>

<style lang="scss" scoped>
    @import "../style/resume/main";
</style>