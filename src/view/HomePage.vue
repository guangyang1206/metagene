<template>
  <div id="HomePage">
    <!-- 轮播图 -->
    <div id="swiper" class="container-fuild">
      <div class="swiper-container banner-swiper">
        <div class="swiper-wrapper">
          <div class="swiper-slide" v-for="(item,index) in swiperList" :key="index">
            <img class="swiper-lazy" :data-src="item.img" alt="轮播图">
            <div class="swiper-lazy-preloader"></div>
            <div class="swiper-slide-title">
                <h1>{{item.title}}</h1>
                <p>{{item.content}}</p>
            </div>
          </div>
        </div>
        <!-- 如果需要分页器 -->
        <div class="swiper-pagination"></div>

        <!-- 如果需要导航按钮 -->
<!--        <div class="swiper-button-prev"></div>-->
<!--        <div class="swiper-button-next"></div>-->
      </div>
    </div>
    <!-- 大数据管理系统 -->
    <div id="bigData" class="container-fuild">
      <div class="row bigData-container">
        <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
          <img class="img-responsive" src="@/assets/img/img1.png" alt="大数据管理系统">
        </div>
        <div class="col-xs-12 col-sm-12 col-md-6">
          <h2 class="bigData-title">
            大数据基因管理
            <small>/ Big Data Management System</small>
          </h2>
          <p>当今最领先的响应式自助建站平台。无论您是普通互联网用户，还是专业网站制作人员，都能使用起飞页设计出最具专业水准的网站。想创建一个简单的单页式站点，还是一个专业的公司网站，亦或是一个别具一格的博客？起飞页可以满足您的所有需求。</p>
          <p>我们的流线式网页布局设计方案和可视化图文内容编辑模式让网站制作和维护成为一件轻松惬意的事。无论您是普通互联网用户，还是专业网站制作人员。</p>
          <h2 class="bigData-device">PC/PAD/Phone &nbsp; 全设备支持</h2>
          <a href="#" class="btn btn-lg btn-block btn-info">联系我们</a>
        </div>
      </div>
    </div>
    <!-- 您身边的IT专家 -->
    <div id="contactUs" class="container-fuild text-center">
      <div class="container contactUs-container wow slideInUp">
        <h1>您身边的基因顾问</h1>
        <h3>7x24小时提供出色的服务</h3>
        <button
          class="btn btn-default btn-sm"
          onmouseleave="this.style.borderColor='#ffffff'; this.style.backgroundColor='#ffffff'; this.style.color='#3f3f3f';"
          onmouseenter="this.style.backgroundColor='transparent'; this.style.borderColor='#ffffff'; this.style.color='#ffffff';"
        >了解更多</button>
        <div class="contactUs-contactWay">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
    </div>
    <!-- 客户评价 -->
