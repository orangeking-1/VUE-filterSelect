# VUE-filterSelect
基于element-ui封装的一个筛选下拉框

## 功能
一个能删选内容的下拉框

## 效果图
![效果图](https://github.com/orangekingliness/image-folder/blob/master/vue-filterSelect/1.png)
![效果图](https://github.com/orangekingliness/image-folder/blob/master/vue-filterSelect/2.png)

## 实例
```
// filterCondition 为筛选条件, 格式为[{id:1,label:'待审核'}，{id:2,label:'全部'}]
// filterData 筛选的数据，格式为[{dataId:1,dataName:'sdk-ase-dd'},...]

// 调用实例
<filterSelect
            :defaultValue='defaultFirstBridgeVal'
            :filterCondition="bridgeConditionArr"
            v-on:selectConditionFunc='changeCdnFunc'
            :filterData="filterBridgeData"
            v-on:pitchOnFunc='pitchOnBridgeItemFunc'
            ></filterSelect>
            
data () {
  return {
    defaultFirstBridgeVal: '',
    bridgeConditionArr: [{
        id: 1,
        label: '全部'
      }, {
        id: 2,
        label: '待审核'
      }],
    filterBridgeData: [{dataId:1,dataName:'sdk-ase-dd'}，{dataId:2,dataName:'sdk-ase-dd'}],  
  }
}

methods: {
  changeCdnFunc (data) {
      console.log(data)
  },
  pitchOnBridgeItemFunc (data) {
    console.log(data)
  }
}

```

