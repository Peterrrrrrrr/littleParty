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
    <div class="content">
      <div class="party">
        <div class="group">
          <p class="title">中饭</p>
          <p class="status" id="lauch" :style="{ color: switch1Color }">{{switch1Text}}</p>
          <switch :checked="switch1Checked" @click="switch1Change" />
        </div>
      </div>
      <div class="party">
        <div class="group">
          <p class="title">晚饭</p>
          <p class="status" :style="{ color: lauchcolor }">可约</p>
          <switch :checked="switchChecked" @click="switch1Change" />
        </div>
      </div>
      <div class="party">
        <div class="group">
          <p class="title">宵夜</p>
          <p class="status">可约</p>
          <switch :checked="switchChecked" @click="switchChange" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      switchChecked: true,
      switch1Checked: false,
      switch1Color: "#687684",
      switch1Text: "不约",
      lauchcolor: "#4C9EEB",
      busyColor: "#687684",
      lauch: [],
    };
  },
  methods: {
    switch1Change(e) {
      console.log(e);
      this.switch1Checked = !this.switch1Checked;
      this.switch1Color = this.switch1Checked ? "#4C9EEB" : "#687684";
      this.switch1Text = this.switch1Checked ? "可约" : "不约";
    },
  },
};
</script>

<style lang="scss">
p span {
  color: #000000;
  font-family: "PingFang SC";
}

@mixin justify-center {
  display: flex;
  justify-content: center;
}

@mixin align-center {
  display: flex;
  align-items: center;
}

.top {
  width: 100%;
  height: 251px;
  background: #fafafa;
  @include justify-center;

  .profile {
    width: 192px;
    height: 116px;
    top: 26px;
    position: relative;

    img {
      width: 70px;
      height: 70px;
    }

    .week {
      position: absolute;
      top: 0px;
      right: 19px;
      font-size: 25px;
      line-height: 35px;
    }

    .date {
      position: absolute;
      top: 48px;
      right: 0px;
      font-size: 20px;
      line-height: 28px;
      color: #262626;
    }

    .nickname {
      position: absolute;
      left: 12px;
      bottom: 0px;
      font-size: 18px;
      line-height: 25px;
    }
  }

  .count {
    border: 1px solid rgba(60, 60, 67, 0.18);
    border-radius: 6px;
    background-color: rgba(255, 255, 255, 1);
    width: 300px;
    height: 50px;
    position: absolute;
    top: 156px;
    @include align-center;

    .num {
      font-weight: 500px;
      font-size: 30px;
      margin-left: 82px;
    }

    .txt {
      font-weight: 400px;
      font-size: 13px;
      margin-left: 81px;
    }
  }
}

.content {
  width: 100%;
  height: 327px;
  border-bottom: 0.5px solid #ced5dc;

  .party {
    width: 100%;
    height: 108px;
    border-top: 0.5px solid #ced5dc;
    position: relative;
    @include justify-center;
    align-items: center;

    .group {
      width: 210px;
      height: 73px;
      position: relative;

      .title {
        font-size: 30px;
        line-height: 42px;
        position: absolute;
        top: 0px;
        left: 0px;
      }

      .status {
        font-size: 15px;
        line-height: 21px;
        position: absolute;
        bottom: 0px;
        left: 7px;
      }

      switch {
        position: absolute;
        top: 21px;
        right: 0px;
      }
    }
  }
}
</style>
