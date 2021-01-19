<template>
  <div>
    <div class="top">
      <div class="profile">
        <img src="/static/images/AvatarBig.png" alt="AvatarBig" />
        <p class="week">周三</p>
        <p class="date">1月13日</p>
        <p class="nickname">Peter</p>
      </div>
      <div class="count">
        <span class="num">0</span>
        <span class="txt">饭局</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
p{
  color: #000000;
  font-family:"PingFang SC";
}
span{
  color: #000000;
  font-family:"PingFang SC";
}
.top {
  width: 100%;
  height: 251px;
  background: #fafafa;
  display: flex;
  justify-content: center;
}
.profile {
  width: 192px;
  height: 116px;
  top: 26px;
  position: relative;
}
.profile img {
  width: 70px;
  height: 70px;
}
.profile .week {
  position: absolute;
  top: 0px;
  right: 19px;
  font-size: 25px;
  line-height: 35px;
}
.profile .date {
  position: absolute;
  top: 48px;
  right: 0px;
  font-size: 20px;
  line-height: 28px;
  color: #262626;
}
.profile .nickname {
  position: absolute;
  left: 12px;
  bottom: 0px;
  font-size: 18px;
  line-height: 25px;
}
.count{
  border: 1px solid rgba(60, 60, 67, 0.18);
  border-radius: 6px;
  background-color: rgba(255, 255, 255, 1);
  width: 300px;
  height: 50px;
  position: absolute;
  top:156px
}
.count .num{
  font-weight: 500px;
  font-size: 30px;
  line-height: 50px;
  margin-left: 82px;
}
.count .txt{
  font-weight: 400px;
  font-size: 20px;
  margin-left: 81px;
  line-height: 50px;
}
</style>