<!--    <div id="customer" class="container-fuild">-->
<!--      <div class="container customer-container">-->
<!--        <p class="customer-title text-center">合作伙伴</p>-->
<!--        <div class="swiper-container customer-swiper hidden-xs">-->
<!--&lt;!&ndash;          <div class="swiper-wrapper">&ndash;&gt;-->
<!--&lt;!&ndash;            <div&ndash;&gt;-->
<!--&lt;!&ndash;              class="swiper-slide customer-block"&ndash;&gt;-->
<!--&lt;!&ndash;              v-for="(item,index) in customerList"&ndash;&gt;-->
<!--&lt;!&ndash;              :key="index"&ndash;&gt;-->
<!--&lt;!&ndash;            >&ndash;&gt;-->
<!--&lt;!&ndash;              <div class="customer-logo">&ndash;&gt;-->
<!--&lt;!&ndash;                <img class="center-block" :src="item.logo" alt="logo">&ndash;&gt;-->
<!--&lt;!&ndash;              </div>&ndash;&gt;-->
<!--&lt;!&ndash;              <div class="customer-yh">&ndash;&gt;-->
<!--&lt;!&ndash;                <img src="@/assets/img/yinhao.png" alt="引号">&ndash;&gt;-->
<!--&lt;!&ndash;              </div>&ndash;&gt;-->
<!--&lt;!&ndash;              <div class="customer-content1">&ndash;&gt;-->
<!--&lt;!&ndash;                <small>{{item.content}}</small>&ndash;&gt;-->
<!--&lt;!&ndash;              </div>&ndash;&gt;-->
<!--&lt;!&ndash;              <div class="customer-content2">{{item.title}}</div>&ndash;&gt;-->
<!--&lt;!&ndash;            </div>&ndash;&gt;-->
<!--&lt;!&ndash;          </div>&ndash;&gt;-->
<!--          &lt;!&ndash; 如果需要导航按钮 &ndash;&gt;-->
<!--&lt;!&ndash;          <div class="swiper-button-prev"></div>&ndash;&gt;-->
<!--&lt;!&ndash;          <div class="swiper-button-next"></div>&ndash;&gt;-->
<!--&lt;!&ndash;          <div class="vc_row wpb_row vc_row-fluid row vc_custom_1524036800444"><div class="wpb_column vc_column_container vc_col-sm-12"><div class="vc_column-inner"><div class="wpb_wrapper">&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;            <h2 style="font-size: 22px;color: #047abc;text-align: left" class="vc_custom_heading vc_custom_1524811768850">Customers and Collaborators</h2>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;            <div class="wpb_text_column wpb_content_element ">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;              <div class="wpb_wrapper">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                <div class="wondercarousellightbox_options" data-skinsfoldername="" data-jsfolder="https://www.petagene.com/wp-content/plugins/wonderplugin-carousel/engine/" style="display:none;"></div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                <div class="wonderplugincarousel-container" id="wonderplugincarousel-container-2">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                  <div class="wonderplugincarousel" id="wonderplugincarousel-2" data-carouselid="2" data-width="200" data-height="60"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-skin="gallery" data-showimgtitle="false" data-sameheight="true" data-sameheightresponsive="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-fullwidth="false" data-centerimage="false" data-fitimage="false" data-fitcenterimage="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-fixaspectratio="false" data-autoplay="true" data-random="false" data-circular="true"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-pauseonmouseover="true" data-continuous="true" data-responsive="true" data-showhoveroverlay="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-showhoveroverlayalways="false" data-hidehoveroverlayontouch="false" data-lightboxresponsive="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxshownavigation="false" data-lightboxnogroup="false" data-lightboxshowtitle="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxshowdescription="false" data-lightboxaddsocialmedia="false" data-usescreenquery="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-donotinit="false" data-addinitscript="false" data-doshortcodeontext="false" data-lightboxshowsocial="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxshowfacebook="true" data-lightboxshowtwitter="true" data-lightboxshowpinterest="true"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxsocialrotateeffect="true" data-donotcircularforless="false" data-deferloading="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-hidecontainerbeforeloaded="false" data-hidecontaineroninit="true" data-lightboximagekeepratio="true"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-showplayvideo="false" data-triggerresize="false" data-lightboxfullscreenmode="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxcloseonoverlay="true" data-lightboxvideohidecontrols="false" data-lightboxautoslide="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxshowtimer="true" data-lightboxshowplaybutton="true" data-lightboxalwaysshownavarrows="false"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxshowtitleprefix="true" data-spacing="4" data-rownumber="1" data-visibleitems="6"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-arrowstyle="mouseover" data-arrowimage="arrows-48-48-2.png" data-arrowwidth="48" data-arrowheight="48"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-navstyle="none" data-navimage="bullet-16-16-0.png" data-navwidth="16" data-navheight="16" data-navspacing="8"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-hoveroverlayimage="hoveroverlay-64-64-5.png" data-lightboxthumbwidth="90" data-lightboxthumbheight="60"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxthumbtopmargin="12" data-lightboxthumbbottommargin="4" data-lightboxbarheight="64"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxtitlebottomcss="{color:#333; font-size:14px; font-family:Armata,sans-serif,Arial; overflow:hidden; text-align:left;}"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxdescriptionbottomcss="{color:#333; font-size:12px; font-family:Arial,Helvetica,sans-serif; overflow:hidden; text-align:left; margin:4px 0px 0px; padding: 0px;}"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-continuousduration="2500" data-autoplaydir="left" data-scrollmode="page" data-interval="3000"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-transitionduration="1000" data-lightboxtitlestyle="bottom" data-lightboximagepercentage="75"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxdefaultvideovolume="1" data-lightboxoverlaybgcolor="#000" data-lightboxoverlayopacity="0.9"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxbgcolor="#fff" data-lightboxtitleprefix="%NUM / %TOTAL"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxtitleinsidecss="color:#fff; font-size:16px; font-family:Arial,Helvetica,sans-serif; overflow:hidden; text-align:left;"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxdescriptioninsidecss="color:#fff; font-size:12px; font-family:Arial,Helvetica,sans-serif; overflow:hidden; text-align:left; margin:4px 0px 0px; padding: 0px;"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-playvideoimage="playvideo-64-64-0.png" data-playvideoimagepos="center" data-imgtitle="title"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-circularlimit="3" data-deferloadingdelay="0" data-lightboxsocialposition="position:absolute;top:100%;right:0;"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxsocialpositionsmallscreen="position:absolute;top:100%;right:0;left:0;"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxsocialdirection="horizontal" data-lightboxsocialbuttonsize="32" data-lightboxsocialbuttonfontsize="18"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-sameheightmediumscreen="769" data-sameheightmediumheight="200" data-sameheightsmallscreen="415"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-sameheightsmallheight="150" data-triggerresizedelay="100" data-lightboxslideinterval="5000"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxtimerposition="bottom" data-lightboxtimercolor="#dc572e" data-lightboxtimeropacity="1"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-lightboxbordersize="0" data-lightboxborderradius="0"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-screenquery="{ 'tablet': { 'screenwidth': 800, 'visibleitems': 2 }, 'mobile': { 'screenwidth': 480, 'visibleitems': 1 } }"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       data-jsfolder="https://www.petagene.com/wp-content/plugins/wonderplugin-carousel/engine/"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                       style="display: block; position: relative; margin: 0px auto; width: 100%; max-width: 1200px; direction: ltr;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                    <div class="amazingcarousel-list-container"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                         style="overflow: visible; position: relative; margin: 0px auto; width: 1000px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                      <div class="amazingcarousel-list-wrapper" style="overflow: hidden; width: 1000px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                        <ul class="amazingcarousel-list"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            style="display: block; position: relative; list-style-type: none; list-style-image: none; background-image: none; background-color: transparent; padding: 0px; margin: 0px 0px 0px -175.194px; white-space: nowrap; width: auto;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-0"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/10/AZ_new_LR-1.jpeg" alt="AstraZeneca"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-title="AstraZeneca" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px; visibility: visible;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-1"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/NHS.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="NHS" data-title="NHS" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px; visibility: visible;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2019/08/Univ-of-Gothenburg.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="University of Gothenburg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2019/08/Univ-of-Gothenburg-300x221.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img src="https://www.petagene.com/wp-content/uploads/2019/08/Univ-of-Gothenburg.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        alt="University of Gothenburg logo" data-title="University of Gothenburg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        style="width: auto; height: 60px; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px; visibility: visible;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-3"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/lux.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="University of Luxembourg" data-title="University of Luxembourg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px; visibility: visible;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-4"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/01/na_alliance-partner_2c_rgb_crop.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="NetApp Alliance Partner logo" data-title="NetApp" data-description="NetApp Alliance Partner logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px; visibility: visible;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-5"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2018/06/dell-emc.png" alt="DellEMC" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-6"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/google.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="Google" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-7"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2019/08/wekaio_logo_web.png" title="Weka.io logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2019/08/wekaio_logo_web-300x167.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img src="https://www.petagene.com/wp-content/uploads/2019/08/wekaio_logo_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        alt="Weka.io logo" data-title="Weka.io logo" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-8"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/cam.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="University of Cambridge" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-9"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/intel.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="Intel" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-10"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/PHI.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="Precision Health Informatics"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      data-title="Precision Health Informatics" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-11"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2019/08/KNIH_logo_eng1_colour.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="National Institute of Health Republic of Korea logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2019/08/KNIH_logo_eng1_colour-300x57.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/08/KNIH_logo_eng1_colour.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="National Institute of Health Republic of Korea logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-title="National Institute of Health Republic of Korea logo" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-12"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://www.cegat.de/en/" target="_blank"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2020/01/CeGaT_Logo_RGB_m-S_Color-carousel.jpg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="CeGaT Logo" data-description="CeGaT logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-13"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://www.prinsesmaximacentrum.nl/en" target="_blank"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/08/prinses-maxima-centrum-logo-en.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="Princess Maxima Center logo" data-title="Princess Maxima Center logo" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-14"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://www.sentieon.com/" target="_blank"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/08/Sentieonlogo_web.png" alt="Sentieon logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-title="Sentieon logo" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-15"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2019/08/ToMMo-logo_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="Tohoku Medical Megabank Organisation"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2019/08/ToMMo-logo_web-300x200.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img src="https://www.petagene.com/wp-content/uploads/2019/08/ToMMo-logo_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        alt="Tohoku Medical Megabank Organisation logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        data-title="Tohoku Medical Megabank Organisation" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-16"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2019/08/Baylor_College_of_Medicine_Logo_square_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="Baylor College of Medicine logo" data-description="Baylor College of Medicine"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2019/08/Baylor_College_of_Medicine_Logo_square_web-300x300.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/08/Baylor_College_of_Medicine_Logo_square_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="Baylor College of Medicine logo" data-title="Baylor College of Medicine logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-description="Baylor College of Medicine"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-17"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://wwwen.uni.lu/lcsb" target="_self"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/08/LCSB-words-logo_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="Luxembourg Centre for Systems Biomedicine logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-title="Luxembourg Centre for Systems Biomedicine" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-18"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/kings.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="King's College London" data-title="King's College London"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-19"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://www.tgen.org/" target="_blank"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/10/TGen_Color_LOGO_medium.png" alt="TGen"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-title="TGen" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-20"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://www.petagene.com/wp-content/uploads/2021/03/elixir.jpg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                    title="elixir"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                    data-thumbnail="https://www.petagene.com/wp-content/uploads/2021/03/elixir-300x129.jpg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                    class="wondercarousellightbox wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                    data-group="wondercarousellightbox-2" data-mediatype="0"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2021/03/elixir.jpg" alt="elixir" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-21"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2021/03/LifeCell-Corporate-Logo.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="LifeCell Corporate Logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2021/03/LifeCell-Corporate-Logo-300x83.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2021/03/LifeCell-Corporate-Logo.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="LifeCell Corporate Logo" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-22"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2021/05/BioSkrybGenomics_Logo.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="BioSkryb Genomics"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2021/05/BioSkrybGenomics_Logo.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2021/05/BioSkrybGenomics_Logo.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="BioSkryb Genomics" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-0"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/10/AZ_new_LR-1.jpeg" alt="AstraZeneca"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-title="AstraZeneca" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-1"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/NHS.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="NHS" data-title="NHS" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2019/08/Univ-of-Gothenburg.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="University of Gothenburg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2019/08/Univ-of-Gothenburg-300x221.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img src="https://www.petagene.com/wp-content/uploads/2019/08/Univ-of-Gothenburg.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        alt="University of Gothenburg logo" data-title="University of Gothenburg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-3"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/lux.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="University of Luxembourg" data-title="University of Luxembourg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-4"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/01/na_alliance-partner_2c_rgb_crop.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="NetApp Alliance Partner logo" data-title="NetApp" data-description="NetApp Alliance Partner logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-5"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2018/06/dell-emc.png" alt="DellEMC" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-6"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/google.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="Google" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-7"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2019/08/wekaio_logo_web.png" title="Weka.io logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2019/08/wekaio_logo_web-300x167.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img src="https://www.petagene.com/wp-content/uploads/2019/08/wekaio_logo_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        alt="Weka.io logo" data-title="Weka.io logo" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-8"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/cam.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="University of Cambridge" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-9"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/intel.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="Intel" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-10"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/PHI.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="Precision Health Informatics"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      data-title="Precision Health Informatics" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-11"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2019/08/KNIH_logo_eng1_colour.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="National Institute of Health Republic of Korea logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2019/08/KNIH_logo_eng1_colour-300x57.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/08/KNIH_logo_eng1_colour.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="National Institute of Health Republic of Korea logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-title="National Institute of Health Republic of Korea logo" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-12"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://www.cegat.de/en/" target="_blank"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2020/01/CeGaT_Logo_RGB_m-S_Color-carousel.jpg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="CeGaT Logo" data-description="CeGaT logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-13"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://www.prinsesmaximacentrum.nl/en" target="_blank"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/08/prinses-maxima-centrum-logo-en.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="Princess Maxima Center logo" data-title="Princess Maxima Center logo" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-14"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://www.sentieon.com/" target="_blank"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/08/Sentieonlogo_web.png" alt="Sentieon logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-title="Sentieon logo" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-15"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2019/08/ToMMo-logo_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="Tohoku Medical Megabank Organisation"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2019/08/ToMMo-logo_web-300x200.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img src="https://www.petagene.com/wp-content/uploads/2019/08/ToMMo-logo_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        alt="Tohoku Medical Megabank Organisation logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        data-title="Tohoku Medical Megabank Organisation" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                        style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-16"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2019/08/Baylor_College_of_Medicine_Logo_square_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="Baylor College of Medicine logo" data-description="Baylor College of Medicine"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2019/08/Baylor_College_of_Medicine_Logo_square_web-300x300.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/08/Baylor_College_of_Medicine_Logo_square_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="Baylor College of Medicine logo" data-title="Baylor College of Medicine logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-description="Baylor College of Medicine"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-17"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://wwwen.uni.lu/lcsb" target="_self"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/08/LCSB-words-logo_web.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="Luxembourg Centre for Systems Biomedicine logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-title="Luxembourg Centre for Systems Biomedicine" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-18"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><img src="https://www.petagene.com/wp-content/uploads/2018/06/kings.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      alt="King's College London" data-title="King's College London"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                      style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-19"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://www.tgen.org/" target="_blank"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2019/10/TGen_Color_LOGO_medium.png" alt="TGen"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-title="TGen" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-20"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a href="https://www.petagene.com/wp-content/uploads/2021/03/elixir.jpg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                    title="elixir"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                    data-thumbnail="https://www.petagene.com/wp-content/uploads/2021/03/elixir-300x129.jpg"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                    class="wondercarousellightbox wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                                                    data-group="wondercarousellightbox-2" data-mediatype="0"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2021/03/elixir.jpg" alt="elixir" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-21"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2021/03/LifeCell-Corporate-Logo.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="LifeCell Corporate Logo"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2021/03/LifeCell-Corporate-Logo-300x83.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2021/03/LifeCell-Corporate-Logo.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="LifeCell Corporate Logo" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <li class="amazingcarousel-item amazingcarousel-item-22"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              style="display: inline-block; position: relative; background-image: none; background-color: transparent; margin: 0px; padding: 0px; float: none;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            <div class="amazingcarousel-item-container" style="position: relative; margin: 0px 2px;">&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              <div class="amazingcarousel-image"><a&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                href="https://www.petagene.com/wp-content/uploads/2021/05/BioSkrybGenomics_Logo.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                title="BioSkryb Genomics"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-thumbnail="https://www.petagene.com/wp-content/uploads/2021/05/BioSkrybGenomics_Logo.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                class="wondercarousellightbox wondercarousellightbox-2" data-group="wondercarousellightbox-2"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                data-mediatype="0"><img&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                src="https://www.petagene.com/wp-content/uploads/2021/05/BioSkrybGenomics_Logo.png"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                alt="BioSkryb Genomics" data-description=""&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                                style="width: auto; height: 60px; visibility: visible; max-width: none; max-height: 100%; margin-top: 0px; margin-left: 0px;"></a>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          </li>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <div style="clear:both;"></div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                        </ul>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                      </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                      <div class="amazingcarousel-prev"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                           style="overflow: hidden; position: absolute; cursor: pointer; width: 48px; height: 48px; background: url('https://www.petagene.com/wp-content/plugins/wonderplugin-carousel/engine/arrows-48-48-2.png') left top no-repeat; display: none;"></div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                      <div class="amazingcarousel-next"&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                           style="overflow: hidden; position: absolute; cursor: pointer; width: 48px; height: 48px; background: url('https://www.petagene.com/wp-content/plugins/wonderplugin-carousel/engine/arrows-48-48-2.png') right top no-repeat; display: none;"></div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                    </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                    <div class="amazingcarousel-nav"></div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                  </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;              </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;            </div>&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;          </div></div></div></div>&ndash;&gt;-->
<!--        </div>-->
<!--        <div class="row visible-xs customer-block">-->
<!--          <div class="col-xs-12" v-for="(item,index) in customerList" :key="index">-->
<!--            <div class="customer-logo">-->
<!--              <img class="center-block" :src="item.logo" alt="logo">-->
<!--            </div>-->
<!--            <div class="customer-yh">-->
<!--              <img src="@/assets/img/yinhao.png" alt="引号">-->
<!--            </div>-->
<!--            <div class="customer-content1">-->
<!--              <small>{{item.content}}</small>-->
<!--            </div>-->
<!--            <div class="customer-content2">-->
<!--              <small>{{item.title}}</small>-->
<!--            </div>-->
<!--          </div>-->
<!--        </div>-->
<!--      </div>-->
<!--    </div>-->
    <!-- 为什么选择我们 -->
    <div id="whyChooseUs" class="conatiner-fuild">
      <div class="container">
        <div class="whyChooseUs-title text-center">
          <p>我们的优势</p>
          <p>THE REASON TO CHOOSING US</p>
        </div>
        <div class="row">
          <div
            class="col-xs-12 col-sm-6 col-md-3 server-wrapper"
            v-for="(item,index) in serverList"
            :key="index"
          >
            <div
              class="server-block wow slideInUp"
              onmouseenter="this.style.color='#28f';this.style.borderColor='#28f'"
              onmouseleave="this.style.color='#666';this.style.borderColor='#ccc'"
            >
              <img class="center-block" :src="item.logo" alt="logo">
              <p class="text-center">{{item.title}}</p>
              <div
                class="text-center"
                v-html="item.content"
                onmouseenter="this.style.color='#28f'"
                onmouseleave="this.style.color='#ccc'"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Swiper from "swiper";
