<template>
  <div class="content">
    <div class="block">
      <div class="group">
        <p class="name">东说西说三缺一</p>
        <div class="avatar">
          <img src="/static/images/AvatarBig.png" alt="Avatar" />
          <img src="/static/images/AvatarBig.png" alt="Avatar" />
        </div>
        <p class="number">等三人</p>
        <button>有局可约</button>
      </div>
    </div>
    <div class="block">
      <div class="group">
        <p class="name">东说西说三缺一</p>
        <div class="avatar">
          <img src="/static/images/AvatarBig.png" alt="Avatar" />
          <img src="/static/images/AvatarBig.png" alt="Avatar" />
        </div>
        <p class="number">等三人</p>
        <button>有局可约</button>
      </div>
    </div>
    <div class="block">
      <div class="group">
        <p class="name">东说西说三缺一</p>
        <div class="avatar">
          <img src="/static/images/AvatarBig.png" alt="Avatar" />
          <img src="/static/images/AvatarBig.png" alt="Avatar" />
        </div>
        <p class="number">等三人</p>
        <button>有局可约</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang='scss'>
p {
  color: #000000;
  font-family: "PingFang SC";
}
@mixin ele-center {
  display: flex;
  justify-content: center;
  align-items: center;
}
.content {
  width:100%;
  height: 900px;
  display: flex;
  justify-content: center;
  // align-items: center;
  // flex-direction: column;

}
.block {
  margin-top:9px;
  width: 96%;
  height: 120px;
  background: rgba(135, 185, 231, 0.1);
  border-radius: 15px;
  @include ele-center;
  .group {
    width: 307px;
    height: 65px;
    position: relative;
    .name {
      position: absolute;
      top: 0;
      left: 0;
      font-size: 18px;
      line-height: 25px;
      color: #000000;
    }
    .avatar {
      position: absolute;
      left: 11px;
      bottom: 0;
      width: 56px;
      height: 25px;
      display: flex;
      justify-content: space-between;
      img {
        width: 25px;
        height: 25px;
      }
    }
    .number {
      position: absolute;
      left: 76px;
      bottom: 3px;
      font-size: 12px;
      line-height: 17px;
      color: #a1a1a1;
    }
    button {
      position: absolute;
      top: 0;
      right: 0;
      width: 130px;
      height: 65px;
      background-color: #59BC6C;
      border-radius: 10px;
      color:#ffffff;
      font-size: 16px;
      letter-spacing:2px;
      @include ele-center;
    }
    button::after{
      border: 0;
    }
  }
}
</style>