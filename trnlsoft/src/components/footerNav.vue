<template>
  <div class="footer">
  	<el-container class="show_outbox hidden-xs-only">
      <el-main class="show_box">
      	<el-row class="footer">
    	    <el-col :sm="5" :md="5" :lg="5" :xl="5">
    	    	<h2>服务项目</h2>
    		    <router-link  :to="item.to" v-for="(item,index) of list1" :key="index" tag="li" @mouseenter.native="mouseenter(item)" @mouseleave.native="mouseleave(item)">
    	        <span :class="{showborder:item.detailShow}">{{item.html}}</span>
    	    	</router-link>
    	    </el-col>
    	    <el-col :sm="5" :md="5" :lg="5" :xl="5">
    	    	<h2>关于我们</h2>
    		    <router-link  :to="item.to" v-for="(item,index) of list2" :key="index" tag="li" @mouseenter.native="mouseenter(item)" @mouseleave.native="mouseleave(item)">
              <span :class="{showborder:item.detailShow}">{{item.html}}</span>
            </router-link>
    	    </el-col>
    	    <el-col :sm="4" :md="4" :lg="4" :xl="4">
    	    	<h2>开发实例</h2>
    		    <router-link  :to="item.to" v-for="(item,index) of list3" :key="index" tag="li" @mouseenter.native="mouseenter(item)" @mouseleave.native="mouseleave(item)">
              <span :class="{showborder:item.detailShow}">{{item.html}}</span>
            </router-link>
    	    </el-col>
    	    <el-col :sm="5" :md="5" :lg="5" :xl="5">
    	    	<h2>联系我们</h2>
    		   	<router-link  :to="item.to" v-for="(item,index) of list4" :key="index" tag="li" @mouseenter.native="mouseenter(item)" @mouseleave.native="mouseleave(item)">
              <span :class="{showborder:item.detailShow}">{{item.html}}</span>
            </router-link>
    	    </el-col>
    	    <el-col :sm="5" :md="5" :lg="5" :xl="5">
    	    	<h2>微信咨询</h2>
    		    	<li>
        				<img src="../../static/images/HT-code.png" class="code" alt="">
        			</li>
    	    </el-col>
    	  </el-row> 
	   </el-main> 
  </el-container> 
  
	<div class="footer_box  hidden-xs-only">
		   	<div class="footer_copyright">
		    	<span>广东天软农联信息科技有限公司版权所有·粤ICP备16080075号-1</span>
		    	<span>友情链接: 中华贺氏湖南商会网 精品农联网</span>
		    </div>
  </div>
  
    	<el-collapse  class="collspse_box" v-model="activeName" accordion>
			  <el-collapse-item class="collspse_item" :xs="24" title="服务项目" name="1">
			    <router-link  :to="item.to" v-for="(item,index) of list1" :key="index" tag="li" class="li">
		        {{item.html}}
		    	</router-link>
			  </el-collapse-item>
			  <el-collapse-item class="collspse_item" :xs="24" title="关于我们" name="2">
			    <router-link  :to="item.to" v-for="(item,index) of list2" :key="index" tag="li" class="li">
	            {{item.html}}
	        </router-link>
			  </el-collapse-item>
			  <el-collapse-item class="collspse_item" :xs="24" title="开发实例" name="3">
			    <router-link  :to="item.to" v-for="(item,index) of list3" :key="index" tag="li" class="li">
	            {{item.html}}
	        </router-link>
			  </el-collapse-item>
			  <el-collapse-item class="collspse_item" :xs="24" title="联系我们" name="4">
			    <router-link  :to="item.to" v-for="(item,index) of list4" :key="index" tag="li" class="li">
	            {{item.html}}
	        </router-link>
	  		</el-collapse-item>
	    </el-collapse>
   		<el-row class="footer_copy">
   			<el-col :xs="24">
   				tel:18022208988
   			</el-col>
   		</el-row>
  </div>
</template>

