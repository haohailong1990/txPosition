##腾讯地图定位API
###页面中需要引入以下js文件
1,腾讯js文件 
>http://map.qq.com/api/js?v=2.exp&libraries=drawing,geometry,autocomplete,convertor"

2,定位插件
>ThreeLinkAge_tengxun.js###返回的数据格式![link](https://github.com/haohailong1990/txPosition/blob/master/images/1.png)
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
new ThreeLinkAge({  data:result.data,  provice:aoProvice,  city:aoCity,  district:aoDistrict,  location:true,  updateCounter: function(list){  },  success:function(data){  },
  updateProvice:function(data){
  }         })
</pre>
###实例化参数说明
* data:ajax获取的json数组数据
* provice:页面省下拉框dom* city:页面市下拉框dom* district:页面柜台下拉框dom* location:是否启用腾讯定位(值为true or false)* updateCounter:参数list返回当前市的柜台List集合
* success: 定位成功回调
* updateProvice:省份更新回调