import { WOW } from 'wowjs';
export default {
  name: "HomePage",
  data() {
    return {
      swiperList: [
        {
          img: require("@/assets/img/banner3.png"),
          path: "",
          title: 'Reducing Storage Costs and Data Transfer Times',
          content: '宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介',
        },
        {
          img: require("@/assets/img/banner4.png"),
          path: "",
          title: '您身边的基因顾问',
          content: '宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介',
        },
        {
          img: require("@/assets/img/banner1.png"),
          path: "",
          title: '标题1',
          content: '宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介',
        },
        {
          img: require("@/assets/img/banner2.jpg"),
          path: "",
          title: '标题2',
          content: '宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介',
        },
      ],
      customerList: [
        {
          logo: require("@/assets/img/logo_hp.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_kk.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_toyota.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_kk.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_hp.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_toyota.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_kk.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_hp.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_toyota.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_hp.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_kk.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_hp.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        }
      ],
      serverList: [
        {
          logo: require("@/assets/img/tel.png"),
          title: "核心优势1",
          content: "<p>由专业客服提供人工服务</p>负责疑难问题和故障受理"
        },
        {
          logo: require("@/assets/img/computer.png"),
          title: "核心优势2",
          content: "<p>利用远程视频工具，提供协助</p>帮助客户进行调试、解决故障"
        },
        {
          logo: require("@/assets/img/qq.png"),
          title: "核心优势3",
          content: "<p>利用企业QQ提供在线解答</p>帮助企业快速准确解决问题和故障"
        },
        {
          logo: require("@/assets/img/skill.png"),
          title: "核心优势4",
          content: "<p>由技术支持工程师，负责问题解答</p>需求受理及故障受理"
        }
      ]
    };
  },
  mounted() {

    /* banner-swiper */
    new Swiper(".banner-swiper", {
      loop: true, // 循环模式选项
      effect: 'fade',
      //自动播放
      autoplay: {
        delay: 3000,
        stopOnLastSlide: false,
        disableOnInteraction: false
      },
      // 如果需要分页器
      pagination: {
        el: ".swiper-pagination",
        clickable: true
      },
      // 如果需要前进后退按钮
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev"
      },
      // 延迟加载
      lazy: {
        loadPrevNext: true
      },
      observer: true, //修改swiper自己或子元素时，自动初始化swiper
      observeParents: true //修改swiper的父元素时，自动初始化swiper
    });
    /* customer-swiper */
    new Swiper(".customer-swiper", {
      loop: true, // 循环模式选项
      slidesPerView: 3,
      //自动播放
      autoplay: {
        delay: 3000,
        stopOnLastSlide: false,
        disableOnInteraction: false
      },
      // 如果需要前进后退按钮
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev"
      },
      observer: true, //修改swiper自己或子元素时，自动初始化swiper
      observeParents: true //修改swiper的父元素时，自动初始化swiper
    });
    /* wowjs动画 */
    var wow = new WOW({
      boxClass: 'wow',
      animateClass: 'animated',
      offset: 0,
      mobile: true,
      live: true
    })
    wow.init();
  }
};
</script>

