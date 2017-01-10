<template>
  <div id="app">
  	<router-view></router-view>
    <navHeader></navHeader>
    <limitText></limitText>
		<addText></addText>
  </div>
</template>

<script>
import navHeader from './components/header.vue'
import limitText from './components/limitText.vue'
import addText from './components/addText.vue'
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
			navHeader,
      limitText,
      addText
	}
}
</script>

<style>
@import "./assets/css/iconfont.css";
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;
  color: #2c3e50;
  margin-top: 60px;*/
}

h1, h2 {
  font-weight: normal;
}
a {
  color: #42b983;
}
#wrapper::-webkit-scrollbar {
				width: 0px;
			}
      * {
  margin: 0;
  padding: 0;
  -webkit-tap-highlight-color: transparent;
  -webkit-text-size-adjust: none; }

p {
  margin: 0;
  padding: 0; }

a {
  text-decoration: none !important; }

.L_img {
  display: block !important;
  margin: 4.6rem auto 1.25rem;
  width: 4.8rem;
  height: auto; }

.L_con {
  width: 100%;
  text-align: center;
  font-size: 0.55rem;
  color: #666666; }
  .L_con span {
    position: relative;
    top: 0.275rem; }

.locationPositon {
  width: 100%;
  height: 1.825rem;
  position: relative;
  border-bottom: 1px solid #e8e8e8;
  background: #ffffff; }

.positionSelect {
  position: absolute;
  left: 1.25rem;
  top: 50%;
  -webkit-transform: translateY(-50%);
      -ms-transform: translateY(-50%);
          transform: translateY(-50%);
  font-size: 0.55rem;
  color: #333333;
  width: 13.275rem;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap; }

.posIcon {
  position: absolute;
  left: 0.5rem;
  top: 50%;
  -webkit-transform: translateY(-50%);
      -ms-transform: translateY(-50%);
          transform: translateY(-50%);
  color: #2dbe60; }

.rightIcon {
  position: absolute;
  right: 0.5rem;
  top: 50%;
  -webkit-transform: translateY(-50%);
      -ms-transform: translateY(-50%);
          transform: translateY(-50%);
  color: #CCCCCC; }

.bgColor {
  background: #f5f5f5; }

.extraText {
  width: 100%;
  height: 7.2rem;
  position: relative;
  background: #ffffff; }
  .extraText p {
    font-size: 0.5rem;
    color: #333333;
    padding: 0.6rem 0.5rem 0; }

.extraTextScore {
  width: 2.275rem;
  height: 0.525rem;
  color: #2dbe60;
  position: absolute;
  right: 0.5rem;
  bottom: 3.025rem;
  font-size: 0.5rem; }

.submitButtom {
  width: 12.75rem;
  height: 1.5rem;
  background: #2dbe60;
  position: absolute;
  left: 50%;
  -webkit-transform: translateX(-50%);
      -ms-transform: translateX(-50%);
          transform: translateX(-50%);
  bottom: 0.5rem;
  border-radius: 0.75rem;
  color: #ffffff;
  font-size: 0.65rem;
  text-align: center;
  line-height: 1.5rem; }

#wrapper {
  position: absolute;
  z-index: 1;
  top: 10.4rem;
  bottom: 0;
  left: 0;
  width: 100%;
  overflow: auto; }

#scroller {
  position: absolute;
  z-index: 1;
  /*  -webkit-touch-callout:none;*/
  -webkit-tap-highlight-color: transparent;
  width: 100%;
  padding: 0; }

#scroller ul {
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: left; }

#wrapper1 {
  position: absolute;
  z-index: 1;
  top: 2.425rem;
  bottom: 0;
  left: 0;
  width: 100%;
  overflow: auto !important;
  background: #f5f5f5; }

#scroller1 {
  position: absolute;
  z-index: 1;
  /*  -webkit-touch-callout:none;*/
  -webkit-tap-highlight-color: transparent;
  width: 100%;
  padding: 0; }

#scroller1 ul {
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: left; }

.titleIcon {
  width: 100%;
  height: 1.375rem;
  position: relative; }

.titleIcon-title {
  position: absolute;
  left: 1.5rem;
  top: 0.53rem;
  font-size: 0.5rem;
  color: #666666; }

.titleIcon-i {
  position: absolute;
  left: 0.5rem;
  top: 0.5rem;
  color: #2DBE60; }

.PositionInfo {
  padding: 0.35rem 0rem 0.5rem 0rem!important; }
  .PositionInfo > li {
    list-style: none;
    border: 1px solid #e8e8e8;
    border-radius: 8px;
    background: #ffffff;
    position: relative;
    margin: 0px 0.5rem 0.5rem 0.5rem;}

.listTitle {
  height: 1.175rem;
  font-size: 0.5rem;
  color: #888888;
  border-bottom: 1px solid #E8E8E8;
  position: relative; }

.listDate {
  position: absolute;
  left: 0.5rem;
  top: 0.375rem; }

.listHour {
  position: absolute;
  left: 3.85rem;
  top: 0.375rem; }

.positionIcon {
  position: absolute;
  left: 0.5rem;
  top: 1.6rem;
  color: #CCCCCC; }
.positionIconBlue{
	position: absolute;
  left: 0.5rem;
  top: 1.6rem;
  color: #2DBE60;
}
.positionIconInfo {
  font-size: 0.55rem;
  color: #333333;
  padding: 0.5rem 0.65rem 0 1.2rem;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
  overflow: hidden;
  margin-bottom: 0.5rem; }

.positionText {
  font-size: 0.45rem;
  color: #999999;
  padding: 0 0.825rem 0.5rem 1.2rem; }

#allmap {
  width: 100%;
  height: 500px; }

.searchText {
  width: 100%;
  height: 1.925rem;
  background: #ffffff;
  position: relative;
  margin-bottom: 0.5rem; }
  .searchText input {
    width: 11.2rem;
    height: 1.1rem;
    position: absolute;
    top: 50%;
    -webkit-transform: translateY(-50%);
        -ms-transform: translateY(-50%);
            transform: translateY(-50%);
    border: none;
    background: #f2f2f2;
    border-radius: 6px;
    padding-left: 0.5rem;
    font-size: 0.55rem;
    color: #333333; }
  .searchText input:focus {
    outline: none; }
  .searchText input::-webkit-input-placeholder {
    color: #878787; }
  .searchText span {
    position: absolute;
    right: 0.5rem;
    top: 50%;
    -webkit-transform: translateY(-50%);
        -ms-transform: translateY(-50%);
            transform: translateY(-50%);
    font-size: 0.6rem;
    color: #2DBE60; }

.hidden li {
  height: 1.775rem;
  border-bottom: 1px solid #e8e8e8;
  background: #ffffff;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  font-size: 0.55rem;
  color: #333333;
  padding: 0 1rem;
  line-height: 1.775rem; }

.lanren {
  margin: 0 auto;
  overflow: hidden;
  text-align: left;
  background: #fff; }

.lanren ul.list {
  overflow: hidden;
  padding: 0 !important;
  text-align: center;
  font-size: 0.55rem;
  color: #999999; }

.lanren ul.list li {
  height: 1.775rem;
  border-bottom: 1px solid #e8e8e8;
  background: #ffffff;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  font-size: 0.55rem;
  color: #333333;
  padding: 0 1rem;
  line-height: 1.775rem;
  cursor: pointer; 
  text-align: left;}

.lanren ul.list p {
  text-align: center;
  font-size: 0.55rem; }

.lanren .more {
  overflow: hidden;
  text-align: center;
  height: 1.775rem;
  line-height: 1.775rem; }

.lanren .more a {
  color: #999999;
  margin: 0 auto;
  text-align: center;
  font-size: 0.55rem; }

.lanren .more p {
  font-size: 0.55rem;
  color: #999999; }

textarea {
  resize: none;
  width: 100%;
  border: none; }

textarea:focus {
  outline: none; }

.falseIcon {
  position: absolute;
  right: 2.8rem;
  top: 50%;
  -webkit-transform: translateY(-50%);
      -ms-transform: translateY(-50%);
          transform: translateY(-50%);
  color: #ffffff;
  font-size: 0.575rem !important;
  display: none;
  background: #bdbdbd;
  width: 0.65rem;
  height: 0.65rem;
  border-radius: 100%;
  text-align: center;
  line-height: normal; }

.inputFid {
  width: 12.85rem;
  height: 1.1rem;
  position: absolute;
  top: 50%;
  -webkit-transform: translateY(-50%);
      -ms-transform: translateY(-50%);
          transform: translateY(-50%);
  left: 0.5rem;
  border: none;
  background: #f2f2f2;
  border-radius: 6px;
  font-size: 0.55rem;
  color: #333333; }

</style>
