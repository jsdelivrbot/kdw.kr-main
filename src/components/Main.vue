<template>
  <div id="main">
      <center><h2>안녕하세요 ? KDW KR 입니다.</h2></center>
      <div :class="$style['list']">
        <div v-for="card in list" :class="$style['card']">
          <div :class="$style['title']">{{card.title}}</div>
          <div :class="$style['desc']" v-html="card.desc"></div>
          <a :class="$style['url']" :href="card.url" target="_blank">{{card.url}}</a>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      list: [
        {title: '포트폴리오', desc: '김대운의 포트폴리오 사이트 입니다.', url: 'https://portfolio.kdw.kr'},
        {title: '유틸', desc: '각종 기능을 모아둔 유틸 사이트 입니다.<br> 인코딩/디코딩, 글자수 세기, 글자 뒤집기, 글자 변환 지원.', url: 'https://utils.kdw.kr'},
        {title: '에듀', desc: '웹, 앱 등 독학을 위한 여러 자료를 모아둔 사이트 입니다.', url: 'https://edu.kdw.kr'},
      ]
    }
  }
}
</script>

<style lang="scss" module>
.list {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  flex-flow: row wrap;
}
.card {
  width: 20rem;
  height: 10rem;
  background-color: #ffffff;
  box-shadow: 0 2px 12px 0 rgba(0,0,0,.1);
  border: 1px solid #ebeef5;
  text-align: center;
  word-break: keep-all;
  word-wrap: break-word;
  .title {
    font-size: 1.8rem;
    border-bottom: 1px solid #ebeef5;
    margin-bottom: 0.125rem;
    padding: 0.5rem;
  }
  .desc {
    font-size: 1rem;
    padding: 0.25rem;
  }
  .url {
    font-size: 0.75rem;
    padding: 0.25rem;
  }
}
</style>
