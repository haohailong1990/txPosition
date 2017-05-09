##腾讯地图定位API
###页面中需要引入以下js文件
1,腾讯js文件 
>http://map.qq.com/api/js?v=2.exp&libraries=drawing,geometry,autocomplete,convertor"

2,定位插件
>ThreeLinkAge_tengxun.js
###返回的数据格式参数说明
* 第一个数组的name代表返回的省名称
* 第二个数组的name代表返回的市名称
* 最里层的list返回当前省市的柜台信息
* adress - 返回的详细地址
* conterId - 当前的柜台Id
* counterName - 返回的柜台名称
* loaction - 返回的经纬度

### 实例化对象后台
<pre>
new ThreeLinkAge({
  updateProvice:function(data){
  }
</pre>
###实例化参数说明
* data:ajax获取的json数组数据
* provice:页面省下拉框dom
* success: 定位成功回调
* updateProvice:省份更新回调