
 <!DOCTYPE html>
<!--STATUS OK-->
<html>
	<head>
		<meta http-equiv="X-UA-Compatible" content="IE=Edge" />
		<meta http-equiv="content-type" content="text/html;charset=gbk" />
		<meta property="wb:webmaster" content="3aababe5ed22e23c" />
		<meta name="referrer" content="always" />
		<title>怎么把本地工程上传到到github？_百度知道</title>
		<link rel="shortcut icon" href="/favicon.ico" type="image/x-icon" />
		<link rel="icon" sizes="any" mask href="//www.baidu.com/img/baidu.svg" />
      			
<script>
    window.alogObjectConfig = {
        product: '102',
        page: '102_3', 
        monkey_page: 'zhidao-ques',
        speed_page: '3',
        speed: {
            sample: '0.02'
        },
        monkey: {
            sample: '0.01'
        },
        exception: { 
            sample: '0.01'
        },
        feature: {
            sample: '0.01'
        },
        cus: {
            sample: '0.01',
            custom_metrics: ['c_sbox', 'c_menu', 'c_ask', 'c_best']
        },
        csp: {
            sample: '0.02',
            'default-src': [
                {match: '*bae.baidu.com', target: 'Accept,Warn'},
                {match: '*.baidu.com,*.bdstatic.com,*.bdimg.com,localhost,*.hao123.com,*.hao123img.com', target: 'Accept'},
                {match: /^(127|172|192|10)(\.\d+){3}$/, target: 'Accept'},
                {match: '*', target: 'Accept,Warn'}
            ]
        }
    };
 
    void function(a,b,c,d,e,f,g){a.alogObjectName=e,a[e]=a[e]||function(){(a[e].q=a[e].q||[]).push(arguments)},a[e].l=a[e].l||+new Date,d="https:"===a.location.protocol?"https://fex.bdstatic.com"+d:"http://fex.bdstatic.com"+d;var h=!0;if(a.alogObjectConfig&&a.alogObjectConfig.sample){var i=Math.random();a.alogObjectConfig.rand=i,i>a.alogObjectConfig.sample&&(h=!1)}h&&(f=b.createElement(c),f.async=!0,f.src=d+"?v="+~(new Date/864e5)+~(new Date/864e5),g=b.getElementsByTagName(c)[0],g.parentNode.insertBefore(f,g))}(window,document,"script","/hunter/alog/alog.min.js","alog"),void function(){function a(){}window.PDC={mark:function(a,b){alog("speed.set",a,b||+new Date),alog.fire&&alog.fire("mark")},init:function(a){alog("speed.set","options",a)},view_start:a,tti:a,page_ready:a}}();
    void function(n){var o=!1;n.onerror=function(n,e,t,c){var i=!0;return!e&&/^script error/i.test(n)&&(o?i=!1:o=!0),i&&alog("exception.send","exception",{msg:n,js:e,ln:t,col:c}),!1},alog("exception.on","catch",function(n){alog("exception.send","exception",{msg:n.msg,js:n.path,ln:n.ln,method:n.method,flag:"catch"})})}(window);
</script>

		
<script>
	!function(document, window){
		var log = {
			list: [],
			host: 'https://' + location.host + '/api/httpscheck',
			log: function(param) {
				var a = [];
		    	for(var k in param) {
		    		a.push(k + '=' + param[k]);
		    	}
		    	var msg = a.join('&');
		    	if(~this.list.indexOf(msg)){
		    		return;
		    	}
		    	this.list.push(msg);
		  		var img = new Image();
		    	var key = '_ik_log_' + (Math.random()*2147483648 ^ 0).toString(36);
		    	window[key] = img;
		    		img.onload = img.onerror = img.onabort = function() {
		        		img.onload = img.onerror = img.onabort = null;
		        		window[key] = null;
			    		img = null;
		    	};
		  		img.src = this.host + '?' + msg;
			}
		};

		function HTTPSWarningLog(){
			this.selector = [
				'link',
				'script',
				'img',
				'embed',
				'iframe'
			];
			this.warningCounter = 0;
			this.init();
		};

		HTTPSWarningLog.prototype = {
			init: function(){
				this.fetch();
			},

			fetch: function(){
				for(var tags = this.selector, i =0, len = tags.length; i < len;i++) {
					this.getTag(tags[i]);
				}
			},

			getTag: function(tag) {
				var domList = document.getElementsByTagName(tag);
				if(!domList.length) {
					return;
				}
				for(var i = 0,len = domList.length;i<len;i++) {
					var el = domList[i];
					var url = el.getAttribute(el.tagName==='LINK' ? 'href' : 'src');
                    if(el.getAttribute('rel') === 'canonical') {
                        continue;
                    }
					if(url && 'https:' === location.protocol && !url.indexOf('http:')){
						this.sendLog(el, el.tagName.toLowerCase(),url);
						this.warningCounter++;
					}
				}
			},
			
			sendLog: function(el, type, url){
				log.log({
					url: location.href,
					wtype: type,
					wurl: url
				});
			}
		};

		function domReady(fn){
		    if(document.addEventListener) {
		        document.addEventListener('DOMContentLoaded', function() {
		            document.removeEventListener('DOMContentLoaded',arguments.callee, false);
		            fn();
		        }, false);
		    }else if(document.attachEvent) {
		        document.attachEvent('onreadystatechange', function() {
		            if(document.readyState == 'complete') {
		                document.detachEvent('onreadystatechange', arguments.callee);
		                fn();
		            }
		        });
		    }
		};

		domReady(function(){
			new HTTPSWarningLog();
			for(var i=1; i<6; i++) {
				!function(i){
					setTimeout(function(){
						new HTTPSWarningLog();
					}, i*i*i*1000);
				}(i);
			}
		});
	}(document, window);
</script>
		        
<meta name="keywords" content="工程\github"/>
<meta name="description" content="怎么把本地工程上传到到github？"/>
<link rel="canonical" href="http://zhidao.baidu.com/question/1925885591182532307.html"/>
<script>
        if (location.hash && location.hash.indexOf('bdres2exe=') > -1) {
            document.write('<script src="//m.baidu.com/static/as/res2exe/js/res2exe_1.0.3.min.js?v=091818"></' + 'script>');
        }
    </script>

		<script type="text/javascript">
			!function(){var n={},t={};n.context=function(n,e){var i=arguments.length;if(i>1)t[n]=e;else if(1==i){if("object"!=typeof n)return t[n];for(var o in n)n.hasOwnProperty(o)&&(t[o]=n[o])}},"F"in window||(window.F=n)}();;
			
            
																																							
			F.context('user', {"isLogin":"0","stoken":"","name":"","imId":"","id":"","wealth":"","gradeIndex":"","isMavin":""});
			F.context('user')['internalAdmin'] = null;

							F.context('defaultQuery', '{"title":"","value":""}');
									
			            
                                                F.context('productsDomain', {
                'zuoye': 'http://zuoye.baidu.com',
                'baobao': 'http://baobao.baidu.com',
                'doctor': 'http://muzhi.baidu.com'
            });
            F.context('isQuality', false);
            F.context('now', 1490637368);
		</script>
        <script>F.context('sysTaskAutoInit', 1);</script>

		
<script type="text/javascript">
    	var dontTriggerPrompt = true;
    	
        F.context('page',{
        	isAdopted: '0'
            ,misAsk: '0'
            ,delAsk: '0'
            ,isLocked: '0'
            ,isReplyLocked: '0'
            ,isFromWap: "0"
            ,cid: '1246'
            ,cidTop: '74'
            ,cidMid: '1073'
            ,qid: '1925885591182532307'
            ,tags: '操作系统'
            ,title: '怎么把本地工程上传到到github？'
            ,giveScore: '0'
            ,encodeUid: '40c04069236f25705e790e14'
                        ,uid: '336511040'
            ,imId: '40c0f7d2f7d1b3acecbdecbb0e14'
            ,passPhoto: '0'
                                    ,qb_test_case: '19'
                        ,rpRecommand: 'false'                        ,rankFile: '0' 
                        ,userName: '饕餮超旖旎'
            ,user : {
                sex: '1'
                ,iconType: '6'
                ,gradeIndex: '5'
                ,gradeIndexC: '五'
                                ,grAnswerNum: '38'
                                                                                                                                                                ,goodRate: '48'
                            }
                                    ,con: '库已经创建好，已经把库用客户端下载带本地，然后把工程文件放在这个目录下，可是用客户端就是push不上去，为什么？我哪里弄错了吗？'
                                    ,answerNum: ''
            ,isView: '1'
            ,isGetWealth:'0'
                        ,pgcArr: [790,791,792,794,795]
            ,isCompanyIask: '0'
            ,bdplayer:'mozilla\/5.0 (windows nt 6.1; wow64) applewebkit\/537.36 (khtml, like gecko) chrome\/56.0.2924.87 safari\/537.36'
        });
        
        F.context('user')['internalAdmin'] = null;

                F.context('answers', {});
        F.context('relateWords', {});
                F.context('egg', {
            id: '8'
            ,flashUrl: 'http:\/\/img.iknow.bdimg.com\/gglft\/gglft_flash.swf'
            ,onlineTime: '2013-11-15'
            ,offlineTime: '2013-12-01'
            ,loginRate: '0.7'
            ,notLoginRate: '0.3'
            ,targetUrl: 'http:\/\/zhidao.baidu.com\/s\/gglft\/index.html?isegg=1'
            ,btnText: '确定'
            ,dialogText: '恭喜你捡到一张刮刮卡，立刻参与刮刮乐翻天活动，拍立得、iPad mini、iPhone 5手机等超多大奖等你刮出来~'
            ,dialogBackground: ''
            ,dialogTextMargin: '0'
            ,active: '0'
            ,activeUrl: ''
            ,activeStatus: ''
            ,guideLogin: '1'
            ,dialogTextLogin: ''
            ,btnTextLogin: ''
            ,dialogTextActive: ''
            ,btnTextActive: ''
            ,dialogBackground: ''
            ,limitGrade: '0'
            ,limitGoodRate: '0'
        });
                        F.context('cmsTopic', [
                                    {
                'url': 'http:\/\/zhidao.baidu.com\/s\/qinliugan.html',
                'title': 'H7N9禽流感病毒问题解答',
                'qid': '538944731,538944974,538945159,538945410,538945640,538945806,538946023,538947972,538948119,538948841,538948985,538949170,538949278,538949607,538951811,538952044,538952289,539260208,539271130,539272340,539272652,539272848,539273004,538758680,537145971,537481975,537482138,537491741,537496345,537145971,539271582,539310838,96016332,16608956,16608956,534580619',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen18.html',
                'title': '传统医学解读人体奥秘',
                'qid': '',
                'expert': '正安中医梁冬,薄化君大夫,罗炳翔大夫'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen17.html',
                'title': '我们有文化，遇见“流氓”也不怕！',
                'qid': '',
                'expert': '打假第一人王海'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/topic\/zhichangtiaocao\/index.html',
                'title': '跳槽前必读8大问题',
                'qid': '530550652,530550695,530550746,530550777,530550821,530550859,530550898,530550937',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/topic\/zhichangmianshi\/index.html',
                'title': 'HR不懂爱，他的提问你答不来！',
                'qid': '529252350,529252523,529252831,529253040,529253301,529253429,529256645,529256979,529257198,529257285',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen16.html',
                'title': '孙云晓解答青春叛逆期教育',
                'qid': '',
                'expert': '青研中心孙云晓'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen16.html',
                'title': '孙宏艳解答青春叛逆期教育',
                'qid': '',
                'expert': '青研中心孙宏艳'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen15.html?fr=qbzt',
                'title': '雷明解答职场中的跳槽疑惑',
                'qid': '',
                'expert': '心理咨询雷明'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen15.html?fr=qbzt',
                'title': '唐宁解答女性职场疑惑',
                'qid': '',
                'expert': '职场唐宁'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen14.html?fr=qbzt',
                'title': '北大售票帝裴济洋教你买票回家！',
                'qid': '',
                'expert': 'peijiyang_pku'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/jiaogui.html?fr=qbzt',
                'title': '权威解读2013驾考新规',
                'qid': '496005611,105728210',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/topic\/shi\/index.html?fr=qbzt',
                'title': '被误读最深的名言锦句',
                'qid': '510380393,510380025,510380524,510380639,510380685,510380918,510381072,510380301',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen13.html?fr=qbzt',
                'title': '交管局李晓东处长解答驾考新规',
                'qid': '',
                'expert': '交管局李晓东'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen13.html?fr=qbzt',
                'title': '交管局李勤处长解读新交规',
                'qid': '',
                'expert': '交管局李勤'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen12.html?fr=qbzt',
                'title': '胡柳解答保险理财',
                'qid': '',
                'expert': '保险理财胡柳'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen12.html?fr=qbzt',
                'title': '魏德善解答证券投资',
                'qid': '',
                'expert': '证券专家魏德善'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen06.html?fr=qbzt',
                'title': '金韵蓉老师教你精油护肤',
                'qid': '',
                'expert': 'lafasojyr'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/topic\/kuaidu\/suhuaji\/index.html?fr=qbzt',
                'title': '你的食物含塑化剂吗',
                'qid': '499771676,274675532,273938276,275181078,274282140,499772730,275226786,274536152,282757232,274210910,275395808,499772593,275355018,274093929',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/topic\/kuaidu\/youjia\/index.html?fr=qbzt',
                'title': '油价是升还是降',
                'qid': '7701062,7720360,23590745,239386624,302573038,218721231,337321559',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/topic\/kuaidu\/2012usa\/index.html?fr=qbzt',
                'title': '美国总统是如何选出来的',
                'qid': '494863184,494863014,494869926,494869853,494868987',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/topic\/Chicken\/index.html?fr=qbzt',
                'title': '45天鸡能不能吃',
                'qid': '503005578,503006139,503006460,503006854,503007374,503007374',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/topic\/1942\/index.html?fr=qbzt',
                'title': '你知道1942吗？',
                'qid': '502766042,502766042,502647814,502647814,502777253,502776800,502650170,502650170',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/topic\/jiehuo\/jiankangyaoyan\/index.html?fr=qbzt',
                'title': '健康流言知真假',
                'qid': '178807906,334055366,498402753,291937633,209426382,414548424,7540625,222613405,498406267,498408474,109760622,388525641',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/www.baidu.com\/search\/zhidao\/jingshenbing\/index.html?fr=qbzt',
                'title': '大家都有病',
                'qid': '492345830,491605430,492350128,492350240,492350299,281444990,492440880,489745109,492443590,492443722',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/www.baidu.com\/search\/zhidao\/gangnamstyle\/index.html?fr=qbzt',
                'title': '江南Style红的很科学',
                'qid': '478958350,487057430,483904315,485109741,487057528,485109517,487057485,487057395,487057395,487057363,480719567',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/www.baidu.com\/search\/zhidao\/bing\/index.html?fr=qbzt',
                'title': '其实这都不是病',
                'qid': '480816980,480792024,481137959,480812943,480813792',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/www.baidu.com\/search\/zhidao\/aizheng\/index.html?fr=qbzt',
                'title': '吃也会得癌症！',
                'qid': '328576004,480213867,480213973,480218158,480232828',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/www.baidu.com\/search\/zhidao\/2012gongfu\/index.html?fr=qbzt',
                'title': '江湖神功知多少',
                'qid': '475780308,473798866,475780429,473806239,475780510,473800706,475780712,475782468,475780619,473801366',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen11.html?fr=qbzt',
                'title': '姚海峰医生解答宠物健康',
                'qid': '',
                'expert': '姚海峰博士'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen11.html?fr=qbzt',
                'title': '王天明专业解答宠物营养',
                'qid': '',
                'expert': '宠物营养'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen10.html?fr=qbzt',
                'title': '苏芩谈远离爱留下的伤',
                'qid': '',
                'expert': '知名作家苏芩'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen08.html?fr=qbzt',
                'title': '张国庆分析中日关系',
                'qid': '',
                'expert': '社科院张国庆'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen06.html?fr=qbzt',
                'title': '小P老师教你彩妆造型',
                'qid': '',
                'expert': 'yoka小P老师'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen06.html?fr=qbzt',
                'title': '梅琳老师教你美肌护肤',
                'qid': '',
                'expert': 'lafasoml'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen06.html?fr=qbzt',
                'title': '美丽主持人李静的美容问答',
                'qid': '',
                'expert': 'lafasolj'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen05.html?fr=qbzt',
                'title': '伊能静解答如何演电影',
                'qid': '',
                'expert': 'yinengjing2013'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen05.html?fr=qbzt',
                'title': '导演赵林山揭秘电影',
                'qid': '',
                'expert': 'daoyanzls'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen05.html?fr=qbzt',
                'title': '五岳散人谈美食',
                'qid': '',
                'expert': 'wysr2012'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen04.html?fr=qbzt',
                'title': '早教专家李跃儿谈早教',
                'qid': '',
                'expert': 'lyer2013bd'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen04.html?fr=qbzt',
                'title': '产科主任余梅教孕产',
                'qid': '',
                'expert': 'ym2013bd'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/topic\/muru\/index.html?fr=qbzt',
                'title': '妈妈最关心的8个问题',
                'qid': '526309070,526865300,526865300,526308815,526865218,526865157,526865101,526865101,526309710,526865031',
                'expert': ''
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen03.html?fr=qbzt',
                'title': '健身专家王友松教健身',
                'qid': '',
                'expert': 'wangyousong7'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen03.html?fr=qbzt',
                'title': '顾中一教你健康营养',
                'qid': '',
                'expert': 'guzhongyi'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen03.html?fr=qbzt',
                'title': '李湘教你减肥秘诀',
                'qid': '',
                'expert': 'lixiangzslx'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/zhishilingxiu02.html?fr=qbzt',
                'title': '心血管病专家贾玉和谈病痛',
                'qid': '',
                'expert': 'jiayuhe7'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/zhishilingxiu02.html?fr=qbzt',
                'title': '糖尿病专家向红丁谈病痛',
                'qid': '',
                'expert': 'xianghongd3'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/zhishilingxiu01.html?fr=qbzt',
                'title': '金领小V谈职场生存学',
                'qid': '',
                'expert': '小V2013'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/zhishilingxiu01.html?fr=qbzt',
                'title': '杜子建说创业',
                'qid': '',
                'expert': '杜子建2012'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen08.html?fr=qbzt',
                'title': '张召忠谈钓鱼岛争端',
                'qid': '',
                'expert': 'zshaozhong2012'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen07.html?fr=qbgl',
                'title': '崔玉涛谈婴幼儿护理',
                'qid': '',
                'expert': '儿科医生崔玉涛'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/zhishilingxiu02.html?fr=qbzt',
                'title': '急诊女超人于莺谈病痛',
                'qid': '',
                'expert': 'yuyingjzk'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/zhishilingxiu01.html?fr=qbzt',
                'title': '薛蛮子谈天使投资',
                'qid': '',
                'expert': '薛蛮子2012'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/wowen09.html?fr=qbgl',
                'title': '郑渊洁让童年如童话',
                'qid': '',
                'expert': '作家郑渊洁'
            },
                                                {
                'url': 'http:\/\/zhidao.baidu.com\/s\/maya.html?fr=qbgl',
                'title': '2012世界末日真相',
                'qid': '384640140,193245477,62563072,306563588,158114723,409478947,12992979,129335529,84523086,13774477,161887534',
                'expert': ''
            }
                                ]);
                        
        
        F.context('isForAnswerHq', '0');
                F.context({
            'itopicSyncAdminStr': '["553869863","408584470","663150510","1601193224","1305370811","1253985996","240173754","2421480383","282555480","617337308","703281543","1824698773","2560348928","49725318","220659661","161331174","1372601133","1969665018","837552203","365536315","331452762"]'
        });

    </script>

        <!--[if lte IE 8]>
            <script>
                (function(){
                    var e="abbr,article,aside,audio,canvas,datalist,details,dialog,eventsource,figure,footer,header,hgroup,mark,menu,meter,nav,output,progress,section,time,video".split(","),
                    i=e.length;
                    while(i--){document.createElement(e[i])}
                 })();
            </script>
        <![endif]-->
	<link rel="stylesheet" type="text/css" href="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/common/pkg/common_ad30a18.css" /><link rel="stylesheet" type="text/css" href="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/pkg/aio_58302c6.css" /><link rel="stylesheet" type="text/css" href="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/common/widget/userbar-renew/userbar-renew_55ab471.css" /><link rel="stylesheet" type="text/css" href="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/common/widget/search-box-new/search-box-new_4de721e.css" /><link rel="stylesheet" type="text/css" href="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/widget/top-nav-bar/top-nav-bar_21267b2.css" /><link rel="stylesheet" type="text/css" href="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/widget/read-opt/img-preview/preview_c4405d5.css" /><link rel="stylesheet" type="text/css" href="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/widget/bottom-union/bottom-union_d935508.css" /></head>
    
    
    <script> alog('speed.set', 'ht', +new Date); </script>


	<body class="layout-center has-menu">
		

