<script setup>
import { ROUTES } from '@/app/router/helper';
import HeaderMenuIndex from '@/components/HeaderMenuIndex/HeaderMenuIndex.vue';
// import HeaderCompareLink from '@/components/HeaderCompareLink/HeaderCompareLink.vue';
import RecentArrivalsGoods from '@/components/RecentArrivalsGoods/RecentArrivalsGoods.vue';
// import HeaderFavoriteLink from '@/components/HeaderFavoriteLink/HeaderFavoriteLink.vue';
import MobileOpenMenu from '@/components/MobileOpenMenu/MobileOpenMenu.vue';
import SearchMobile from '@/components/SearchMobile/SearchMobile.vue';
import MainbannerForm from '@/components/MainbannerForm/MainbannerForm.vue';
import MainbannerFormMob from '@/components/MainbannerFormMob/MainbannerFormMob.vue';
import FeedBack from '@/components/FeedBack/FeedBack.vue';
import Search from '@/components/Search/Search.vue';
import { BACKEND_URL_API_PRICELIST } from '@/app/stores/helper';
import { useCartsStore } from '@/app/stores/modules/cart';

const { cartCount } = useCartsStore();
</script>

<template>
    <div>
        <div class="mob_header">
            <RouterLink :to="ROUTES.main" class="logo"></RouterLink>
            <div class="mob_header_mes">
