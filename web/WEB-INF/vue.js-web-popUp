
<%@ page import="com.leaseAndLending.entity.RoomEntity" %>
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<!DOCTYPE html>
<html lang="en">

<head>
	<meta charset="UTF-8">
	<title>房屋详情</title>
	<link rel="stylesheet" href="webpage/zc/css/base.css">
	<link rel="stylesheet" href="webpage/zc/layui/css/layui.css">
	<link rel="stylesheet" href="../webpage/main/plug-in/hplus/skin/WdatePicker.css" />
	<link rel="stylesheet" href="webpage/zc/leaseAndLending/css/popUp.css"/>
	<script type="text/javascript" src="webpage/zc/js/My97DatePicker/WdatePicker.js"></script>
	<script src="webpage/zc/js/jquery-3.2.1.js"></script>
	<script src="webpage/zc/js/layer/layer.js"></script>
	<script type="text/javascript" src="plug-in/tools/curdtools_zh-cn.js"></script>


	<script src="webpage/zc/js/vue.min.js"></script>
	<script src="webpage/zc/js/vue-resource.min.js"></script>
	<style>
		* {
			font-size: 14px;
			box-sizing: border-box;
		}

		body {
			background: #f9f9f9;
			margin-bottom: 30px;
		}

		.center {
			text-align: center;
		}

		.header-top {
			overflow: hidden;
			height: 45px;
			line-height: 45px;
			padding: 0 20px;
		}

		.bc {
			height: 30px;
			background-color: #1598ed;
			color: #fff;
			padding: 0 10px;
			line-height: 30px;
			margin-left: 20px;
			border-radius: 4px;
			margin-top: 5px;
			cursor: pointer;
		}

		.bc img {
			vertical-align: middle;
		}

		.djbh>div {
			width: 100px;
			font-size: 16px;
		}

		.gdt {
			padding: 20px;
			border: 1px solid #1598ed;
		}

		.tr1 td input {
			width: 100%;
			height: 100%;
			text-align: center;
			border: 0;
		}

		.splc {
			width: 96%;
			padding: 0px 30px;
			border-radius: 10px;
			margin: 0 auto;
			height: 240px;
			background-color: #c2e8ff;
			box-shadow: 1px 2px 10px #787879;
			margin-bottom: 10px;
			display: none;
		}

		.content {
			width: 96%;
			padding: 0px 30px;
			border-radius: 10px;
			margin: 0 auto;
			/* height: 800px; */
			background-color: #fff;
		}

		.content-top {
			width: 285px;
			margin: 0 auto;
			padding: 0 10px;
			height: 50px;
			text-align: center;
			line-height: 50px;
			font-size: 24px;
			color: #4b98df;
			text-align: center;

		}

		.two-heng {
			width: 285px;
			margin: 0 auto;
			height: 4px;
			border-top: 1px solid #4b98df;
			border-bottom: 1px solid #4b98df;
		}

		.zjhz-bigbox {
            margin-top: 10px;
			padding: 10px;
			border: 1px solid #4b98df;
		}

		.dataImg {
			background-image: url("lib/images/日历.png");
			background-repeat: no-repeat;
			background-position: 95%;

		}

		.zjhz-top {
			width: 100%;
			text-align: center;
			color: #fff;
			height: 38px;
			background: #67bef3;
			line-height: 38px;
		}

		/* 楼宇列表 */
		.zhejiu {
			width: 100%;
			overflow: hidden;
			border: 1px solid #67bef3;
			display: flex;
			word-wrap: break-word;
			margin-bottom: -1px;
		}

		.zhejiu>div {
			width: 25%;
			height: 40px;
			line-height: 40px;
			text-align: center;
			border-left: 1px solid #67bef3;
			border-bottom: 1px solid #67bef3;
			background: #c2e8ff;
			color: #333;
			margin: 0 0 0 -1px;
			border-bottom: none;
		}

		.zhejiu>input {
			width: 25%;
			height: 40px;
			line-height: 40px;
			text-align: left;
			border: 0;
			border-left: 1px solid #67bef3;
			border-bottom: none;

		}

		.djzt {
			margin-top: 10px;
			width: 100%;
			height: 40px;
			color: #000;
			display: flex;
		}

		.djzt>div {
			width: 15.5%;
		}

		.djzt>div:nth-of-type(odd) {
			text-align: right;
			height: 38px;
			line-height: 38px;
		}

		.djzt>div:nth-of-type(even) {
			text-align: left;
			height: 38px;
			line-height: 38px;
		}

		.tbbox {
			overflow: auto;
			height: 250px;
		}

		#table1 {
			width: 100%;
		}

		.table1 th,
	   .table1	td {
			border: 1px solid #67bef3;
			height: 38px;
		}

		.table2 th,
	   .table2	td {
			border: 1px solid #67bef3;
			height: 38px;
		}

	 .table1 th {
			background: #c2e8ff;
		}
		.table2 th {
			background: #c2e8ff;
		}

		.zjmx {
			width: 100%;
			/* height: 210px; */
			border: 1px solid #67bef3;
			margin-top: 20px;
		}

		.zjmx-top-title {
			width: 150px;
			height: 40px;
			line-height: 40px;
			text-align: center;
			color: #fff;
			background-color: #67bef3;
		}

		.zjmx-bigbox {
			padding: 10px;
			border: 1px solid #4b98df;
			/* max-height: 300px; */
			/* height: 332px; */
		}

		#table2 {
			width: 100%;

		}

		.tb-mx {
			width: 100%;
			margin: 0 auto;
			/* max-height: 269px; */
			overflow: auto;
		}

		.tb-max {
			width: 98%;
			margin: 10px auto;
			/* max-height: 250px; */
		}
		.tb-max .active {
			display: block;
		}

		.tab {
			border-bottom: 0;
		}

		.tab span {
			height: 38px;
			width: 100px;
			display: block;
			font-size: 14px;
			line-height: 38px;
			text-align: center;
			color: #666;
			border-radius: 4px 4px 0 0;
			cursor: pointer;
			border: 1px solid #eee;

		}

		.tab .active {
			width: 97px;
			background-color: #8bbeea;
			color: #fff;
			margin-left: 5px;
		}

		.table1,
		.table2 {
			width: 100%;
			table-layout: fixed;
		}

		.sell {
			height: 40px;
			border: none;
			border-left: 1px solid #67bef3;
			text-align: center;
			text-align-last: center;
			overflow: hidden;
		}

		.choose {
			background: url(../webpage/zc/images/choose.jpg) no-repeat;
			background-position: 106px 9px;
		}

		.download {
			background: url(../webpage/zc/images/download.png) no-repeat;
			background-position: center;
		}

		.look {
			background: url(../webpage/zc/images/eye.png) no-repeat;
			background-position: center;
		}

		.del {
			background: url(../webpage/zc/images/del.png) no-repeat;
			background-position: center;
		}

		.send {
			display: inline-block;
			background: white;
		}

		.start {
			background: url(../webpage/zc/images/date.png) no-repeat;
			background-position: 96% center;
			cursor: pointer;
		}

		.delete {
			display: inline-block;
			text-align: center;
			width: 100%;
			height: 100%;
		}

		.less {
			display: inline-block;
			border: 0;
		}
	</style>