<div id="userbar" class="userbar userbar-renew" data="">
            <ul class="aside-list">
            <li>
                <a href="http://www.baidu.com/" class="toindex">百度首页</a>
            </li>
            <li><a rel="nofollow" alog-alias="usrbar-login" href="javascript:;" id="userbar-login" log="type:2026,pname:account,mod:login,action:show,pos:pop">登录</a></li>
            <li><a rel="nofollow" alog-alias="usrbar-reg" id="userbar-reg" href="https://passport.baidu.com/v2/?reg&tpl=ik&color=green&u=" target="_blank">注册</a></li>
            <li class="shop-entrance">
                <a href="/shop" title="知道商城" log="type:2026,pos:top-right,target:shop-entrance">商城<i class="i-house" style="display: none;"></i></a>
                <span class="lucky-try"></span>
            </li>
        </ul>
    </div>



        
		
<div class="head-wrap">
<hr class="divider">
<header id="header" class="container">
<a href="http://zhidao.baidu.com/culture/topic?name=CICHChinesecalligraphy&amp;fr=Qbhead" title="" target="_blank" class="adTopImg" style="background-image:url(https://gss0.bdstatic.com/7051cy89QMgCncy6lo7D0j9wexYrbOWh7c50/CICH/Chinese_calligraphy/QB%E9%A1%B5-qb%E5%A4%B4%E5%9B%BE%26%E6%8F%90%E9%97%AE%E6%8E%A8%E5%B9%BF%E5%9B%BE130X36.jpg);"></a>

<div id="search-box" class="search-box-new line">
    <ul class="channel grid">
        <li><a log="sc_pos:c_baidu" rel="nofollow" href="http://www.baidu.com/">网页</a></li>
        <li><a log="sc_pos:c_news" rel="nofollow" href="http://news.baidu.com/">新闻</a></li>
        <li><a log="sc_pos:c_tieba" rel="nofollow" href="http://tieba.baidu.com/">贴吧</a></li> 
        <li><strong>知道</strong></li> 
        <li><a log="sc_pos:c_mp3" rel="nofollow" href="http://music.baidu.com/">音乐</a></li> 
        <li><a log="sc_pos:c_pic" rel="nofollow" href="http://image.baidu.com/">图片</a></li>
        <li><a log="sc_pos:c_video" rel="nofollow" href="http://v.baidu.com/">视频</a></li> 
        <li><a log="sc_pos:c_map" rel="nofollow" href="http://map.baidu.com/">地图</a></li> 
                <li><a log="sc_pos:c_doc" rel="nofollow" href="http://wenku.baidu.com/">文库</a></li>
        <li><a log="sc_pos:c_more" href="http://www.baidu.com/more/">更多&raquo;</a></li>
            </ul>
    <div class="search-block clearfix">
      <div class="search-cont clearfix">
        <a class="logo" href="/" title="百度知道"></a>
        <form action="/search" name="search-form" method="get" id="search-form-new" class="search-form">
            <input class="hdi" id="kw" maxlength="256" tabindex="1" size="46" name="word" value="" autocomplete="off" />
            <button alog-action="g-search-anwser" type="submit" id="search-btn" hidefocus="true"  tabindex="2" class="btn-global">搜索答案</button>
            <a href="#" alog-action="g-i-ask" class="i-ask-link" id="ask-btn-new">我要提问</a>
        </form>
      </div>
    </div>
</div>
<script>
                    // 搜索框可用时间打点
                    alog && alog('speed.set', 'c_sbox', +new Date); alog.fire && alog.fire("mark");
                </script>

</header>
</div>

<div class="nav-menu-container" id="j-nav-menu-container">
    <div class="nav-show-control">
        <div class="nav-menu-layout">
            <div class="nav-menu line">
                <div class="nav-menu-content container">
                    <div class="content-box">
                        <div class="menu-item menu-item-index">
                            <a class="menu-title " href="/">
                                首页
                            </a>
                        </div>
                        <div class="menu-item-box">
                            <div class="menu-item menu-item-cat">
                                <a class="menu-title " href="/list?fr=daohang" target="_blank">
                                    问题
                                </a>
                                <div class="menu-content">
                                    <ul class="menu-sub-list">
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?fr=daohang" target="_blank" target="_blank">
                                                全部问题
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=101?fr=daohang" target="_blank" target="_blank">
                                                经济金融
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=102?fr=daohang" target="_blank" target="_blank">
                                                企业管理
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=103?fr=daohang" target="_blank" target="_blank">
                                                法律法规
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=104?fr=daohang" target="_blank" target="_blank">
                                                社会民生
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=105?fr=daohang" target="_blank" target="_blank">
                                                科学教育
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=106?fr=daohang" target="_blank" target="_blank">
                                                健康生活
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=107?fr=daohang" target="_blank" target="_blank">
                                                体育运动
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=108?fr=daohang" target="_blank" target="_blank">
                                                文化艺术
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=109?fr=daohang" target="_blank" target="_blank">
                                                电子数码
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=110" target="_blank" target="_blank">
                                                电脑网络
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=111?fr=daohang" target="_blank" target="_blank">
                                                娱乐休闲
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=113?fr=daohang" target="_blank" target="_blank">
                                                行政地区
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=114?fr=daohang" target="_blank" target="_blank">
                                                心理分析
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=115?fr=daohang" target="_blank" target="_blank">
                                                医疗卫生
                                            </a>
                                        </li>
                                        <!-- <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/list?cid=116?fr=daohang" target="_blank" target="_blank">
                                                资源共享
                                            </a>
                                        </li> -->
                                    </ul>
                                </div>
                            </div>
                            <div class="menu-item menu-item-lanmu">
                                <a class="menu-title" href="javascript:;">
                                    专栏
                                </a>
                                <div class="menu-content">
                                    <ul class="menu-sub-list">
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/daily?fr=daohang" target="_blank">
                                                知道日报
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/liuyan?fr=daohang" target="_blank">
                                                真相问答机
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/bigdata/view" target="_blank">
                                                知道大数据
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/special/home?fr=daohang" target="_blank">
                                                知道多世界
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/culture/index?fr=daohang" target="_blank">
                                                知道非遗
                                            </a>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                            <div class="menu-item menu-item-user">
                                <a class="menu-title" href="javascript:;">
                                    用户
                                </a>
                                <div class="menu-content">
                                    <ul class="menu-sub-list">
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/zhima/" target="_blank">
                                                知道芝麻
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/misc/nowshowstar?fr=daohang" target="_blank">
                                                知道之星
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/user/admin?fr=daohang" target="_blank">
                                                芝麻将
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/uteam?fr=daohang" target="_blank">
                                                芝麻团
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/hangjia?fr=daohang" target="_blank">
                                                知道行家
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/daily/authorcenter?fr=daohang" target="_blank">
                                                日报作者
                                            </a>
                                        </li>
                                        <div class="menu-item-user-list">机构合作<div class="line-bar"></div></div>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/hangjia?fr=daohang" target="_blank">
                                                机构行家
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/opendev?fr=daohang" target="_blank">
                                                开放平台
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/special/view/cooperation?fr=daohang" target="_blank">
                                                品牌合作
                                            </a>
                                        </li>
                                        <div class="menu-item-user-list">知道福利<div class="line-bar"></div></div>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/shop?fr=daohang" target="_blank">
                                                财富商城
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item" href="/s/activity/index.html?fr=daohang" target="_blank">
                                                知道活动
                                            </a>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                            <div class="menu-item menu-item-expert">
                                <a class="menu-title" href="javascript:;">
                                    特色
                                </a>
                                <div class="menu-content">
                                    <ul class="menu-sub-list">
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item menu-sub-item-expert" href="http://jingyan.baidu.com/" target="_blank">
                                                <span class="expert-icon expert-icon-jy"></span>
                                                <span>经验</span>
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item menu-sub-item-expert" href="https://p.baidu.com" target="_blank">
                                                <span class="expert-icon expert-icon-pi"></span>
                                                <span>百度派</span>
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item menu-sub-item-expert" href="http://wenka.baidu.com" target="_blank">
                                                <span class="expert-icon expert-icon-ka"></span>
                                                <span>问咖</span><i class="i-new ml-5"></i>
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item menu-sub-item-expert" href="http://baobao.baidu.com" target="_blank">
                                                <span class="expert-icon expert-icon-baby"></span>
                                                <span>宝宝知道</span>
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item menu-sub-item-expert" href="http://muzhi.baidu.com?from=submenu" target="_blank">
                                                <span class="expert-icon expert-icon-doctor"></span>
                                                <span>拇指医生</span>
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item menu-sub-item-expert" href="http://zuoye.baidu.com" target="_blank">
                                                <span class="expert-icon expert-icon-zuoye"></span>
                                                <span>作业帮</span>
                                            </a>
                                        </li>
                                        <li class="menu-sub-item-wp">
                                            <a class="menu-sub-item menu-sub-item-expert" href="http://ciyuanfan.baidu.com/?ref=pcsyts" target="_blank">
                                                <span class="expert-icon expert-icon-ciyuanfan"></span>
                                                <span>次元饭</span>
                                            </a>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                        <div class="menu-right-section">
                            <ul class="menu-right-list">
                                <li class="menu-right-list-item zhidao-app">
                                    <a href="/zt/ikapp/index.html?fr=home" class="menu-right-list-link" target="_blank">
                                        <span class="item-icon">
                                            
                                        </span>
                                        <span class="item-name">
                                            手机版
                                        </span>
                                    </a>
                                    <span class="right-list-item-devide">
                                        
                                    </span>
                                </li>
                                <li class="menu-right-list-item user-center">
                                    <a href="/ihome" class="menu-right-list-link" target="_blank">
                                        <span class="item-icon">
                                            
                                        </span>
                                        <span class="item-name">
                                            我的知道
                                        </span>
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
<script>
        // 导航可用时间
        alog && alog('speed.set', 'c_menu', +new Date); alog.fire && alog.fire("mark");
    </script>

