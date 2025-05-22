<template>
  <q-layout view="lHh lpr lFf">
    <q-header
      class="q-py-sm"
      style="background-color: #1c1b21;"
      :style="'border-bottom: 2px solid '+ theme_color"
    >
      <q-toolbar>
        <span :style="'font-size: 35px;color:'+theme_color" class="my-font text-h6 q-mr-md">FarisSoftware</span>
        <q-space></q-space>

        <q-tabs v-model="selected_tab" shrink>
          <q-tab :style= "[selected_tab == 't_0' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_portfolio');" style="width:120px;min-height:auto !important;color: white" label="Portfolio" />
          <q-tab :style= "[selected_tab == 't_1' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_about_us');" style="width:120px;min-height:auto !important;color: white" label="About Us" />
          <q-tab :style= "[selected_tab == 't_2' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_services');" style="width:120px;min-height:auto !important;color: white" label="Services" />
          <q-tab :style= "[selected_tab == 't_3' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_testimonial');" style="min-height:auto !important;color: white" label="Testimonial" />
          <q-tab :style= "[selected_tab == 't_4' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_team');" style="width:120px;min-height:auto !important;color: white" label="Team" />
          <!-- <q-tab :style= "[selected_tab == 't_5' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_pricing');" style="width:120px;min-height:auto !important;color: white" label="Pricing" /> -->
          <q-tab :style= "[selected_tab == 't_6' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_news');" style="width:120px;min-height:auto !important;color: white" label="Hiring" />
        </q-tabs>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <q-page>
        <q-carousel
          animated
          v-model="slide"
          arrows
          swipeable
          navigation
          infinite
          autoplay
          control-color="white"
          transition-prev="slide-right"
          transition-next="slide-left"
          height="639px"
        >
          <q-carousel-slide class="q-pa-none" :name="1" img-src="/statics/images/image_1.jpg">
            <div class="full-height full-width flex flex-center" style="background-color: rgba(0, 0, 0, 0.68) !important;">
              <div class="custom-caption">
                <div class="text-h2 main_line animation_2">WELCOME TO <span :style="'color:'+theme_color">FARISSOFTWARE</span></div><br><br><br>
                <div class="text-h4 animation_1">We craft custom web and mobile solutions tailored to your business needs.<br/>From idea to launch, we bring your vision to life with precision and creativity.</div><br/><br/><br/>
                <!-- <div class="animation_2">
                  <q-btn size="md" :style="'background:'+ theme_color +'; color: white'" label="READ MORE"/>
                </div> -->
              </div>
            </div>
          </q-carousel-slide>

          <q-carousel-slide class="q-pa-none":name="2" img-src="/statics/images/image_2.jpg">
            <div class="full-height full-width flex flex-center" style="background-color: rgba(0, 0, 0, 0.68) !important;">
              <div class="custom-caption">
                <div class="text-h2 main_line animation_2" style="font-size:65px;"><span :style="'color:'+theme_color">Full-Cycle Development</span> Services</div><br><br><br>
                <div class="text-h4 animation_1">From UI/UX design to backend development, our team builds scalable and<br/>modern applications that deliver real value. Your success is our priority.</div><br/><br/><br/>
                <!-- <div class="animation_2">
                  <q-btn size="md" :style="'background:'+ theme_color +'; color: white'" label="READ MORE"/>
                </div> -->
              </div>
            </div>
          </q-carousel-slide>

          <q-carousel-slide class="q-pa-none":name="3" img-src="/statics/images/image_3.jpg">
            <div class="full-height full-width flex flex-center" style="background-color: rgba(0, 0, 0, 0.68) !important;">
              <div class="custom-caption">
                <div class="text-h2 main_line animation_2" style="font-size:65px;"><span :style="'color:'+theme_color">Reliable. Innovative. On-Time.</span></div><br><br><br>
                <div class="text-h4 animation_1">At FarisSoftware, we blend technical expertise with creative design<br/> to deliver quality products - on time, every time.<br/><br/>Let's build something great together.</div><br/><br/><br/>
                <!-- <div class="animation_2">
                  <q-btn size="md" :style="'background:'+ theme_color +'; color: white'" label="READ MORE"/>
                </div> -->
              </div>
            </div>
          </q-carousel-slide>
        </q-carousel>

        <div class="row">
          <div class="col-md-3 col-lg-3 col-xs-12 col-sm-12">
            <q-card class="q-pa-sm flex flex-center text-center box-shadow" style="margin: 40px;">
              <q-card-section>
                <q-icon size="110px" name="design_services" :style="'color:'+theme_color"/>
                <div class="text-h6">UI/UX Design</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                User-first interface and experience design that improves engagement, simplifies navigation, and enhances customer satisfaction.
              </q-card-section>
            </q-card>
          </div>

          <div class="col-md-3 col-lg-3 col-xs-12 col-sm-12">
            <q-card class="q-pa-sm flex flex-center text-center box-shadow" style="margin: 40px;">
              <q-card-section>
                <q-icon size="110px" name="web" :style="'color:'+theme_color"/>
                <div class="text-h6">Web Design</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                Beautiful, user-friendly, and responsive website designs that make your brand stand out and deliver a seamless user experience across all devices.
              </q-card-section>
            </q-card>
          </div>

          <div class="col-md-3 col-lg-3 col-xs-12 col-sm-12">
            <q-card class="q-pa-sm flex flex-center text-center box-shadow" style="margin: 40px;">
              <q-card-section>
                <q-icon size="110px" name="brush" :style="'color:'+theme_color"/>
                <div class="text-h6">Graphic Design</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                Creative and professional graphic assets, including logos, banners, and branding materials that help your business leave a lasting impression.
              </q-card-section>
            </q-card>
          </div>

          <div class="col-md-3 col-lg-3 col-xs-12 col-sm-12">
            <q-card class="q-pa-sm flex flex-center text-center box-shadow" style="margin: 40px;">
              <q-card-section>
                <q-icon size="110px" name="code" :style="'color:'+theme_color"/>
                <div class="text-h6">Website Development</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                Custom-built websites using modern technologies that are fast, secure, and scalable—tailored to meet your specific business goals.
              </q-card-section>
            </q-card>
          </div>

          <div class="col-md-3 col-lg-3 col-xs-12 col-sm-12">
            <q-card class="q-pa-sm flex flex-center text-center box-shadow" style="margin: 40px;">
              <q-card-section>
                <q-icon size="110px" name="developer_mode" :style="'color:'+theme_color"/>
                <div class="text-h6">Web App Development</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                Robust and dynamic web applications designed for performance and scalability, helping you streamline operations and deliver value to your users.
              </q-card-section>
            </q-card>
          </div>

          <div class="col-md-3 col-lg-3 col-xs-12 col-sm-12">
            <q-card class="q-pa-sm flex flex-center text-center box-shadow" style="margin: 40px;">
              <q-card-section>
                <q-icon size="110px" name="smartphone" :style="'color:'+theme_color"/>
                <div class="text-h6">Mobile App Development</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                Cross-platform and native mobile apps for iOS and Android—engineered to be intuitive, fast, and aligned with your business objectives.
              </q-card-section>
            </q-card>
          </div>

          <div class="col-md-3 col-lg-3 col-xs-12 col-sm-12">
            <q-card class="q-pa-sm flex flex-center text-center box-shadow" style="margin: 40px;">
              <q-card-section>
                <q-icon size="110px" name="shopping_cart" :style="'color:'+theme_color"/>
                <div class="text-h6">E-Commerce Solutions</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                End-to-end e-commerce development tailored to your business—complete with secure payment integration, product management, and seamless UX.
              </q-card-section>
            </q-card>
          </div>

          <div class="col-md-3 col-lg-3 col-xs-12 col-sm-12">
            <q-card class="q-pa-sm flex flex-center text-center box-shadow" style="margin: 40px;">
              <q-card-section>
                <q-icon size="110px" name="support_agent" :style="'color:'+theme_color"/>
                <div class="text-h6">Maintenance & Support</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                Ongoing support, updates, and performance monitoring to ensure your website or app runs smoothly, securely, and efficiently—always.
              </q-card-section>
            </q-card>
          </div>
        </div>

        <div class="quote">
          <div class="q-pt-xl full-width full-height flex flex-center" style="background-color: #000000ad !important;">
            <h3 class="text-white text-center text-lineheight-lg">Whether you're launching a startup or growing <br/> your business, FarisSoftware is here to turn<br />your vision into a powerful digital product.
              <br />
              <br />
              <q-btn
                @click="scrollToElement('id_contact_us');"
                size="lg"
                :style="'background:'+ theme_color +'; color: white'"
                label="Contact Us"
              />
            </h3>
          </div>
        </div>

        <div style="background: #f7f7f7" id="id_portfolio">
          <br />
          <div class="row">
            <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
              <h5 class="text-center text-h3">Our Portfolio
                <br>
                <span class="text-center text-grey-8 text-h6">Showcasing our best work that delivers innovation and excellence.</span>
              </h5>
            </div>
          </div>

          <br />

          <div class="row text-center" style="padding-bottom: 99px">
            <div class="col-md-12 col-sm-12 col-xs-12 col-lg-12">
              <div style="line-height:0">
                <span v-for="sample in portfolio_samples" :key="sample.index">
                  <q-flashcard :no-hover="hover" :style="style">
                    <q-flashcard-section transition="nudge-in" :active="active">
                      <img :src="'/statics/images/'+sample.index+'.jpg'" width=340 height=263>
                    </q-flashcard-section>

                    <q-flashcard-section transition="fade-in" class="fit" :active="active">
                      <div class="fit" :style="background_style"></div>

                      <q-flashcard-section transition="drop-down" class="text-center my-header text-bold" :active="active">
                        {{ sample.title }}
                      </q-flashcard-section>

                      <q-flashcard-section transition="slide-up-in" class="my-text" :active="active">
                        {{ sample.description }}
                      </q-flashcard-section>

                      <q-flashcard-section
                        transition="fade-in"
                        class="fit flex justify-center items-end q-pb-lg"
                        :active="active"
                      >
                        <q-btn :style="'color:'+theme_color" style="background-color:white" round icon="link" :href="sample.url" target="_blank"/>
                      </q-flashcard-section>
                    </q-flashcard-section>
                  </q-flashcard>

                  <br v-if="index==3" />
                </span>
              </div>
            </div>
          </div>
        </div>

        <div class="row" id="id_about_us">
          <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
            <h5 class="text-center text-h3">About Us
              <br />
              <span class="text-center text-grey-8 text-h6">Innovative software solutions crafted to bring your vision to life.</span>
            </h5>
          </div>
        </div>

        <div class="row text-center flex flex-center">
          <div class="col-md-8 col-lg-8 col-sx-8 col-sm-8 q-gutter-md flex flex-center">
            <div class="text-caption text-grey-9">
              <q-label class="text-h6 text-grey-9">
                As the founder and CEO, I bring together a strong background in electrical engineering with a passion for programming and web development. With experience in both technical and digital domains, I lead our company with a clear vision — to deliver smart, functional, and innovative solutions.
                We are an ambitious tech company focused on engineering, custom software development, and modern web solutions. Driven by quality, innovation, and a client-first approach, we aim to create long-term value and set new standards in every project we take on.
              </q-label>
            </div>
          </div>
        </div>

        <br />
        <br />

        <div style="background: #f7f7f7" id="id_services">
          <div class="row">
            <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
              <h5 class="text-center text-h3">Our Services
                <br />
                <span class="text-center text-grey-8 text-h6">Comprehensive digital solutions tailored to accelerate your business growth.</span>
              </h5>
            </div>
          </div>

          <div class="q-pa-xl">       
            <div class="row q-col-gutter-sm">
              <div class="col-md-4 col-lg-4 col-sm-12 col-xs-12">
                <q-item class="box-shadow q-pa-none q-ml-xs ">
                  <q-item-section side :style="'background-color:' + theme_color" class="q-pa-sm q-mr-none text-white">
                    <q-icon name="compare_arrows" size="65px"></q-icon>
                  </q-item-section>

                  <q-item-section class="q-pa-md q-ml-none">
                    <q-item-label class="text-h6 text-grey-9 text-uppercase">UI/UX Design</q-item-label>
                    <q-item-label class="text-grey-8">Crafting intuitive and engaging user experiences that make your apps and websites stand out.</q-item-label>
                  </q-item-section>
                </q-item>
              </div>

              <div class="col-md-4 col-lg-4 col-sm-12 col-xs-12">
                <q-item class="box-shadow q-pa-none q-ml-xs">
                  <q-item-section side :style="'background-color:' + theme_color" class="q-pa-sm q-mr-none text-white">
                    <q-icon name="web" size="65px"></q-icon>
                  </q-item-section>

                  <q-item-section class="q-pa-md q-ml-none">
                    <q-item-label class="text-h6 text-grey-9 text-uppercase">Website Development</q-item-label>
                    <q-item-label class="text-grey-8">Building responsive, high-performance websites tailored to your business goals.</q-item-label>
                  </q-item-section>
                </q-item>
              </div>

              <div class="col-md-4 col-lg-4 col-sm-12 col-xs-12">
                <q-item class="box-shadow q-pa-none q-ml-xs q-mr-xs">
                  <q-item-section side :style="'background-color:' + theme_color" class="q-pa-sm q-mr-none text-white">
                    <q-icon name="fab fa-wordpress" size="65px"></q-icon>
                  </q-item-section>

                  <q-item-section class="q-pa-md q-ml-none">
                    <q-item-label class="text-h6 text-grey-9 text-uppercase">Web Application Development</q-item-label>
                    <q-item-label class="text-grey-8">Creating scalable and secure web apps with modern technologies for seamless user interactions.</q-item-label>
                  </q-item-section>
                </q-item>
              </div>
            </div>

            <div class="row q-col-gutter-sm q-mt-lg">
              <div class="col-md-4 col-lg-4 col-sm-12 col-xs-12">
                <q-item class="box-shadow q-pa-none q-ml-xs ">
                  <q-item-section side :style="'background-color:' + theme_color" class="q-pa-sm q-mr-none text-white">
                    <q-icon name="settings" size="65px"></q-icon>
                  </q-item-section>

                  <q-item-section class="q-pa-md q-ml-none">
                    <q-item-label class="text-h6 text-grey-9 text-uppercase">Mobile App Development</q-item-label>
                    <q-item-label class="text-grey-8">Designing and developing native and cross-platform mobile apps for iOS and Android.</q-item-label>
                  </q-item-section>
                </q-item>
              </div>

              <div class="col-md-4 col-lg-4 col-sm-12 col-xs-12">
                <q-item class="box-shadow q-pa-none q-ml-xs">
                  <q-item-section side :style="'background-color:' + theme_color" class="q-pa-sm q-mr-none text-white">
                    <q-icon name="fas fa-database" size="65px"></q-icon>
                  </q-item-section>

                  <q-item-section class="q-pa-md q-ml-none">
                    <q-item-label class="text-h6 text-grey-9 text-uppercase">E-Commerce Solutions</q-item-label>
                    <q-item-label class="text-grey-8">Delivering robust online stores with smooth checkout experiences to boost your sales.</q-item-label>
                  </q-item-section>
                </q-item>
              </div>

              <div class="col-md-4 col-lg-4 col-sm-12 col-xs-12">
                <q-item class="box-shadow q-pa-none q-ml-xs q-mr-xs">
                  <q-item-section side :style="'background-color:' + theme_color" class="q-pa-sm q-mr-none text-white">
                    <q-icon name="dynamic_feed" size="65px"></q-icon>
                  </q-item-section>

                  <q-item-section class="q-pa-md q-ml-none">
                    <q-item-label class="text-h6 text-grey-9 text-uppercase">Maintenance & Support</q-item-label>
                    <q-item-label class="text-grey-8">Providing ongoing technical support and updates to keep your software running flawlessly.</q-item-label>
                  </q-item-section>
                </q-item>
              </div>
            </div>
          </div>          
        </div>

        <div class="quote" id="id_testimonial">
          <div style="background-color: #000000ad !important;">
            <q-carousel
              v-model="review_slide"
              swipeable
              animated
              infinite
              autoplay
              arrows
              navigation
              padding
              navigation-position="bottom"
              class="text-white full-height bg-transparent q-mx-xl"
            >
              <q-carousel-slide style="padding-bottom: 140px" name="style" class="column no-wrap flex-center">
                <img :style="'margin-top:100px;border-radius:5px;border: 4px solid ' + theme_color" src="/statics/images/team_1.jpg" width=150 height=150 />

                <div class="q-mt-md text-h6 text-center">
                  <span :style="'color:'+theme_color">Sarah Johnson</span>
                  <br />
                  <span class="text-overline">CEO, BrightTech Solutions</span>
                </div>

                <div class="q-mt-md text-h6 text-center">
                  "The team delivered our app on time with exceptional quality. Their communication and creativity made the entire process smooth and enjoyable."
                </div>
              </q-carousel-slide>

              <q-carousel-slide style="padding-bottom: 140px" name="tv" class="column no-wrap flex-center">
                <img :style="'margin-top:100px;border-radius:5px;border: 4px solid ' + theme_color" src="/statics/images/team_2.jpg" width=150 height=150 />

                <div class="q-mt-md text-h6 text-center">
                  <span :style="'color:'+theme_color">Michael Lee</span>
                  <br />
                  <span class="text-overline">Founder, GreenLeaf E-Commerce</span>
                </div>

                <div class="q-mt-md text-h6 text-center">
                  "Their expertise in UI/UX design transformed our website’s user experience, resulting in higher engagement and sales."
                </div>
              </q-carousel-slide>

              <q-carousel-slide style="padding-bottom: 140px" name="layers" class="column no-wrap flex-center">
                <img :style="'margin-top:100px;border-radius:5px;border: 4px solid ' + theme_color" src="/statics/images/team_3.jpg" width=150 height=150 />

                <div class="q-mt-md text-h6 text-center">
                  <span :style="'color:'+theme_color">Emily Davis</span>
                  <br />
                  <span class="text-overline">Product Manager, NextGen Mobile</span>
                </div>

                <div class="q-mt-md text-h6 text-center">
                  "Reliable, innovative, and supportive — they were our go-to partner for mobile app development from start to launch."
                </div>
              </q-carousel-slide>
            </q-carousel>
          </div>
        </div>

        <div class="row" id="id_team">
          <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
            <h5 class="text-center text-h3">Our Team
              <br />
              <span class="text-center text-grey-8 text-h6">Meet the passionate professionals dedicated to delivering innovative software solutions.</span>
            </h5>
          </div>
        </div>

        <div class="row text-center flex flex-center">
          <div class="col-md-12 col-lg-12 col-sx-12 col-sm-12 q-px-xl" style="width:100%; overflow:auto;">
            <q-carousel
              v-model="team_slide"
              transition-prev="slide-right"
              transition-next="slide-left"
              swipeable
              animated="false"
              infinite
              autoplay
              control-color="primary"
              navigation="none"
              padding
              height="300px"
              class="rounded-borders"
            >
              <q-carousel-slide v-for="val in [1,2,3]" :key="val" :name="val" class="column no-wrap">
                <div class="row fit justify-center items-center q-gutter-xs q-col-gutter no-wrap">
                  <span v-for="team in team_samples" :key="team.index">
                    <q-flashcard :no-hover="hover" :style="team_style">
                      <q-flashcard-section transition="['nudge-out', 'fade-out']" :active="active">
                        <img :src="team.image" width=260 height=263>
                      </q-flashcard-section>

                      <q-flashcard-section transition="fade-in" class="fit" :active="active">
                        <div class="fit" :style="background_style"></div>

                        <q-flashcard-section transition="shake-down" class="text-center team-header" :active="active">
                          {{ team.name }}
                        </q-flashcard-section>

                        <q-flashcard-section transition="spin-in" class="team-text" :active="active">
                          {{ team.role }}
                        </q-flashcard-section>

                        <!-- <q-flashcard-section
                          style="padding-bottom: 50px"
                          transition="slide-up-in"
                          class="fit flex justify-center items-end"
                          :active="active"
                        >
                          <q-btn
                            class="q-mr-md"
                            :style="'color:'+theme_color"
                            style="background-color:white"
                            round
                            icon="card_giftcard"
                          />

                          <q-btn :style="'color:'+theme_color" style="background-color:white" round icon="link"/>
                        </q-flashcard-section> -->
                      </q-flashcard-section>
                    </q-flashcard>
                  </span>
                </div>
              </q-carousel-slide>
            </q-carousel>
          </div>
        </div>

        <!-- <div class="pricing" id="id_pricing">
          <div class="" style="background-color: #000000ad !important; min-height: 500px;">
            <div class="row">
              <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
                <h5 class="text-center text-white">Our Pricing Plan
                  <br />
                  <span class="text-center text-grey text-h6">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span>
                </h5>
              </div>
            </div>

            <div class="row q-col-gutter-sm q-px-xl">
              <div class="col-lg-3 col-md-3 col-xs-12 col-sm-6 q-px-lg">
                <q-card>
                  <q-card-section class="text-white" style="background: #ec982f">
                    <div class="text-h6 text-center">
                      FREE
                    </div>
                  </q-card-section>

                  <q-card-section class="q-pa-md">
                    <q-list dense padding style="border-bottom: 1px solid lightgrey;">
                      <q-item>
                        <span class="text-weight-bold">For small size companies</span>
                      </q-item>
                      <q-item> 50 GB storage</q-item>
                      <q-item>10 Domains</q-item>
                      <q-item>15 Projects</q-item>
                      <q-item>Free Deployment</q-item>
                    </q-list>
                  </q-card-section>

                  <q-card-section class="q-pa-none" style="color: #ec982f">
                    <div class="text-center">
                      <span class="text-h2 text-center">$0</span>/mo
                    </div>
                  </q-card-section>

                  <q-card-section>
                    <div class="text-center q-px-lg">
                      <q-btn
                        size="md"
                        class="full-width q-pa-xs"
                        style="background: #ec982f;
                        color: white"
                        label="Choose Plan"
                      />

                      <br />

                      <div class="q-mt-md">Terms and Conditions apply</div>
                    </div>
                  </q-card-section>
                </q-card>
              </div>

              <div class="col-lg-3 col-md-3 col-xs-12 col-sm-6 q-px-lg">
                <q-card>
                  <q-card-section class="text-white" style="background: #f4655f">
                    <div class="text-h6 text-center">
                      STANDARD
                    </div>
                  </q-card-section>

                  <q-card-section class="q-pa-md">
                    <q-list dense padding style="border-bottom: 1px solid lightgrey;">
                      <q-item>
                        <span class="text-weight-bold">For medium companies</span>
                      </q-item>
                      <q-item>50 GB storage</q-item>
                      <q-item>10 Domains</q-item>
                      <q-item>15 Projects</q-item>
                      <q-item>Free Deployment</q-item>
                    </q-list>
                  </q-card-section>

                  <q-card-section class="q-pa-none" style="color: #f4655f">
                    <div class="text-center">
                      <span class="text-h2 text-center">$50</span>/mo
                    </div>
                  </q-card-section>

                  <q-card-section>
                    <div class="text-center q-px-lg">
                      <q-btn
                        size="md"
                        class="full-width q-pa-xs"
                        style="background: #f4655f; color: white;"
                        label="Choose Plan"
                      />
                      <br />
                      <div class="q-mt-md">Terms and Conditions apply</div>
                    </div>
                  </q-card-section>
                </q-card>
              </div>

              <div class="col-lg-3 col-md-3 col-xs-12 col-sm-6 q-px-lg">
                <q-card>
                  <q-card-section class="text-white q-pa-md" style="background: #8b3bbd">
                    <div class="text-h6 text-center">
                      PREMIUM
                    </div>
                  </q-card-section>

                  <q-card-section class="q-pa-md">
                    <q-list dense padding style="border-bottom: 1px solid lightgrey;">
                      <q-item>
                        <span class="text-weight-bold">For average companies</span>
                      </q-item>
                      <q-item>50 GB storage</q-item>
                      <q-item>10 Domains</q-item>
                      <q-item>15 Projects</q-item>
                      <q-item>Free Deployment</q-item>
                    </q-list>
                  </q-card-section>

                  <q-card-section class="q-pa-none" style="color: #8b3bbd">
                    <div class="text-center">
                      <span class="text-h2 text-center">$250</span>/mo
                    </div>
                  </q-card-section>

                  <q-card-section>
                    <div class="text-center q-px-lg">
                      <q-btn
                        size="md"
                        class="full-width q-pa-xs"
                        :style="'background: #8b3bbd; color: white'"
                        label="Choose Plan"
                      />
                      <br />
                      <div class="q-mt-md">Terms and Conditions apply</div>
                    </div>
                  </q-card-section>
                </q-card>
              </div>

              <div class="col-lg-3 col-md-3 col-xs-12 col-sm-6 q-px-lg">
                <q-card>
                  <q-card-section class="text-white" style="background: #3b97d1">
                    <div class="text-h6 text-center">
                      PROFESSIONAL
                    </div>
                  </q-card-section>

                  <q-card-section class="q-pa-md">
                    <q-list dense padding style="border-bottom: 1px solid lightgrey;">
                      <q-item>
                        <span class="text-weight-bold">For large companies</span>
                      </q-item>
                      <q-item>50 GB storage</q-item>
                      <q-item>10 Domains</q-item>
                      <q-item>15 Projects</q-item>
                      <q-item>Free Deployment</q-item>
                    </q-list>
                  </q-card-section>

                  <q-card-section class="q-pa-none" style="color: #3b97d1">
                    <div class="text-center">
                      <span class="text-h2 text-center">$500</span>/mo
                    </div>
                  </q-card-section>

                  <q-card-section>
                    <div class="text-center q-px-lg">
                      <q-btn
                        size="md"
                        class="full-width q-pa-xs"
                        style="background:#3b97d1; color: white"
                        label="Choose Plan"
                      />
                      <br />

                      <div class="q-mt-md">Terms and Conditions apply</div>
                    </div>
                  </q-card-section>
                </q-card>
              </div>
            </div>

            <br />
            <br />
          </div>
        </div> -->

        <div class="row" id="id_news">
          <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
            <h5 class="text-center text-h3">Hiring
              <br />
              <span class="text-center text-grey-8 text-h6">Join our team of innovators and help shape the future of digital solutions.</span>
            </h5>
          </div>
        </div>

        <div class="row text-center flex flex-center">
          <div class="col-md-12 col-lg-12 col-sx-12 col-sm-12 q-gutter-md flex flex-center">
            <div class="col-md-4 col-lg-4 col-sx-12 col-sm-12">
              <q-card @mouseover="hoverOver(1)" @mouseout="hoverOutTimeout(1)" style="border: none;" class="my-card text-center box-shadow" flat bordered>
                <q-img src="/statics/images/about_1.jpg" />

                <q-card-section class="text-left">
                  <div
                    :class="about_heading_1"
                    :style="'color: ' + about_heading_color_1"
                    class="about_heading_1 text-h6 q-mt-sm q-mb-xs"
                  >
                    UI / UX Designer (Remote)
                  </div>

                  <div class="text-caption text-grey-9 q-mt-sm">
                    We're looking for a creative UI/UX Designer to craft user-centered designs for web and mobile platforms — all from the comfort of your remote workspace.
                  </div>
                </q-card-section>
              </q-card>
            </div>

            <div class="col-md-4 col-lg-4 col-sx-12 col-sm-12">
              <q-card @mouseover="hoverOver(2)" @mouseout="hoverOutTimeout(2)" :style="'color: ' + about_heading_color_2" style="border: none;" class="my-card text-center box-shadow" flat bordered>
                <q-img src="/statics/images/about_2.jpg"/>

                <q-card-section class="text-left">
                  <div :class="about_heading_2" :style="'color: ' + about_heading_color_2" class="text-h6 q-mt-sm q-mb-xs">Mobile Developer (Remote)</div>

                  <div class="text-caption text-grey-9 q-mt-sm">
                    We’re hiring a skilled Mobile Developer to build high-quality iOS and Android apps with smooth performance — all in a remote, collaborative environment.
                  </div>
                </q-card-section>
              </q-card>
            </div>

            <div class="col-md-4 col-lg-4 col-sx-12 col-sm-12">
              <q-card @mouseover="hoverOver(3)" @mouseout="hoverOutTimeout(3)" style="border: none;" class="my-card text-center box-shadow" flat bordered>
                <q-img src="/statics/images/about_3.jpg" />

                <q-card-section class="text-left">
                  <div :class="about_heading_3" :style="'color: ' + about_heading_color_3" class="text-h6 q-mt-sm q-mb-xs">Partnership Manager (Remote)</div>

                  <div class="text-caption text-grey-9 q-mt-sm">
                    We're seeking a Partnership Manager to build and maintain strategic relationships that drive business growth — all in a flexible remote role.
                  </div>
                </q-card-section>
              </q-card>
            </div>
          </div>
        </div>

        <br />
        <br />

        <div class="contact_us" id="id_contact_us">
          <div style="background-color: #000000ad !important;">
            <div class="row" id="id_news">
              <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
                <h5 class="text-center text-white text-h3">Contact Us
                  <br />
                  <span class="text-center text-grey text-h6">Our team is ready to collaborate and support you every step of the way.</span>
                </h5>
              </div>
            </div>

            <div class="row text-center flex flex-center q-pb-lg">
              <div class="col-md-6 col-lg-6 col-sx-12 col-sm-12 q-gutter-lg q-px-xl q-pb-none q-ma-none">
                <q-input bg-color="white" outlined label="Your Name *">
                  <template v-slot:append>
                    <q-icon name="person" :style="'color:' + theme_color" />
                  </template>
                </q-input>

                <q-input bg-color="white" outlined label="Your Email *">
                  <template v-slot:append>
                    <q-icon name="email" :style="'color:' + theme_color" />
                  </template>
                </q-input>

                <q-input bg-color="white" outlined label="Your Phone *">
                  <template v-slot:append>
                    <q-icon name="phone" :style="'color:' + theme_color" />
                  </template>
                </q-input>
              </div>

              <div class="col-md-6 col-lg-6 col-sx-12 col-sm-12 q-gutter-lg q-px-xl q-pb-none q-ma-none">
                <q-input class="" type="textarea" bg-color="white" outlined label="Your Message *">
                  <template v-slot:append>
                    <q-icon name="chat" :style="'color:' + theme_color" />
                  </template>
                </q-input>
              </div>
            </div>

            <div class="row flex flex-center text-center q-pb-xl q-mt-md">
              <div class="col-md-12 col-lg-12 col-sx-12 col-sm-12">
                <q-btn size="lg" :style="'background:'+ theme_color +'; color: white'" label="Send Message"/>
              </div>
            </div>
          </div>
        </div>

        <q-toolbar class="flex flex-center text-white" style="background-color: #1c1b21;" :style="'border-top: 2px solid '+ theme_color">
          <div class="q-pa-sm q-gutter-sm">
            Copyright © 2025 By FarisSoftware. All Rights Reserved.
          </div>
        </q-toolbar>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<style src="@quasar/quasar-ui-qflashcard/dist/index.css"></style>