</head>

<body>

	<%--<!-- 整个大的盒子 --*>--%>
	<div id="app" style="width:100%;height: 100%;">
		<div class="box">
			<%--<!-- 头的顶部内容 -->--%>
			<div class="header-top">
				<div>
					<div class="fr" style="margin:0 20px 0;">
						<!-- 增加 -->
						<%--<div class="fl bc" id="xz">--%>
							<%--<img src="../webpage/zc/images/xz.png" alt="">--%>
							<%--新增--%>
						<%--</div>--%>
						<!-- 保存 -->
						<div class="fl bc" v-on:click="alterEntity">
							<img src="../webpage/zc/images/bc-1.png" alt="">
							保存
						</div>
                        <div class="fl bc" v-on:click="deleteEntity" v-show="roomInfo.id!=null">
                            <img src="../webpage/zc/images/shouh.png" alt="">
                            删除
                        </div>

                        <div class="fl bc" onclick="">
							<img src="../webpage/zc/images/day.png" alt="" v-on:click="testData">
							打印
						</div>
					</div>
				</div>
			</div>
			<!-- 头部结束 -->
			<!-- 审批单内容 -->
			<div class="content">
				<!-- title -->
				<div class="content-top">
					房屋详情
				</div>
				<!-- 下划线 -->
				<div class="two-heng"></div>
				<!-- 	楼宇处理列表 -->
				<div class="zjhz-bigbox">
					<div class="zjhz-smallbox">
						<div class="zhejiu" id="topbox">

							<div style="display: none" id="roomId">${roomEntity.id}</div>

							<!-- 楼宇号 -->
							<div class="remark">楼宇号</div>
							<input type="text" readonly="readonly" class="count" v-model="roomInfo.buildingNum" v-on:click="selectBuilding">
							<div class="style">楼宇坐落</div>
							<input type="text" readonly="readonly" class="count"   v-model="buildingInfo.buildingLocation">
						</div>
						<div class="zhejiu">
							<%--<div>坐落位置</div>--%>
							<%--<input type="text" readonly="readonly" v-model="buildingSelected.buildingLocation">--%>
							<div class="end">房间号</div>
							<input type="text" :readonly="writeAble ? false: 'readonly' " v-model="roomInfo.roomNum">
							<div>单位名称</div>
							<input type="text" readonly="readonly" v-model="userInfo.coName">
						</div>
						<div class="zhejiu">
							<div>建筑面积</div>
							<input type="text" :readonly="writeAble ? false: 'readonly' " v-model="roomInfo.structureArea">
							<div class="end">使用面积</div>
							<input type="text" :readonly="writeAble ? false: 'readonly' " v-model="roomInfo.useableArea">
						</div>

						<div class="zhejiu">
							<div>楼层</div>
							<input type="text" :readonly="writeAble ? false: 'readonly' " v-model="roomInfo.floor">
							<div class="end">房间状态</div>
							<select :readonly="writeAble ? false: 'readonly' "  v-model="roomInfo.roomStatus" class="seleOne" autocomplete="off">
								<option value="1" selected="selected">闲置</option>
								<option value="2">出租</option>
								<option value="3">自用</option>
								<option value="4">装修</option>
							</select>
						</div>
						<div class="zhejiu">
						</div>
						<%--隐藏部分--%>
						<div class="zhejiu" v-show="false">
							<div>单位代码</div>
							<input type="text" readonly="readonly" v-model="userInfo.coCode">
							<div>备用</div>
							<input type="text" readonly="readonly">
						</div>

					</div>
					<!-- 结束 -->
					<!-- 外包层 -->
					<div class="zjmx">
						<!-- 按钮 -->
						<div class="tab">
							<div style="width:400px;height:38px;background:#fff; display: flex;margin-left: 10px;">
								<span v-on:click="subTagClick(1)" class="fl" v-bind:class="{active : subTable==1}" id="card">资产卡片</span>
								<span v-on:click="subTagClick(2)" class="fl" v-bind:class="{active : subTable==2}" id="update">附件上传</span>
							</div>
						</div>
						<!-- 资产卡片 -->
						<div class="tb-max" id="" v-show="subTable==1">
							<table class="table1" id="table2">
								<thead>
								<tr>
									<th style="width: 100px;">
										<img src="../webpage/zc/images/add.png" alt="" class="add_facard" v-on:click="addfacard">
									</th>
									<th style="width:133px">资产编号</th>
									<th style="width:133px">资产名称</th>
									<th style="width:133px">资产类别</th>
									<th style="width:133px">数量</th>
									<th style="width:133px">单位名称</th>
									<th style="width:133px">原值</th>
									<th style="width:133px">净值</th>
									<th style="width:133px">累计折旧</th>
								</tr>
								</thead>
								<tbody class="tbody1" id="tbody">
								<tr v-for="(facard,index) in facardData">
									<td><span class='delete'><img src='../webpage/zc/images/less.png' alt='' style='margin-top:10px;' class='less' v-on:click="delRow(index,'facard')"></span></td>
									<td style="color:#2828ff" v-on:click="openFaCard(facard.cardId)">{{facard.cardId}}</td>
									<td>{{facard.faName}}</td>
									<td>{{facard.fatypeCode}}</td>
									<td style="text-align: end">{{facard.qty}}</td>
									<td>{{facard.coName}}</td>
									<td style="text-align: end">{{facard.cost}}</td>
									<td style="text-align: end">{{facard.depLeft}}</td>
									<td style="text-align: end">{{facard.depTotal}}</td>


								</tr>

								</tbody>
							</table>
						</div>

						<!-- 附件上传 -->
						<div class="tb-max" v-show="subTable==2">
							<table class="table1" id="table1">
								<thead>
								<tr>
									<th style="width:2%">
										<img src="../webpage/zc/images/yun.png" onclick="upfile()">
									</th>
									<th style="width:133px">文件名称</th>
									<th style="width:133px">附件</th>
									<th style="width:133px">下载</th>
									<th style="width:133px">查看</th>
									<th style="width:133px">删除</th>
								</tr>
								</thead>
								<tbody class="tbody1" id="tbody">
									<tr v-for="(file,index) in fileData">
										<td></td>
										<td>{{file.fileName}}</td>
										<td>{{file.filePath}}</td>
										<td class='center'><img onclick='downloadxxFjFile1(this)' src='webpage/zc/images/download.png' alt=''></td>
										<td class='center'><img onclick='downloadxxFjFile2(this)' src='webpage/zc/images/eye.png' alt=''></td>
										<td class='center'><img v-on:click="delRow(index,'file')" src='webpage/zc/images/del.png' alt=''></td>
									</tr>
								</tbody>
							</table>
						</div>
					</div>
				</div>
			</div>

		</div>

		<div class="ceng" v-show="popUp" >
           <div class="kuangJia" style="width: 800px; height: 496px; margin: 150px auto;">
			<div  class="popUp">
				<div class="placeSele">
					<span style="color:white">请选择</span>
					<span class="guanBi"  v-on:click="closePopUp">x</span>
				</div>
				<div class="header searchColums-box">
					<div>
						<div class="tableTit">
							<span class="keyWords">楼宇信息关键字 :</span>
							<input type="text" class="tableInt" v-model="searchKey">
							<a href="javascript:;" class="search" v-on:click="getDataList">搜索</a>
							<a href="javascript:;" class="reset" v-on:click="searchKey='';getDataList()"
							   >重制</a>
						</div>
					</div>


				</div>
				<%--查询弹出框 表格--%>
				<div class="tableContent">
					<table  v-if="queryType=='room'" >
						<tr class="tableList">
							<th id="id" style="display:none">房间id</th>
							<th id="null" style="width:6%"></th>
							<th id="buildingNum" style="width:13%">楼宇号</th>
							<th id="roomNum" style="width:13%">房间号</th>
							<th id="roomStatus" style="width:13%">房间状态</th>
							<th id="floor" style="width:13%">楼层</th>
							<th id="structureArea" style="width:13%">建筑面积</th>
							<th id="useableArea" style="width:13%">使用面积</th>
							<th id="coName" style="width:13%;border-right: none;">单位名称</th>
						</tr>
						<tbody class="tableList2">
						<tr v-for="(rowData,index) in dataList" v-on:click="selected(index)"
							v-bind:class="{selected:rowSelected.includes(index)}">
							<td style="width:6%">{{index+1}}</td>
							<td style="width:13%">{{rowData.buildingNum}}</td>
							<td style="width:13%">{{rowData.roomNum}}</td>
							<td style="width:13%">{{rowData.roomStatus}}</td>
							<td style="width:13%">{{rowData.floor}}</td>
							<td style="width:13%">{{rowData.structureArea}}</td>
							<td style="width:13%">{{rowData.useableArea}}</td>
							<td style="width:13%;border-right: none;">{{rowData.coName}}</td>
						</tr>
						</tbody>
					</table>
					<table  v-if="queryType=='room_faCard'" id="facardTable" class="tableList">
						<thead  class="tableList1">
						<tr>
							<th id="index" style="width: 29px;background: #F4F4F4;border-bottom: 3px solid #dddddd"></th>
							<th style="width: 25px;"><input type="checkbox" v-on:click="selectAll()" v-model="checkedAll"></th>
							<th id="cardId" style="width: 138px;">卡片编号</th>
							<th id="faName" style="width: 93px; ">资产名称</th>
							<th id="fatypeName" style="width: 99px;">资产类别</th>
							<th id="cost" style="width: 76px;">原值</th>
							<th id="depLeft" style="width: 75px;">净值</th>
							<th id="depTotal" style="width: 93px;">累计折旧</th>
							<th id="qty" style="width: 79px;">数量</th>
							<th id="coName" style="border-right: none; width: 131px;">单位名称</th>
						</tr>
						</thead>
						<tbody class="tableList2">
						<tr v-for="(rowData,index) in dataList" v-on:click="selected(index)"
							v-bind:class="{selected:rowSelected.includes((dataListPage-1)*dataListRows+index)}" >
							<td style="width: 28px;background: #F4F4F4;font-size: 12px;">{{(dataListPage-1)*dataListRows+index+1}}</td>
							<td style="width: 26px;"><input type="checkbox" v-model="rowSelected.indexOf((dataListPage-1)*dataListRows+index)!=-1"></td>
							<td style="width: 131px;"><span style="width: 20px; font-size: 12px; color: #000000;line-height: 18px;">{{rowData.cardId}}</span></td>
							<td style="width: 95px;overflow: hidden">{{rowData.faName}}</td>
							<td style="width: 95px;overflow: hidden"><span style="width: 94px; height: 19px; display: inline-block;overflow: hidden;">{{rowData.fatypeName}}</span></td>
							<td style="width: 76px;">{{rowData.cost}}</td>
							<td style="width: 76px;">{{rowData.depLeft}}</td>
							<td style="width: 95px;">{{rowData.depTotal}}</td>
							<td style="width: 80px;">{{rowData.qty}}</td>
							<td style="border-right: none;width: 124px;">{{rowData.coName}}</td>
						</tr>
						</tbody>
					</table>
					<table  v-if="queryType=='building'" id="buildingTable" class="tableList">
						<thead class="tableList1">
							<tr>
							<th id="index" style="width: 46px;background: #F4F4F4;border-bottom: 3px solid #dddddd"></th>
							<th id="buildingNum" style="width: 145px;">楼宇号</th>
							<th id="buildingLocation" style="width: 130px; ">坐落位置</th>
							<th id="buildingArea" style="width: 120px;">楼宇面积</th>
							<th id="buildingFloor" style="width: 110px;">层数</th>
							<th id="buildingRooms" style="width: 110px;">房间数</th>
							<th id="coName" style="width: 146px;">单位名称</th>
							</tr>
						</thead>
						<tbody class="tableList2" >
							<tr v-for="(rowData,index) in dataList" v-on:click="selected(index)"
							v-bind:class="{selected:rowSelected.includes((dataListPage-1)*dataListRows+index)}">
							<td style="width: 46px;background: #F4F4F4;">{{(dataListPage-1)*dataListRows+index+1}}</td>
							<td style="width: 145px;overflow: hidden">{{rowData.buildingNum}}</td>
							<td style="width: 130px;overflow: hidden">{{rowData.buildingLocation}}</td>
							<td style="width: 120px;">{{rowData.buildingArea}}</td>
							<td style="width: 110px;">{{rowData.buildingFloor}}</td>
							<td style="width: 110px;">{{rowData.buildingRooms}}</td>
							<td style="width: 138px;">{{rowData.coName}}</td>
							</tr>
						</tbody>
					</table>

				</div>

			</div>
			   <%--尾部--%>
			   <div class="footer">
				   <div class="footSele">
					   <select name="" id="" v-model="dataListRows" class="seleTwo">
						   <option value="10">10</option>
						   <option value="20">20</option>
						   <option value="30">30</option>
						   <option value="50">50</option>

					   </select>
					   <span class="line"></span>
					   <span class="left1">
								<img src="webpage/zc/images/retreatquickly.png" v-on:click="pageChange(-9)" alt="" width="13px" height="13px">
							</span>
					   <span class="left2">
								<img src="webpage/zc/images/shangyiye.png" alt="" v-on:click="pageChange(-1)" id="decreasePage" width="13px" height="13px">
							</span>
					   <span class="line"></span>
					   <span class="num">
								<span class="numStart">
									<input type="text" v-model="dataListPage">
								</span>/
								<span class="numEnd">{{Math.ceil(dataListCount/dataListRows)}}</span>
								<span class="line"></span>
							</span>
					   <span class="left1" >
								<img src="./../webpage/zc/images/xiayiye.png"  v-on:click="pageChange(1)" id="addPage" alt="" width="13px" height="13px">
							</span>
					   <span class="left2">
								<img src="./../webpage/zc/images/forward.png" v-on:click="pageChange(9)" alt="" width="13px" height="13px">
							</span>
					   <span class="line"></span>
					   <span class="right">
								<img src="./../webpage/zc/images/shuaxin.png" alt="" v-on:click="" width="15px" height="15px">
							</span>
					   <span class="pages">
								<span class="change"></span>
								<span class="totalPages">共{{dataListCount}}条</span>
							</span>
				   </div>
				   <div class="footBtn">
					   <button class="enter" v-on:click="confirmPopUp">确认</button>
					   <button class="close" v-on:click="closePopUp">关闭</button>
				   </div>
			   </div>

		   </div>
		</div>

	</div>