<div id="body" class="container">

<div class="layout-wrap">
<div id="top-nav-bar" class="top-nav-bar">
<div class="container2">
<a class="toplogo" href="http://zhidao.baidu.com" title="百度知道"></a>
<div class="topsearch">
<form action="/search" name="search-nav-form" id="search-nav-form" method="get">
<input class="hdi" id="nav-kw" maxlength="256" tabindex="1" size="46" name="word" value="" autocomplete="off" />
<button alog-action="g-search-anwser" type="submit" id="search-btn-nav" hidefocus="true"  tabindex="2" class="i-search-link">搜索答案</button>
</form>
</div>
</div>
</div>
<div style="display:none">
<nav class="wgt-nav f-12" alog-group="qb-cate-nav">
<a href="/">百度知道</a>
&gt;<a href="/browse/74">电脑/网络</a>
&gt;<a href="/browse/1073">编程语言</a>
&gt;<a href="/browse/1246">PHP</a>
</nav>
</div>
<section class="line qb-section">
<article class="grid qb-content" id="qb-content">
<div class="wgt-ask accuse-response line mod-shadow " id="wgt-ask">
<h1 accuse="qTitle">
<i class="iknow-qb_home_icons i-status-being grid mr-10"></i>
<span class="ask-title ">怎么把本地工程上传到到github？</span>
</h1>
<div class="line mt-5 q-content" accuse="qContent">
<span class="con">库已经创建好，已经把库用客户端下载带本地，然后把工程文件放在这个目录下，可是用客户端就是push不上去，为什么？我哪里弄错了吗？</span>
</div>
<div class="line f-aid ask-info ff-arial" id="ask-info">
<span class="grid-r ask-time">
<ins class="share-area">
</ins>
</span>
<a class="" alog-action="qb-ask-uname" rel="nofollow" href="/usercenter?uid=40c04069236f25705e790e14" target="_blank">饕餮超旖旎</a>
<span id="v-times" class="f-pipe" style="display: none"></span>
<ins class="accuse-area"></ins>
</div>
</div>
<script>
    // 提问区域可用时间
    alog && alog('speed.set', 'c_ask', +new Date); alog.fire && alog.fire("mark");
</script>
<script type="text/javascript">
        F.context('answers')['2225589447'] = {uid:"1363803991",imId:"57ff646179e5bf98e4b88de68e89e79a84e7979b4951",isAnonymous:"1",isCurrentUser:"0",mapUrl:"",refer:"",replyAskNum:"1",threadId:"8902357789",hasComment:"0",qid:"1925885591182532307",raid:"478873459",recommendCanceled:"0"};
        F.context('answers')['2225589447'].encodeUid = '57ff4069236f25705e794951';
            </script>
<div class="wgt-best mod-shadow  " id="best-answer-2225589447">
<div class="hd line ">
<span class="grid-r f-aid pos-time answer-time f-pening">
推荐于2016-07-01 04:36:25
</span>
<div id="act-link-banner-wp" class="grid-r"></div>
<span class="iknow-qb_home_icons answer-type answer-best grid"></span>
<span class="answer-title h2 grid">
最佳答案</span>
</div>
<div class="bd answer" id="answer-2225589447">
<div class="line info f-aid">
</div>
<div class="line content">
<pre id="best-content-2225589447" accuse="aContent" class="best-text mb-10" style="">注册GitHub后你就会有0.3G的免费空间，不过只能创建公开项目，这也满足代码分享的目的，我最喜欢的倒是它的代码展示方式，可以直接浏览你的代码，代码是经过高亮、添加行号处理过的，十分漂亮，体验一流，比如这个Webpy托管的地方。而作为想要了解你代码的人，可以选择直接在线浏览自己感兴趣的，也可以直接下载压缩包，或者直接使用Git clone到本地。<br />因为GitHub是基于Git版本控制系统，所以你上传修改代码什么的，都需要使用Git工具。我这里主要是用来分享和展示代码，所以不想在版本控制方面做过多的阐述，下面就简单讲解一下怎么在GitHub上新建一个项目，还有把自己的代码传上去。下面的前提是你已经注册了GitHub和下载安装了Git——Git下载、Windows版本下载。<br />上传分享代码<br />1.在GitHub上建立项目<br />登录GitHub后，你可以在右边靠中那里找到一个按钮“New Repository”，点击过后，填入项目名称、说明和网址过后就可以创建了，然后会出现一个提示页面，记下类似git@github.com:XXX/XXX.git的地址，这个就是你这个项目的地址了。<br />2.配置Git以及上传代码<br />安装Git成功后，如果是Windows下，选择Git Bash，在命令行中完成一切，可能开始有点麻烦，不过就那几条命令行，用几次就记住啦。首先初始设置Git：<br />1 git config --global user.name &quot;Your Real Name&quot; 2 git config --global user.email you@email.address<br /><br />然后开始进行最麻烦的一步了，你需要上传文件到GitHub的Git系统上，得需要一个SSH密匙来认证，下面就开始生成密钥和提交密钥。打开Git Bash,创建SSH key:<br />1 ssh-keygen -C &#39;your@email.address&#39; -t rsa<br /><br />然后要你输入SSH密匙的存放位置，可以不管，直接回车使用默认路径。再输入你想要的密码，SSH key就生成了。现在你需要将这个Key提交到GitHub，首先打开Key保存的位置，里面会有三个文件，找到id_rsa.pub，用文本编辑器打开，复制里面的全部字符。到GitHub，在右上方工具栏里找到Account Settings。在这个页面上有一个SSH Public Keys标签，选择Add another public key。Title可以随便填一个，Key就粘贴刚才的字符，提交。<br />完成这些工作后，就可以上传自己的代码了。找到自己要分享上传的代码文件夹，右击选择Git Bash，或者在Git Bash中进入这个文件夹。建立一个仓库：<br />1 git init<br /><br />选择要添加进仓库的文件：<br />1 git add .<br /><br />一般如果你想分享这个文件夹里的所有代码，就在 add后面加“.”，上面的例子就是这样，如果传指定的，只需要把“.”改为文件名即可，现在只是选择了要加入仓库的文件，下面才是添加进入仓库：<br />1 git commit -m &#39;Test&#39;<br /><br />-m后面跟一个参数，表示说明，将代码提交到GitHub后，将会在代码文件信息上显示这个说明，如下图标记的地方。<br />搞了这么久，现在才开始把本地仓库上传到GitHub了，下面两行命令搞定问题：<br />1 2 git remote add origin git@github.com:XXX/XXX.git 3 git push -u origin master<br /><br />这个git@github.com:XXX/XXX.git就是上面创建项目是生成的地址。现在打开你的项目网址，你就可以发现你的代码已经展示出来了。如果你要更新代码的话，就重复上面的吧。<br />如果提交了敏感信息，比如代码中设置的自己的密码什么的忘删除就上传上去了怎么办？重新修改过后上传依然有历史记录，而使用Git删除历史记录貌似很麻烦，于是就采用删除项目吧，删除了再重新上传。删除项目需要在GitHub网站上右上方找到admin按钮，进去后右边最下面有个删除的按钮，这样就可以删除了。<br />一些可能遇到的问题解决：<br />如果输入$ git remote add origin git@github.com:djqiang（github帐号名）/gitdemo（项目名）.git<br />提示出错信息：fatal: remote origin already exists.<br />解决办法如下：<br />1、先输入$ git remote rm origin<br />2、再输入$ git remote add origin git@github.com:djqiang/gitdemo.git 就不会报错了！<br />3、如果输入$ git remote rm origin 还是报错的话，error: Could not remove config section ‘remote.origin’. 我们需要修改gitconfig文件的内容<br />4、找到你的github的安装路径，我的是C:&#92;Users&#92;ASUS&#92;AppData&#92;Local&#92;GitHub&#92;PortableGit_ca477551eeb4aea0e4ae9fcd3358bd96720bb5c8&#92;etc<br />5、找到一个名为gitconfig的文件，打开它把里面的[remote &quot;origin&quot;]那一行删掉就好了！<br />如果输入$ ssh -T git@github.com<br />出现错误提示：Permission denied (publickey).因为新生成的key不能加入ssh就会导致连接不上github。<br />解决办法如下：<br />1、先输入$ ssh-agent，再输入$ ssh-add ~/.ssh/id_key，这样就可以了。<br />2、如果还是不行的话，输入ssh-add ~/.ssh/id_key 命令后出现报错Could not open a connection to your authentication agent.解决方法是key用Git Gui的ssh工具生成，这样生成的时候key就直接保存在ssh中了，不需要再ssh-add命令加入了，其它的user，token等配置都用命令行来做。<br />3、最好检查一下在你复制id_rsa.pub文件的内容时有没有产生多余的空格或空行，有些编辑器会帮你添加这些的。<br />如果输入$ git push origin master<br />提示出错信息：error:failed to push som refs to …….<br />解决办法如下：<br />1、先输入$ git pull origin master //先把远程服务器github上面的文件拉下来<br />2、再输入$ git push origin master<br />3、如果出现报错 fatal: Couldn’t find remote ref master或者fatal: ‘origin’ does not appear to be a git repository以及fatal: Could not read from remote repository.<br />4、则需要重新输入$ git remote add origingit@github.com:djqiang/gitdemo.git<br />使用git在本地创建一个项目的过程<br />$ makdir ~/hello-world    //创建一个项目hello-world<br />$ cd ~/hello-world       //打开这个项目<br />$ git init             //初始化<br />$ touch README<br />$ git add README        //更新README文件<br />$ git commit -m ‘first commit’     //提交更新，并注释信息“first commit”<br />$ git remote add origin git@github.com:defnngj/hello-world.git     //连接远程github项目<br />$ git push -u origin master     //将本地项目更新到github项目上去</pre>
<div class="replyask-box mb-15">
<div class="replyask line replyask-ask" id="replyask-478873459">
<div class="ask-supply-line"></div>
<div class="ask ask-supply f-12 grid">追问</div>
<div class="replyask-content line ml-10" accuse="qRA" id="replyask-content-478873459">
<pre accuse="qRA">$ git init &#47;&#47;初始化<br />$ git add -all<br />$ git commit -m &#39;all&#39;<br />$ git remote add origin git@github.com:defnngj&#47;hello-world.git &#47;&#47;连接远程github项目<br />$ git push -u origin master &#47;&#47;将本地项目更新到github项目上去<br /><br />弄好了，来点简便的这样更好</pre>
</div></div>
</div>
<div class="quality-content-view-more mb-15">
</div><div class="newbest-content-meta line mt-15 ff-arial">
<div class="ft-info grid">
<i class="i-quality-icon"></i>
本回答由<span>电脑网络分类达人 郭强</span>推荐</div>
<div class="grid-r f-aid ">
<ins class="accuse-area" alog-alias="qb-accuse-link-best"></ins>
<span alog-action="qb-comment-btnbestbox" class="comment f-black cursor" id="comment-2225589447"><i class="iknow-qb_home_icons i-icon-comment mr-5"></i>评论</span>
<div class="qb-zan-eva">
<span 
		alog-action="qb-zan-btnbestbox" 
		class="iknow-qb_home_icons evaluate evaluate-32
						" 
		id="evaluate-2225589447" 
		data-evaluate="6" 
		>
</span>
<span 
		alog-action="qb-evaluate-outer" 
		class="iknow-qb_home_icons evaluate evaluate-bad evaluate-32 
						" 
		id="evaluate-bad-2225589447" 
		data-evaluate="2" 
		>
</span>
</div>
</div>
</div>
</div>
</div>
</div>
<script>
                    // 高质or满意or特型or推荐答案打点时间
                    alog && alog('speed.set', 'c_best', +new Date); alog.fire && alog.fire("mark");
                </script>
