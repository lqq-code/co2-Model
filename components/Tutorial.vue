<template>
  <div class="bg_contanier">
    <div class="button_list">
      <el-button type="primary" @click="handleButtonShow1">site1</el-button>
      <el-button type="primary" @click="handleButtonShow2">site2</el-button>
      <el-button type="primary" @click="handleButtonShow3">site3</el-button>
      <el-button type="primary" @click="handleButtonShow4">site4</el-button>
      <el-button type="primary" @click="handleButtonShow5">site5</el-button>
      <el-button type="primary" @click="handleButtonShow6">site6</el-button>
    </div>
    <img src="../assets/images/bg.png" class="bg_img" >
      <el-popover
        placement="top-start"
        title="Gym (The first floor of the Beaurepaire Centre)"
        width="380"
        trigger="click"
        content="The first floor of the Beaurepaire Centre.">
        <div class="siteimg">
        <img src="../assets/images/site1.png" style="width:100%;height:100%;object-fit: cover;" />
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
        <div class="siteimg">
        <img src="../assets/images/site2.png"  style="width:100%;height:100%;object-fit:contain;" />
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
        <div class="siteimg">
        <img src="../assets/images/site3.png"  style="width:100%;height:100%;object-fit:contain;" />
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
        <div class="siteimg">
        <img src="../assets/images/site4.png"  style="width:100%;height:100%;object-fit:contain;" />
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
        <div class="siteimg">
        <img src="../assets/images/site5.png"  style="width:100%;height:100%;object-fit:contain;" />
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
        <div class="siteimg">
        <img src="../assets/images/site6.png"  style="width:100%;height:100%;object-fit:contain;" />
        </div>
        <el-button icon="el-icon-location" slot="reference"
         :style="{
            display: isShow6 ? '' : 'none'
          }"
        class="showbutton site6_button"></el-button>
      </el-popover>
    </img>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      isShow1: false,
      isShow2: false,
      isShow3: false,
      isShow4: false,
      isShow5: false,
      isShow6: false,
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
.bg_contanier {
  width: 100%;
  height: 100%;
  position: relative;
}
.button_list{
  position: absolute;
  padding:15px 0 0 95px;
}
.bg_img {
  width: 100%;
  height: 100vh;
  transform: scale(0.8);

}
.siteimg{
  width:350px;
  height:200px;
  margin:auto
}
.showbutton{
  position: absolute;
  transform: scale(0.6);
  border: none;
}
.site1_button {
    left: 32%;
    top: 10%;
}
.site2_button{
    left: 34%;
    bottom: 10%;
}
.site3_button{
    left: 34%;
    top: 21%;
}
.site4_button{
    left: 47%;
    top: 32%;
}
.site5_button{
    right: 22%;
    top: 17%;
}
.site6_button{
    left: 25%;
    bottom: 36%;

}



</style>
