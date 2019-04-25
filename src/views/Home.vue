<template>
<div>
  <div class="header-bar">
    <div class="header-menu">
        <Menu mode="horizontal" theme="primary" active-name="1">
            <MenuItem name="1">
                患者管理
            </MenuItem>
            <MenuItem name="3-1">用户管理</MenuItem>
            <MenuItem name="3-2">角色管理</MenuItem>
            <MenuItem name="3-3">科室管理</MenuItem>
        </Menu>
    </div>
    <div class="header-user">
      <Dropdown>
        <div class="user-msg">
          <Icon type="md-contact" color="#fff" size="20"/>
           <span class="name">个人中心</span> 
          <Icon type="ios-arrow-down"></Icon>
        </div>
        <DropdownMenu slot="list">
            <DropdownItem>个人资料</DropdownItem>
            <DropdownItem>退出</DropdownItem>
        </DropdownMenu>
      </Dropdown>
    </div>

  </div>

</div>
   
</template>
<script>
    export default {
        data () {
            return {
                theme1: 'light'
            }
        }
    }
</script>
<style lang="scss" >
.header-bar{
  position: relative;

  .header-menu{
    .ivu-menu-horizontal{
      height: 52px;
      line-height: 52px;
    }
  }
  .header-user{
    width: 120px;
    background: #007772;
    padding:8px 0;
    padding-left: 5px;
    border-radius: 18px 0 0 18px;
    position: absolute;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
    z-index: 1000;
    .user-msg{
      color: #fff; 
      i{
        margin:0 5px;
        vertical-align: middle;
      }
      .name{
        // vertical-align: text-bottom;
      }
    }
  }
}
</style>