<script>
                    // 首屏时间打点
                    void function(e,t){for(var n=t.getElementsByTagName("img"),a=+new Date,i=[],o=function(){this.removeEventListener&&this.removeEventListener("load",o,!1),i.push({img:this,time:+new Date})},s=0;s< n.length;s++)!function(){var e=n[s];e.addEventListener?!e.complete&&e.addEventListener("load",o,!1):e.attachEvent&&e.attachEvent("onreadystatechange",function(){"complete"==e.readyState&&o.call(e,o)})}();alog("speed.set",{fsItems:i,fs:a})}(window,document);
                </script>
<div class="wgt-bottom-union mod-shadow line">
<h2><i class="iknow-qb_home_icons"></i>为您推荐：</h2>
<script>
        var cpro_psid = "u2115503";
    
    var cpro_pswidth = "450";
    var cpro_psheight = "25";
    var cpro_psdata = {
        titff:'微软雅黑',
        titfs: '14',
        rss2: "#333",
                rss3:'#34b458'
    }
    </script>
<script type="text/javascript">
        // 广告拦截打点
        F.context('ads_log_bottomrequest', 1);
        // 广告同步加载
        if (typeof BAIDU_SS_HHRUN!='function'){with(document)0[(getElementsByTagName('head')[0]||body).appendChild(createElement('script')).src='//su.bdimg.com/static/dspui/js/ue.js?v='+~(-new Date()/5600e5)]}else {BAIDU_SS_HHRUN()}
    </script>
</div>
<div class="wgt-related mt-5 mod-shadow" id="wgt-related">
<h2><i class="iknow-qb_home_icons"></i>其他类似问题</h2>
<div class="related-list line">
<ul class="list-34 related-ul" alog-group="qb-relative-que">
<li >
<span class="grid-r f-aid ff-arial">2015-12-07</span>
<a href="/question/1432820230183516659.html?qbl=relate_question_0" target="_blank" 
                    log="fr:qrl,pms:newqb,page:qb-new,pos:relative_title,index:1,cid:1246" class="related-link" data-qid="1432820230183516659">怎么将本地文件上传到github<em class="praise-num ml-5" title="所有回答获得1个赞同">
<i class="iknow-qb_home_icons i-evaluate"></i><span class="ml-5 ff-arial">1</span>
</em>
</a>
</li>
<li >
<span class="grid-r f-aid ff-arial">2016-07-12</span>
<a href="/question/755372107075242364.html?qbl=relate_question_1" target="_blank" 
                    log="fr:qrl,pms:newqb,page:qb-new,pos:relative_title,index:2,cid:1246" class="related-link" data-qid="755372107075242364">怎么将本地文件上传到github</a>
</li>
<li >
<span class="grid-r f-aid ff-arial">2015-09-20</span>
<a href="/question/370385277318375844.html?qbl=relate_question_2" target="_blank" 
                    log="fr:qrl,pms:newqb,page:qb-new,pos:relative_title,index:3,cid:1246" class="related-link" data-qid="370385277318375844">怎么将本地文件上传到github</a>
</li>
<li >
<span class="grid-r f-aid ff-arial">2016-01-12</span>
<a href="/question/585126306803616085.html?qbl=relate_question_3" target="_blank" 
                    log="fr:qrl,pms:newqb,page:qb-new,pos:relative_title,index:4,cid:1246" class="related-link" data-qid="585126306803616085">怎么将本地文件上传到github<em class="praise-num ml-5" title="所有回答获得1个赞同">
<i class="iknow-qb_home_icons i-evaluate"></i><span class="ml-5 ff-arial">1</span>
</em>
</a>
</li>
<li >
<span class="grid-r f-aid ff-arial">2016-08-18</span>
<a href="/question/1497790577263564619.html?qbl=relate_question_4" target="_blank" 
                    log="fr:qrl,pms:newqb,page:qb-new,pos:relative_title,index:5,cid:1246" class="related-link" data-qid="1497790577263564619">怎么将本地文件上传到github</a>