<style scoped>
@import url(https://fonts.googleapis.com/css?family=Open+Sans);

#wonderplugincarousel-2 .amazingcarousel-image {
  position: relative;
  padding: 4px;
  -moz-box-shadow: 0 0px 0px rgba(0, 0, 0, 0.2);
  -webkit-box-shadow: 0 0px 0px rgba(0, 0, 0, 0.2);
  box-shadow: 0 0px 0px rgba(0, 0, 0, 0.2);
}

#wonderplugincarousel-2 .amazingcarousel-image img {
  display: block;
  width: 100%;
  max-width: 100%;
  border: 0;
  margin: 0;
  padding: 0;
  -moz-border-radius: 0px;
  -webkit-border-radius: 0px;
  border-radius: 0px;
}

#wonderplugincarousel-2 .amazingcarousel-title {
  position: relative;
  font: bold 12px "Open Sans", sans-serif;
  color: #333333;
  margin: 6px;
  text-align: left;
  line-height: 14px;
  overflow: hidden;
}

#wonderplugincarousel-2 .amazingcarousel-description {
  position: relative;
  font: 12px "Open Sans", sans-serif;
  color: #333333;
  margin: 6px;
  text-align: left;
  line-height: 14px;
  overflow: hidden;
}

#wonderplugincarousel-2 .amazingcarousel-list-container {
  padding: 8px 0;
}

