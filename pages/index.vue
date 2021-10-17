<template>
  <div class="bg_contanier">
    <el-container>
      <el-aside class="aside-item">
        <el-menu >
          <el-menu-item index="1">
             <i class="el-icon-location"></i>
            <span slot="title" @click="handleButtonShow1">Site1 - GYM</span>
          </el-menu-item>
          <el-menu-item index="2">
             <i class="el-icon-location"></i>
            <span slot="title" @click="handleButtonShow2">Site2 - David Derham Lecture Theatre</span>
          </el-menu-item>
          <el-menu-item index="3">
             <i class="el-icon-location"></i>
            <span slot="title" @click="handleButtonShow3">Site3 - Union House</span>
          </el-menu-item>
          <el-menu-item index="4">
             <i class="el-icon-location"></i>
            <span slot="title" @click="handleButtonShow4">Site4 - Chemistry laboratory</span>
          </el-menu-item>
          <el-menu-item index="5">
             <i class="el-icon-location"></i>
            <span slot="title" @click="handleButtonShow5">Site5 - McCoy Building</span>
          </el-menu-item>
          <el-menu-item index="6">
             <i class="el-icon-location"></i>
            <span slot="title" @click="handleButtonShow6">Site6 -  Alan Gilbert PAR</span>
          </el-menu-item>
        </el-menu>
        <el-menu
              router
              class="menu-history">
              <el-submenu index="1">
                <template slot="title">
                  <i class="el-icon-notebook-2"></i>
                  <span>Historical Data</span>
                </template>
                <el-menu-item-group>
                  <nuxt-link :to="'/may'">
                  <el-menu-item >
                    <i class="el-icon-date"></i>May
                  </el-menu-item>
                    </nuxt-link>
                  <el-menu-item index="1-2">
                    <i class="el-icon-date"></i>June
                  </el-menu-item>
                  <el-menu-item index="1-3">
                    <i class="el-icon-date"></i>July
                  </el-menu-item>
                  <el-menu-item index="1-4">
                    <i class="el-icon-date"></i>August
                  </el-menu-item>
                   <nuxt-link :to="'/sep'">
                  <el-menu-item index="1-5">
                    <i class="el-icon-date"></i>September
                  </el-menu-item>
                    </nuxt-link>
                </el-menu-item-group>
              </el-submenu>
        </el-menu>
      </el-aside>
      <el-main class="main-item">
        <div class="div-img">
        <img src="../assets/images/bg.png" class="bg_img" >
          <el-popover
            placement="top-start"
            title="Gym (The first floor of the Beaurepaire Centre)"
            width="390"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
              <el-table
                ref="singleTable"
                :data="tableData"
                highlight-current-row
                style="width: 100%">
                <el-table-column
                  property="name"
                  label="Name"
                  width="140">
                </el-table-column>
                <el-table-column
                  property="average"
                  label="Average"
                  width="120">
                </el-table-column>
                <el-table-column
                  property="maximum"
                  label="Maximum"
                  width="120">
                </el-table-column>
              </el-table>
            </div>
            <el-button icon="el-icon-location" slot="reference"
              :style="{
                display: isShow1 ? '' : 'none'
              }"
            class="showbutton site1_button"></el-button>
          </el-popover>

          <el-popover
            placement="top-start"
            title="David Derham Lecture Theatre PAR 106"
            width="380"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
              <el-table
                ref="singleTable"
                :data="tableData"
                highlight-current-row
                style="width: 100%">
                <el-table-column
                  property="name"
                  label="Name"
                  width="140">
                </el-table-column>
                <el-table-column
                  property="average"
                  label="Average"
                  width="120">
                </el-table-column>
                <el-table-column
                  property="maximum"
                  label="Maximum"
                  width="120">
                </el-table-column>
              </el-table>
            </div>
            <el-button icon="el-icon-location" slot="reference"
            :style="{
                display: isShow2 ? '' : 'none'
              }"
              class="showbutton site2_button"></el-button>
          </el-popover>

          <el-popover
            placement="top-start"
            title="Union House, Main Dining Room"
            width="380"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
              <el-table
                ref="singleTable"
                :data="tableData"
                highlight-current-row
                style="width: 100%">
                <el-table-column
                  property="name"
                  label="Name"
                  width="140">
                </el-table-column>
                <el-table-column
                  property="average"
                  label="Average"
                  width="120">
                </el-table-column>
                <el-table-column
                  property="maximum"
                  label="Maximum"
                  width="120">
                </el-table-column>
              </el-table>
            </div>
            <el-button icon="el-icon-location" slot="reference"
            :style="{
                display: isShow3 ? '' : 'none'
              }"
            class="showbutton site3_button"></el-button>
          </el-popover>
          <el-popover
            placement="top-start"
            title="Chemistry laboratory (Chemistry building)"
            width="380"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
              <el-table
                ref="singleTable"
                :data="tableData"
                highlight-current-row
                style="width: 100%">
                <el-table-column
                  property="name"
                  label="Name"
                  width="140">
                </el-table-column>
                <el-table-column
                  property="average"
                  label="Average"
                  width="120">
                </el-table-column>
                <el-table-column
                  property="maximum"
                  label="Maximum"
                  width="120">
                </el-table-column>
              </el-table>
            </div>
            <el-button icon="el-icon-location" slot="reference"
            :style="{
                display: isShow4 ? '' : 'none'
              }"
            class="showbutton site4_button"></el-button>
          </el-popover>

          <el-popover
            placement="top-start"
            title="Room 409 McCoy Building : PAR 200"
            width="380"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
              <el-table
                ref="singleTable"
                :data="tableData"
                highlight-current-row
                style="width: 100%">
                <el-table-column
                  property="name"
                  label="Name"
                  width="140">
                </el-table-column>
                <el-table-column
                  property="average"
                  label="Average"
                  width="120">
                </el-table-column>
                <el-table-column
                  property="maximum"
                  label="Maximum"
                  width="120">
                </el-table-column>
              </el-table>
            </div>
            <el-button icon="el-icon-location" slot="reference"
            :style="{
                display: isShow5 ? '' : 'none'
              }"
            class="showbutton site5_button"></el-button>
          </el-popover>

          <el-popover
            placement="top-start"
            title="Room 230 (Janes Office) Alan Gilbert PAR 104"
            width="380"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
             <div class="data-item">
              <el-table
                ref="singleTable"
                :data="tableData"
                highlight-current-row
                style="width: 100%">
                <el-table-column
                  property="name"
                  label="Name"
                  width="140">
                </el-table-column>
                <el-table-column
                  property="average"
                  label="Average"
                  width="120">
                </el-table-column>
                <el-table-column
                  property="maximum"
                  label="Maximum"
                  width="120">
                </el-table-column>
              </el-table>
            </div>
            <el-button icon="el-icon-location" slot="reference"
            :style="{
                display: isShow6 ? '' : 'none'
              }"
            class="showbutton site6_button"></el-button>
          </el-popover>
        </img>
        </div>
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      drawer: false,
      isShow1: false,
      isShow2: false,
      isShow3: false,
      isShow4: false,
      isShow5: false,
      isShow6: false,
      direction: 'rtl',
      tableData:[
        {
        name:'co2 concentration',
        average:'xxx',
        maximum:'xx'
        },
        {
        name:'mask efficienncy',
        average:'xxx',
        maximum:'xx'
        },
        {
        name:'occpuants',
        average:'xxx',
        maximum:'xx'
        },
        {
        name:'covid-risk',
        average:'xxx',
        maximum:'xx'
        },
      ],
    };
  },
  computed: {},
  methods: {
    handleButtonShow1() {
          this.isShow1 = !this.isShow1
    },
    handleButtonShow2() {
          this.isShow2 = !this.isShow2
    },
    handleButtonShow3() {
          this.isShow3 = !this.isShow3
    },
    handleButtonShow4() {
          this.isShow4 = !this.isShow4
    },
    handleButtonShow5() {
          this.isShow5 = !this.isShow5
    },
    handleButtonShow6() {
          this.isShow6 = !this.isShow6
    },
  }
};
</script>
<style scope>
.el-menu{
  border:none;
}
.el-menu-item-group__title{
  padding:0;
}
a {
  text-decoration: none;
}
.bg_contanier {
  width: 100%;
  height: 100%;
  position: relative;
  margin-top: -100px;
}
.aside-item{
  width: 300px;
  transform: scale(0.8);
}
.main-item{
  padding: 0;
}
.menu-history{
  margin-top: 100px;
}
.bg_img {
  width: 100%;
  height: 100%;
  transform: scale(0.8);
}
.data-item{
}
.showbutton{
  position: absolute;
  transform: scale(0.6);
  border: none;
  transition: all 1s ease-in-out ;
}
.site1_button {
    left: 50%;
    top: 12%;
    animation: shake 800ms ease-in-out;
}
.site2_button{
    left: 52%;
    bottom: 39%;
    animation: shake 800ms ease-in-out;
}
.site3_button{
    left: 51%;
    top: 19%;
    animation: shake 800ms ease-in-out;
}
.site4_button{
    left: 58%;
    top: 24%;
    animation: shake 800ms ease-in-out;
}
.site5_button{
    right: 20%;
    top: 18%;
    animation: shake 800ms ease-in-out;
}
.site6_button{
    left: 46%;
    bottom: 55%;
    animation: shake 800ms ease-in-out;
}
@keyframes shake {
  0%,90% {
    transform: translate3d(0, -2px, 0);
  }
  20%,80% {
    transform: translate3d(0, +3px, 0);
  }
  30%,70% {
    transform: translate3d(0, -5px, 0);
  }
  40%,60% {
    transform: translate3d(0, +5px, 0);
  }
  50% {
    transform: translate3d(0, -5px, 0);
  }
}
</style>
