<template>
    <section class="location_blk">
        <div class="location_wrapper">
            <div class="locationImg">
                <img
                    v-if="location == 1"
                    src="../assets/images/location/location3.png"
                    alt=""
                />
                <img
                    v-if="location == 2"
                    src="../assets/images/location/location2.png"
                    alt=""
                />
                <img
                    v-if="location == 3"
                    src="../assets/images/location/location1.png"
                    alt=""
                />
                <img
                    v-if="location == 4"
                    src="../assets/images/location/location4.png"
                    alt=""
                />
            </div>

            <div class="location_content">
                <div class="location">
                    <h1>OUR LOCATION</h1>
                    <div :class="{ checked: tab1 }" @click="check(1)">
                        CHR BL HEADQUARTER
                    </div>
                    <div :class="{ checked: tab2 }" @click="check(2)">
                        CHR PT MILL
                    </div>
                    <br />
                    <div :class="{ checked: tab3 }" @click="check(3)">
                        CHR SL MILL
                    </div>
                    <div :class="{ checked: tab4 }" @click="check(4)">
                        CHR VN MILL
                    </div>
                </div>
                <div class="location_info">
                    <h1 v-if="location == 1">CHR BL HEADQUARTER</h1>
                    <h1 v-if="location == 2">CHR PT MILL</h1>
                    <h1 v-if="location == 3">CHR SL MILL</h1>
                    <h1 v-if="location == 4">CHR VN MILL</h1>
                    <div class="info" v-if="location == 1">
                        <div>
                            <i class="fas fa-phone-alt"></i>
                            <p>886-2-26194660</p>
                        </div>
                        <div>
                            <i class="fas fa-fax"></i>
                            <p>886-2-26194670</p>
                        </div>
                        <div>
                            <i class="fas fa-envelope"></i>
                            <p>chunyuco@ms36.hinet.net</p>
                        </div>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            <p>
                                No. 557, Sec. 4, Zhangshui Rd., Pitou Township,
                                Changhua County 523010 , Taiwan (R.O.C.)
                            </p>
                        </div>
                    </div>
                    <div class="info" v-if="location == 2">
                        <div>
                            <i class="fas fa-phone-alt"></i>
                            <p>886-2-26194660</p>
                        </div>
                        <div>
                            <i class="fas fa-fax"></i>
                            <p>886-2-26194670</p>
                        </div>
                        <div>
                            <i class="fas fa-envelope"></i>
                            <p>chunyuco@ms36.hinet.net</p>
                        </div>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            <p>
                                No. 219, Guanhai Blvd., Bali Dist., <br />
                                New Taipei City 249005 , Taiwan (R.O.C.)
                            </p>
                        </div>
                    </div>
                    <div class="info" v-if="location == 3">
                        <div>
                            <i class="fas fa-phone-alt"></i>
                            <p>86-0596836-7700</p>
                        </div>
                        <div>
                            <i class="fas fa-fax"></i>
                            <p>86-0596836-7700</p>
                        </div>
                        <div>
                            <i class="fas fa-envelope"></i>
                            <p>vic.chen@chunyuco.com.tw</p>
                        </div>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            <p>
                                No. 557, Sec. 4, Zhangshui <br />
                                Rd., Pitou Township, Changhua County 523010 ,
                                Taiwan (R.O.C.)
                            </p>
                        </div>
                    </div>
                    <div class="info" v-if="location == 4">
                        <div>
                            <i class="fas fa-phone-alt"></i>
                            <p>886-2-26194660</p>
                        </div>
                        <div>
                            <i class="fas fa-fax"></i>
                            <p>886-2-26194670</p>
                        </div>
                        <div>
                            <i class="fas fa-envelope"></i>
                            <p>chunyuco@ms36.hinet.net</p>
                        </div>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            <p>
                                Lo C-4D-CN,Khu Cong Nghiep My Phuoc 3, Phuong
                                Thoi Hoa, Ben Cat, Binh Duong, Vietnam
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="mobile_location_wrapper">
            <h1>OUR LOCATION</h1>
            <div class="location_card">
                <div class="mobile_location_border"></div>
                <div>
                    <img src="../assets/images/location/location2.png" alt="" />
                </div>
                <div class="location_info">
                    <h2>
                        CHR BL <br />
                        HEADQUARTER
                    </h2>
                    <div class="info">
                        <div>
                            <i class="fas fa-phone-alt"></i>
                            <p>886-2-26194660</p>
                        </div>
                        <div>
                            <i class="fas fa-fax"></i>
                            <p>886-2-26194670</p>
                        </div>
                        <div>
                            <i class="fas fa-envelope"></i>
                            <p>chunyuco@ms36.hinet.net</p>
                        </div>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            <p>
                                No. 219, Guanhai Blvd., Bali Dist., <br />
                                New Taipei City 249005 , Taiwan (R.O.C.)
                            </p>
                        </div>
                    </div>
                    <div class="check_btn">
                        <div>CHECK</div>
                        <div>
                            <img src="../assets/images/work/next.png" alt="" />
                        </div>
                    </div>
                </div>
            </div>
            <div class="location_card">
                <div class="mobile_location_border"></div>
                <div>
                    <img src="../assets/images/location/location2.png" alt="" />
                </div>
                <div class="location_info">
                    <h2>
                        CHR BL <br />
                        HEADQUARTER
                    </h2>
                    <div class="info">
                        <div>
                            <i class="fas fa-phone-alt"></i>
                            <p>886-2-26194660</p>
                        </div>
                        <div>
                            <i class="fas fa-fax"></i>
                            <p>886-2-26194670</p>
                        </div>
                        <div>
                            <i class="fas fa-envelope"></i>
                            <p>chunyuco@ms36.hinet.net</p>
                        </div>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            <p>
                                No. 219, Guanhai Blvd., Bali Dist., <br />
                                New Taipei City 249005 , Taiwan (R.O.C.)
                            </p>
                        </div>
                    </div>
                    <div class="check_btn">
                        <div>CHECK</div>
                        <div>
                            <img src="../assets/images/work/next.png" alt="" />
                        </div>
                    </div>
                </div>
            </div>
            <div class="location_card">
                <div class="mobile_location_border"></div>
                <div>
                    <img src="../assets/images/location/location1.png" alt="" />
                </div>
                <div class="location_info">
                    <h2>
                        CHR BL <br />
                        HEADQUARTER
                    </h2>
                    <div class="info">
                        <div>
                            <i class="fas fa-phone-alt"></i>
                            <p>886-2-26194660</p>
                        </div>
                        <div>
                            <i class="fas fa-fax"></i>
                            <p>886-2-26194670</p>
                        </div>
                        <div>
                            <i class="fas fa-envelope"></i>
                            <p>chunyuco@ms36.hinet.net</p>
                        </div>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            <p>
                                No. 219, Guanhai Blvd., Bali Dist., <br />
                                New Taipei City 249005 , Taiwan (R.O.C.)
                            </p>
                        </div>
                    </div>
                    <div class="check_btn">
                        <div>CHECK</div>
                        <div>
                            <img src="../assets/images/work/next.png" alt="" />
                        </div>
                    </div>
                </div>
            </div>
            <div class="location_card">
                <div class="mobile_location_border"></div>
                <div>
                    <img src="../assets/images/location/location4.png" alt="" />
                </div>
                <div class="location_info">
                    <h2>
                        CHR BL <br />
                        HEADQUARTER
                    </h2>
                    <div class="info">
                        <div>
                            <i class="fas fa-phone-alt"></i>
                            <p>886-2-26194660</p>
                        </div>
                        <div>
                            <i class="fas fa-fax"></i>
                            <p>886-2-26194670</p>
                        </div>
                        <div>
                            <i class="fas fa-envelope"></i>
                            <p>chunyuco@ms36.hinet.net</p>
                        </div>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            <p>
                                No. 219, Guanhai Blvd., Bali Dist., <br />
                                New Taipei City 249005 , Taiwan (R.O.C.)
                            </p>
                        </div>
                    </div>
                    <div class="check_btn">
                        <div>CHECK</div>
                        <div>
                            <img src="../assets/images/work/next.png" alt="" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="location_border"></div>
    </section>
</template>
<script>
export default {
    name: "location",
    data() {
        return {
            location: 1,
            tab1: true,
            tab2: false,
            tab3: false,
            tab4: false,
        };
    },
    methods: {
        check(num) {
            this.location = num;
            if (num == 1) {
                this.tab1 = true;
                this.tab2 = false;
                this.tab3 = false;
                this.tab4 = false;
            } else if (num == 2) {
                this.tab1 = false;
                this.tab2 = true;
                this.tab3 = false;
                this.tab4 = false;
            } else if (num == 3) {
                this.tab1 = false;
                this.tab2 = false;
                this.tab3 = true;
                this.tab4 = false;
            } else if (num == 4) {
                this.tab1 = false;
                this.tab2 = false;
                this.tab3 = false;
                this.tab4 = true;
            }
        },
    },
};
</script>