#wonderplugincarousel-2 .amazingcarousel-item-container {
  text-align: center;
  padding: 4px;
}

#wonderplugincarousel-2 .amazingcarousel-prev {
  left: 0%;
  top: 50%;
  margin-left: -60px;
  margin-top: -24px;
}

#wonderplugincarousel-2 .amazingcarousel-next {
  right: 0%;
  top: 50%;
  margin-right: -60px;
  margin-top: -24px;
}

#wonderplugincarousel-2 .amazingcarousel-nav {
  position: absolute;
  width: 100%;
  top: 100%;
}

#wonderplugincarousel-2 .amazingcarousel-bullet-wrapper {
  margin: 4px auto;
}

.amazingcarousel-socialmedia-button {
  display: inline-block;
  margin: 4px;
}

.amazingcarousel-socialmedia-button a {
  box-shadow: none;
}

.amazingcarousel-socialmedia-icon {
  display: table-cell;
  width: 32px;
  height: 32px;
  font-size: 18px;
  border-radius: 50%;
  color: #fff;
  vertical-align: middle;
  text-align: center;
  cursor: pointer;
  padding: 0;
}

.amazingcarousel-socialmedia-rotate {
  transition: transform .4s ease-in;
}

.amazingcarousel-socialmedia-rotate:hover {
  transform: rotate(360deg);
}
/* 整体盒子 */
#HomePage {
  width: 100%;
}