</li>
</ul>
</div>
<div class="related-more clearfix">
<a log="fr:qrl,pms:newqb,pos:relative_more" alog-action="qb-relative-more" target="_blank" rel="nofollow" href="/search?word=怎么把本地工程上传到到github？&ie=gbk&fr=qrl&cid=1246&qbl=relate_question_more" class="line f-14 mt-5">
更多类似问题<span class="ff-arial">&nbsp;&gt;</span>
</a>
</div>
</div>
<div class="wgt-topic mod-shadow" id="wgt-topic">
<h2><i class="iknow-qb_home_icons"></i><em>github</em>的相关知识</h2>
<ul class="topic-list list-34" alog-group="qb-relative-title">
<li>
<span class="grid-r f-aid ff-arial">2013-11-18</span>
<a href="/question/710906078687995485.html?fr=qrl&index=0&qbl=topic_question_0" log="pos:exttitle,topic:1,index:1" target="_blank" data-qid="710906078687995485">
我们是如何保持Github网站的高性能
<i class="iknow-qb_home_icons i-evaluate ml-5"></i><span class="ml-5 f-red f-12 ff-arial" title="回答获得1个赞同">1</span>
</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">2014-04-09</span>
<a href="/question/1732231753051148027.html?fr=qrl&index=1&qbl=topic_question_1" log="pos:exttitle,topic:1,index:2" target="_blank" data-qid="1732231753051148027">
github怎么用 ubuntu
<i class="iknow-qb_home_icons i-evaluate ml-5"></i><span class="ml-5 f-red f-12 ff-arial" title="回答获得5个赞同">5</span>
</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">2014-05-02</span>
<a href="/question/1574156218917530180.html?fr=qrl&index=2&qbl=topic_question_2" log="pos:exttitle,topic:1,index:3" target="_blank" data-qid="1574156218917530180">
在GitHub里创建的代码库默认的是在GitHub官网，怎么样才能让...
<i class="iknow-qb_home_icons i-evaluate ml-5"></i><span class="ml-5 f-red f-12 ff-arial" title="回答获得2个赞同">2</span>
</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">2013-09-26</span>
<a href="/question/623367919249905364.html?fr=qrl&index=3&qbl=topic_question_3" log="pos:exttitle,topic:1,index:4" target="_blank" data-qid="623367919249905364">
国内类似于Github的网站
<i class="iknow-qb_home_icons i-evaluate ml-5"></i><span class="ml-5 f-red f-12 ff-arial" title="回答获得1个赞同">1</span>
</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">2014-03-31</span>
<a href="/question/390808263682627325.html?fr=qrl&index=4&qbl=topic_question_4" log="pos:exttitle,topic:1,index:5" target="_blank" data-qid="390808263682627325">
github上的代码怎么在ubuntu环境下载到本地
<i class="iknow-qb_home_icons i-evaluate ml-5"></i><span class="ml-5 f-red f-12 ff-arial" title="回答获得16个赞同">16</span>
</a>
</li>
</ul>
<div class="topic-more clearfix">
<a log="pos:extmore,topic:1" class="mt-5" alog-alias="qb-relgrup-more" target="_blank" rel="nofollow" href="/search?word=github&ie=gbk&fr=qrl&cid=1246&qbl=topic_question_more">
更多关于<em>github</em>的知识<span class="ff-arial">&nbsp;&gt;</span>
</a>
</div>
</div>
<div class="wgt-push mod-shadow last ">
<h2 class="hd line"><i class="iknow-qb_home_icons"></i>等待您来回答</h2>
<ul alog-group="qb-push-que" class="bd list-34 line push-ul">
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/245125286127806164.html?push=cookie&group=0&qbl=push_question_0&rpRecommand=c&entry=qb_qb_view" target="_blank">mac版github客户端怎样删除上传重复的文件</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/1450766143074847460.html?push=cookie&group=0&qbl=push_question_1&rpRecommand=c&entry=qb_qb_view" target="_blank">hexo上传到github时出错，小白求助</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/2057044558848728627.html?push=cookie&group=0&qbl=push_question_2&rpRecommand=c&entry=qb_qb_view" target="_blank">为什么向github上传文件会出现something went really wrong，...</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/436868084008721164.html?push=cookie&group=0&qbl=push_question_3&rpRecommand=c&entry=qb_qb_view" target="_blank">如何通过github-deskotp上传代码</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/372675880226391724.html?push=cookie&group=0&qbl=push_question_4&rpRecommand=c&entry=qb_qb_view" target="_blank">如何把代码上传到github 并把链接发给别人</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/1514829057507379860.html?push=cookie&group=0&qbl=push_question_5&rpRecommand=c&entry=qb_qb_view" target="_blank">hexo上传到github时出错，小白求助</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/267623526942336845.html?push=cookie&group=0&qbl=push_question_6&rpRecommand=c&entry=qb_qb_view" target="_blank">如何利用git由本机向github上传文件</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/1545300124781928147.html?push=cookie&group=0&qbl=push_question_7&rpRecommand=c&entry=qb_qb_view" target="_blank">怎么将本地文件上传到github</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/460070587928848645.html?push=cookie&group=0&qbl=push_question_8&rpRecommand=c&entry=qb_qb_view" target="_blank">为什么上传到github上面的文件不见了</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/459942265581431205.html?push=cookie&group=0&qbl=push_question_9&rpRecommand=c&entry=qb_qb_view" target="_blank">每次上传文件到github 上面都需要初始化吗</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">1回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/1307068561152747659.html?push=cookie&group=0&qbl=push_question_10&rpRecommand=c&entry=qb_qb_view" target="_blank">git 文件上传到github以后没有</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/1963337048463533820.html?push=cookie&group=0&qbl=push_question_11&rpRecommand=c&entry=qb_qb_view" target="_blank">github 可以上传一个文件夹吗</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/756672047206508284.html?push=cookie&group=0&qbl=push_question_12&rpRecommand=c&entry=qb_qb_view" target="_blank">怎么将本地文件上传到github</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/308543681835833204.html?push=cookie&group=0&qbl=push_question_13&rpRecommand=c&entry=qb_qb_view" target="_blank">sourcetree怎么上传到github</a>
</li>
<li>
<span class="grid-r f-aid ff-arial">0回答</span>
<a class="media-980" log="pms:newqb,pos:pushlist,page:qb-new" href="/question/1642888368592271700.html?push=cookie&group=0&qbl=push_question_14&rpRecommand=c&entry=qb_qb_view" target="_blank">在github上传代码ssh方法和htttp方法上传有冲突吗</a>
</li>
</ul>
<div class="ft line more-push clearfix">
<a alog-action="qb-push-more" log="pms:newqb,pos:pushlist,page:question" target="_blank" rel="nofollow" href="/browse/?qbl=push_question_more">更多等待您来回答的问题<span class="ff-arial">&nbsp;&gt;</span></a>
</div>
</div>
</article>
<aside class="grid-r qb-side" id="qb-side">
<div></div>
<div class="wgt-nologin mod-shadow re-bt">
<a class="button" id="nologin-login">登录</a>
<p class="ml-10">还没有百度账号？<br><a href="https://passport.baidu.com/v2/?reg&tpl=ik&color=green&u=" target="_blank" id="nologin-reg">立即注册</a>
</div>
<div class="qbside-top-line"></div>
<div class="wgt-nologin-daily" id="wgt-nologin-daily">
<div class="wgt-daily mod-shadow">
<div class="daily-line mb-10 pt-10">
<h3 class="grid">知道日报</h3>
<span class="grid"></span>
<a href="http://zhidao.baidu.com/daily/square/" target="_blank" alog-action="qb-daily-review" class="grid-r f-aid f-yahei">全部文章</a>
</div>
<div id="daily-carousel"></div>
<div class="wgt-daily-wall"><em></em><s></s></div>
</div>
<div class="qbside-top-line"></div>
</div>
<div class="widget-new-graphic">
<style>.ec-ad {margin-left: -10px;padding-top: 5px;padding-bottom: 12px;}.ec-ad .ec-row-title .ec-title {font: normal 14px/34px 'Microsoft YaHei';padding-left: 10px;color: #666;}.ec-ad .ec-img-list {font-size: 0;}.ec-ad .ec-img-list .ec-img-item {width: 83px;display: inline-block;font-size: 12px;margin-left: 10px;vertical-align: top;}.ec-ad .ec-img {vertical-align: top;}.ec-ad .ec-img-desc {margin-top: 7px;text-align: center;color: #2d64b3;display: block;font-size: 12px;line-height: 18px;}</style><div class="ec-ad"><div class="ec-row-title"><h3 class="ec-title">相关搜索</h3></div><div class="ec-row-desc"><div class="ec-img-list"><a href="https://www.baidu.com/s?wd=%CE%A2%D0%C5%B9%AB%D6%DA%BA%C5%D4%F5%C3%B4%CD%C6%B9%E3&tn=SE_pczhidaotuwenqb_zdqb2016&lqsource=-1&dmaseid=dmaseid301&qid=f36654142bc5b7ed" class="ec-img-item" target="_blank"><img src="https://gss0.baidu.com/7LsWdDW5_xN3otqbppnN2DJv/dmas/pic/item/c3ec08fa513d2697ecdb2ecb5dfbb2fb4316d818.jpg" class="ec-img" width="83" height="83" alt=""><span class="ec-img-desc">微信公众号怎么推广</span></a><a href="https://www.baidu.com/s?wd=%B2%DF%BB%AE%C5%E0%D1%B5%B0%E0&tn=SE_pczhidaotuwenqb_zdqb2016&lqsource=-1&dmaseid=dmaseid301&qid=f36654142bc5b7ed" class="ec-img-item" target="_blank"><img src="https://gss0.baidu.com/7LsWdDW5_xN3otqbppnN2DJv/dmas/pic/item/78d5ad6eddc451da52bfa27ebefd5266d11632de.jpg" class="ec-img" width="83" height="83" alt=""><span class="ec-img-desc">策划培训班</span></a><a href="https://www.baidu.com/s?wd=2015%BB%D8%BA%CF%D6%C6%CD%F8%D3%CE%C5%C5%D0%D0&tn=SE_pczhidaotuwenqb_zdqb2016&lqsource=-1&dmaseid=dmaseid301&qid=f36654142bc5b7ed" class="ec-img-item" target="_blank"><img src="https://gss0.baidu.com/7LsWdDW5_xN3otqbppnN2DJv/dmas/pic/item/58c79f3df8dcd10035f007b47a8b4710b9122f33.jpg" class="ec-img" width="83" height="83" alt=""><span class="ec-img-desc">2015回合制网游排行</span></a></div></div></div>
</div>
<style type="text/css">
    .ec-ad .ec-row-title .ec-title {
    	padding-left: 0;
    }
    .ec-ad .ec-img-list {
    	width: 290px;
    }
    .ec-ad .ec-img-list .ec-img-item {
    	margin-left: 0;
    	margin-right: 10px;
    }
    </style>
<div style="display:none">
1
2
3
</div>
<div id="union-asplu" class="union-asplu line mod-noshadow wgt-ads"></div>
<div style="padding: 20px 9px 20px 10px;widget:250px;height:250px;">
    <script src="//dup.baidustatic.com/js/ds.js"></script>
    
<script>
    (function() {
        var s = "_" + Math.random().toString(36).slice(2);
        document.write('<div id="' + s + '"></div>');
        (window.slotbydup=window.slotbydup || []).push({
            id: '2598853',
            container: s,
            size: '250,250',
            display: 'inlay-fix'
        });
    })();
</script>
</div>
<div class="cms-slide cms-slide-lazy mod-noshadow">
<script type="text/javascript">
		F.context('cmsRight', [
															
							{
					'url':'http://ciyuanfan.baidu.com/?ref=pcqbyc',
					'src':'https://gss0.bdstatic.com/7051cy89RsgCncy6lo7D0j9wexYrbOWh7c50/zhidaoziyuanwei/ciyuanfan270.jpeg?t=1490024787'
				},																		
							{
					'url':'http://zhidao.baidu.com/culture/topic?name=CICHChinesecalligraphy&fr=rcircular',
					'src':'https://gss0.bdstatic.com/7051cy89RsgCncy6lo7D0j9wexYrbOWh7c50/CICH/Chinese_calligraphy/QB%E9%A1%B5-%E5%8F%B3%E4%BE%A7%E6%8E%A8%E5%B9%BF%E4%BD%8D-270X170.jpg?t=1490024787'
				},																		
							{
					'url':'https://zhidao.baidu.com/pcs/lianghui/index.html',
					'src':'https://gss0.bdstatic.com/7051cy89RcgCncy6lo7D0j9wexYrbOWh7c50/NJP/TwoSessions270X170.jpg?t=1490024787'
				}							]);
	</script>
<div class="cms-scroll" id="cms-scroll">
<div class="cms-mask" id="cms-mask"></div>
</div>
<p class="mt-15" id="cms-company">
<a rel="nofollow" href="http://zhidao.baidu.com/liuyan" target="_blank" data-img="https://gss0.bdstatic.com/70cFsjip0QIZ8tyhnq/img/iknow/sula2015chunjie/zhenxiangwendaji116.jpg?t=1490024787">
</a>
</p>
</div>
<div class="cms-slide mod-noshadow">
<div class="cms-inner">
<p class="cms-link-title">精彩知识在知道</p>
<ul class="pb-5 mt-5" id="cms-link">
<li><a alog-action="qb-inner-link" href="http://zhidao.baidu.com/special/view/cooperation" target="_blank">百度知道品牌合作指南</a></li>
<li><a alog-action="qb-inner-link" href="https://zhidao.baidu.com/liuyan" target="_blank">【真相问答机】，揭穿流言！</a></li>
<li><a alog-action="qb-inner-link" href="http://yuedu.baidu.com/partner/browse/profile?id=0b0a8f77168884868762d627" target="_blank">免费领取《知道日报》主题专刊</a></li>
<li><a alog-action="qb-inner-link" href="http://zhidao.baidu.com/bigdata/list" target="_blank">知道大数据，用数据解读生活点滴</a></li>
</ul>
</div>
</div>
</aside>
</section>
<div style="margin: 30px 0;width: 960px;height:90px;">

<script>
    (function() {
        var s = "_" + Math.random().toString(36).slice(2);
        document.write('<div id="' + s + '"></div>');
        (window.slotbydup=window.slotbydup || []).push({
            id: '2598845',
            container: s,
            size: '960,90',
            display: 'inlay-fix'
        });
    })();
</script>
</div>
</div>
<script type="text/javascript">
window.baidu_hh_hotword={
    id: [],
    page_url: 'http://zhidao.' + 'baidu.com/question/1925885591182532307',
    di: "u2146910",
    maxword: 10,
    frequency: 3
}
window.baidu_hh_hotword.id.push("best-content-2225589447");
</script>
<script src="//su.bdimg.com/static/dspui/js/w.js?v=1"></script></div>


		
<div class="wgt-footer-new">
    <div class="footer-wp">
        <ul class="footer-list clearfix">
            <li class="footer-list-item footer-list-guide">
                <div class="footer-title"><span class="icon-guide"></span>新手帮助</div>
                <ul class="footer-link clearfix">
                    <li><a href="http://tieba.baidu.com/p/3615879106" target="_blank">如何答题</a></li>
                    <li><a href="http://tieba.baidu.com/p/3615829242" target="_blank">获取采纳</a></li>
                    <li><a href="http://tieba.baidu.com/p/3615827221" target="_blank">使用财富值</a></li>
                </ul>
            </li>  
            <li class="footer-list-item footer-list-intro">
                <div class="footer-title"><span class="icon-intro"></span>玩法介绍</div>
                <ul class="footer-link clearfix">
                    <li><a href="/shop" target="_blank">知道商城</a></li>
                    <li><a href="/uteam" target="_blank">知道团队</a></li>
                    <li><a href="/hangjia" target="_blank">行家认证</a></li>
                    <li><a href="http://zhidao.baidu.com/s/hi-quality/index.html" target="_blank">高质量问答</a></li>
                </ul>
            </li>  
            <li class="footer-list-item footer-list-sug">
                <div class="footer-title"><span class="icon-sug"></span>投诉建议</div>
                <ul class="footer-link clearfix">
                    <li><a href="http://tousu.baidu.com/zhidao" target="_blank">举报不良信息</a></li>
                    <li><a href="http://ikefu.baidu.com/web/zhishisousuo#" target="_blank">意见反馈</a></li>
                    <li><a href="http://tousu.baidu.com/zhidao#3" target="_blank">投诉侵权信息</a></li>
                    <!-- <li><a href="http://ikefu.baidu.com/web/zhishisousuo#" target="_blank">机器人道道</a></li>-->
                </ul>
            </li> 
        </ul>
    </div>
    <div class="footer-new">
        <p class="jt1128">
         &copy;2017 Baidu&nbsp;&nbsp; <a rel="nofollow" href="http://www.baidu.com/duty/" target="_blank">使用百度前必读</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a rel="nofollow" href="http://help.baidu.com/question?prod_en=zhidao&class=597&id=1001104" target="_blank">知道协议</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a rel="nofollow" href="/special/view/cooperation" target="_blank">百度知道品牌合作</a>
        </p>
    </div>
</div>


	    
<div id="anttongji"></div>

        
        
<script type="text/javascript">
            try {
                (function() {var param_a = 1;var param_b = 111;var param_c = 115;var param_d = 257;var string_a = param_a.toString();var string_b = param_b.toString();var string_c = param_c.toString();var string_d = param_d.toString();var int_A = string_a.length + string_b.length;var int_B = string_c.length + string_d.length;result = int_A.toString()+int_B.toString();var xhr = null;if (window.XMLHttpRequest) {xhr = new XMLHttpRequest(); } else if (window.ActiveXObject) {xhr = new ActiveXObject("Microsoft.XMLHTTP");}if(xhr) {xhr.open("POST", "/question/api/replynum?t=" + new Date().getTime(), true);xhr.setRequestHeader("Content-Type", "application/x-www-form-urlencoded");xhr.onload = function(){};var qid = "1925885591182532307";var logid = 3367764274;xhr.send("qid=" + qid + "&replyT=" + result + "&logid=" + logid);}})();
            } catch (e) {
                //...
            }
        </script>

        
                    

        
    <script>
    void function(a,b,c,d,e,f){function g(b){a.attachEvent?a.attachEvent("onload",b,!1):a.addEventListener&&a.addEventListener("load",b)}function h(a,c,d){d=d||15;var e=new Date;e.setTime((new Date).getTime()+1e3*d),b.cookie=a+"="+escape(c)+";path=/;expires="+e.toGMTString()}function i(a){var c=b.cookie.match(new RegExp("(^| )"+a+"=([^;]*)(;|$)"));return null!=c?unescape(c[2]):null}function j(){var a=i("PMS_JT");if(a){h("PMS_JT","",-1);try{a=a.match(/{["']s["']:(\d+),["']r["']:["']([\s\S]+)["']}/),a=a&&a[1]&&a[2]?{s:parseInt(a[1]),r:a[2]}:{}}catch(c){a={}}a.r&&b.referrer.replace(/#.*/,"")!=a.r||alog("speed.set","wt",a.s)}}if(a.alogObjectConfig){var k=a.alogObjectConfig.sample,l=a.alogObjectConfig.rand;d="https:"===a.location.protocol?"https://fex.bdstatic.com"+d:"http://fex.bdstatic.com"+d,k&&l&&l>k||(g(function(){alog("speed.set","lt",+new Date),e=b.createElement(c),e.async=!0,e.src=d+"?v="+~(new Date/864e5)+~(new Date/864e5),f=b.getElementsByTagName(c)[0],f.parentNode.insertBefore(e,f)}),j())}}(window,document,"script","/hunter/alog/dp.min.js");
    </script>
		
			<script>
				var _hmt = _hmt || [];
				(function() {
					var hm = document.createElement("script");
					hm.src = "https://hm.baidu.com/hm.js?6859ce5aaf00fb00387e6434e4fcc925";
					var s = document.getElementsByTagName("script")[0];
					s.parentNode.insertBefore(hm, s);
				})();
			</script>
		

	</body><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/common/lib/mod_96dd55b.js"></script><script type="text/javascript">require.resourceMap({"res":{"common:widget\/lib\/swfupload\/swfupload.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/common\/widget\/lib\/swfupload\/swfupload_b24a26d.js"},"common:widget\/js\/ui\/suggestion-new\/suggestion-new.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/common\/widget\/js\/ui\/suggestion-new\/suggestion-new_0d26480.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/lib\/jquery.ui\/jquery.ui.autocomplete.js","common:widget\/js\/ui\/base\/base.js"]},"common:widget\/js\/logic\/search-box-new\/search-box-new.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/common\/widget\/js\/logic\/search-box-new\/search-box-new_c6b0786.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/ui\/suggestion-new\/suggestion-new.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/util\/form\/form.js","common:widget\/js\/util\/log\/log.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/lib\/jquery.placeholder\/jquery.placeholder.js"]},"common:widget\/js\/ui\/clipboard\/clipboard.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/common\/widget\/js\/ui\/clipboard\/clipboard_581e531.js"},"question:widget\/read-opt\/img-preview\/preview.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/read-opt\/img-preview\/preview_22279e0.js","deps":["common:widget\/lib\/jquery\/jquery.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/js\/logic\/category\/category.js","common:widget\/js\/util\/log\/log.js"]},"question:widget\/ask\/pc-exp\/ask-img.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/ask\/pc-exp\/ask-img_2de3204.js","deps":["common:widget\/lib\/jquery\/jquery.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/js\/logic\/category\/category.js","common:widget\/js\/util\/log\/log.js","question:widget\/read-opt\/img-preview\/preview.js"]},"common:widget\/js\/logic\/editor\/editor.js":{"pkg":"common:p3","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/store\/store.js","common:widget\/js\/logic\/editor\/config\/config.js","common:widget\/js\/logic\/editor\/lang\/lang.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/ui\/tip\/tip.js","common:widget\/js\/util\/https\/https.js","common:widget\/js\/util\/log\/log.js","common:widget\/js\/util\/webuploader\/webuploader.js","common:widget\/js\/logic\/editor\/fileUploader\/fileUploader.js"]},"common:widget\/js\/logic\/editor\/addon\/addon.js":{"pkg":"common:p3","deps":["common:widget\/lib\/jquery\/jquery.js","common:widget\/js\/logic\/authcode\/authcode.js"]},"common:widget\/js\/logic\/editor\/config\/config.js":{"pkg":"common:p3","deps":["common:widget\/lib\/jquery\/jquery.js","common:widget\/js\/util\/uri\/uri.js"]},"common:widget\/js\/logic\/editor\/fileUploader\/fileUploader.js":{"pkg":"common:p3","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/lib\/swfupload\/swfupload.js"]},"common:widget\/js\/logic\/editor\/lang\/lang.js":{"pkg":"common:p3"},"common:widget\/js\/logic\/editor\/prototype\/prototype.js":{"pkg":"common:p3","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/util\/log\/log.js"]},"question:widget\/js\/app-guide\/app-guide.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/js\/app-guide\/app-guide_e973e23.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/util\/log\/log.js"]},"question:widget\/js\/editor\/config\/config.js":{"pkg":"question:p2","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/uri\/uri.js"]},"question:widget\/js\/editor\/editor.js":{"pkg":"question:p2","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/logic\/editor\/editor.js","common:widget\/js\/logic\/editor\/prototype\/prototype.js","common:widget\/js\/logic\/editor\/addon\/addon.js","question:widget\/js\/editor\/config\/config.js","common:widget\/js\/ui\/tip\/tip.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/ui\/base\/base.js","common:widget\/lib\/jquery.placeholder\/jquery.placeholder.js"]},"question:widget\/ask\/replyer\/replyer.js":{"pkg":"question:p2","deps":["common:widget\/js\/util\/tangram\/tangram.js","question:widget\/js\/editor\/editor.js","common:widget\/js\/util\/log\/log.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/logic\/submit\/submit.js","question:widget\/js\/app-guide\/app-guide.js"]},"question:widget\/newbest\/asker.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/newbest\/asker_9672751.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","question:widget\/js\/editor\/editor.js","common:widget\/js\/logic\/mini-editor\/mini-editor.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/logic\/submit\/submit.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/js\/util\/log\/log.js","common:widget\/js\/ui\/tip\/tip.js"]},"question:widget\/js\/video\/video.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/js\/video\/video_749fae0.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/suffix-str\/suffix-str.js","common:widget\/js\/util\/log\/log.js"]},"question:widget\/js\/psask-bindsms\/psask-bindsms.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/js\/psask-bindsms\/psask-bindsms_8c99828.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/log\/log.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/js\/logic\/phone-bind\/phone-bind.js"]},"question:widget\/js\/admin\/officialAdmin\/officialAdmin.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/js\/admin\/officialAdmin\/officialAdmin_2986824.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/js\/logic\/category\/category.js","common:widget\/js\/util\/event\/event.js"]},"question:widget\/js\/set-tag\/set-tag.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/js\/set-tag\/set-tag_bcfade4.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/ui\/base\/base.js","common:widget\/js\/util\/template\/template.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/js\/ui\/scrollbar\/scrollbar.js","common:widget\/js\/util\/tangram\/string.js"]},"question:widget\/js\/admin\/userAdmin\/userAdmin.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/js\/admin\/userAdmin\/userAdmin_b2c685f.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/ui\/dialog\/dialog.js","common:widget\/js\/logic\/category\/category.js","question:widget\/js\/set-tag\/set-tag.js","common:widget\/lib\/jquery.placeholder\/jquery.placeholder.js"]},"question:widget\/js\/unloginask-bindsms\/unloginask-bindsms.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/js\/unloginask-bindsms\/unloginask-bindsms_9960dc1.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/log\/log.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/ui\/dialog\/dialog.js"]},"question:widget\/js\/audio\/jplayer\/jplayer.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/js\/audio\/jplayer\/jplayer_058fa6c.js","deps":["common:widget\/lib\/jquery\/jquery.js"]},"question:widget\/js\/audio\/audio.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/js\/audio\/audio_cae7476.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/log\/log.js","question:widget\/js\/audio\/jplayer\/jplayer.js"]},"question:widget\/js\/mavin-msg\/mavin-msg.js":{"pkg":"question:p6","deps":["common:widget\/lib\/jquery\/jquery.js","common:widget\/js\/util\/event\/event.js","common:widget\/js\/ui\/base\/base.js","common:widget\/js\/logic\/msg\/msg.js"]},"question:widget\/user\/mavin\/mavin.js":{"pkg":"question:p6","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/log\/log.js","common:widget\/js\/ui\/carousel\/carousel.js"]},"question:widget\/js\/weather\/weather.js":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/widget\/js\/weather\/weather_48530fb.js","deps":["common:widget\/js\/util\/tangram\/tangram.js","common:widget\/js\/util\/log\/log.js","common:widget\/lib\/jquery.placeholder\/jquery.placeholder.js"]}},"pkg":{"common:p3":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/common\/pkg\/editor_f72e2fa.js","has":["common:widget\/js\/logic\/editor\/editor.js","common:widget\/js\/logic\/editor\/addon\/addon.js","common:widget\/js\/logic\/editor\/config\/config.js","common:widget\/js\/logic\/editor\/fileUploader\/fileUploader.js","common:widget\/js\/logic\/editor\/lang\/lang.js","common:widget\/js\/logic\/editor\/prototype\/prototype.js"]},"question:p2":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/pkg\/editor_03606b2.js","has":["question:widget\/js\/editor\/config\/config.js","question:widget\/js\/editor\/editor.js","question:widget\/ask\/replyer\/replyer.js"]},"question:p6":{"url":"https:\/\/gss0.bdstatic.com\/7051cy792sgCpNKfpU_Y_D3\/static\/question\/pkg\/mavin_3a61af0.js","has":["question:widget\/js\/mavin-msg\/mavin-msg.js","question:widget\/user\/mavin\/mavin.js"]}}});</script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/common/pkg/framework_35930a1.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/common/pkg/more_fc10a72.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/common/widget/js/logic/qianbao-iframe/qianbao-dialog_a3c13c6.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/common/pkg/validate_d964132.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/common/pkg/module_da15f4e.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/common/widget/userbar-renew/userbar-renew_5f2e977.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/widget/top-nav-bar/top-nav-bar_2a4fc18.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/widget/js/business/business_546d2ae.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/widget/ask/share/share_e1dc32b.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/widget/js/ck/ck_8e1d0e9.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/pkg/module_088dc7e.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/widget/newbest/newbest_9b3edc3.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/widget/user/nologin/nologin_06f5f7d.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/pkg/login_921e1c2.js"></script><script type="text/javascript" src="https://gss0.bdstatic.com/7051cy792sgCpNKfpU_Y_D3/static/question/widget/user/nologin-daily/nologin-daily_903e843.js"></script><script type="text/javascript">
