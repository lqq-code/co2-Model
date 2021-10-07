<template>
  <div class="bg_contanier">
    <img src="../assets/images/bg.png" class="bg_img" >
      <el-popover
        placement="top-start"
        title="Gym"
        width="500"
        trigger="hover"
        content="The first floor of the Beaurepaire Centre.">
        <div style="width:350px;height:200px;margin:auto">
        <img src="../assets/images/site1.png"  style="width:100%;height:100%;object-fit: cover;" />
        </div>
        <el-button icon="el-icon-location" slot="reference" class="site1_button"></el-button>
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
}
.bg_img {
  position: relative;
  transform: scale(0.8);
}
.site1_button {
    position: absolute;
    right: 22%;
    top: 90%;
    border: none;
}
.img_site1{
    transform: scale(0.1);
  }


</style>