</body>
<script type="text/javascript">
    var vm = new Vue({
        el: '#app',
        data: {
        	status:'',
        	//子表数据
			facardData: [],
			fileData:[],
			roomInfo:{},
			// buildingInfo:{id:'',buildingNum:''},
			userInfo:{},
			buildingInfo:{},
			//当前选择的字表
			subTable:1,
			//弹出框显示
			popUp:false,
			//查询类型
            queryType: '',
            //能否多选
            single: false,
            //查询框 表格数据
            dataList: [],
			//带序号的表格数据
			dataListI:{},
			dataListCount:0,
			dataListRows:10,
			dataListPage:1,
			//已选择行的真实行号
            rowSelected: [],
			// //当前页中已选择行的逻辑行号
			// rowSelectedPage:[],
			writeAble:true,
			searchKey:'',
			checkedAll:false

		},
		computed:{
            fileId:function () {
                fileArrary=[]
                this.fileData.forEach(function (i) {
                    fileArrary.push(i.fileName+','+i.filePath)
                })
                return fileArrary;
            },
			cardId:function () {
				cardArray=[]
				this.facardData.forEach(function (i) {
					cardArray.push(i.cardId)
				})
				return cardArray;
			},
			exclude:function () {
				type = this.queryType
				switch (type) {
					case 'room_faCard':
						return this.cardId
				}
			},
		},
        created: function () {
        	this.roomInfo.id=$('#roomId').text();
        	if(this.roomInfo.id==''){
        		this.status='add'
			}else{
        		this.status='other'
			}
        	this.getInfo();
            // console.log('!');
        },
		watch: {
			//每页显示行数
			dataListRows: function () {
				this.dataListPage = 1;
				this.getDataList();
			},
			//监控页   当page改变时更新表
			dataListPage: function () {
				// console.log(this.dataListPage)
				this.getDataList();
			}
		},
        methods: {
        	testData:function(){
        		console.log('test')
        		console.log(this.cardId())
			},
            //页面验证
            validating:function(){
        	    if(this.roomInfo.buildingId==null ||this.roomInfo.buildingId=='' || this.roomInfo.buildingNum==null || this.roomInfo.roomNum==null || this.roomInfo.roomNum==null ||this.roomInfo.floor==null||this.roomInfo.floor==''||this.roomInfo.roomStatus==null){
					this.popTip('请填写相关信息',5)
					return false
				}
        	    return true
            },
			subTagClick:function (num) {
				this.subTable=num;
			},
			//子表数据查询
			getDataList: function () {
        		//清空全选
				this.checkedAll=false;
				this.$http.post(
                    '/leaseAndLendingController.do?layerQuery_data',
                    { queryType: this.queryType,
						rows:this.dataListRows,
						page:this.dataListPage,
						exclude:this.exclude,
						searchKey:this.searchKey
					},
                    { emulateJSON: true }
                ).then(function (res) {
					this.dataList = res.body.dataList;
                    this.dataListCount = res.body.count;
                    //把数据存入dataListI
                    for(var i=0;i<res.body.dataList.length;i++){
                    	vm.dataListI[(vm.dataListPage-1)*vm.dataListRows+i]=res.body.dataList[i]
					}
                    // console.log(this.dataListI)
                }, function () {
                    console.log('请求失败处理');
                });
            },
			//页面初始房间信息查询
			getInfo: function () {
				this.$http.get(
						'/roomController.do?getInfo&roomId='+this.roomInfo.id
				).then(function (res) {
					if(res.body.room !=null){
						this.roomInfo = res.body.room;
					}
					if(res.body.facardList !=null){
                        this.facardData=res.body.facardList;
                    }
                    if(res.body.fileList !=null){
                        this.fileData=res.body.fileList;
                    }

					this.userInfo = res.body.userInfo;
					this.roomInfo.coName = res.body.userInfo.coName;
					this.roomInfo.coCode = res.body.userInfo.coCode;
					// console.log(this.roomInfo)
				}, function () {
					console.log('页面初始化 数据请求失败');
				});
			},
            selected: function (i) {
        		//得到真实序号
        		trueIndex=(this.dataListPage-1)*this.dataListRows+i
                // console.log(this.rowSelected)
				//单选逻辑
				if(this.single){
					this.rowSelected=[];
					this.rowSelected.push(trueIndex)
				}else{
					if (this.rowSelected.includes(trueIndex)) {
						this.rowSelected.splice(this.rowSelected.indexOf(trueIndex), 1)
					} else {
						this.rowSelected.push(trueIndex)
					}
				}
            },
			//全选
			selectAll:function(){
				startIndex=(this.dataListPage-1)*this.dataListRows
				endIndex=this.dataListPage*this.dataListRows-1
				//去重 增加选中的行号
				if(this.checkedAll==false){
					rowSet=new Set(this.rowSelected)
					for(i=startIndex;i<=endIndex;i++){
						rowSet.add(i)
					}
					vm.rowSelected=Array.from(rowSet)
				}else{
					for(i=startIndex;i<=endIndex;i++){
						vm.rowSelected.splice(this.rowSelected.indexOf(i), 1)
					}
				}

			},
			addRoom: function () {
				this.single=false;
				this.queryType='room';
				this.getDataList();
				this.popUp=true;
			},
			addfacard: function () {
				this.single=false;
				this.queryType='room_faCard';
				this.getDataList();
				this.popUp=true;
			},
			selectBuilding:function () {
        		//修改时不可改变关联楼宇
        		if(this.status!='add'){
        			return
				}
				this.single=true;
				this.queryType='building';
				this.getDataList();
				this.popUp=true;
			},
            //add update
			alterEntity:function(){
				//页面验证
				if(!this.validating()){return}
				//开始save update
				this.$http.post(
						'roomController.do?alter',
						{
							room:this.roomInfo,
							cardId:this.cardId,
							fileId:this.fileId
						}
				).then(function (res) {
					this.popTip('保存成功',1)
				},function () {
					this.popTip('保存失败',5)
				})
			},
			//删除操作
			deleteEntity:function() {
				layer.confirm("确定要删除吗?",{
					btn: ["确定","取消"]//, //按钮
					//shade: false //不显示遮罩
				},function (y) {
					vm.$http.post(
							'roomController.do?doDel',
							{id: vm.roomInfo.id},
							{emulateJSON: true}
					).then(function (res) {
								vm.popTip('删除成功',1)
							},
							function () {
								vm.popTip('删除失败',5)
							})
				},function (n) {
					return;
				})
			},

			//删除子表中所选行
			delRow:function (index,table){
				switch(table){
					case 'facard':
						this.facardData.splice(index,1);
						break;
					case 'file':
						this.fileData.splice(index,1);
						break;
				}
			},
			closePopUp: function () {
				this.rowSelected=[];
				this.dataListRows=10;
				this.dataListPage=1;
				this.popUp=false;
			},
			confirmPopUp: function (queryType){
				queryType=this.queryType;
				switch(queryType){
					case 'room_faCard':
						this.rowSelected.forEach(function (i) {
							vm.facardData.push(vm.dataListI[i])
						})
						break;
					case 'building':
						this.roomInfo.buildingId=this.dataListI[this.rowSelected[0]].id;
						this.roomInfo.buildingNum=this.dataListI[this.rowSelected[0]].buildingNum;
						this.buildingInfo=this.dataListI[this.rowSelected[0]];

						break;
				}
				//清空选择行
				this.rowSelected=[];
				this.dataListPage=1;
				this.checkedAll=false;
				this.popUp=false;
			},
			openFaCard:function(cardId){
				url="assetsController.do?selAssets&cardId="+cardId;
				addOneTab("资产卡片", url);
			},
			//查询弹出框 分页按钮
			pageChange:function (type) {
				switch (type) {
					case -1:
						if(this.dataListPage==1){
							this.popTip('已经是第一页',5)
							return
						}
						this.dataListPage=parseInt(this.dataListPage)-1;
						break
					case 1:
						if(this.dataListPage==Math.ceil(this.dataListCount/this.dataListRows)){
							this.popTip('已经时最后一页',5)
							return
						}
						this.dataListPage=parseInt(this.dataListPage)+1;
						break
					//第一页
					case 9:
						this.dataListPage=Math.ceil(this.dataListCount/this.dataListRows)
						break
					//最后一页
					case -9:
						this.dataListPage=1
						break
				}
			},
			//弹出提示框
			popTip:function (msg,icon) {
				layer.msg(msg, {
					time: 2000,
					icon: icon,
					shade: 0.3,
					shadeClose: true
				})
			}
        }
    })


	/**
	 * 相关附件的多文件上传处理
	 */
	function upfile(type) {
		var filePath = "";
		layer.open({
			type : 2,
			title : "上传文件",
			shadeClose : false,
			shade : 0.5,
			area : [ "400px", "40%" ],
			content : "webpage/zc/popUp/upLease.jsp?type=" + type
		});
	}

	//关闭弹出
	function closeitRelevant() {
		layer.closeAll();
	}
	//显示上传状态
	function showmsgRelevant(msg) {
		layer.msg(msg, {
			time : 2000,
			icon : 1,
			shade : 0.3,
			shadeClose : true
		}, function() {
			layer.closeAll();
		});
	}
	//上传成功之后回传上传文件的信息
	function backfullpathRelevant(fname) {
		var htmlStr = '';
		var file = fname.split("|");
		var zsCount = $("#tbody1").find("tr").length;//上传文件数量
		//轮播图片用
		//var lbimg="";
		for ( var i = 0; i < file.length; i++) {
			var filePath = file[i].split(",");
			var oldfilename=filePath[0].split(".");

			//把文件子表数据写入vue data
			vm.fileData.push({fileName:filePath[0],filePath:filePath[1]});
		}
	}

	/**
	 * 下载文件
	 * @author dongll
	 * @date 2018-09-30
	 */
	function downloadxxFjFile1(obj) {
		var filePath = $(obj).parent("td").parent("tr").find("td").eq(2).text();//下载路径
		var oldName = $(obj).parent("td").parent("tr").find("td").eq(1).text();//原文件名
		if (filePath == "") {
			return;
		} else {
			var form = $("<form>");//定义一个form表单
			form.attr("style", "display:none");
			form.attr("target", "");
			form.attr("method", "post");
			form.attr("action", "commonAssetsController.do?download");//URL
			var input = $("<input>");
			input.attr("type", "hidden");
			input.attr("name", "oldName");
			input.attr("value", oldName);
			form.append(input);

			var input = $("<input>");
			input.attr("type", "hidden");
			input.attr("name", "filePath");
			input.attr("value", filePath);
			form.append(input);
			$("body").append(form);//将表单放置在web中
			form.submit();//表单提交
			form.remove();//移除该临时元素

		}
	}
	function downloadxxFjFile2(obj) {
		var filePath = $(obj).parent("td").parent("tr").find("td").eq(2).text();//下载路径
		var oldName = $(obj).parent("td").parent("tr").find("td").eq(1).text();//原文件名
		if (filePath == "") {
			return;
		} else {
			var myWindow = window.open("", "_blank");
			myWindow.document
					.write("<form action='commonAssetsController.do?downloadInline' method='post' name='myform' style='display:none;' accept-charset='UTF-8'>"
							+ "<input type='hidden' name='oldName' value='"+oldName+"'/>"
							+ "<input type='hidden' name='filePath' value='"+filePath+"'/>"
							+ "</form>");
			myWindow.document.myform.submit();
		}
	}


</script>

</html>

