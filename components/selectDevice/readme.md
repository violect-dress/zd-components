
<a href="../../readme.md"><button>返回</button></a>


####参数 props

| 参数 | 类型 | 父级 | 说明 | 默认值
| :--- | :---|:---| :--- | :---
| stationId |  [String, Number] || 场站ID, 也可通过show方法注入 | ''
| treeProps | Object || 左边树相关参数| {}
| req | Function | treeProps | 树型结构请求函数 | `/core/station/region/listWithTree/${stationId}`
|dataProp | String | treeProps | 树形结构请求后取的属性 | rows
|listToTree|Boolean|treeProps | 区域树是否需要转树形结构 | false
|label|String|treeProps | 树的label字段 | 'name'
|value|String|treeProps | 树的value字段 | 'id'
|||||
| tableProps | Object || 右边列表相关参数| {}
| req | Function | tableProps | 列表请求函数 | `/sub-camera/device/config/getCameraDevice`
| handleParams | Function | tableProps | 列表处理请求数据函数 | 参数：对象{areaId,stationId}
| singleSelect | Boolean | tableProps | 是否单选 | false
|||||
| paginationProps | Object || 分页相关参数| {}
| size | Object |Number| 分页相关参数| 10
|||||
| dialogProps | Object || dialog相关参数| {}
|||||
| submitProps | Object || 提交数据时相关参数| {}
| handleParams | Function | submitProps | 提交数据处理函数 | 参数：对象{addList,delList,stationId}

####事件 events

| 事件 | 说明 | 参数
| :--- | :---|:---| :--- | :---
| success | 处理成功后触发 | ''
|changeLine | 行被'选择'或'取消选择'时触发| {row, close} row为该行数据，close为关闭弹窗函数

####方法 methods

| 方法名 | 说明 | 参数
| :--- | :---|:---| :--- | :---
| show | 打开弹窗 | {selectedData(已选择数据), stationId(场站ID)}
|dialogBeforeClose | 关闭弹窗| 