!function(){    require.async('common:widget/userbar-renew/userbar-renew.js');
}();
!function(){    require.async('common:widget/js/logic/search-box-new/search-box-new.js');
}();
!function(){    require.async('common:widget/menu/menu.js', function(menu){
    	menu.init();
    });
    // 导航menu可用时间打点
    alog && alog('speed.set', 'c_menu', +new Date); alog.fire && alog.fire("mark");
}();
!function(){	require.async('question:widget/top-nav-bar/top-nav-bar.js');
}();
!function(){    require.async('question:widget/ask/ask.js');
    require.async('question:widget/ask/pc-exp/ask-img.js');
}();
!function(){    require.async('question:widget/value-comment/value-comment.js',function(vc){
        vc.init('2225589447');
    });
}();
!function(){	require.async(['common:widget/lib/jquery/jquery.js', 'common:widget/js/util/log/log.js'], function($, log) {
		if ($('.wgt-best .best-text .answer-expand').size() != 0) {
			log.addKey({
				answer_expand_show: 1
			});
		}
        $(".wgt-best .best-text").on('click', ".answer-expand", function(e) {
        	$(this).hide();
        	$(".wgt-best .best-text .answer-expand-content").hide();
        	$(".wgt-best .best-text .answer-collapse-content").show();
        	$(".wgt-best .best-text .answer-collapse").css('display', 'block');
        	log.send({page:'question',pos:'qb-detail-expand-btn-click'});
        });
        $(".wgt-best .best-text").on('click', ".answer-collapse", function(e) {
        	$(this).hide();
        	$(".wgt-best .best-text .answer-collapse-content").hide();
        	$(".wgt-best .best-text .answer-expand-content").show();
        	$(".wgt-best .best-text .answer-expand").show();
        });
    });
}();
!function(){    require.async('common:widget/js/util/log/log.js', function(log) {
        // 展现相关问题的PV，ps：不知道以前怎么这么写，related_search_show和网友都在找参数是一样的？
        log.addKey({related_search_show: '1'});
        // 为您推荐展现pv
        log.addKey({bottom_union: '1'});
    });
}();
!function(){    require.async('question:widget/related/related.js', function(rel){
        rel({
            cmsRelq: "",
            cmsRelqrl: "",
            isLog: false                    });
    });
}();
!function(){    require.async(['common:widget/js/util/tangram/tangram.js', 'common:widget/js/util/log/log.js'], function($, log) {        
        // 展现相关问题的PV
        log.addKey({topic_show: '1'});

        // 实验
        
        var relateTopicQids = [];
        $('#wgt-topic a[data-qid]').each(function(){
            relateTopicQids.push($(this).data('qid'));
        });
        F.context('page').relateTopicQids = relateTopicQids.join('_');
    });
}();
!function(){        require.async('common:widget/js/util/log/log.js', function(log){
            //展现推送问题的PV
            log.addKey({push: '1'});
            log.init({key:2016, query: '.wgt-push .ft a'});
        });
    }();
!function(){    
    require.async('question:widget/user/nologin/nologin.js');
}();
!function(){require.async('question:widget/user/info/daily/daily.js', function(Daily){
	Daily.init({"date":"2017.03.28","term":"1307","list":[{"id":"46741","title":"\u4ed9\u4eba\u7403\u80fd\u9632\u7535\u8111\u8f90\u5c04\uff1f\u5e38\u7528\u7535\u8111\u5e94\u8be5\u5982\u4f55\u62b5\u6297\u8f90\u5c04\uff1f","mt_img_src":"https:\/\/gss0.baidu.com\/8_BXsjip0QIZ8tyhnq\/timg?wh_rate=0&wapiknow&quality=100&size=w250&sec=0&di=945cda46682b712d9e4052fcdeb9b84d&src=http%3A%2F%2Fiknow02.bosstatic.bdimg.com%2Fzhidaoribao%2F2017%2F0328%2F22.jpg"},{"id":"46843","title":"\u7814\u7a76\u8868\u660e\uff0c\u5403\u8fa3\u66f4\u6709\u76ca\u5065\u5eb7\uff1f","mt_img_src":"https:\/\/gss0.baidu.com\/8_BXsjip0QIZ8tyhnq\/timg?wh_rate=0&wapiknow&quality=100&size=w250&sec=0&di=023018277d8253e6d6716bc2344e5d07&src=http%3A%2F%2Ff.hiphotos.baidu.com%2Fzhidao%2Fwh%253D800%252C450%2Fsign%3D93b6cd1275d98d1076810439110f943a%2F503d269759ee3d6de890dc254a166d224e4ade8e.jpg"},{"id":"46912","title":"\u4f5c\u4e3a\u8def\u75f4\uff0c\u600e\u6837\u624d\u662f\u6b63\u786e\u7684\u627e\u8def\u65b9\u5f0f\uff1f","mt_img_src":"https:\/\/gss0.baidu.com\/8_BXsjip0QIZ8tyhnq\/timg?wh_rate=0&wapiknow&quality=100&size=w250&sec=0&di=1e8763fc554f51aa883f37319703cdda&src=http%3A%2F%2Fh.hiphotos.baidu.com%2Fzhidao%2Fwh%253D800%252C450%2Fsign%3D8e08fb19de2a60595245e912180418af%2Fa8773912b31bb051271ea4f83f7adab44aede02c.jpg"},{"id":"46600","title":"\u5510\u671d\u6218\u795e\u674e\u9756\uff0c\u662f\u600e\u4e48\u53d8\u6210\u4ed9\u754c\u7684\u6258\u5854\u674e\u5929\u738b\uff1f","mt_img_src":"https:\/\/gss0.baidu.com\/8_BXsjip0QIZ8tyhnq\/timg?wh_rate=0&wapiknow&quality=100&size=w250&sec=0&di=6f76a5fc808bb08a001456e97a875cee&src=http%3A%2F%2Fa.hiphotos.baidu.com%2Fzhidao%2Fwh%253D800%252C450%2Fsign%3D430c828c0023dd542126af60e1399fea%2F37d3d539b6003af3b29822883c2ac65c1038b63c.jpg"},{"id":"46862","title":"\u4f60\u5916\u8bed\u603b\u5b66\u4e0d\u597d\uff0c\u8fd9\u5176\u5b9e\u5f88\u79d1\u5b66\u4e28\u8111\u6d1e\u95ee\u7b54","mt_img_src":"https:\/\/gss0.baidu.com\/8_BXsjip0QIZ8tyhnq\/timg?wh_rate=0&wapiknow&quality=100&size=w250&sec=0&di=27b5e746560d5e2915fc12e0696b0281&src=http%3A%2F%2Ff.hiphotos.baidu.com%2Fzhidao%2Fwh%253D800%252C450%2Fsign%3D9397fdbf053387449c902774613ff5cd%2F1f178a82b9014a9093b0e552a0773912b21bee57.jpg"},{"id":"46871","title":"\u5185\u5fc3\u654f\u611f\u662f\u4e00\u79cd\u600e\u6837\u7684\u4f53\u9a8c\uff1f","mt_img_src":"https:\/\/gss0.baidu.com\/8_BXsjip0QIZ8tyhnq\/timg?wh_rate=0&wapiknow&quality=100&size=w250&sec=0&di=b80e6c7323ccd620617afa504d40b1c0&src=http%3A%2F%2Fb.hiphotos.baidu.com%2Fzhidao%2Fwh%253D800%252C450%2Fsign%3D932a8c2ae9fe9925cb596158049872eb%2F6159252dd42a28349d98a2e452b5c9ea15cebf27.jpg"},{"id":"46758","title":"\u73cd\u73e0\u868c\u662f\u600e\u4e48\u556a\u556a\u556a\u7684\u5462\uff1f","mt_img_src":"https:\/\/gss0.baidu.com\/8_BXsjip0QIZ8tyhnq\/timg?wh_rate=0&wapiknow&quality=100&size=w250&sec=0&di=2693d8421bcec30486ff007f5ea2166f&src=http%3A%2F%2Ff.hiphotos.baidu.com%2Fzhidao%2Fwh%253D800%252C450%2Fsign%3Dbed8008bf11986184112e78c7add0247%2Fd000baa1cd11728b4ad309c8c1fcc3cec2fd2c59.jpg"}]}, '0');
});
}();
!function(){    
    require.async('question:widget/user/nologin-daily/nologin-daily.js');
}();
!function(){			require.async('common:widget/js/logic/union/union.js', function(union){
				// args[2, 3]自定义定向使用, common:union中有限制只能调用一次;
				union('968278', 'union-asplu', {
					'zdquery'       : '',
					'zdclassid' : '1246',
					'zhidaoqid'         : '1925885591182532307'
				});
			});
		}();
