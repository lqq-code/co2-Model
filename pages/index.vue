<template>
  <div class="bg_contanier">
    <el-container>
      <el-aside class="aside-item">
        <el-card class="box-card">
          <div class="text">
           Study to Identify and Evaluate Areas with Poor Ventilation and Evaluate Risks posed by Airborne Transmission.
          </div>
          <div class="text">
           Course Name : Master of Environmental Science.
          </div>
        </el-card>
        <el-menu class="aside-menu">
          <el-submenu index="1">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span slot="title" @click="handleButtonShow1">Site1 - GYM</span>
              </template>
              <el-menu-item-group>
                <nuxt-link :to="'./site1'">
                  <el-menu-item >
                    <i class="el-icon-date"></i>Historical Data
                  </el-menu-item>
                </nuxt-link>
              </el-menu-item-group>
          </el-submenu>
          <el-submenu index="2">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span slot="title" @click="handleButtonShow2">Site2 - David Lecture Theatre</span>
              </template>
              <el-menu-item-group>
                <nuxt-link :to="'./site2'">
                  <el-menu-item >
                    <i class="el-icon-date"></i>Historical Data
                  </el-menu-item>
                </nuxt-link>
              </el-menu-item-group>
          </el-submenu>
          <el-submenu index="3">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span slot="title" @click="handleButtonShow3">Site3 - Union House</span>
              </template>
              <el-menu-item-group>
                <nuxt-link :to="'./site3'">
                  <el-menu-item >
                    <i class="el-icon-date"></i>Historical Data
                  </el-menu-item>
                </nuxt-link>
              </el-menu-item-group>
          </el-submenu>
          <el-submenu index="4">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span slot="title" @click="handleButtonShow4">Site4 - Chemistry LAB</span>
              </template>
              <el-menu-item-group>
                <nuxt-link :to="'./site4'">
                  <el-menu-item >
                    <i class="el-icon-date"></i>Historical Data
                  </el-menu-item>
                </nuxt-link>
              </el-menu-item-group>
          </el-submenu>
          <el-submenu index="5">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span slot="title" @click="handleButtonShow42">Site5 - Chemistry teaching room</span>
              </template>
              <el-menu-item-group>
                <nuxt-link :to="'./site7'">
                  <el-menu-item >
                    <i class="el-icon-date"></i>Historical Data
                  </el-menu-item>
                </nuxt-link>
              </el-menu-item-group>
          </el-submenu>
          <el-submenu index="6">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span slot="title" @click="handleButtonShow5">Site6 - Room 409 McCoy Building</span>
              </template>
              <el-menu-item-group>
                <nuxt-link :to="'./site5'">
                  <el-menu-item >
                    <i class="el-icon-date"></i>Historical Data
                  </el-menu-item>
                </nuxt-link>
              </el-menu-item-group>
          </el-submenu>
          <el-submenu index="7">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span slot="title" @click="handleButtonShow6">Site7 -  Jane's Office</span>
              </template>
              <el-menu-item-group>
                <nuxt-link :to="'./site6'">
                  <el-menu-item >
                    <i class="el-icon-date"></i>Historical Data
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
            width="500"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
                <el-table
                  :data="tableData1"
                  :span-method="objectSpanMethod"
                  border
                  style="width: 100%; margin-top: 20px">
                  <el-table-column
                    fixed
                    prop="id"
                    label="July"
                    width="215">
                  </el-table-column>
                  <el-table-column
                    prop="name"
                    label="parameter">
                  </el-table-column>
                  <el-table-column
                    prop="amount1"
                    label="value">
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
            width="500"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
              <el-table
                  :data="tableData2"
                  :span-method="objectSpanMethod"
                  border
                  style="width: 100%; margin-top: 20px">
                  <el-table-column
                    fixed
                    prop="id"
                    label="July"
                    width="215">
                  </el-table-column>
                  <el-table-column
                    prop="name"
                    label="parameter">
                  </el-table-column>
                  <el-table-column
                    prop="amount1"
                    label="value">
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
            width="500"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
              <el-table
                  :data="tableData3"
                  :span-method="objectSpanMethod"
                  border
                  style="width: 100%; margin-top: 20px">
                  <el-table-column
                    fixed
                    prop="id"
                    label="July"
                    width="215">
                  </el-table-column>
                  <el-table-column
                    prop="name"
                    label="parameter">
                  </el-table-column>
                  <el-table-column
                    prop="amount1"
                    label="value">
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
            title="Chemistry LAB"
            width="500"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
              <el-table
                  :data="tableData4"
                  :span-method="objectSpanMethod"
                  border
                  style="width: 100%; margin-top: 20px">
                  <el-table-column
                    fixed
                    prop="id"
                    label="July"
                    width="215">
                  </el-table-column>
                  <el-table-column
                    prop="name"
                    label="parameter">
                  </el-table-column>
                  <el-table-column
                    prop="amount1"
                    label="value">
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
            title="Chemistry teaching room"
            width="500"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
              <el-table
                  :data="tableData42"
                  border
                  style="width: 100%; margin-top: 20px">
                  <el-table-column
                    fixed
                    prop="id"
                    label="July"
                    width="215">
                  </el-table-column>
                  <el-table-column
                    prop="name"
                    label="parameter">
                  </el-table-column>
                  <el-table-column
                    prop="amount1"
                    label="value">
                  </el-table-column>
              </el-table>
            </div>
            <el-button icon="el-icon-location" slot="reference"
            :style="{
                display: isShow42 ? '' : 'none'
              }"
            class="showbutton site42_button"></el-button>
          </el-popover>
          <el-popover
            placement="top-start"
            title="Room 409 McCoy Building : PAR 200"
            width="500"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
            <div class="data-item">
              <el-table
                  :data="tableData5"
                  :span-method="objectSpanMethod"
                  border
                  style="width: 100%; margin-top: 20px">
                  <el-table-column
                    fixed
                    prop="id"
                    label="July"
                    width="215">
                  </el-table-column>
                  <el-table-column
                    prop="name"
                    label="parameter">
                  </el-table-column>
                  <el-table-column
                    prop="amount1"
                    label="value">
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
            width="500"
            trigger="click"
            content="The first floor of the Beaurepaire Centre.">
             <div class="data-item">
              <el-table
                  :data="tableData6"
                  :span-method="objectSpanMethod"
                  border
                  style="width: 100%; margin-top: 20px">
                  <el-table-column
                    fixed
                    prop="id"
                    label="July"
                    width="215">
                  </el-table-column>
                  <el-table-column
                    prop="name"
                    label="parameter">
                  </el-table-column>
                  <el-table-column
                    prop="amount1"
                    label="value">
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
      isShow42: false,
      isShow5: false,
      isShow6: false,
      direction: 'rtl',
      tableData1: [{
              id: 'Normal period (7.1-7.15)',
              name: 'Occupants',
              amount1: '12.10',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average CO2 level',
              amount1: '477.15',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average P',
              amount1: '0.0015',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Occupants',
              amount1: '5.28',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average CO2 level',
              amount1: '419.55',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average P',
              amount1: '0.00060',
      }],
      tableData2: [{
              id: 'Normal period (7.1-7.15)',
              name: 'Occupants',
              amount1: '21.48',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average CO2 level',
              amount1: '425.73',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average P',
              amount1: '0.00010',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Occupants',
              amount1: '9.20',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average CO2 level',
              amount1: '403.59',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average P',
              amount1: '0.000048',
      }],
      tableData3: [{
              id: 'Normal period (7.1-7.15)',
              name: 'Occupants',
              amount1: '1.05',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average CO2 level',
              amount1: '423.59',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average P',
              amount1: '0.039',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Occupants',
              amount1: '0.54',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average CO2 level',
              amount1: '410.76',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average P',
              amount1: '0.0009',
      }],
      tableData4: [{
              id: 'Normal period (7.1-7.15)',
              name: 'Occupants',
              amount1: '1.58',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average CO2 level',
              amount1: '418.73',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average P',
              amount1: '0.0000016',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Occupants',
              amount1: '1.14',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average CO2 level',
              amount1: '408.67',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average P',
              amount1: '0.0000071',
      }],
      tableData42: [{
              id: 'Normal period (7.1-7.15)',
              name: 'Occupants',
              amount1: '2.95',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Occupants',
              amount1: '2.69',
      }],
      tableData5: [{
              id: 'Normal period (7.1-7.15)',
              name: 'Occupants',
              amount1: '0.086',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average CO2 level',
              amount1: '435.77',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average P',
              amount1: '0',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Occupants',
              amount1: '0.035',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average CO2 level',
              amount1: '397.69',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average P',
              amount1: '0',
      }],
      tableData6: [{
              id: 'Normal period (7.1-7.15)',
              name: 'Occupants',
              amount1: '0.27',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average CO2 level',
              amount1: '430.83',
            }, {
              id: 'Normal period (7.1-7.15)',
              name: 'Average P',
              amount1: '0',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Occupants',
              amount1: '0.18',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average CO2 level',
              amount1: '413.84',
            }, {
              id: 'Lockdown period (7.16-7.27)',
              name: 'Average P',
              amount1: '0',
      }]
    };
  },
  computed: {},
  methods: {
    objectSpanMethod({ row, column, rowIndex, columnIndex }) {
        if (columnIndex === 0) {
          if (rowIndex % 3 === 0) {
            return {
              rowspan: 3,
              colspan: 1
            };
          } else {
            return {
              rowspan: 0,
              colspan: 0
            };
          }
        }
    },
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
     handleButtonShow42() {
          this.isShow42 = !this.isShow42
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
.text{
  text-align: justify;
  font-size: 18px;
  line-height: 30px;
  color:#074382;
  margin-bottom: 10px;
}

.aside-item{
  width: 340px;
  transform: scale(0.8);
}
.aside-menu{
  width: 340px;
  margin-top: 100px;
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
.site42_button{
    left: 60%;
    top: 26%;
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
