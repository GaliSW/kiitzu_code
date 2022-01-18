<template>
    <section class="work_blk">
        <div class="work_img">
            <div class="productImg">
                <img
                    v-if="name == 1"
                    class="animate__animated animate__zoomIn"
                    src="../assets/images/work/work1.png"
                    alt=""
                />
                <img
                    v-if="name == 2"
                    class="animate__animated animate__zoomIn"
                    src="../assets/images/work/work2.png"
                    alt=""
                />
                <img
                    v-if="name == 3"
                    class="animate__animated animate__zoomIn"
                    src="../assets/images/work/work3.png"
                    alt=""
                />
            </div>
            <div class="subImg">
                <img src="../assets/images/work/workText.png" alt="" />
            </div>
        </div>
        <div class="work_para">
            <div class="work_wrapper">
                <h1>WHY YOU SHOULD WORK WITH US</h1>
                <h2
                    v-if="name == 1"
                    class="animate__animated animate__fadeInLeft"
                >
                    Design
                </h2>
                <h2
                    v-if="name == 2"
                    class="animate__animated animate__fadeInLeft"
                >
                    Production
                </h2>
                <h2
                    v-if="name == 3"
                    class="animate__animated animate__fadeInLeft"
                >
                    In House Laboratory
                </h2>
                <p
                    v-if="name == 1"
                    class="animate__animated animate__fadeInRight"
                >
                    Years of experience in cooperation with major sports brands
                    and understanding of various customer needs. Provide new
                    design ideas every season and continue to invest in new
                    machines to increase R&D efficiency. R&D staff of each
                    factory to provide localized services quickly and shorten
                    the development time. Leading the brand to break through the
                    past new concepts to conceive new products like never
                    before.s
                </p>
                <p
                    v-if="name == 2"
                    class="animate__animated animate__fadeInRight"
                >
                    We have hundreds of machines for weaving,jacquard, knitting,
                    braiding, etc. Mature and professional partner with strict
                    control of raw materials and processing quality. Monthly
                    production capacity of 25 million yards, can provide a large
                    number of stable products. Four production bases to pursue
                    localized production and reduce transportation time.
                    Distribute the external risks, support each other and reduce
                    delay. To face the global crisis, we have flexibly adjusted
                    our production line to maintain a stable supply. New
                    production lines and innovation continue to be launched.
                </p>
                <p
                    v-if="name == 3"
                    class="animate__animated animate__fadeInRight"
                >
                    Our laboratory adheres to the spirit of prudent research,
                    strict quality control of our products, and the development
                    of industry-leading technologies. Textile-related tests are
                    conducted in accordance with international standard test
                    methods and environmental conditions to obtain reliable and
                    relevant data.
                </p>
            </div>
            <div class="work_btn">
                <div class="prev" @click="prev">
                    <div>
                        <img src="../assets/images/work/prev.png" alt="" />
                    </div>
                    <div>PREVIOUS</div>
                </div>
                <div class="next" @click="next">
                    <div>NEXT</div>
                    <div>
                        <img src="../assets/images/work/next.png" alt="" />
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="mobile_work_blk">
        <h1>
            WHY YOU <br />
            SHOULD WORK <br />
            WITH US
        </h1>
        <div class="work_wrapper">
            <div>
                <img src="../assets/images/work/work1.png" alt="" />
                <h2>Design</h2>

                <p>
                    Years of experience in cooperation with major sports brands
                    and understanding of various customer needs. Provide new
                    design ideas every season and continue to invest in new
                    machines to increase R&D efficiency. R&D staff of each
                    factory to provide localized services quickly and shorten
                    the development time. Leading the brand to break through the
                    past new concepts to conceive new products like never
                    before.
                </p>
            </div>
            <div>
                <img src="../assets/images/work/work2.png" alt="" />
                <h2>Production</h2>
                <p>
                    We have hundreds of machines for weaving,jacquard, knitting,
                    braiding, etc. Mature and professional partner with strict
                    control of raw materials and processing quality. Monthly
                    production capacity of 25 million yards, can provide a large
                    number of stable products. Four production bases to pursue
                    localized production and reduce transportation time.
                    Distribute the external risks, support each other and reduce
                    delay. To face the global crisis, we have flexibly adjusted
                    our production line to maintain a stable supply. New
                    production lines and innovation continue to be launched.
                </p>
            </div>

            <div>
                <img src="../assets/images/work/work3.png" alt="" />
                <h2>In House Laboratory</h2>
                <p>
                    Our laboratory adheres to the spirit of prudent research,
                    strict quality control of our products, and the development
                    of industry-leading technologies. Textile-related tests are
                    conducted in accordance with international standard test
                    methods and environmental conditions to obtain reliable and
                    relevant data.
                </p>
            </div>
        </div>
    </section>
</template>
<script>
import "animate.css";
export default {
    name: "work",
    data() {
        return {
            name: 1,
        };
    },
    methods: {
        prev() {
            if (this.name == 1) {
                this.name = 3;
            } else {
                this.name -= 1;
            }
        },
        next() {
            if (this.name == 3) {
                this.name = 1;
            } else {
                this.name += 1;
            }
        },
    },
};
</script>