<script>
export default {
  name: 'FooterNav',
  data(){
  	return{
      list1:[{
        name: 'Website',
        to: '/server',
        html: '网站系统开发',
        detailShow: false
      },
      {
        name: 'Customization',
        to: '/server/customization',
        html: '软件定制服务',
        detailShow: false
      },
      {
        name: 'Platform',
        to: '/server/platform',
        html: '电商平台开发',
        detailShow: false
      },
      {
        name: 'Wechat',
        to: '/server/wechat',
        html: '微信公众号深度开发',
        detailShow: false
      },
      {
        name: 'Mobile',
        to: '/server/mobile',
        html: '移动APP开发',
        detailShow: false
      }],
       list2:[{
        name: 'Introduction',
        to: '/about',
        html: '公司介绍',
        detailShow: false
      },
      {
        name: 'Cultural',
        to: '/about/cultural',
        html: '文化理念',
        detailShow: false
      },
      {
        name: 'News',
        to: '/about/news',
        html: '新闻动态',
        detailShow: false
      },
      {
        name: 'Partner',
        to: '/about/partner',
        html: '合作伙伴',
        detailShow: false
      }],
      list3:[{
        name: 'Food',
        to: '/case',
        html: '美食APP',
        detailShow: false
      },
      {
        name: 'Vegetarian',
        to: '/case/vegetarian',
        html: '素食APP',
        detailShow: false
      },
      {
        name: 'Pineapple',
        to: '/case/pineapple',
        html: '菠萝油',
        detailShow: false
      },
      {
        name: 'Flow',
        to: '/case/flow',
        html: '流量无忧',
        detailShow: false
      }],
      list4:[{
        name: 'Company',
        to: '/connection',
        html: '广州总公司',
        detailShow: false
      },
      {
        name: 'Branch',
        to: '/connection/branch',
        html: '顺德办事处',
        detailShow: false
      }],
      activeName: '0'
    }
  },
  methods:{
    mouseenter:function(item) {
      item.detailShow = true;
    },
    mouseleave:function(item) {
      item.detailShow = false;
    }
	}
}
</script>

<style lang="less" scoped>
	div.footer{
		width: 100%;
		background: #3D444F;
    .footer{
        margin: 0 auto;
        padding: 30px 0;
        text-align: center;
        .showborder{
        	border-bottom: 1px solid #FFFFFF;
        	color: #FFFFFF;
        }
        h2{
            color: #FFFFFF;
            text-align: left;
            font-size: 0.18rem;
            padding-bottom: 0.2rem;
        }
        li{
            cursor: pointer;
            text-align: left;
            color: #999;
            font-size: 0.14rem;
            padding: 0.05rem 0;
        }
        img.code{
            width: 85px;
        }
    }
	}
	.footer_box{
		width: 100%;
		padding:20px 0;
		background-color: #373D47;
        .footer_copyright{
            margin: 0 auto;
            display: flex;
            justify-content: space-around;
            span{
                font-size: 0.14rem;
                color: #FFFFFF;
            }
        }
	}
	.collspse_box{
		display: none;
	}
	.footer_copy{
		display: none;
		background-color: #373D47;
		text-align: center;
		div{
			height: 48px;
    	line-height: 48px;
			font-size: 0.16rem;
			color: #FFFFFF;
		}
	}
	@media only screen and (max-width: 767px){
		.collspse_box{
			display: block;
		}
		.footer_copy{
			display: block;
		}
	}
	.li{
    	font-size: 0.16rem;
	    color: #919399;
	    line-height: 48px;
	    height: 48px;
	    cursor: pointer;
    }
</style>
<style>
	.el-collapse-item__header {
    height: 48px;
    line-height: 48px;
    color: #FFFFFF!important;
    font-size: 0.16rem!important;
    text-align: left;
    padding-left: 20px;
    box-sizing: border-box!important;
	}
	.el-collapse-item__header{
		background: #3D444F!important;
	}
	.el-collapse-item__content {
		background: #3D444F!important;
    padding-bottom: 0;
    font-size: 0.16rem;
    color: #919399;
    padding-left: 20px;
    text-align: left;
    box-sizing: border-box!important;
	}
	.el-collapse, .el-collapse-item__header, .el-collapse-item__wrap {
    border-bottom: 1px solid transparent!important;
    overflow: hidden;
	}
</style>
