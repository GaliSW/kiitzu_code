<template>
    <section class="banner_blk">
        <div v-if="bannerIndex == 1" class="animate__animated animate__fadeIn">
            <img src="../assets/images/banner/banner.png" alt="" />
        </div>
        <div v-if="bannerIndex == 2" class="animate__animated animate__fadeIn">
            <img src="../assets/images/banner/banner2.jpg" alt="" />
        </div>
        <div v-if="bannerIndex == 3" class="animate__animated animate__fadeIn">
            <img src="../assets/images/banner/banner3.jpg" alt="" />
        </div>
        <div class="dot">
            <div
                v-if="bannerIndex == 1"
                contextmenu=""
                class="dot_check dot1"
            ></div>
            <div class="dot1" v-if="bannerIndex !== 1" @click="dotTab(1)"></div>

            <div v-if="bannerIndex == 2" class="dot_check dot2"></div>

            <div class="dot2" v-if="bannerIndex !== 2" @click="dotTab(2)"></div>

            <div v-if="bannerIndex == 3" class="dot_check dot3"></div>

            <div class="dot3" v-if="bannerIndex !== 3" @click="dotTab(3)"></div>
        </div>
        <div class="banner_btn">
            <div class="prev" @click="prev">
                <img src="../assets/images/banner/prev.png" alt="" />
            </div>
            <div class="next" @click="next">
                <img src="../assets/images/banner/next.png" alt="" />
            </div>
        </div>
        <div class="banner_vd"><i class="far fa-play-circle"></i></div>
    </section>
    <div class="cookie_blk">
        <div>
            <p>
                We value and respect your privacy. Chun Yu Ribbon uses its own
                and selected third-party cookies on this site to improve
                performance, for analytics and for advertising. By browsing this
                site, you are agreeing to this. We encourage you to review our
                full "Privacy and Cookies Policy" for more information.
                <a href="#">Cookies Policy</a>
            </p>
            <div @click="closeCookie">Accept</div>
        </div>
    </div>
</template>
<script>
import "animate.css";
export default {
    name: "banner",
    data() {
        return {
            bannerA: true,
            bannerIndex: 1,
        };
    },
    created() {
        setInterval(() => {
            if (this.bannerIndex == 3) {
                this.bannerIndex = 1;
            } else {
                this.bannerIndex += 1;
            }
        }, 4500);
    },
    methods: {
        prev() {
            if (this.bannerIndex == 1) {
                this.bannerIndex = 3;
            } else {
                this.bannerIndex -= 1;
            }
        },
        next() {
            if (this.bannerIndex == 3) {
                this.bannerIndex = 1;
            } else {
                this.bannerIndex += 1;
            }
        },
        dotTab(num) {
            this.bannerIndex = num;
        },
        closeCookie() {
            document.querySelector(".cookie_blk").style.display = "none";
        },
    },
};
</script>
