<template>
  <div class="bg_contanier">
    <img src="../assets/images/bg.png" class="bg_img" >
      <el-popover
        placement="top-start"
        title="Gym (The first floor of the Beaurepaire Centre)"
        width="380"
        trigger="hover"
        content="The first floor of the Beaurepaire Centre.">
        <div class="siteimg">
        <img src="../assets/images/site1.png"  style="width:100%;height:100%;object-fit: cover;" />
        </div>
        <el-button icon="el-icon-location" slot="reference" class="site1_button"></el-button>
      </el-popover>

      <el-popover
        placement="top-start"
        title="David Derham Lecture Theatre PAR 106"
        width="380"
        trigger="hover"
        content="The first floor of the Beaurepaire Centre.">
        <div class="siteimg">
        <img src="../assets/images/site2.png"  style="width:100%;height:100%;object-fit:contain;" />
        </div>
        <el-button icon="el-icon-location" slot="reference" class="site2_button"></el-button>
      </el-popover>

      <el-popover
        placement="top-start"
        title="Union House, Main Dining Room"
        width="380"
        trigger="hover"
        content="The first floor of the Beaurepaire Centre.">
        <div class="siteimg">
        <img src="../assets/images/site3.png"  style="width:100%;height:100%;object-fit:contain;" />
        </div>
        <el-button icon="el-icon-location" slot="reference" class="site3_button"></el-button>
      </el-popover>

      <el-popover
        placement="top-start"
        title="Chemistry laboratory (Chemistry building)"
        width="380"
        trigger="hover"
        content="The first floor of the Beaurepaire Centre.">
        <div class="siteimg">
        <img src="../assets/images/site4.png"  style="width:100%;height:100%;object-fit:contain;" />
        </div>
        <el-button icon="el-icon-location" slot="reference" class="site4_button"></el-button>
      </el-popover>

      <el-popover
        placement="top-start"
        title="Room 409 McCoy Building : PAR 200"
        width="380"
        trigger="hover"
        content="The first floor of the Beaurepaire Centre.">
        <div class="siteimg">
        <img src="../assets/images/site5.png"  style="width:100%;height:100%;object-fit:contain;" />
        </div>
        <el-button icon="el-icon-location" slot="reference" class="site5_button"></el-button>
      </el-popover>

      <el-popover
        placement="top-start"
        title="Room 230 (Janes Office) Alan Gilbert PAR 104"
        width="380"
        trigger="hover"
        content="The first floor of the Beaurepaire Centre.">
        <div class="siteimg">
        <img src="../assets/images/site6.png"  style="width:100%;height:100%;object-fit:contain;" />
        </div>
        <el-button icon="el-icon-location" slot="reference" class="site6_button"></el-button>
      </el-popover>
    </img>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {};
  },
  computed: {},
  methods: {}
};
</script>
<style scope>
.bg_contanier {
  width: 100%;
  height: 100%;
  position: relative;

}
.bg_img {
  width: 100%;
  height: 100%;
}
.siteimg{
  width:350px;
  height:200px;
  margin:auto
}

.site1_button {
    position: absolute;
    left: 32%;
    top: 3%;
    transform: scale(0.8);
    border: none;
}
.site2_button{
    position: absolute;
    left: 31%;
    bottom: 1%;
    transform: scale(0.8);
    border: none;
}
.site3_button{
    position: absolute;
    left: 29%;
    top: 16%;
    transform: scale(0.8);
    border: none;
}

.site4_button{
    position: absolute;
    left: 47%;
    top: 29%;
    transform: scale(0.8);
    border: none;
}
.site5_button{
    position: absolute;
    right: 17%;
    top: 12%;
    transform: scale(0.8);
    border: none;
}
.site6_button{
    position: absolute;
    left: 19%;
    bottom: 34%;
    transform: scale(0.8);
    border: none;
}



</style>
