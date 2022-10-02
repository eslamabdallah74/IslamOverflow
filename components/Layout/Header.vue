<template>
    <div>
        <header class="header-area bg-dark">
            <div class="container">
                <div class="row align-items-center">
                    <div class="col-lg-2">
                        <div class="logo-box">
                            <NuxtLink to="/" class="logo"> IslamOverflow</NuxtLink>
                            <div class="user-action">
                                <div class="off-canvas-menu-toggle icon-element icon-element-xs shadow-sm"
                                    data-toggle="tooltip" data-placement="top" title="Main menu">
                                    <i class="la la-bars"></i>
                                </div>
                            </div>
                        </div>
                    </div><!-- end col-lg-2 -->
                    <div class="col-lg-10">
                        <div class="menu-wrapper">
                            <nav class="menu-bar ml-auto pr-2">
                                <ul>
                                    <li>
                                        <a href="#"> الأسألة <IconDownArrow /> </a>
                                        <ul class="dropdown-menu-item">
                                            <li > <NuxtLink to="/Questions"> أجدد الأسألة</NuxtLink></li>
                                            <li > <NuxtLink to="/Questions/Ask"> سؤال جديد</NuxtLink></li>
                                        </ul>
                                    </li>
                                    <li>
                                        <a href="#"> الصفحه الشخصية <IconDownArrow /> </a>
                                        <ul class="dropdown-menu-item">
                                            <li > <NuxtLink to="/Profile/Edit-Profile">تعديل الصفة الشخصية</NuxtLink></li>

                                        </ul>
                                    </li>
                                </ul><!-- end ul -->
                            </nav><!-- end menu-bar -->
                            <div class="nav-right-button">
                                <NuxtLink class="btn theme-btn theme-btn-outline mr-2" to="/Login"><IconLogin /> تسجيل الدخول </NuxtLink>
                                <NuxtLink class="btn theme-btn" to="/Register"><IconSignup />   اشتراك </NuxtLink>
                            </div><!-- end nav-right-button -->
                        </div><!-- end menu-wrapper -->
                    </div><!-- end col-lg-10 -->
                </div><!-- end row -->
            </div><!-- end container -->
        </header>
    </div>
</template>