<script>
  import { scroll } from 'quasar';
  import {QFlashcard, QFlashcardSection} from '@quasar/quasar-ui-qflashcard';

  const { getScrollTarget, setScrollPosition } = scroll;

  export default {
    components: {
      QFlashcard,
      QFlashcardSection
    },
    data() {
      return {
        slide: 1,
        review_slide: 'style',
        selected_tab: 't_0',
        team_slide: 1,
        bg_color: 'rgb(0, 163, 82)',
        hover: false,
        active: false,
        theme_color: 'rgb(0, 163, 82)',
        background_style: 'background-color:rgba(0, 163, 82, 0.7);',
        about_heading_1: [],
        about_heading_2: [],
        about_heading_3: [],
        about_heading_color_1: '#424242',
        about_heading_color_2: '#424242',
        about_heading_color_3: '#424242',
        portfolio_samples: [
          {
            index: 1,
            url: 'https://rainierplace.com',
            title: 'Rainier Place',
            description: 'Rainier Place is a modern student housing community offering fully furnished apartments with secure access, on-site amenities, and a vibrant living environment — just steps from Edmonds College.',
          },
          {
            index: 2,
            url: 'https://stoneandchalk.com.au',
            title: 'Stone & Chalk',
            description: `Stone & Chalk is Australia's largest innovation community, supporting startups, scaleups, corporates, and government to solve big problems, move faster, and create real impact.`,
          },
          {
            index: 3,
            url: 'https://kiwiwrite.com',
            title: 'Kiwiwrite',
            description: 'KiwiWrite Math is a web-based assistive tool that enables students with dysgraphia and other handwriting challenges to complete math assignments digitally, fostering accessibility and confidence in learning.',
          },
        ],
        team_samples: [
          {
            index: 1,
            name: 'Faris Halilovic',
            role: 'Founder, CEO',
            image: '/statics/images/faris.png'
          },
          {
            index: 2,
            name: 'Helil Gazov',
            role: 'Director',
            image: '/statics/images/helil.png'
          },
          {
            index: 3,
            name: 'Vladyslav Zientsov',
            role: 'Senior Web Developer',
            image: '/statics/images/vlad.png'
          },
        ],
      }
    },
    computed: {
      style() {
        return {
          width: '340px',
          height: '263px',
          backgroundImage: `url('https://raw.githubusercontent.com/quasarframework/quasar-ui-qflashcard/dev/demo/src/statics/bgimg.jpg')`, // eslint-disable-line
          textAlign: 'center',
          boxShadow: '1px 1px 2px #e6e6e6',
          display: 'inline-block'
        }
      },
      team_style() {
        return {
          width: '260px',
          height: '263px',
          backgroundImage: `url('https://raw.githubusercontent.com/quasarframework/quasar-ui-qflashcard/dev/demo/src/statics/bgimg.jpg')`, // eslint-disable-line
          textAlign: 'center',
          boxShadow: '1px 1px 2px #e6e6e6',
          display: 'inline-block'
        }
      }
    },
    methods: {
      scrollToElement (id) {
        let el = document.getElementById(id);
        const target = getScrollTarget(el);
        const offset = el.offsetTop + 3;
        const duration = 900;

        setScrollPosition(target, offset, duration);
      },
      changeBgColor() {
        this.theme_color = this.bg_color;
        this.background_style = 'background-color:' + this.bg_color.split(')')[0] + ',0.7)';
      },
      hoverOver: function(index) {
        this['about_heading_color_' + index] = this.theme_color;
        this['about_heading_' + index] = ['animated', 'bounceIn'];              
      },
      hoverOutTimeout: function(index) {
        this['about_heading_color_' + index] = '#424242';
        setTimeout(() => {
          this['about_heading_' + index] = [];                
        }, 1000);
      },
    }
  }