<!--                <div class="header_icon">-->
<!--                    <HeaderCompareLink count />-->
<!--                    <HeaderFavoriteLink count />-->
<!--                </div>-->
                <MobileOpenMenu />
            </div>
        </div>

        <div class="main_banner">
            <div class="container row">
                <HeaderMenuIndex />

                <div class="mainbanner_content">
                    <div class="header_top">
                        <div class="search_panel row">
                            <Search />
                        </div>
                        <div class="header_top_wrap row">
                            <a href="tel:74954315426" class="phone"><b>+7 495</b> 431 54 26</a>
                            <div class="header_top_wrap_menu row">
                                <FeedBack />
                                <a :href="BACKEND_URL_API_PRICELIST" download>
                                    <div class="icon"><svg width="15" height="14" viewBox="0 0 15 14" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path
                                                d="M14.7334 9.03797C14.3182 8.59494 13.3956 8.37342 12.1499 8.37342C11.4118 8.37342 10.6275 8.46203 9.70485 8.59494C8.7279 7.71618 7.91632 6.68199 7.30588 5.53797C7.76722 4.20886 8.09016 2.92405 8.09016 1.94937C8.09016 1.1962 7.81335 0 6.70614 0C6.3832 0 6.1064 0.177215 5.92186 0.443038C5.46052 1.24051 5.64506 3.01266 6.5216 4.87342C5.8813 6.65147 5.11046 8.38366 4.21491 10.057C1.76981 11.0316 0.155118 12.0949 0.0167162 12.9367C-0.0755517 13.3354 0.201252 14 1.17007 14C2.60022 14 4.16877 12.0063 5.36826 9.96835C6.75292 9.51111 8.17178 9.15565 9.61258 8.90506C11.3657 10.3671 12.8881 10.5886 13.6262 10.5886C15.1025 10.5886 15.2409 9.56962 14.7334 9.03797ZM6.15253 0.575949C6.5216 0.0443038 7.35202 0.221519 7.35202 1.28481C7.35202 1.99367 7.12135 3.14557 6.66001 4.47468C5.82959 2.61392 5.82959 1.1519 6.15253 0.575949ZM0.29352 12.981C0.431922 12.2722 1.81594 11.2975 3.98424 10.4557C2.78475 12.4051 1.58527 13.6456 0.847127 13.6456C0.385788 13.6456 0.247386 13.2468 0.29352 12.981ZM9.38191 8.63924C8.08199 8.87187 6.80203 9.19768 5.55279 9.61392C6.23562 8.43035 6.79205 7.1835 7.21361 5.89241C7.81998 6.88762 8.54789 7.80976 9.38191 8.63924ZM9.98165 8.81646C11.4579 8.59494 12.7036 8.63924 13.2572 8.72785C14.595 8.99367 14.1337 10.5443 12.6574 10.1899C11.5963 9.96835 10.7198 9.3924 9.98165 8.81646Z"
                                                fill="white"></path>
                                        </svg></div>
                                    <span>Скачать прайс</span>
                                </a>
                                <RouterLink :to="ROUTES.delivery">
                                    <div class="icon"><svg width="15" height="16" viewBox="0 0 15 16" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path
                                                d="M3.97777 10.2811C4.06125 10.5832 4.37384 10.7605 4.67597 10.6771C4.97811 10.5936 5.15537 10.281 5.0719 9.97881L3.97777 10.2811ZM0.719434 2.30498C0.417396 2.22118 0.104605 2.3981 0.0208032 2.70014C-0.0629983 3.00218 0.11392 3.31498 0.415966 3.39878L0.719434 2.30498ZM13.575 10.6298C13.8784 10.551 14.0605 10.2411 13.9816 9.93772C13.9028 9.63434 13.593 9.45235 13.2896 9.5312L13.575 10.6298ZM6.01457 12.0172C6.24886 12.8652 5.73456 13.7599 4.82353 13.9967L5.10904 15.0954C6.60513 14.7066 7.51935 13.2015 7.10867 11.7149L6.01457 12.0172ZM4.82353 13.9967C3.90656 14.235 2.98641 13.7028 2.75015 12.8476L1.65602 13.1499C2.06475 14.6294 3.61885 15.4827 5.10904 15.0954L4.82353 13.9967ZM2.75015 12.8476C2.51586 11.9995 3.03014 11.1048 3.94118 10.8681L3.65566 9.76942C2.15955 10.1582 1.24532 11.6632 1.65602 13.1499L2.75015 12.8476ZM3.94118 10.8681C4.85813 10.6298 5.77829 11.162 6.01457 12.0172L7.10867 11.7149C6.69995 10.2354 5.14585 9.3822 3.65566 9.76942L3.94118 10.8681ZM5.0719 9.97881L3.44319 4.08342L2.34907 4.3857L3.97777 10.2811L5.0719 9.97881ZM2.00869 2.66268L0.719434 2.30498L0.415966 3.39878L1.70523 3.75647L2.00869 2.66268ZM3.44319 4.08342C3.25164 3.39007 2.70254 2.85519 2.00869 2.66268L1.70523 3.75647C2.02729 3.84583 2.26714 4.08912 2.34907 4.3857L3.44319 4.08342ZM6.70434 12.4154L13.575 10.6298L13.2896 9.5312L6.41882 11.3167L6.70434 12.4154Z"
                                                fill="white" />
                                            <path
                                                d="M5.53624 5.3365C5.16921 4.00799 4.9857 3.34373 5.29721 2.82043C5.60872 2.29712 6.29358 2.11914 7.66336 1.76317L9.11622 1.3856C10.4859 1.02963 11.1709 0.851635 11.7103 1.15376C12.2499 1.45589 12.4334 2.12015 12.8004 3.44866L13.1898 4.85776C13.5568 6.18627 13.7403 6.85052 13.4287 7.3738C13.1173 7.89717 12.4324 8.07515 11.0626 8.43112L9.60977 8.80866C8.24007 9.16463 7.55514 9.34262 7.01559 9.04053C6.47603 8.73836 6.29252 8.07409 5.9255 6.74563L5.53624 5.3365Z"
                                                stroke="white" stroke-width="1.2" />
                                        </svg></div>
                                    <span>Доставка</span>
                                </RouterLink>
                                <RouterLink :to="ROUTES.contacts">
                                    <div class="icon"><svg width="15" height="14" viewBox="0 0 15 14" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path
                                                d="M2.14272 1.07143V12.8571H8.57129V1.07143H2.14272ZM1.607 0H9.107C9.24908 0 9.38535 0.0564411 9.48581 0.156907C9.58628 0.257373 9.64272 0.393634 9.64272 0.535714V13.3929C9.64272 13.5349 9.58628 13.6712 9.48581 13.7717C9.38535 13.8721 9.24908 13.9286 9.107 13.9286H1.607C1.46492 13.9286 1.32866 13.8721 1.2282 13.7717C1.12773 13.6712 1.07129 13.5349 1.07129 13.3929V0.535714C1.07129 0.393634 1.12773 0.257373 1.2282 0.156907C1.32866 0.0564411 1.46492 0 1.607 0Z"
                                                fill="white" />
                                            <path
                                                d="M3.21429 3.21436H7.5V4.28578H3.21429V3.21436ZM3.21429 6.42864H7.5V7.50007H3.21429V6.42864ZM3.21429 9.64293H7.5V10.7144H3.21429V9.64293ZM9.64286 7.50007H11.7857V8.5715H9.64286V7.50007ZM9.64286 9.64293H11.7857V10.7144H9.64286V9.64293ZM0 12.8572H15V13.9286H0V12.8572Z"
                                                fill="white" />
                                            <path
                                                d="M9.64272 5.35707V12.8571H12.857V5.35707H9.64272ZM9.107 4.28564H13.3927C13.5348 4.28564 13.6711 4.34209 13.7715 4.44255C13.872 4.54302 13.9284 4.67928 13.9284 4.82136V13.3928C13.9284 13.5349 13.872 13.6711 13.7715 13.7716C13.6711 13.8721 13.5348 13.9285 13.3927 13.9285H9.107C8.96492 13.9285 8.82866 13.8721 8.7282 13.7716C8.62773 13.6711 8.57129 13.5349 8.57129 13.3928V4.82136C8.57129 4.67928 8.62773 4.54302 8.7282 4.44255C8.82866 4.34209 8.96492 4.28564 9.107 4.28564Z"
                                                fill="white" />
                                        </svg></div>
                                    <span>Контакты</span>
                                </RouterLink>
                            </div>
                            <div class="header_icon cart">
                                <RouterLink :to="ROUTES.cart">
                                    <div class="icon">
                                        <span>{{ cartCount }}</span>
                                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
                                            <g id="Group 9042964">
                                                <path id="Vector" d="M5.03305 3.44444H23L20.5556 12H6.34931M21.7778 16.8889H7.11111L4.66667 1H1M8.33333 21.7778C8.33333 22.4528 7.78612 23 7.11111 23C6.4361 23 5.88889 22.4528 5.88889 21.7778C5.88889 21.1027 6.4361 20.5556 7.11111 20.5556C7.78612 20.5556 8.33333 21.1027 8.33333 21.7778ZM21.7778 21.7778C21.7778 22.4528 21.2306 23 20.5556 23C19.8805 23 19.3333 22.4528 19.3333 21.7778C19.3333 21.1027 19.8805 20.5556 20.5556 20.5556C21.2306 20.5556 21.7778 21.1027 21.7778 21.7778Z" stroke="#EE3810" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                                            </g>
                                        </svg>
                                    </div>
                                </RouterLink>
        <!--                        <HeaderCompareLink active count />-->
        <!--                        <HeaderFavoriteLink active count />-->
                            </div>
                        </div>
                    </div>
                    <div class="mainbanner_bg row">
                        <div class="mainbanner_titles">
                            <h1>Стройматериалы <b>оптом</b></h1>
                            <div class="description">Доставим ваш заказ в лучшем виде, в указанный срок. Доставка
                                осуществляется грузовым транспортом или курьером.</div>
                            <div class="sub_description">
                                <div class="icon">
                                    <svg width="27" height="30" viewBox="0 0 27 30" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path
                                            d="M15.9744 19.0483H0.732955V14.7159H15.8608C17.0824 14.7159 18.0862 14.5218 18.8722 14.1335C19.6676 13.7453 20.2547 13.2055 20.6335 12.5142C21.0218 11.8229 21.2112 11.0133 21.2017 10.0852C21.2112 9.17614 21.0218 8.36174 20.6335 7.64205C20.2547 6.91288 19.6771 6.33996 18.9006 5.9233C18.1335 5.49716 17.1581 5.28409 15.9744 5.28409H10.2642V30H5.00852V0.90909H15.9744C18.2282 0.90909 20.1364 1.31629 21.6989 2.13068C23.2614 2.93561 24.4451 4.02936 25.25 5.41193C26.0644 6.78504 26.4716 8.3286 26.4716 10.0426C26.4716 11.8229 26.0597 13.3902 25.2358 14.7443C24.4119 16.089 23.2188 17.1449 21.6562 17.9119C20.0938 18.6695 18.1998 19.0483 15.9744 19.0483ZM16.642 21.2074V25.5398H0.732955V21.2074H16.642Z"
                                            fill="#FF781F" />
                                    </svg>
                                </div>
                                <span>Ваш заказ должен быть не менее 20.000 тысяч рублей</span>
                            </div>
                        </div>
                        <MainbannerForm />
                        <div class="mainbanner_bg_photo"></div>
                    </div>
                    <div class="mainbanner_products row">
                        <RecentArrivalsGoods></RecentArrivalsGoods>
                        <div class="mainbanner_products_preview">
                            <div class="mainbanner_products_preview_item">
                                <div class="photo"><img src="/images/catalog/list/MaskGroup-2.png" /></div>
                                <div class="text">
                                    <RouterLink :to="ROUTES.catalog + '/new'" class="name">Все для окрашивания потолка
                                    </RouterLink>
                                    <div class="desc">Всё очень просто - половину всех купленных стройматериалов Вы
                                        получаете по себестоимости, то есть по оптовой цене!</div>
                                </div>
                            </div>
                            <div class="mainbanner_products_preview_item">
                                <div class="photo"><img src="/images/catalog/list/MaskGroup.png" /></div>
                                <div class="text">
                                    <RouterLink :to="ROUTES.catalog + '/new'" class="name">Фасадные краски: все виды
                                    </RouterLink>
                                    <div class="desc">Всё очень просто - половину всех купленных стройматериалов Вы
                                        получаете по себестоимости, то есть по оптовой цене!</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <SearchMobile />
        <div class="sub_description_mob container">
            <div class="icon">
                <svg width="27" height="30" viewBox="0 0 27 30" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path
                        d="M15.9744 19.0483H0.732955V14.7159H15.8608C17.0824 14.7159 18.0862 14.5218 18.8722 14.1335C19.6676 13.7453 20.2547 13.2055 20.6335 12.5142C21.0218 11.8229 21.2112 11.0133 21.2017 10.0852C21.2112 9.17614 21.0218 8.36174 20.6335 7.64205C20.2547 6.91288 19.6771 6.33996 18.9006 5.9233C18.1335 5.49716 17.1581 5.28409 15.9744 5.28409H10.2642V30H5.00852V0.90909H15.9744C18.2282 0.90909 20.1364 1.31629 21.6989 2.13068C23.2614 2.93561 24.4451 4.02936 25.25 5.41193C26.0644 6.78504 26.4716 8.3286 26.4716 10.0426C26.4716 11.8229 26.0597 13.3902 25.2358 14.7443C24.4119 16.089 23.2188 17.1449 21.6562 17.9119C20.0938 18.6695 18.1998 19.0483 15.9744 19.0483ZM16.642 21.2074V25.5398H0.732955V21.2074H16.642Z"
                        fill="#FF781F" />
                </svg>
            </div>
            <span>Ваш заказ должен быть не менее 20.000 тысяч рублей</span>
        </div>
        <MainbannerFormMob />
    </div>
</template>