/* 轮播图 */
#swiper {
  height: 600px;
}
#swiper .banner-swiper {
  width: 100%;
  height: 100%;
}
#swiper .banner-swiper .swiper-slide img {
  width: 100%;
  height: 100%;
}
#swiper .banner-swiper .swiper-slide{
  position: relative;
}
#swiper .banner-swiper .swiper-slide-title {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 999999999;
  width: 100%;
  height: 100%;
  color: #fff;
  background: rgba(51, 51, 51, 0.534);
  text-align: center;
  line-height: 80px;
}
#swiper .banner-swiper .swiper-slide-title > h1{
  font-size: 50px;
  margin-top: 12%;
}
#swiper .banner-swiper .swiper-slide-title > p{
  font-size: 20px;
  margin-top: 1%;
  font-weight: 700;
}
/* 大数据管理系统 */
#bigData {
  padding: 100px;
  transition: all ease 0.6s;
  box-sizing: border-box;
}
#bigData .bigData-title {
  padding-bottom: 10px;
  border-bottom: 1px solid #ccc;
}
#bigData p {
  font-size: 14px;
  color: #333;
  line-height: 2rem;
}
#bigData .bigData-device {
  margin: 50px 0 20px;
}

/* 您身边的IT专家 */
#contactUs {
  color: #fff;
  height: 400px;
  background: url("../assets/img/contact_us_bg.jpg") 0 0 no-repeat;
  background-size: 100% 100%;
  transition: all ease 0.6s;
}
#contactUs .contactUs-container {
  padding-top: 50px;
}
#contactUs .contactUs-container button {
  width: 300px;
  height: 50px;
  margin-top: 40px;
}
#contactUs .contactUs-container .contactUs-contactWay span {
  display: inline-block;
  width: 48px;
  height: 48px;
  margin: 30px;
}
#contactUs .contactUs-container .contactUs-contactWay span:nth-of-type(1) {
  background: url("../assets/img/weixin.png") 0 0 no-repeat;
  background-size: 100% 100%;
}
#contactUs .contactUs-container .contactUs-contactWay span:nth-of-type(2) {
  background: url("../assets/img/weibo.png") 0 0 no-repeat;
  background-size: 100% 100%;
}
#contactUs .contactUs-container .contactUs-contactWay span:nth-of-type(3) {
  background: url("../assets/img/twitter.png") 0 0 no-repeat;
  background-size: 100% 100%;
}