!function(){    require.async('question:widget/ad-right/ad-right.js');
}();
!function(){    require('common:widget/js/logic/ie-prompt/ie-prompt.js');
}();
!function(){    
require.async(['common:widget/js/util/tangram/tangram.js', 'common:widget/js/util/log/log.js', 'common:widget/js/util/event/event.js', 'common:widget/js/logic/submit/submit.js', 'common:widget/js/ui/dialog/dialog.js', 'question:widget/js/file/file.js', 'question:widget/js/left-promotion/left-promotion.js', 'question:widget/js/video/video.js', 'common:widget/js/ui/tip/tip.js', 'question:widget/ask/share/share.js', 'common:widget/js/util/https/https.js'], function($, log, ec, Submit, Dialog, File, LeftPromotion, Video, Tip, share, https){

    // 打点QB页用户可操作时间
    alog('speed.set', 'drt', +new Date);
    // F.context('new_qb_fr', 'new_qb_' + 0);

    $(function(){ 
                                    
            log.addKey({
                qbleftdown: $('.qbleftdown').find('li').size(),
                qbrightdown:$('.qbrightdown').find('.r').size()
            });
            if ( $( '.qbleftdown a' ).size() ) {
                log.addKey({
                    ec_ads: '2',
                    ec_ads_count: $('.qbleftdown').find('a.ec_ad_title, span.ec_qad_title, a.EC_ad_title').size()
                }); 
                $('.qbleftdown a').click(function(){
                    var $parent = $( this ).parent();
                    if ( this.id || this.className == 'EC_ad_title'
                        || $(this).hasClass('ec_ik220_adtitle')
                        || $(this).hasClass('ec_ik220_desc')
                        || $parent.hasClass( 'EC_ads_answer' )
                        || this.className == 'EC_ads_listurl'
                        || this.className == 'ec_ad_title'
                        || $parent.hasClass('ec_qad_title')
                        || $parent.hasClass('ec_qad_answerer') ) {
                        log.send({
                            type: 2014,
                            evtType: 'click',
                            pos: 'ec_ads'
                        });
                    }
                });
            }
            require.async('question:widget/js/card/card.js', function(card){
                $('.user-name').each(function(index, item){
                    new card({ target: item, type: 'normal' });
                });
                $('.mavin-name').each(function(index, item){
                    new card({target: item, type: 'mavin' });
                });
                $('.opendev-name').each(function(index, item){
                    new card({target: item, type: 'opendev'});
                });
                $('.uadmin-a').each(function(index, item) {
                    new card({target: item, type: 'uadminIcon'});
                });
                $('.business-name').each(function(index, item){
                    new card({target: item, type: 'business' });
                });
                $('.quality-business-name').each(function (index, item) {
                    new card({target: item, type: 'qbusiness'});
                });
            });
            $('.fixed-ask-e').click(function(e){
                e.preventDefault();
                var username = $(this).attr('username');
                require.async('common:widget/js/logic/iask/iask.js', function(fixedAsk){
                    fixedAsk(username);
                });
            });
            $('.replyask-shrink a').click(function(e){
                e.preventDefault();
                var flag = this.innerHTML.indexOf('更多追问') != -1;

                var dl = $(this).html( flag ? '<i class="i-incline-up"></i>收起追问' : '<i class="i-incline-down"></i>更多追问' ).parent().prevAll('.replyask');
                $($.makeArray(dl).reverse().slice(flag ? 0 : 3, dl.length)).css('display', flag ? 'block' : 'none');
            });
            $('.replyask-box').each(function (index, item) {
                if ($(item).find('.replyask-shrink').size() == 0) {
                    if ($(item).find('.ask-supply').size() == 2) {
                        // $(item).find('.replyask').last().find('.ask-supply-line').hide();
                    }
                    if ($(item).find('.ask-supply').size() == 1) {
                        // $(item).find('.ask-supply-line').hide();
                    }
                    // $(item).find('.ask-supply-line').last().hide();
                }
            });
            if($('.thunder-wrap').size()){
                require.async('question:widget/js/thunder/thunder.js', function(thunder){
                    $(function(){
                        thunder.init();
                    });
                });
            }
            $.each(F.context('answers'), function(index, item){
                if(item.user){
                    if (item.user.isFromBusiness > 0) {
                        $.ajax({
                            url: '/business/submit/onbusinessbrowse',
                            type: 'POST',
                            dataType: 'json',
                            data: {
                                businessId: item.user.business.businessId,
                                page: '1',
                                token: F.context('businessToken')
                            }
                        })
                        .done(function () {
                        })
                        .fail(function () {
                        });
                    }   
                }
            });
                
            $.ajax({
                url: '/mavin/api/mavinpv',
                type: 'GET',
                dataType: 'json',
                data: {
                    qid: F.context('page')['qid']
                }
            })
            .done(function () {
            })
            .fail(function () {
            });
            if ($('.newbest-mavin-prolink').size()) {
                log.send({
                    type: 2014,
                    pos: 'newbest-mavin-prolink',
                    action: 'pv',
                    page: 'question',
                    qid: F.context('page')['qid']
                })
            }
            $(document).on('click', '.ikqb_img', function(){
                log.send({
                    type: 2014,
                    bigimg: 'click'
                });
            });
            $('a.optimus').on('click', function() {
                log.send({
                    type: 2014,
                    area: 'ad-right-optimus',
                    action: 'click',
                    cid: F.context('page')['cid'],
                    cidTop: F.context('page')['cidTop'],
                    cidMid: F.context('page')['cidMid']
                });
            });

            $('#wgt-nologin-daily').click(function(e){
                e.stopPropagation();

                if($(e.target).closest('#daily-carousel').size() && !$(e.target).closest('.carousel-control').size()){
                    log.send({
                        type: 2014,
                        page: 'question',
                        pos: 'no-login-daily',
                        action: 'click'
                    });
                }
            });

            $('.wgt-daily').on('click', 'a', function(){
                log.send({
                    type: 2014,
                    page: 'question',
                    pos: 'login-daily',
                    action: 'click'
                });
            });
            $('.qbrightdown a').click(function(){
                log.send({
                    type: 2014,
                    qid: F.context('page')['qid'],
                    area: 'medical-right-txt-ads',
                    action: 'click'
                });
            });
            if($('ikaudio').size()){
                log.addKey({
                    'audio' : 1
                });

                require.async('question:widget/js/audio/audio.js', function(audio){
                    audio.init();
                });
            }
            require.async('question:widget/js/comment/comment.js', function(comm){
                comm.getCount();
            });
            $('.recommend-text, .best-text, .answer-text, .replyask-content').each(function(i, answerText){
                $(answerText).find('pre[t="code"]').each(function(i, pre){
                    var loadSyntax = function(){
                        SyntaxHighlighter(pre);
                    };
                    
                    $(pre).text($(pre).html($(pre).html().replace(/<br\s*\/?>/ig, '##IK_LINEBREAK##')).text().split('##IK_LINEBREAK##').join('\n'));

                    $(pre).addClass('brush:'+$(pre).attr('l')+';toolbar:false;');
                    if (window.SyntaxHighlighter) {
                        SyntaxHighlighter.highlight(pre);
                        $(answerText).find('.syntaxhighlighter .code .line').each(function(index, line){
                            $(answerText).find('.syntaxhighlighter .gutter .line').eq(index).height($(line).height());
                        });
                    } else {
                        var sioUrl = https.autoTrans('http://img.iknow.bdimg.com/libs/SyntaxHighlighter/shCore.min.js');
                        $.sio(sioUrl).callByBrowser(function(){
                            SyntaxHighlighter.defaults['quick-code'] = false;
                            SyntaxHighlighter.config.stripBrs = true;
                            SyntaxHighlighter.highlight(pre);
                            $(answerText).find('.syntaxhighlighter .code .line').each(function(index, line){
                                $(answerText).find('.syntaxhighlighter .gutter .line').eq(index).height($(line).height());
                            });
                        });
                    }
                });

                $(answerText).find('ikvideo').each(function(i, video){
                    var id = 'VIDEO_' + $.id(),
                        src = $(video).attr('src'),
                        sid;

                    var container = $('<div/>').attr('id', id).insertBefore($(video));
                    if (src.indexOf('youku') > -1 && (sid = src.match(/sid\/(.*?)[\?\/]/))) {
                        if (sid[1]) {
                            src = 'http://player.youku.com/player.php/sid/'+sid[1]+'/v.swf';
                        }
                    }

                    container.html('<embed src="'+src+'" allowFullScreen="true" quality="high" width="'+$(video).attr('width')+'" height="'+$(video).attr('height')+'" align="'+$(video).attr('align')+'" allowScriptAccess="never" type="application/x-shockwave-flash"></embed>');
                });
            });

                        require.async('common:widget/js/ui/lazyload/lazyload.js', function(lazyload){
            $('.wgt-replyer-best .avatar-48 a, .wgt-replyer-best .avatar-66 a, .wgt-replyer-special .avatar-66 a,.wgt-replyer-best .avatar-69 a, .wgt-replyer-best .avatar-70 a, .wgt-replyer-best .avatar-66 a, #cms-company a').lazyload();
        });
        $('.ikqb-map').each(function(index, item) {
            var ifreamObj = $("<iframe/>").attr({
                frameborder: '0'
                ,width:"430" 
                ,height:"310"
                ,style: 'display:none;'
                ,className: 'answer-map'
            }),
            tmpsrc = $(item).attr("map") || $(item).attr("src");
            ifreamObj.attr('src', "//zhidao.baidu.com/html/map" + tmpsrc.replace(/^iknow/i, ''));

            $(item).before(ifreamObj).remove();
            ifreamObj.after(
                $("<p/>").addClass('f-aid').html("本数据来源于百度地图，最终结果以百度地图最新数据为准。")
            ).show();
        });
                var mavinUidAry = [];
        $.object.each(F.context('answers'), function(item, key){
            if(item.user && item.user.mavinName){
                mavinUidAry.push(item.uid);
            }
        });

        if(mavinUidAry.length){
            var options = {
                uids: mavinUidAry.join(',')
            };

            $.post('/mavin/api/getmavinpv', options);
        }
        
            

                                                    log.addKey({
                nsma: "2"
            });
                
                        
                                        if ($('video.edui-faked-video').size() > 0) {
            Video.init();
        }
                   
                require.async('common:widget/js/logic/ut/ut.js', function(UT){
            UT.start(['userbar','header','wgt-ask','answer-editor','wgt-answers']);
        });

        if ( $('file').size() == 0 ) {
            logPV();
        } else {
            File.init(logPV);
        }
        
        if (F.context('user')['isUserAdmin'] != '1'){
            require.async('question:widget/js/select-search/select-search.js', function(A){
                A.init();
            }); 
        }
                var adTopImg = $('.adTopImg');
        if(adTopImg.length && adTopImg.css('display') != 'none') {
            log.addKey({
                adTopImg_new: 1
            });
            adTopImg.on('click', function() {
                log.send({
                    page: 'question',
                    pos: 'adTopImg_new',
                    action: 'click',
                    type: 2014
                });
            });
        }
        
        log.init({key:2014, query: 'body',action:'click'});
        function logPV(){
            var logOptions = {
                type: 2014,
                page: 'question', 
                action: 'entrance',
                screen: parseInt($('body').height()/$(window).height()),
                qid: F.context('page')['qid'],
                cid: F.context('page')['cid'],
                view: F.context('page').isView,
                cidTop: F.context('page')['cidTop'],
                cidMid: F.context('page')['cidMid'],
                refer: document.referrer
            };
            log.addKey({
                 sample_new_qb: 0
            });
            log.addKey({
                evaSampling: 900
            });

            
            log.addKey({
                 sample_qb_50per: "2"
            });

            log.addKey({
                 qid: F.context('page')['qid']
            });

            if (F.context('page').relateQids) {
                logOptions.relateQids = F.context('page').relateQids;
            }

            if (F.context('page').relateTopicQids) {
                logOptions.relateTopicQids = F.context('page').relateTopicQids;
            }
            if ($('a.optimus').length) {
                log.addKey({'optimus': 1});
            }
            if ($('.classinfo').length) {
                log.addKey({'classinfo': 1});
            }
            var uadminIcon = $('.uadmin-a');
            var uadminIconSize = uadminIcon.length;
            if (uadminIconSize) {
                logOptions.uadminIconNum = uadminIconSize;
            }
            
            setTimeout(function(){
                log.send(logOptions, true);
            }, 100);
        }
                    log.addKey({'qb_test_case': '19'});
                var loc_ans = $.url.getQueryValue(location.href, 'loc_ans');
        if(!loc_ans) {
            var myAnswerList = $('.wgt-best .answer-mine, .wgt-recommend .answer-mine, .wgt-special .answer-mine'),
                myAnswer = null; 
            if(myAnswerList.size()){        
                myAnswer = myAnswerList.first();        
                setTimeout(function(){
                    $(document).scrollTop(myAnswer.offset().top - 10);
                }, 200);       
            }
        }else {
            var locAnswerList = $('.wgt-best .answer, .wgt-recommend .answer, .wgt-special .answer'),
                locAnswer = null;
            locAnswerList.each(function(index, item) {
                if($(item).attr("id").indexOf(loc_ans) != -1) {
                    locAnswer = $(item);
                }
            });
            if(locAnswer) {
                setTimeout(function(){
                    $(document).scrollTop(locAnswer.parent().offset().top - 10);
                }, 200);  
            }
        }
        if (F.context('egg')) {
            require.async('question:widget/js/egg/egg.js', function(egg){
                $(function(){
                    egg.init(F.context('egg'));
                });
            });
        }
        var grid68  = $('.qb-content'), 
            qid = F.context('page')['qid'];
        $.each({
            'qb-content'            : '.q-content a@',                      
            'qb-supply-content'     : '.q-supply-content a@',               
            'qb-best-text'          : '.wgt-best .best-text a@',            
            'qb-special-bast-text'  : '.wgt-special .best-text a@',         
            'qb-recommend-text'     : '.wgt-recommend .recommend-text a@',  
            'qb-answer-text'        : '.answer-text a@',                    
            'qb-replyask-ask'       : '.ask+dd a',                          
            'qb-replyask-reply'     : '.reply+dd a',                        
            'qb-best-thank'         : '.thank pre a',                       
            'qb-answer-refer'       : '.answer-refer a'                     
        }, function(key, val){
            var aLink = grid68.find( val.replace(/\@$/, '[title!="点击查看大图"]') )
                        .not('.app-keyword,.inner-link')
                        .filter(function(){ 
                            return this.getAttribute('href').match(/^http/i) && this.innerHTML != '' && !$(this).closest('.ed2k-wrap').size() && !$(this).closest('.thunder-wrap').size() 
                        });
            if(aLink.length > 0){
                $(aLink).each(function(i,item){
                    log.send({
                        'type'  : 2014,
                        'page'  : 'question',
                        'qid'   : qid,
                        'area'  : key,
                        'action': 'linkPv',
                        'text'  : item.getAttribute('href'),
                        'host'  : item.getAttribute('href').split('/')[2]
                    });
                });
            }
            aLink.click(function(){
                log.send({
                    'type'  : 2014,
                    'page'  : 'question',
                    'qid'   : qid,
                    'area'  : key,
                    'action': 'linkClick',
                    'text'  : this.getAttribute('href'),
                    'host'  : this.getAttribute('href').split('/')[2]
                });
            });
            grid68.find( val.replace(/\@$/, '') ).attr('rel', 'nofollow');
        });
        $(document).keydown(function(e){
            if(e.ctrlKey && e.keyCode == 67){
                var isStandard = Boolean(window.getSelection),
                    selection = isStandard ? window.getSelection() : document.selection.createRange(),
                    text = (isStandard ? selection + '' : selection.text).replace(/\n+/g,''),
                    textLen = text.length;
                log.send({
                    type: 2014,
                    page: 'question',
                    qid: F.context('page')['qid'],
                    uid: F.context('user')['id'],
                    action: 'ctrl+c',
                    text: (textLen > 0 && textLen < 50) ? text : ''
                });
            }
        });
        var BAIDUID = $.cookie.get('BAIDUID') ? $.cookie.get('BAIDUID') : '0',
            recordkey = 'IK_' + BAIDUID.split(':')[0],
            recordCookie = $.cookie.get(recordkey) || 0,
            recordCidKey = 'IK_CID_'+F.context('page').cidTop,
            recordCidCookie = $.cookie.get(recordCidKey) || 0,
            cookieOpt = {
                expires : 1000*60*60*24*365,
                path : '/'
            };
        $.cookie.set(recordkey, parseInt(recordCookie) + 1, cookieOpt);
        $.cookie.set(recordCidKey, parseInt(recordCidCookie) + 1, cookieOpt);
        $.cookie.remove(recordkey,{
            path : '/question'
        });
        var cookieArr = document.cookie && document.cookie.split('; ');
        if(cookieArr.length){
            $.each(cookieArr, function(i, item){
                var cookieKey = item.split('=')[0];
                if(cookieKey != recordkey && cookieKey.match(/IK_[0-9A-Z]{32}/)){
                    $.cookie.remove(cookieKey, {path: '/'});
                }
            });
        }
        if ($.cookie.get('IK_REFER_QID')) {
            $.cookie.remove('IK_REFER_QID', {path: '/'});
        }
        $(document).on('click', 'a[href*="/question/"]', function(){
            $.cookie.set('IK_REFER_QID', F.context('page').qid, {
                expires: 20000,
                path: '/'
            });
        });
        
                            $(document).on('click', '.ikqb_img_alink', function(evt){
                if($.browser.msie&&$.browser.version==6){
                    return false;
                }
                var imgTarget = $(this).find('img'),
                    imgBigSrc = $(this).attr('href'),
                    maxWidth = $(this).parent('p').outerWidth(),
                    imgSmallSrc = imgTarget.attr('esrc'),
                    sourceWidth = imgTarget.width(),
                    sourceHeight = imgTarget.height();

                if(imgTarget.hasClass('img_show')){
                    imgTarget.attr('src',imgBigSrc);
                    if(!imgTarget.hasClass('ikqb_img')){
                        imgTarget.removeClass('ikqb_img');
                        imgTarget.animate({
                            'width':'100%'
                        },500);
                    }else{
                        imgTarget.animate({
                            'maxWidth':'500px',
                            'maxHeight':'340px'
                        },500);
                    }
                    imgTarget.removeClass('img_show');
                }else{
                    $(this).append('<i class="ikqb_img_loading"></i>');
                    var bigImg = new Image();
                    bigImg.onload = function(){
                        imgTarget.attr('src',imgBigSrc);
                        if(sourceWidth == bigImg.width){
                            imgTarget.removeClass('ikqb_img');
                            imgTarget.animate({
                                'width':'120%'
                            },500);
                        }else{
                            imgTarget.animate({
                                'maxWidth':bigImg.width>maxWidth?maxWidth:bigImg.width,
                                'maxHeight':bigImg.height
                            },500);
                        }
                        imgTarget.addClass('img_show');
                        $('.ikqb_img_loading').remove();
                    }
                    bigImg.src = imgBigSrc;
                }
                evt.preventDefault();
            });
                $('#search-form').submit(function(e) {
            log.send({
                type: 2014, 
                page: 'question', 
                position: 'searchbtn',
                action: 'click'
            });
            e.preventDefault();
        });
    });
    
    //统计QB页用户名片的展现量、查看QB页用户名片的用户数
    $('.user-name').on('mouseenter', function (e) {
        log.send({
            'page': 'qb',
            'type': 2060,
            'action': 'hover',
            'area': 'user-name'
        });
    }).on('click', function (e) {
        log.send({
            'page': 'qb',
            'type': 2060,
            'action': 'click',
            'area': 'user-name'
        });
    });
    //“向TA求助”的点击量、点击用户数
    $('body').on('click', '.fixed-ask, .fixed-ask-e', function (e) {
        log.send({
            'page': 'qb',
            'type': 2060,
            'action': 'click',
            'area': 'fixed-ask'
        });
    });
    // “举报“下“描述不清”等三项的展现量（PV）、  “描述不清”等三项的点击总量、 “描述不清”等三项的点击用户数
    $('body').on('mouseenter', '.wgt-accuse .accuse-enter', function (e) {
        log.send({
            'page': 'qb',
            'type': 2060,
            'action': 'hover',
            'area': 'accuse-enter'
        });
    }).on('click', '.wgt-accuse a', function (e) {
        log.send({
            'page': 'qb',
            'type': 2060,
            'action': 'click',
            'area': 'wgt-accuse-a'
        });
    });

    // 新增分享打点统计
    if ($.url.getQueryValue(location.href, 'sharesource')) {
        log.send({
            module: 'question',
            page: 'qb',
            project: 'new-qb-share',
            postion: 'new-share',
            action: 'view-by-share-' + $.url.getQueryValue(location.href, 'sharesource')
        });
    }

    // 个人行家回答特型tooltip
    var mavinTips = [];
    var mavinTimeout = [];
    $('.mavin-reply-icon').each(function (index) {
        var me = this;
        var mavinLevelTitle = $(this).attr('data-title');
        var mavinMajor = $(this).attr('data-major');
        var content = '<p class="mavin-reply-tip"><span class="mr-5">[' + mavinLevelTitle + ']</span>已完成<span class="enhance">实名认证</span>+<span class="enhance">行业认证</span>';
        if (mavinMajor == 1) {
            content += '+<span class="enhance">专业认证</span>';
        }
        content += '</p>';

        $(this).mouseenter(function (e) {
            $('div[role="tooltip"]').hide();
            clearTimeout(mavinTimeout[index]);
            mavinTimeout[index] = setTimeout(function () {

                if (!mavinTips[index]) {
                    mavinTips[index] = new Tip({
                        'target': me,
                        'tooltipClass' : 'tip-white',
                        'autoDispose': false,
                        'direction': 'top',
                        'content': content,
                        'position': {
                            my: 'left-20 top'
                        }
                    });
                }
                mavinTips[index].show();
            }, 70);

        }).mouseleave(function (e) {
            mavinTimeout[index] = setTimeout(function () {
                mavinTips[index] && mavinTips[ index ].hide();
            }, 70);
        });
    });
    window.onload = function () {

        var sendLog = function() {
            var is_topads_truely_show = null;           // 顶部网盟
            var is_bottomwangmeng_truely_show = null;   // 底部网盟为你推荐
            var is_leftads_truely_show = null;          // 实际展示左下广告
            var is_rightads_truely_show = null;         // 实际展示左下广告
            
            // 顶部网盟广告 -- 从元素高度判断
            if (F.context('ads_log_toprequest')) {
                if ($('.left-top-ads').height() == 0
                    || $('.left-top-ads').width() == 0) {
                    is_topads_truely_show = 0;
                } else {
                    is_topads_truely_show = 1;
                }
            } else {
                is_topads_truely_show = 0;
            }

            // 底部为你推荐网盟广告 -- 从iframe判断
            if (F.context('ads_log_bottomrequest')) {
                if ($('.wgt-bottom-union').find('iframe').size() == 0) {
                    is_bottomwangmeng_truely_show = 0;
                } else {
                    is_bottomwangmeng_truely_show = 1;
                }
            } else {
                is_bottomwangmeng_truely_show = 0;
            }

            // 同步凤巢广告 -- 从元素高度判断
            if (F.context('ads_log_leftdown')) {
                if ($('#qbleftdown-container').height() == 0
                    || $('#qbleftdown-container').width() == 0) {
                    is_leftads_truely_show = 0;
                } else {
                    is_leftads_truely_show = 1;
                }
            } else {
                is_leftads_truely_show = 0;
            }

            // 同步右侧广告，看是否存在dom以及是否展示
            if (F.context('ads_log_right')) {
                if ($('.widget-sma').height() == 0
                    || $('.widget-sma').width() == 0) {
                    is_rightads_truely_show = 0;
                } else {
                    is_rightads_truely_show = 1;
                }
            } else {
                is_rightads_truely_show = 0;
            }

            // 得到浏览器信息
            function getBrowserType() {
                if (navigator.userAgent.toLowerCase().indexOf('se 2.x')>-1) {
                    return 'Sougo';
                } else if (navigator.userAgent.toLowerCase().indexOf('maxthon')>-1) {
                    return 'maxthon';
                } else if (navigator.userAgent.toLowerCase().indexOf('qqbrowser')>-1) {
                    return 'qqbrowser';
                } else if (navigator.userAgent.toLowerCase().indexOf('msie')>-1) {
                    return 'IE';
                } else if (/chrome\/(\d+\.\d+)/i.test(navigator.userAgent)) {
                    return 'Chrome';
                } else if (/firefox\/(\d+\.\d+)/i.test(navigator.userAgent)) {
                    return 'Firefox';
                } else {
                    return 'other';
                }
            }
            var browsert_type = getBrowserType();

            var adsLogParams = {
                type: 2014,
                page: 'question', 
                action: 'ads_block_info_hour',
                is_topwangmeng_should_show: F.context('ads_log_toprequest') || 0,
                is_topwangmeng_truely_show: is_topads_truely_show,
                is_bottomwangmeng_should_show: F.context('ads_log_bottomrequest') || 0,
                is_bottomwangmeng_truely_show: is_bottomwangmeng_truely_show,
                is_leftads_should_show: F.context('ads_log_leftdown') || 0,
                is_leftads_truely_show: is_leftads_truely_show,
                is_rightads_should_show: F.context('ads_log_right') || 0,
                is_rightads_truely_show: is_rightads_truely_show,
                browser_type: browsert_type
            };

            log.send(adsLogParams);
        };

        setTimeout(sendLog, 1000);
    };
    /*
     * 设置hunter用户体验报告
     * @FE-hanzonge @PM-liulin04
     * @date 2016-01-05
     *
     * 模糊匹配：mid=73716，取一定量pv
     * 非模糊匹配：mid-qid映射关系为，
     *      73707->124553427
     *      73708->258966527
     *      73709->145354616
     *      73710->1509811702495467100
     *      73711->334249256
     */
    window.Hunter = window.Hunter || {};
    Hunter.userConfig = Hunter.userConfig || [];
    var tempHid = null;
    var pageQid = F.context('page').qid;
    
    if (pageQid == 124553427) {
        tempHid = 73707;
    } else if (pageQid == 258966527) {
        tempHid = 73708;
    } else if (pageQid == 145354616) {
        tempHid = 73709;
    } else if (pageQid == 1509811702495467100) {
        tempHid = 73710;
    } else if (pageQid == 334249256) {
        tempHid = 73711;
    } else {
        if (parseInt(Math.random()*100) < 5) {
            tempHid = 73716;
        }
    }

    if (tempHid) { 
        Hunter.userConfig.push({
            hid: tempHid
        });
    }
    function jumpShare() {

        if ($('.jump-top-box').size() != 0) {
            // 调整返回顶部和任务列表的顺序
            $('.jump-top-box').find('.jump-top').before($('.jump-top-box').find('.jump-task-list'));

            // 加入分享功能
            var jumpShare = [
                '<div class="jump-share">',
                    '<div class="jump-share-tit">分享</div>',
                    '<div class="share-area"></div>',
                '</div>'
            ].join('');

            $('.jump-top-box').find('.jump-task-list').before(jumpShare);

            share.init({
                target: $('.jump-share .share-area'),
                pageUrl: 'http://zhidao.baidu.com/question/' + F.context('page').qid,
                title: document.title,
                pos: 'rightSilde',
                logOpt: {
                    module: 'question',
                    page: 'qb',
                    project: 'new-qb-share',
                    postion: 'new-share-right'
                }
            });
            // 如果有行家工作室，放在最顶部
            if ($('.jump-top-box').find('.jump-goto-mavin').size()) {
                $('.jump-top-box').find('.jump-share').before($('.jump-top-box').find('.jump-goto-mavin'));
            }

            jumpTimer && clearInterval(jumpTimer);
        }
    }

    var jumpTimer = setInterval(function () {
        jumpShare();
    }, 1000)




});

}();
!function(){								                				require.async('common:widget/js/logic/dom-ready/dom-ready.js', function(D){ D.init([]) });
            }();
</script>    
<script type="text/javascript">
    require.async('common:widget/lib/jquery/jquery.js', function ($) {
        //  var ie = /msie (\d+\.\d+)/i.test(navigator.userAgent) ? (document.documentMode || +RegExp['$1']) : undefined;
        if (!/chrome|firefox|safari|msie 10|rsv:11|msie [89]/i.test(navigator.userAgent)) {
            return;
        }

        window.BaiduHttps = window.BaiduHttps || {};
        window.BaiduHttps.callbacks = function (data) {
            if (data && data.s === 0) {
                window.supportHttps = 1;
                setTimeout(function () {
                    $('a[href^="http://www.baidu.com/s?"]').each(function (index, item) {
                        var link = $(item).attr('href');
                        if (~link.indexOf('?wd=') || ~link.indexOf('&wd=')) {
                            link = link.replace(/^http/, 'https');
                            $(item).attr('href', link);
                        }
                    });
                }, 2000);
            }
        };

        var script = document.createElement('script');
        script.type = 'text/javascript';
        script.src = 'https://www.baidu.com/con?from=zhidao';
        document.body.appendChild(script);
    });
</script>
</html>