</script>

<style lang="sass" scoped>
  .main_line
    font-size: 75px;
    letter-spacing: 5px;
    line-height: 60px;
    font-weight: 600;

  .custom-caption
    text-align: center;
    padding: 12px;
    color: white;

  .animation_1
    -webkit-animation: bounceIn 1s ease-in 800ms both;
    animation: bounceIn 1s ease-in 800ms both;

  .animation_2
    -webkit-animation: flipInX 2s ease-in-out 800ms both;
    animation: flipInX 1s ease-in-out 800ms both;

  .animation_3
    -webkit-animation: lightSpeedIn 1s ease-in 800ms both;
    animation: lightSpeedIn 1s ease-in 800ms both;

  .description
    padding: 10px
    background-color: black
    color: white
    box-shadow: 1px 1px 2px #e6e6e6

  .my-header
    width: 200px
    top: 0
    height: 45px
    color: black
    background-color: rgba(255,255,255, 0.8)
    text-transform: uppercase
    text-align: center
    font-size: 17px
    margin: 20px 0 0 68px
    padding: 25px

  .my-text
    width: 100%
    top: 0
    height: 90px
    color: white
    text-align: center
    font-size: 15px
    margin: 79px 0 0 0
    padding: 20px
    line-height: normal
    font-family: Georgia, serif
    font-style: italic

  .my-button-container
    width: 100%

  .my-button
    text-decoration: none
    text-transform: uppercase
    margin: 0 0 20px 0
    text-align: center
    padding: 7px 14px
    background-color: #000
    color: #fff
    text-transform: uppercase
    box-shadow: 0 0 1px #000
    transition-delay: 0.2s

  .my-button:hover
    box-shadow: 0 0 5px #000

  .box-shadow:hover
    box-shadow: 0 10px 13px -6px rgba(0, 0, 0, 0.2), 0 20px 31px 3px rgba(0, 0, 0, 0.14), 0 8px 38px 7px rgba(0, 0, 0, 0.12) !important;

  .my-card
    width: 350px
    max-width: 350px
    margin-top: 10px

  .team-header
    width: 100%
    top: 0
    height: 45px
    color: white
    text-transform: uppercase
    text-align: center
    font-size: 17px
    margin: 60px 0 0 0
    padding: 12px

  .team-text
    width: 100%
    top: 0
    height: 90px
    color: white
    text-align: center
    font-size: 15px
    margin: 100px 0 0 0
    padding: 20px
    line-height: normal
    font-family: Georgia, serif
    font-style: italic
  
  .quote
    background: url(/statics/images/parallax.jpg);
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    background-repeat: no-repeat;
  
  .pricing
    background: url(/statics/images/pricing.jpg);
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    background-repeat: no-repeat;
  
  .contact_us
    background: url(/statics/images/contact_us.jpg);
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    background-repeat: no-repeat;
  
  .custom_tab
    width: 130px;
</style>
