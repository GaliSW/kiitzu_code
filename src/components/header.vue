<template>
    <header>
        <div class="header_wrapper">
            <ul>
                <li class="about">
                    ABOUT <span class="line"></span>
                    <div class="about_blk" id="about_blk">
                        <div class="about_wrapper">
                            <div class="about_content">
                                <img
                                    src="../assets/images/header/about01.png"
                                    alt=""
                                />
                                <div class="about01">Corporate Vision</div>
                            </div>
                            <div class="about_content">
                                <img
                                    src="../assets/images/header/about02.png"
                                    alt=""
                                />
                                <div class="about01">Sustainability</div>
                            </div>
                            <div class="about_content">
                                <img
                                    src="../assets/images/header/about03.png"
                                    alt=""
                                />
                                <div class="about01">Location</div>
                            </div>
                            <div class="about_content">
                                <img
                                    src="../assets/images/header/about04.png"
                                    alt=""
                                />
                                <div class="about01">Join Us</div>
                            </div>
                        </div>
                    </div>
                </li>
                <li class="news">NEWS<span class="line"></span></li>
                <li class="product">PRODUCT<span class="line"></span></li>
                <li class="logo">
                    <img src="../assets/images/header/Vector-4.png" alt="" />
                    <img src="../assets/images/header/Vector.png" alt="" />
                    <img src="../assets/images/header/Vector-1.png" alt="" />
                    <img src="../assets/images/header/Vector-6.png" alt="" />
                    <img src="../assets/images/header/Vector-2.png" alt="" />
                    <img src="../assets/images/header/Vector-3.png" alt="" />
                    <img src="../assets/images/header/Vector-5.png" alt="" />
                </li>
                <li class="contact">CONTACT<span class="line"></span></li>
                <li class="download">DOWLOAD<span class="line"></span></li>
                <li class="header_tab">
                    <span @click="tab" v-if="modeCh">繁</span>
                    <span @click="tab" v-if="modeEn">EN</span>
                    <span @click="search"><i class="fas fa-search"></i></span>
                </li>
                <li class="menu_btn">
                    <input type="checkbox" id="menu" />
                    <label for="menu" @click="menuBar"> |&nbsp;|&nbsp;|</label>
                </li>
            </ul>
        </div>
    </header>
    <div class="search_blk">
        <div class="search_wrapper">
            <div>
                <label for="search"><i class="fas fa-search"></i></label>
                <input type="text" name="" id="search" placeholder="search" />
                <label class="search_close" @click="closeSearch"
                    ><i class="fas fa-times"></i
                ></label>
            </div>
        </div>
    </div>
    <div class="menu">
        <div class="menu_wrapper">
            <label class="close_btn" for="menu" @click="menuBar"
                ><i class="fas fa-times"></i
            ></label>
            <div class="menu_center">
                <div class="mobile_search_blk">
                    <div class="mobile_search_wrapper">
                        <div>
                            <label for="search"
                                ><i class="fas fa-search"></i
                            ></label>
                            <input
                                type="text"
                                name=""
                                id="search"
                                placeholder="search"
                            />
                            <label
                                class="mobile_search_close"
                                @click="closeSearch"
                                ><i class="fas fa-times"></i
                            ></label>
                        </div>
                    </div>
                </div>
                <div class="mobile_about">
                    <input type="checkbox" id="about_check" />
                    <label for="about_check">ABOUT</label>

                    <ul class="about_list">
                        <li>Corporate Vision</li>
                        <li>Sustainability</li>
                        <li>Location</li>
                        <li>Join Us</li>
                    </ul>
                </div>
                <div>NEWS</div>
                <div>PRODUCT</div>
                <div>CONTACT</div>
                <div>DOWNLOAD</div>
                <div @click="tab" v-if="modeCh">繁體中文</div>
                <div @click="tab" v-if="modeEn">ENGLISH</div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: "myHeader",
    components: {},
    data() {
        return {
            modeCh: true,
            modeEn: false,
        };
    },
    created() {},
    methods: {
        tab() {
            if (this.modeCh) {
                this.modeEn = true;
                this.modeCh = false;
            } else {
                this.modeCh = true;
                this.modeEn = false;
            }
        },
        search() {
            document.querySelector(".search_blk").style.opacity = 1;
            document.querySelector(".search_blk").style.visibility = "visible";
        },
        closeSearch() {
            document.querySelector(".search_blk").style.opacity = 0;
            document.querySelector(".search_blk").style.visibility = "hidden";
        },
        menuBar() {
            const menuBtn = document.getElementById("menu");
            const menuBlk = document.querySelector(".menu");
            if (menuBtn.checked) {
                menuBlk.style.right = "-100%";
            } else {
                menuBlk.style.right = "0%";
            }
        },
    },
};
</script>