/* 客户评价 */
#customer {
  padding: 50px 0;
  box-sizing: border-box;
  background: #efefef;
  transition: all ease 0.6s;
}
#customer .customer-title {
  font-size: 30px;
  color: rgb(102, 102, 102);
  margin: 0 0 30px;
}
#customer .customer-block {
  background: #fff;
  padding: 30px;
}
#customer .customer-logo img {
  width: 94px;
  height: 94px;
  border: 1px solid #ccc;
}
#customer .customer-yh img {
  width: 34px;
  height: 34px;
}
#customer .customer-content1 {
  padding-bottom: 20px;
  border-bottom: 1px solid #0ce9f1;
}
#customer .customer-content2 {
  padding-top: 20px;
}
/* 为什么选择我们 */
#whyChooseUs {
  padding: 100px;
}
#whyChooseUs .whyChooseUs-title {
  margin-bottom: 50px;
}
#whyChooseUs .whyChooseUs-title p:nth-of-type(1) {
  font-size: 25px;
  font-weight: 500;
}
#whyChooseUs .whyChooseUs-title p:nth-of-type(2) {
  font-size: 14px;
}
#whyChooseUs .server-block {
  padding: 50px 20px;
  border: 1px solid #ccc;
  border-bottom: 5px solid #ccc;
}
#whyChooseUs .server-block img {
  width: 48px;
  height: 48px;
}
#whyChooseUs .server-block > p {
  font-size: 20px;
  margin: 30px 0;
}
#whyChooseUs .server-block > div {
  color: #ccc;
}
/* 媒体查询（手机） */
@media screen and (max-width: 768px) {
  #swiper {
    height: 200px;
  }
  #bigData {
    padding: 30px;
  }
  #bigData .bigData-title {
    font-size: 20px;
  }
  #bigData .bigData-device {
    font-size: 20px;
    margin: 10px 0 10px;
  }
  #contactUs {
    height: 200px;
    transition: all ease 0.6s;
  }
  #contactUs .contactUs-container {
    padding-top: 0;
  }
  #contactUs .contactUs-container h1 {
    font-size: 25px;
  }
  #contactUs .contactUs-container h3 {
    font-size: 18px;
  }
  #contactUs .contactUs-container button {
    width: 200px;
    height: 30px;
    margin-top: 20px;
  }
  #contactUs .contactUs-container .contactUs-contactWay span {
    display: inline-block;
    width: 28px;
    height: 28px;
    margin: 10px;
  }
  #customer {
    padding: 30px 0;
    box-sizing: border-box;
    background: #fff;
  }
  #customer .customer-title {
    font-size: 16px;
    font-weight: bold;
  }
  #customer .customer-logo img {
    width: 48px;
    height: 48px;
  }
  #customer .customer-block {
    padding: 30px;
  }
  #customer .customer-block > div {
    padding: 30px 0;
  }
  #whyChooseUs {
    padding: 20px 0;
    transition: all ease 0.6s;
  }
  #whyChooseUs .whyChooseUs-title p:nth-of-type(1) {
    font-size: 20px;
    font-weight: 700;
  }
  #whyChooseUs .whyChooseUs-title p:nth-of-type(2) {
    font-size: 12px;
  }
  #whyChooseUs .server-block {
    padding: 50px 0;
    border: 1px solid #ccc;
    border-bottom: 5px solid #ccc;
  }
  #whyChooseUs .server-block img {
    width: 48px;
    height: 48px;
  }
  #whyChooseUs .server-block > p {
    font-size: 20px;
    margin: 30px 0;
  }
  #whyChooseUs .server-block > div {
    color: #ccc;
  }
}

/* 媒体查询（平板） */
@media screen and (min-width: 768px) and (max-width: 996px) {
  #swiper {
    height: 400px;
  }
  #bigData {
    padding: 60px;
  }
  #bigData .bigData-title {
    font-size: 30px;
  }
  #bigData .bigData-device {
    font-size: 30px;
    margin: 30px 0 15px;
  }
  #contactUs {
    height: 300px;
  }
  #contactUs .contactUs-container {
    padding-top: 50px;
  }
  #contactUs .contactUs-container h1 {
    font-size: 30px;
  }
  #contactUs .contactUs-container h3 {
    font-size: 20px;
  }
  #contactUs .contactUs-container button {
    width: 300px;
    height: 50px;
    margin-top: 30px;
  }
  #contactUs .contactUs-container .contactUs-contactWay span {
    display: inline-block;
    width: 32px;
    height: 32px;
    margin: 15px;
  }
  #customer .customer-title {
    font-size: 24px;
  }
  #whyChooseUs {
    padding: 20px 0;
  }
}
</style>

