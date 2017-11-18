<template>
<div class="box">
  <router-link  to="/">去首页</router-link>
  <br>
  <h2>基础用法</h2>
  <Row>
    <Col span="12">col-12</Col>
    <Col span="12">col-12</Col>
  </Row>
  <Row>
    <Col span="8">col-8</Col>
    <Col span="8">col-8</Col>
    <Col span="8">col-8</Col>
  </Row>
  <br>

  <h2>间距</h2>
  <Row :gutter="16">
    <Col span="6">
      <div>col-6</div>
    </Col>
    <Col span="6">
      <div>col-6</div>
    </Col>
    <Col span="6">
      <div>col-6</div>
    </Col>
    <Col span="6">
      <div>col-6</div>
    </Col>
  </Row>
  <br>

  <h2>栅格顺序</h2>
  <Row type="flex">
    <Col span="6" order="4">1 | order-4</Col>
    <Col span="6" order="3">2 | order-3</Col>
    <Col span="6" order="2">3 | order-2</Col>
    <Col span="6" order="1">4 | order-1</Col>
  </Row>
  <br>

  <h2>偏移</h2>
  <Row>
    <Col span="8">col-8</Col>
    <Col span="8" offset="8">col-8 | offset-8</Col>
  </Row>
  <Row>
    <Col span="6" offset="8">col-6 | offset-8</Col>
    <Col span="6" offset="4">col-6 | offset-4</Col>
  </Row>
  <br>

  <h2>Flex布局</h2>
  <p>通过给row设置参数justify为不同的值，来定义子元素的排布方式。在flex模式下有效。</p>
  <Row type="flex" justify="start" class="code-row-bg">
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
  </Row>
  <p>子元素向右排列</p>
  <Row type="flex" justify="end" class="code-row-bg">
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
  </Row>
  <p>子元素居中排列</p>
  <Row type="flex" justify="center" class="code-row-bg">
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
  </Row>
  <p>子元素等宽排列</p>
  <Row type="flex" justify="space-between" class="code-row-bg">
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
  </Row>
  <p>子元素分散排列</p>
  <Row type="flex" justify="space-around" class="code-row-bg">
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
      <Col span="4">col-4</Col>
  </Row>
  <br>

  <p>通过给row设置参数align为不同的值，来定义子元素在垂直方向上的排布方式。在flex模式下有效。</p>
  <p>顶部对齐</p>
  <Row type="flex" justify="center" align="top" class="code-row-bg">
      <Col span="4"><p style="height: 80px">col-4</p></Col>
      <Col span="4"><p style="height: 30px">col-4</p></Col>
      <Col span="4"><p style="height: 100px">col-4</p></Col>
      <Col span="4"><p style="height: 60px">col-4</p></Col>
  </Row>
  <p>底部对齐</p>
  <Row type="flex" justify="center" align="bottom" class="code-row-bg">
      <Col span="4"><p style="height: 80px">col-4</p></Col>
      <Col span="4"><p style="height: 30px">col-4</p></Col>
      <Col span="4"><p style="height: 100px">col-4</p></Col>
      <Col span="4"><p style="height: 60px">col-4</p></Col>
  </Row>
  <p>居中对齐</p>
  <Row type="flex" justify="center" align="middle" class="code-row-bg">
      <Col span="4"><p style="height: 80px">col-4</p></Col>
      <Col span="4"><p style="height: 30px">col-4</p></Col>
      <Col span="4"><p style="height: 100px">col-4</p></Col>
      <Col span="4"><p style="height: 60px">col-4</p></Col>
  </Row>
  <br>

<h2>响应式</h2>
<Row>
    <Col :xs="2" :sm="4" :md="6" :lg="8">Col</Col>
    <Col :xs="20" :sm="16" :md="12" :lg="8">Col</Col>
    <Col :xs="2" :sm="4" :md="6" :lg="8">Col</Col>
</Row>
<br>

<h2>其它属性的响应式</h2>
<p>span pull push offset order 属性可以通过内嵌到 xs sm md lg 属性中来使用。
其中 :xs="6" 相当于 :xs="{ span: 6 }"。</p>
<Row>
    <Col :xs="{ span: 5, offset: 1 }" :lg="{ span: 6, offset: 2 }">Col</Col>
    <Col :xs="{ span: 11, offset: 1 }" :lg="{ span: 6, offset: 2 }">Col</Col>
    <Col :xs="{ span: 5, offset: 1 }" :lg="{ span: 6, offset: 2 }">Col</Col>
</Row>
<br>

</div>
</template>

<script>
export default {

}
</script>


<style lang="scss" scoped>

.box {
  overflow: hidden;
    h2 {
        font-size: 16px;
        // text-align: center;
    }
    .ivu-col {
        margin-bottom: 5px;
        background-color: #fcc070;
        &:nth-child(2n) {
          background-color: pink;
        }
        &:hover {
            background-color: skyblue;
            color: #fff;
        }
        > div {
          background-color: #42b983;
        }
    }
}
</style>
