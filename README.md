# wiseTreeView
jQuery Plugin TreeView

* 특징

   - 작은 아이콘/폰트때문에 좁고 답답해 보이는 일반적인 TreeView 대신

   - 노드를 시원시원하게 커스터마이징하고, 노드 내부에 html/아이콘 등도 변경할 수 있게 개발 


<img src="./picture/sample1.png"></img><br/>

<img src="./picture/sample2.png"></img><br/>

<img src="./picture/sample3.png"></img><br/>

<img src="./picture/sample4.png"></img><br/>
 

* 사용법 

``` HTML
    <link rel="stylesheet" href="/wise/common/css/jquery-wiseTreeView-1.0.css">

    <!-- 여기에 jquery 모듈 import -->

    <script src="/wise/common/js/jquery-wiseTreeView-1.0.js"></script>

    <div id=tree style="width:000px"></div>
```

``` javascript
    let list = $("#tree");
```

    위 내용이 공통이며 아래 샘플 4개로 설명함 (위 그림 4개 참조)
    
    (샘플1 : 3796개 데이터 - [샘플1 바로가기](https://sendjay.com/etc/wiseTreeView/sample.html))

    const json = [

{"cd":"11000000","nm_kor":"서울특별시","nm_eng":"Seoul"},

{"cd":"11010000","nm_kor":"종로구","nm_eng":"Jongno-gu"},

{"cd":"11010720","nm_kor":"청운효자동","nm_eng":"Cheongunhyoja-dong"},

{"cd":"11010530","nm_kor":"사직동","nm_eng":"Sajik-dong"},

{"cd":"11010540","nm_kor":"삼청동","nm_eng":"Samcheong-dong"},

{"cd":"11010550","nm_kor":"부암동","nm_eng":"Buam-dong"},

{"cd":"11010560","nm_kor":"평창동","nm_eng":"Pyeongchang-dong"},

{"cd":"11010570","nm_kor":"무악동","nm_eng":"Muak-dong"},

{"cd":"11010580","nm_kor":"교남동","nm_eng":"Gyonam-dong"},

{"cd":"11010600","nm_kor":"가회동","nm_eng":"Gahoe-dong"},

{"cd":"11010610","nm_kor":"종로1.2.3.4가동","nm_eng":"Jongno 1.2.3.4(ilisamsa)-ga-dong"},

{"cd":"11010630","nm_kor":"종로5.6가동","nm_eng":"Jongno 5.6(oryuk)-ga-dong"},

{"cd":"11010640","nm_kor":"이화동","nm_eng":"Ihwa-dong"},

{"cd":"11010730","nm_kor":"혜화동","nm_eng":"Hyehwa-dong"},

{"cd":"11010670","nm_kor":"창신1동","nm_eng":"Changsin 1(il)-dong"},

{"cd":"11010680","nm_kor":"창신2동","nm_eng":"Changsin 2(i)-dong"},

{"cd":"11010690","nm_kor":"창신3동","nm_eng":"Changsin 3(sam)-dong"},

{"cd":"11010700","nm_kor":"숭인1동","nm_eng":"Sungin 1(il)-dong"},

{"cd":"11010710","nm_kor":"숭인2동","nm_eng":"Sungin 2(i)-dong"},

{"cd":"11020000","nm_kor":"중구","nm_eng":"Jung-gu"},

{"cd":"11020520","nm_kor":"소공동","nm_eng":"Sogong-dong"},

{"cd":"11020540","nm_kor":"회현동","nm_eng":"Hoehyeon-dong"},

{"cd":"11020550","nm_kor":"명동","nm_eng":"Myeong-dong"},

{"cd":"11020570","nm_kor":"필동","nm_eng":"Pil-dong"},

{"cd":"11020580","nm_kor":"장충동","nm_eng":"Jangchung-dong"},

{"cd":"11020590","nm_kor":"광희동","nm_eng":"Gwanghui-dong "},

{"cd":"11020600","nm_kor":"을지로동","nm_eng":"Euljiro-dong"},

{"cd":"11020690","nm_kor":"신당동","nm_eng":"Sindang-dong"},

{"cd":"11020700","nm_kor":"다산동","nm_eng":"Dasan-dong"},

{"cd":"11020710","nm_kor":"약수동","nm_eng":"Yaksu-dong"},

{"cd":"11020720","nm_kor":"청구동","nm_eng":"Cheonggu-dong"},

{"cd":"11020650","nm_kor":"신당5동","nm_eng":"Sindang 5(o)-dong"},

{"cd":"11020730","nm_kor":"동화동","nm_eng":"Donghwa-dong"},

{"cd":"11020670","nm_kor":"황학동","nm_eng":"Hwanghak-dong"},

{"cd":"11020680","nm_kor":"중림동","nm_eng":"Jungnim-dong"},

{"cd":"11030000","nm_kor":"용산구","nm_eng":"Yongsan-gu"},

{"cd":"11030510","nm_kor":"후암동","nm_eng":"Huam-dong"},

{"cd":"11030520","nm_kor":"용산2가동","nm_eng":"Yongsan 2(i)-ga-dong"},

{"cd":"11030530","nm_kor":"남영동","nm_eng":"Namyeong-dong"},

{"cd":"11030710","nm_kor":"청파동","nm_eng":"Cheongpa-dong"},

{"cd":"11030720","nm_kor":"원효로1동","nm_eng":"Wonhyoro 1(il)-dong"},

{"cd":"11030570","nm_kor":"원효로2동","nm_eng":"Wonhyoro 2(i)-dong"},

{"cd":"11030580","nm_kor":"효창동","nm_eng":"Hyochang-dong"},

{"cd":"11030590","nm_kor":"용문동","nm_eng":"Yongmun-dong"},

{"cd":"11030730","nm_kor":"한강로동","nm_eng":"Hangangno-dong"},

{"cd":"11030630","nm_kor":"이촌1동","nm_eng":"Ichon 1(il)-dong"},

{"cd":"11030640","nm_kor":"이촌2동","nm_eng":"Ichon 2(i)-dong"},

{"cd":"11030650","nm_kor":"이태원1동","nm_eng":"Itaewon 1(il)-dong"},

{"cd":"11030660","nm_kor":"이태원2동","nm_eng":"Itaewon 2(i)-dong"},

{"cd":"11030740","nm_kor":"한남동","nm_eng":"Hannam-dong"},

{"cd":"11030690","nm_kor":"서빙고동","nm_eng":"Seobinggo-dong"},

{"cd":"11030700","nm_kor":"보광동","nm_eng":"Bogwang-dong"},

{"cd":"11040000","nm_kor":"성동구","nm_eng":"Seongdong-gu"},

{"cd":"11040520","nm_kor":"왕십리2동","nm_eng":"Wangsimni 2(i)-dong"},

{"cd":"11040710","nm_kor":"왕십리도선동","nm_eng":"WangsimniDoseon-dong"},

{"cd":"11040540","nm_kor":"마장동","nm_eng":"Majang-dong"},

{"cd":"11040550","nm_kor":"사근동","nm_eng":"Sageun-dong"},

{"cd":"11040560","nm_kor":"행당1동","nm_eng":"Haengdang 1(il)-dong"},

{"cd":"11040570","nm_kor":"행당2동","nm_eng":"Haengdang 2(i)-dong"},

{"cd":"11040580","nm_kor":"응봉동","nm_eng":"Eungbong-dong"},

{"cd":"11040590","nm_kor":"금호1가동","nm_eng":"Geumho 1(il)-ga-dong"},

{"cd":"11040720","nm_kor":"금호2.3가동","nm_eng":"Geumho 2.3(isam)-ga-dong"},

{"cd":"11040620","nm_kor":"금호4가동","nm_eng":"Geumho 4(sa)-ga-dong"},

{"cd":"11040730","nm_kor":"옥수동","nm_eng":"Oksu-dong"},

{"cd":"11040650","nm_kor":"성수1가1동","nm_eng":"Seongsu 1(il)-ga-1(il)-dong"},

{"cd":"11040660","nm_kor":"성수1가2동","nm_eng":"Seongsu 1(il)-ga-2(i)-dong"},

{"cd":"11040670","nm_kor":"성수2가1동","nm_eng":"Seongsu 2(i)-ga-1(il)-dong"},

{"cd":"11040680","nm_kor":"성수2가3동","nm_eng":"Seongsu 2(i)-ga-3(sam)-dong"},

{"cd":"11040690","nm_kor":"송정동","nm_eng":"Songjeong-dong"},

{"cd":"11040700","nm_kor":"용답동","nm_eng":"Yongdap-dong"},

{"cd":"11050000","nm_kor":"광진구","nm_eng":"Gwangjin-gu"},

{"cd":"11050530","nm_kor":"화양동","nm_eng":"Hwayang-dong"},

{"cd":"11050540","nm_kor":"군자동","nm_eng":"Gunja-dong"},

{"cd":"11050550","nm_kor":"중곡1동","nm_eng":"Junggok 1(il)-dong"},

{"cd":"11050560","nm_kor":"중곡2동","nm_eng":"Junggok 2(i)-dong"},

{"cd":"11050570","nm_kor":"중곡3동","nm_eng":"Junggok 3(sam)-dong"},

{"cd":"11050580","nm_kor":"중곡4동","nm_eng":"Junggok 4(sa)-dong"},

{"cd":"11050590","nm_kor":"능동","nm_eng":"Neung-dong"},

{"cd":"11050630","nm_kor":"광장동","nm_eng":"Gwangjang-dong"},

{"cd":"11050640","nm_kor":"자양1동","nm_eng":"Jayang 1(il)-dong"},

{"cd":"11050650","nm_kor":"자양2동","nm_eng":"Jayang 2(i)-dong"},

{"cd":"11050660","nm_kor":"자양3동","nm_eng":"Jayang 3(sam)-dong"},

{"cd":"11050670","nm_kor":"자양4동","nm_eng":"Jayang 4(sa)-dong"},

{"cd":"11050600","nm_kor":"구의1동","nm_eng":"Guui 1(il)-dong"},

{"cd":"11050610","nm_kor":"구의2동","nm_eng":"Guui 2(i)-dong"},

{"cd":"11050620","nm_kor":"구의3동","nm_eng":"Guui 3(sam)-dong"},

{"cd":"11060000","nm_kor":"동대문구","nm_eng":"Dongdaemun-gu"},

{"cd":"11060810","nm_kor":"용신동","nm_eng":"Yongsin-dong"},

{"cd":"11060820","nm_kor":"제기동","nm_eng":"Jegi-dong"},

{"cd":"11060830","nm_kor":"전농1동","nm_eng":"Jeonnong 1(il)-dong"},

{"cd":"11060840","nm_kor":"전농2동","nm_eng":"Jeonnong 2(i)-dong"},

{"cd":"11060910","nm_kor":"답십리1동","nm_eng":"Dapsimni 1(il)-dong"},

{"cd":"11060860","nm_kor":"답십리2동","nm_eng":"Dapsimni 2(i)-dong"},

{"cd":"11060870","nm_kor":"장안1동","nm_eng":"Jangan 1(il)-dong"},

{"cd":"11060880","nm_kor":"장안2동","nm_eng":"Jangan 2(i)-dong"},

{"cd":"11060800","nm_kor":"청량리동","nm_eng":"Cheongnyangni-dong"},

{"cd":"11060710","nm_kor":"회기동","nm_eng":"Hoegi-dong"},

{"cd":"11060720","nm_kor":"휘경1동","nm_eng":"Hwigyeong 1(il)-dong"},

{"cd":"11060730","nm_kor":"휘경2동","nm_eng":"Hwigyeong 2(i)-dong"},

{"cd":"11060890","nm_kor":"이문1동","nm_eng":"Imun 1(il)-dong"},

{"cd":"11060900","nm_kor":"이문2동","nm_eng":"Imun 2(i)-dong"},

{"cd":"11070000","nm_kor":"중랑구","nm_eng":"Jungnang-gu"},

{"cd":"11070520","nm_kor":"면목2동","nm_eng":"Myeonmok 2(i)-dong"},

{"cd":"11070540","nm_kor":"면목4동","nm_eng":"Myeonmok 4(sa)-dong"},

{"cd":"11070550","nm_kor":"면목5동","nm_eng":"Myeonmok 5(o)-dong"},

{"cd":"11070710","nm_kor":"면목본동","nm_eng":"Myeonmokbon-dong"},

{"cd":"11070570","nm_kor":"면목7동","nm_eng":"Myeonmok 7(chil)-dong"},

{"cd":"11070720","nm_kor":"면목3.8동","nm_eng":"Myeonmok 3.8(sampal)-dong"},

{"cd":"11070590","nm_kor":"상봉1동","nm_eng":"Sangbong 1(il)-dong"},

{"cd":"11070600","nm_kor":"상봉2동","nm_eng":"Sangbong 2(i)-dong"},

{"cd":"11070610","nm_kor":"중화1동","nm_eng":"Junghwa 1(il)-dong"},

{"cd":"11070620","nm_kor":"중화2동","nm_eng":"Junghwa 2(i)-dong"},

{"cd":"11070640","nm_kor":"묵1동","nm_eng":"Muk 1(il)-dong"},

{"cd":"11070650","nm_kor":"묵2동","nm_eng":"Muk 2(i)-dong"},

{"cd":"11070730","nm_kor":"망우본동","nm_eng":"Mangubon-dong"},

{"cd":"11070680","nm_kor":"망우3동","nm_eng":"Mangu 3(sam)-dong"},

{"cd":"11070690","nm_kor":"신내1동","nm_eng":"Sinnae 1(il)-dong"},

{"cd":"11070700","nm_kor":"신내2동","nm_eng":"Sinnae 2(i)-dong"},

{"cd":"11080000","nm_kor":"성북구","nm_eng":"Seongbuk-gu"},

{"cd":"11080810","nm_kor":"성북동","nm_eng":"Seongbuk-dong"},

{"cd":"11080820","nm_kor":"삼선동","nm_eng":"Samseon-dong"},

{"cd":"11080830","nm_kor":"동선동","nm_eng":"Dongseon-dong"},

{"cd":"11080580","nm_kor":"돈암1동","nm_eng":"Donam 1(il)-dong"},

{"cd":"11080590","nm_kor":"돈암2동","nm_eng":"Donam 2(i)-dong"},

{"cd":"11080600","nm_kor":"안암동","nm_eng":"Anam-dong"},

{"cd":"11080610","nm_kor":"보문동","nm_eng":"Bomun-dong"},

{"cd":"11080620","nm_kor":"정릉1동","nm_eng":"Jeongneung 1(il)-dong"},

{"cd":"11080630","nm_kor":"정릉2동","nm_eng":"Jeongneung 2(i)-dong"},

{"cd":"11080640","nm_kor":"정릉3동","nm_eng":"Jeongneung 3(sam)-dong"},

{"cd":"11080650","nm_kor":"정릉4동","nm_eng":"Jeongneung 4(sa)-dong"},

{"cd":"11080660","nm_kor":"길음1동","nm_eng":"Gireum 1(il)-dong"},

{"cd":"11080680","nm_kor":"길음2동","nm_eng":"Gireum 2(i)-dong"},

{"cd":"11080840","nm_kor":"종암동","nm_eng":"Jongam-dong"},

{"cd":"11080710","nm_kor":"월곡1동","nm_eng":"Wolgok 1(il)-dong"},

{"cd":"11080720","nm_kor":"월곡2동","nm_eng":"Wolgok 2(i)-dong"},

{"cd":"11080760","nm_kor":"장위1동","nm_eng":"Jangwi 1(il)-dong"},

{"cd":"11080770","nm_kor":"장위2동","nm_eng":"Jangwi 2(i)-dong"},

{"cd":"11080780","nm_kor":"장위3동","nm_eng":"Jangwi 3(sam)-dong"},

{"cd":"11080850","nm_kor":"석관동","nm_eng":"Seokgwan-dong"},

{"cd":"11090000","nm_kor":"강북구","nm_eng":"Gangbuk-gu"},

{"cd":"11090690","nm_kor":"삼양동","nm_eng":"Samyang-dong"},

{"cd":"11090700","nm_kor":"미아동","nm_eng":"Mia-dong"},

{"cd":"11090710","nm_kor":"송중동","nm_eng":"Songjung-dong"},

{"cd":"11090720","nm_kor":"송천동","nm_eng":"Songcheon-dong"},

{"cd":"11090730","nm_kor":"삼각산동","nm_eng":"Samgaksan-dong"},

{"cd":"11090600","nm_kor":"번1동","nm_eng":"Beon 1(il)-dong"},

{"cd":"11090610","nm_kor":"번2동","nm_eng":"Beon 2(i)-dong"},

{"cd":"11090620","nm_kor":"번3동","nm_eng":"Beon 3(sam)-dong"},

{"cd":"11090630","nm_kor":"수유1동","nm_eng":"Suyu 1(il)-dong"},

{"cd":"11090640","nm_kor":"수유2동","nm_eng":"Suyu 2(i)-dong"},

{"cd":"11090650","nm_kor":"수유3동","nm_eng":"Suyu 3(sam)-dong"},

{"cd":"11090740","nm_kor":"우이동","nm_eng":"Ui-dong"},

{"cd":"11090750","nm_kor":"인수동","nm_eng":"Insu-dong"},

{"cd":"11100000","nm_kor":"도봉구","nm_eng":"Dobong-gu"},

{"cd":"11100590","nm_kor":"창1동","nm_eng":"Chang 1(il)-dong"},

{"cd":"11100600","nm_kor":"창2동","nm_eng":"Chang 2(i)-dong"},

{"cd":"11100610","nm_kor":"창3동","nm_eng":"Chang 3(sam)-dong"},

{"cd":"11100620","nm_kor":"창4동","nm_eng":"Chang 4(sa)-dong"},

{"cd":"11100630","nm_kor":"창5동","nm_eng":"Chang 5(o)-dong"},

{"cd":"11100640","nm_kor":"도봉1동","nm_eng":"Dobong 1(il)-dong"},

{"cd":"11100650","nm_kor":"도봉2동","nm_eng":"Dobong 2(i)-dong"},

{"cd":"11100510","nm_kor":"쌍문1동","nm_eng":"Ssangmun 1(il)-dong"},

{"cd":"11100520","nm_kor":"쌍문2동","nm_eng":"Ssangmun 2(i)-dong"},

{"cd":"11100530","nm_kor":"쌍문3동","nm_eng":"Ssangmun 3(sam)-dong"},

{"cd":"11100540","nm_kor":"쌍문4동","nm_eng":"Ssangmun 4(sa)-dong"},

{"cd":"11100550","nm_kor":"방학1동","nm_eng":"Banghak 1(il)-dong"},

{"cd":"11100560","nm_kor":"방학2동","nm_eng":"Banghak 2(i)-dong"},

{"cd":"11100570","nm_kor":"방학3동","nm_eng":"Banghak 3(sam)-dong"},

{"cd":"11110000","nm_kor":"노원구","nm_eng":"Nowon-gu"},

{"cd":"11110510","nm_kor":"월계1동","nm_eng":"Wolgye 1(il)-dong"},

{"cd":"11110520","nm_kor":"월계2동","nm_eng":"Wolgye 2(i)-dong"},

{"cd":"11110530","nm_kor":"월계3동","nm_eng":"Wolgye 3(sam)-dong"},

{"cd":"11110790","nm_kor":"공릉1동","nm_eng":"Gongneung 1(il)-dong"},

{"cd":"11110560","nm_kor":"공릉2동","nm_eng":"Gongneung 2(i)-dong"},

{"cd":"11110580","nm_kor":"하계1동","nm_eng":"Hagye 1(il)-dong"},

{"cd":"11110590","nm_kor":"하계2동","nm_eng":"Hagye 2(i)-dong"},

{"cd":"11110600","nm_kor":"중계본동","nm_eng":"Junggyebon-dong"},

{"cd":"11110610","nm_kor":"중계1동","nm_eng":"Junggye 1(il)-dong"},

{"cd":"11110640","nm_kor":"중계4동","nm_eng":"Junggye 4(sa)-dong"},

{"cd":"11110780","nm_kor":"중계2.3동","nm_eng":"Junggye 2.3(isam)-dong"},

{"cd":"11110650","nm_kor":"상계1동","nm_eng":"Sanggye 1(il)-dong"},

{"cd":"11110660","nm_kor":"상계2동","nm_eng":"Sanggye 2(i)-dong"},

{"cd":"11110760","nm_kor":"상계3.4동","nm_eng":"Sanggye 3.4(samsa)-dong"},

{"cd":"11110690","nm_kor":"상계5동","nm_eng":"Sanggye 5(o)-dong"},

{"cd":"11110770","nm_kor":"상계6.7동","nm_eng":"Sanggye 6.7(yukchil)-dong"},

{"cd":"11110720","nm_kor":"상계8동","nm_eng":"Sanggye 8(pal)-dong"},

{"cd":"11110730","nm_kor":"상계9동","nm_eng":"Sanggye 9(gu)-dong"},

{"cd":"11110740","nm_kor":"상계10동","nm_eng":"Sanggye 10(sip)-dong"},

{"cd":"11120000","nm_kor":"은평구","nm_eng":"Eunpyeong-gu"},

{"cd":"11120510","nm_kor":"녹번동","nm_eng":"Nokbeon-dong"},

{"cd":"11120520","nm_kor":"불광1동","nm_eng":"Bulgwang 1(il)-dong"},

{"cd":"11120720","nm_kor":"불광2동","nm_eng":"Bulgwang 2(i)-dong"},

{"cd":"11120550","nm_kor":"갈현1동","nm_eng":"Galhyeon 1(il)-dong"},

{"cd":"11120560","nm_kor":"갈현2동","nm_eng":"Galhyeon 2(i)-dong"},

{"cd":"11120570","nm_kor":"구산동","nm_eng":"Gusan-dong"},

{"cd":"11120580","nm_kor":"대조동","nm_eng":"Daejo-dong"},

{"cd":"11120590","nm_kor":"응암1동","nm_eng":"Eungam 1(il)-dong"},

{"cd":"11120600","nm_kor":"응암2동","nm_eng":"Eungam 2(i)-dong"},

{"cd":"11120730","nm_kor":"응암3동","nm_eng":"Eungam 3(sam)-dong"},

{"cd":"11120740","nm_kor":"역촌동","nm_eng":"Yeokchon-dong"},

{"cd":"11120650","nm_kor":"신사1동","nm_eng":"Sinsa 1(il)-dong"},

{"cd":"11120660","nm_kor":"신사2동","nm_eng":"Sinsa 2(i)-dong"},

{"cd":"11120670","nm_kor":"증산동","nm_eng":"Jeungsan-dong"},

{"cd":"11120680","nm_kor":"수색동","nm_eng":"Susaek-dong"},

{"cd":"11120710","nm_kor":"진관동","nm_eng":"Jingwan-dong"},

{"cd":"11130000","nm_kor":"서대문구","nm_eng":"Seodaemun-gu"},

{"cd":"11130520","nm_kor":"천연동","nm_eng":"Cheonyeon-dong"},

{"cd":"11130740","nm_kor":"북아현동","nm_eng":"Bugahyeon-dong"},

{"cd":"11130730","nm_kor":"충현동","nm_eng":"Chunghyeon-dong"},

{"cd":"11130750","nm_kor":"신촌동","nm_eng":"Sinchon-dong"},

{"cd":"11130760","nm_kor":"연희동","nm_eng":"Yeonhui-dong"},

{"cd":"11130620","nm_kor":"홍제1동","nm_eng":"Hongje 1(il)-dong"},

{"cd":"11130640","nm_kor":"홍제3동","nm_eng":"Hongje 3(sam)-dong"},

{"cd":"11130650","nm_kor":"홍제2동","nm_eng":"Hongje 2(i)-dong"},

{"cd":"11130660","nm_kor":"홍은1동","nm_eng":"Hongeun 1(il)-dong"},

{"cd":"11130680","nm_kor":"홍은2동","nm_eng":"Hongeun 2(i)-dong"},

{"cd":"11130690","nm_kor":"남가좌1동","nm_eng":"Namgajwa 1(il)-dong"},

{"cd":"11130700","nm_kor":"남가좌2동","nm_eng":"Namgajwa 2(i)-dong"},

{"cd":"11130710","nm_kor":"북가좌1동","nm_eng":"Bukgajwa 1(il)-dong"},

{"cd":"11130720","nm_kor":"북가좌2동","nm_eng":"Bukgajwa 2(i)-dong"},

{"cd":"11140000","nm_kor":"마포구","nm_eng":"Mapo-gu"},

{"cd":"11140780","nm_kor":"아현동","nm_eng":"Ahyeon-dong"},

{"cd":"11140770","nm_kor":"공덕동","nm_eng":"gongdeok-dong"},

{"cd":"11140750","nm_kor":"도화동","nm_eng":"Dohwa-dong"},

{"cd":"11140590","nm_kor":"용강동","nm_eng":"Yonggang-dong"},

{"cd":"11140600","nm_kor":"대흥동","nm_eng":"Daeheung-dong"},

{"cd":"11140610","nm_kor":"염리동","nm_eng":"Yeomni-dong"},

{"cd":"11140630","nm_kor":"신수동","nm_eng":"Sinsu-dong"},

{"cd":"11140760","nm_kor":"서강동","nm_eng":"Seogang-dong"},

{"cd":"11140660","nm_kor":"서교동","nm_eng":"Seogyo-dong"},

{"cd":"11140680","nm_kor":"합정동","nm_eng":"Hapjeong-dong"},

{"cd":"11140690","nm_kor":"망원1동","nm_eng":"Mangwon 1(il)-dong"},

{"cd":"11140700","nm_kor":"망원2동","nm_eng":"Mangwon 2(i)-dong"},

{"cd":"11140710","nm_kor":"연남동","nm_eng":"Yeonnam-dong"},

{"cd":"11140720","nm_kor":"성산1동","nm_eng":"Seongsan 1(il)-dong"},

{"cd":"11140730","nm_kor":"성산2동","nm_eng":"Seongsan 2(i)-dong"},

{"cd":"11140740","nm_kor":"상암동","nm_eng":"Sangam-dong"},

{"cd":"11150000","nm_kor":"양천구","nm_eng":"Yangcheon-gu"},

{"cd":"11150510","nm_kor":"목1동","nm_eng":"Mok 1(il)-dong"},

{"cd":"11150520","nm_kor":"목2동","nm_eng":"Mok 2(i)-dong"},

{"cd":"11150530","nm_kor":"목3동","nm_eng":"Mok 3(sam)-dong"},

{"cd":"11150540","nm_kor":"목4동","nm_eng":"Mok 4(sa)-dong"},

{"cd":"11150710","nm_kor":"목5동","nm_eng":"Mok 5(o)-dong"},

{"cd":"11150570","nm_kor":"신월1동","nm_eng":"Sinwol 1(il)-dong"},

{"cd":"11150580","nm_kor":"신월2동","nm_eng":"Sinwol 2(i)-dong"},

{"cd":"11150590","nm_kor":"신월3동","nm_eng":"Sinwol 3(sam)-dong"},

{"cd":"11150600","nm_kor":"신월4동","nm_eng":"Sinwol 4(sa)-dong"},

{"cd":"11150610","nm_kor":"신월5동","nm_eng":"Sinwol 5(o)-dong"},

{"cd":"11150620","nm_kor":"신월6동","nm_eng":"Sinwol 6(yuk)-dong"},

{"cd":"11150630","nm_kor":"신월7동","nm_eng":"Sinwol 7(chil)-dong"},

{"cd":"11150640","nm_kor":"신정1동","nm_eng":"Sinjeong 1(il)-dong"},

{"cd":"11150650","nm_kor":"신정2동","nm_eng":"Sinjeong 2(i)-dong"},

{"cd":"11150660","nm_kor":"신정3동","nm_eng":"Sinjeong 3(sam)-dong"},

{"cd":"11150720","nm_kor":"신정4동","nm_eng":"Sinjeong 4(sa)-dong"},

{"cd":"11150690","nm_kor":"신정6동","nm_eng":"Sinjeong 6(yuk)-dong"},

{"cd":"11150700","nm_kor":"신정7동","nm_eng":"Sinjeong 7(chil)-dong"},

{"cd":"11160000","nm_kor":"강서구","nm_eng":"Gangseo-gu"},

{"cd":"11160510","nm_kor":"염창동","nm_eng":"Yeomchang-dong"},

{"cd":"11160520","nm_kor":"등촌1동","nm_eng":"Deungchon 1(il)-dong"},

{"cd":"11160530","nm_kor":"등촌2동","nm_eng":"Deungchon 2(i)-dong"},

{"cd":"11160540","nm_kor":"등촌3동","nm_eng":"Deungchon 3(sam)-dong"},

{"cd":"11160730","nm_kor":"화곡1동","nm_eng":"Hwagok 1(il)-dong"},

{"cd":"11160570","nm_kor":"화곡2동","nm_eng":"Hwagok 2(i)-dong"},

{"cd":"11160580","nm_kor":"화곡3동","nm_eng":"Hwagok 3(sam)-dong"},

{"cd":"11160590","nm_kor":"화곡4동","nm_eng":"Hwagok 4(sa)-dong"},

{"cd":"11160550","nm_kor":"화곡본동","nm_eng":"Hwagokbon-dong"},

{"cd":"11160610","nm_kor":"화곡6동","nm_eng":"Hwagok 6(yuk)-dong"},

{"cd":"11160630","nm_kor":"화곡8동","nm_eng":"Hwagok 8(pal)-dong"},

{"cd":"11160640","nm_kor":"가양1동","nm_eng":"Gayang 1(il)-dong"},

{"cd":"11160650","nm_kor":"가양2동","nm_eng":"Gayang 2(i)-dong"},

{"cd":"11160660","nm_kor":"가양3동","nm_eng":"Gayang 3(sam)-dong"},

{"cd":"11160670","nm_kor":"발산1동","nm_eng":"Balsan 1(il)-dong"},

{"cd":"11160740","nm_kor":"우장산동","nm_eng":"Ujangsan-dong"},

{"cd":"11160690","nm_kor":"공항동","nm_eng":"Gonghang-dong"},

{"cd":"11160700","nm_kor":"방화1동","nm_eng":"Banghwa 1(il)-dong"},

{"cd":"11160710","nm_kor":"방화2동","nm_eng":"Banghwa 2(i)-dong"},

{"cd":"11160720","nm_kor":"방화3동","nm_eng":"Banghwa 3(sam)-dong"},

{"cd":"11170000","nm_kor":"구로구","nm_eng":"Guro-gu"},

{"cd":"11170510","nm_kor":"신도림동","nm_eng":"Sindorim-dong"},

{"cd":"11170520","nm_kor":"구로1동","nm_eng":"Guro 1(il)-dong"},

{"cd":"11170710","nm_kor":"구로2동","nm_eng":"Guro 2(i)-dong"},

{"cd":"11170540","nm_kor":"구로3동","nm_eng":"Guro 3(sam)-dong"},

{"cd":"11170550","nm_kor":"구로4동","nm_eng":"Guro 4(sa)-dong"},

{"cd":"11170560","nm_kor":"구로5동","nm_eng":"Guro 5(o)-dong"},

{"cd":"11170700","nm_kor":"가리봉동","nm_eng":"Garibong-dong"},

{"cd":"11170610","nm_kor":"고척1동","nm_eng":"Gocheok 1(il)-dong"},

{"cd":"11170620","nm_kor":"고척2동","nm_eng":"Gocheok 2(i)-dong"},

{"cd":"11170720","nm_kor":"개봉1동","nm_eng":"Gaebong 1(il)-dong"},

{"cd":"11170640","nm_kor":"개봉2동","nm_eng":"Gaebong 2(i)-dong"},

{"cd":"11170650","nm_kor":"개봉3동","nm_eng":"Gaebong 3(sam)-dong"},

{"cd":"11170670","nm_kor":"오류1동","nm_eng":"Oryu 1(il)-dong"},

{"cd":"11170730","nm_kor":"오류2동","nm_eng":"Oryu 2(i)-dong"},

{"cd":"11170690","nm_kor":"수궁동","nm_eng":"Sugung-dong"},

{"cd":"11170740","nm_kor":"항동","nm_eng":"Hang-dong"},

{"cd":"11180000","nm_kor":"금천구","nm_eng":"Geumcheon-gu"},

{"cd":"11180510","nm_kor":"가산동","nm_eng":"Gasan-dong"},

{"cd":"11180520","nm_kor":"독산1동","nm_eng":"Doksan 1(il)-dong"},

{"cd":"11180530","nm_kor":"독산2동","nm_eng":"Doksan 2(i)-dong"},

{"cd":"11180540","nm_kor":"독산3동","nm_eng":"Doksan 3(sam)-dong"},

{"cd":"11180550","nm_kor":"독산4동","nm_eng":"Doksan 4(sa)-dong"},

{"cd":"11180570","nm_kor":"시흥1동","nm_eng":"Siheung 1(il)-dong"},

{"cd":"11180580","nm_kor":"시흥2동","nm_eng":"Siheung 2(i)-dong"},

{"cd":"11180590","nm_kor":"시흥3동","nm_eng":"Siheung 3(sam)-dong"},

{"cd":"11180600","nm_kor":"시흥4동","nm_eng":"Siheung 4(sa)-dong"},

{"cd":"11180610","nm_kor":"시흥5동","nm_eng":"Siheung 5(o)-dong"},

{"cd":"11190000","nm_kor":"영등포구","nm_eng":"Yeongdeungpo-gu"},

{"cd":"11190730","nm_kor":"영등포본동","nm_eng":"Yeongdeungpobon-dong"},

{"cd":"11190740","nm_kor":"영등포동","nm_eng":"Yeongdeungpo-dong"},

{"cd":"11190540","nm_kor":"여의동","nm_eng":"Yeoui-dong"},

{"cd":"11190550","nm_kor":"당산1동","nm_eng":"Dangsan 1(il)-dong"},

{"cd":"11190560","nm_kor":"당산2동","nm_eng":"Dangsan 2(i)-dong"},

{"cd":"11190750","nm_kor":"도림동","nm_eng":"Dorim-dong"},

{"cd":"11190760","nm_kor":"문래동","nm_eng":"Mullae-dong"},

{"cd":"11190610","nm_kor":"양평1동","nm_eng":"Yangpyeong 1(il)-dong"},

{"cd":"11190620","nm_kor":"양평2동","nm_eng":"Yangpyeong 2(i)-dong"},

{"cd":"11190630","nm_kor":"신길1동","nm_eng":"Singil 1(il)-dong"},

{"cd":"11190650","nm_kor":"신길3동","nm_eng":"Singil 3(sam)-dong"},

{"cd":"11190660","nm_kor":"신길4동","nm_eng":"Singil 4(sa)-dong"},

{"cd":"11190670","nm_kor":"신길5동","nm_eng":"Singil 5(o)-dong"},

{"cd":"11190680","nm_kor":"신길6동","nm_eng":"Singil 6(yuk)-dong"},

{"cd":"11190690","nm_kor":"신길7동","nm_eng":"Singil 7(chil)-dong"},

{"cd":"11190700","nm_kor":"대림1동","nm_eng":"Daerim 1(il)-dong"},

{"cd":"11190710","nm_kor":"대림2동","nm_eng":"Daerim 2(i)-dong"},

{"cd":"11190720","nm_kor":"대림3동","nm_eng":"Daerim 3(sam)-dong"},

{"cd":"11200000","nm_kor":"동작구","nm_eng":"Dongjak-gu"},

{"cd":"11200720","nm_kor":"노량진1동","nm_eng":"Noryangjin 1(il)-dong"},

{"cd":"11200520","nm_kor":"노량진2동","nm_eng":"Noryangjin 2(i)-dong"},

{"cd":"11200530","nm_kor":"상도1동","nm_eng":"Sangdo 1(il)-dong"},

{"cd":"11200540","nm_kor":"상도2동","nm_eng":"Sangdo 2(i)-dong"},

{"cd":"11200550","nm_kor":"상도3동","nm_eng":"Sangdo 3(sam)-dong"},

{"cd":"11200560","nm_kor":"상도4동","nm_eng":"Sangdo 4(sa)-dong"},

{"cd":"11200710","nm_kor":"흑석동","nm_eng":"Heukseok-dong"},

{"cd":"11200630","nm_kor":"사당1동","nm_eng":"Sadang 1(il)-dong"},

{"cd":"11200730","nm_kor":"사당2동","nm_eng":"Sadang 2(i)-dong"},

{"cd":"11200650","nm_kor":"사당3동","nm_eng":"Sadang 3(sam)-dong"},

{"cd":"11200660","nm_kor":"사당4동","nm_eng":"Sadang 4(sa)-dong"},

{"cd":"11200670","nm_kor":"사당5동","nm_eng":"Sadang 5(o)-dong"},

{"cd":"11200680","nm_kor":"대방동","nm_eng":"Daebang-dong"},

{"cd":"11200690","nm_kor":"신대방1동","nm_eng":"Sindaebang 1(il)-dong"},

{"cd":"11200700","nm_kor":"신대방2동","nm_eng":"Sindaebang 2(i)-dong"},

{"cd":"11210000","nm_kor":"관악구","nm_eng":"Gwanak-gu"},

{"cd":"11210520","nm_kor":"보라매동","nm_eng":"Boramae-dong"},

{"cd":"11210540","nm_kor":"청림동","nm_eng":"Cheongnim-dong"},

{"cd":"11210790","nm_kor":"성현동","nm_eng":"Seonghyeon-dong"},

{"cd":"11210570","nm_kor":"행운동","nm_eng":"Haengun-dong"},

{"cd":"11210580","nm_kor":"낙성대동","nm_eng":"Nagseongdae-dong"},

{"cd":"11210800","nm_kor":"청룡동","nm_eng":"Cheongnyong-dong"},

{"cd":"11210780","nm_kor":"은천동","nm_eng":"Euncheon-dong"},

{"cd":"11210610","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"11210620","nm_kor":"인헌동","nm_eng":"Inheon-dong"},

{"cd":"11210630","nm_kor":"남현동","nm_eng":"Namhyeon-dong"},

{"cd":"11210640","nm_kor":"서원동","nm_eng":"Sewon-dong"},

{"cd":"11210650","nm_kor":"신원동","nm_eng":"Sinwon-dong"},

{"cd":"11210660","nm_kor":"서림동","nm_eng":"Serim-dong"},

{"cd":"11210680","nm_kor":"신사동","nm_eng":"Sinsa-dong"},

{"cd":"11210690","nm_kor":"신림동","nm_eng":"Sillim-dong"},

{"cd":"11210710","nm_kor":"난향동","nm_eng":"Nanhyang-dong"},

{"cd":"11210720","nm_kor":"조원동","nm_eng":"Jowon-dong"},

{"cd":"11210730","nm_kor":"대학동","nm_eng":"Daehak-dong"},

{"cd":"11210820","nm_kor":"삼성동","nm_eng":"Samseong-dong"},

{"cd":"11210830","nm_kor":"미성동","nm_eng":"Miseong-dong"},

{"cd":"11210810","nm_kor":"난곡동","nm_eng":"Nangok-dong"},

{"cd":"11220000","nm_kor":"서초구","nm_eng":"Seocho-gu"},

{"cd":"11220510","nm_kor":"서초1동","nm_eng":"Seocho 1(il)-dong"},

{"cd":"11220520","nm_kor":"서초2동","nm_eng":"Seocho 2(i)-dong"},

{"cd":"11220530","nm_kor":"서초3동","nm_eng":"Seocho 3(sam)-dong"},

{"cd":"11220540","nm_kor":"서초4동","nm_eng":"Seocho 4(sa)-dong"},

{"cd":"11220550","nm_kor":"잠원동","nm_eng":"Jamwon-dong"},

{"cd":"11220560","nm_kor":"반포본동","nm_eng":"Banpobon-dong"},

{"cd":"11220570","nm_kor":"반포1동","nm_eng":"Banpo 1(il)-dong"},

{"cd":"11220580","nm_kor":"반포2동","nm_eng":"Banpo 2(i)-dong"},

{"cd":"11220590","nm_kor":"반포3동","nm_eng":"Banpo 3(sam)-dong"},

{"cd":"11220600","nm_kor":"반포4동","nm_eng":"Banpo 4(sa)-dong"},

{"cd":"11220610","nm_kor":"방배본동","nm_eng":"Bangbaebon-dong"},

{"cd":"11220620","nm_kor":"방배1동","nm_eng":"Bangbae 1(il)-dong"},

{"cd":"11220630","nm_kor":"방배2동","nm_eng":"Bangbae 2(i)-dong"},

{"cd":"11220640","nm_kor":"방배3동","nm_eng":"Bangbae 3(sam)-dong"},

{"cd":"11220650","nm_kor":"방배4동","nm_eng":"Bangbae 4(sa)-dong"},

{"cd":"11220660","nm_kor":"양재1동","nm_eng":"Yangjae 1(il)-dong"},

{"cd":"11220670","nm_kor":"양재2동","nm_eng":"Yangjae 2(i)-dong"},

{"cd":"11220680","nm_kor":"내곡동","nm_eng":"Naegok-dong"},

{"cd":"11230000","nm_kor":"강남구","nm_eng":"Gangnam-gu"},

{"cd":"11230510","nm_kor":"신사동","nm_eng":"Sinsa-dong"},

{"cd":"11230520","nm_kor":"논현1동","nm_eng":"Nonhyeon 1(il)-dong"},

{"cd":"11230530","nm_kor":"논현2동","nm_eng":"Nonhyeon 2(i)-dong"},

{"cd":"11230770","nm_kor":"압구정동","nm_eng":"Apgujeong-dong"},

{"cd":"11230780","nm_kor":"청담동","nm_eng":"Cheongdam-dong"},

{"cd":"11230580","nm_kor":"삼성1동","nm_eng":"Samseong 1(il)-dong"},

{"cd":"11230590","nm_kor":"삼성2동","nm_eng":"Samseong 2(i)-dong"},

{"cd":"11230600","nm_kor":"대치1동","nm_eng":"Daechi 1(il)-dong"},

{"cd":"11230790","nm_kor":"대치2동","nm_eng":"Daechi 2(i)-dong"},

{"cd":"11230630","nm_kor":"대치4동","nm_eng":"Daechi 4(sa)-dong"},

{"cd":"11230640","nm_kor":"역삼1동","nm_eng":"Yeoksam 1(il)-dong"},

{"cd":"11230650","nm_kor":"역삼2동","nm_eng":"Yeoksam 2(i)-dong"},

{"cd":"11230660","nm_kor":"도곡1동","nm_eng":"Dogok 1(il)-dong"},

{"cd":"11230670","nm_kor":"도곡2동","nm_eng":"Dogok 2(i)-dong"},

{"cd":"11230680","nm_kor":"개포1동","nm_eng":"Gaepo 1(il)-dong"},

{"cd":"11230800","nm_kor":"개포2동","nm_eng":"Gaepo 2(i)-dong"},

{"cd":"11230710","nm_kor":"개포4동","nm_eng":"Gaepo 4(sa)-dong"},

{"cd":"11230760","nm_kor":"세곡동","nm_eng":"Segok-dong"},

{"cd":"11230720","nm_kor":"일원본동","nm_eng":"Irwonbon-dong"},

{"cd":"11230730","nm_kor":"일원1동","nm_eng":"Irwon 1(il)-dong"},

{"cd":"11230740","nm_kor":"일원2동","nm_eng":"Irwon 2(i)-dong"},

{"cd":"11230750","nm_kor":"수서동","nm_eng":"Suseo-dong"},

{"cd":"11240000","nm_kor":"송파구","nm_eng":"Songpa-gu"},

{"cd":"11240510","nm_kor":"풍납1동","nm_eng":"Pungnap 1(il)-dong"},

{"cd":"11240520","nm_kor":"풍납2동","nm_eng":"Pungnap 2(i)-dong"},

{"cd":"11240530","nm_kor":"거여1동","nm_eng":"Geoyeo 1(il)-dong"},

{"cd":"11240540","nm_kor":"거여2동","nm_eng":"Geoyeo 2(i)-dong"},

{"cd":"11240550","nm_kor":"마천1동","nm_eng":"Macheon 1(il)-dong"},

{"cd":"11240560","nm_kor":"마천2동","nm_eng":"Macheon 2(i)-dong"},

{"cd":"11240570","nm_kor":"방이1동","nm_eng":"Bangi 1(il)-dong"},

{"cd":"11240580","nm_kor":"방이2동","nm_eng":"Bangi 2(i)-dong"},

{"cd":"11240590","nm_kor":"오륜동","nm_eng":"Oryun-dong"},

{"cd":"11240600","nm_kor":"오금동","nm_eng":"Ogeum-dong"},

{"cd":"11240610","nm_kor":"송파1동","nm_eng":"Songpa 1(il)-dong"},

{"cd":"11240620","nm_kor":"송파2동","nm_eng":"Songpa 2(i)-dong"},

{"cd":"11240630","nm_kor":"석촌동","nm_eng":"Seokchon-dong"},

{"cd":"11240640","nm_kor":"삼전동","nm_eng":"Samjeon-dong"},

{"cd":"11240650","nm_kor":"가락본동","nm_eng":"Garakbon-dong"},

{"cd":"11240660","nm_kor":"가락1동","nm_eng":"Garak 1(il)-dong"},

{"cd":"11240670","nm_kor":"가락2동","nm_eng":"Garak 2(i)-dong"},

{"cd":"11240680","nm_kor":"문정1동","nm_eng":"Munjeong 1(il)-dong"},

{"cd":"11240690","nm_kor":"문정2동","nm_eng":"Munjeong 2(i)-dong"},

{"cd":"11240810","nm_kor":"장지동","nm_eng":"Jangji-dong"},

{"cd":"11240820","nm_kor":"위례동","nm_eng":"wirye-dong"},

{"cd":"11240710","nm_kor":"잠실본동","nm_eng":"Jamsilbon-dong"},

{"cd":"11240790","nm_kor":"잠실2동","nm_eng":"Jamsil 2(i)-dong"},

{"cd":"11240800","nm_kor":"잠실3동","nm_eng":"Jamsil 3(sam)-dong"},

{"cd":"11240750","nm_kor":"잠실4동","nm_eng":"Jamsil 4(sa)-dong"},

{"cd":"11240770","nm_kor":"잠실6동","nm_eng":"Jamsil 6(yuk)-dong"},

{"cd":"11240780","nm_kor":"잠실7동","nm_eng":"Jamsil 7(chil)-dong"},

{"cd":"11250000","nm_kor":"강동구","nm_eng":"Gangdong-gu"},

{"cd":"11250750","nm_kor":"강일동","nm_eng":"Gangil-dong"},

{"cd":"11250760","nm_kor":"상일1동","nm_eng":"Sangil 1(il)-dong"},

{"cd":"11250770","nm_kor":"상일2동","nm_eng":"Sangil 2(i)-dong"},

{"cd":"11250530","nm_kor":"명일1동","nm_eng":"Myeongil 1(il)-dong"},

{"cd":"11250540","nm_kor":"명일2동","nm_eng":"Myeongil 2(i)-dong"},

{"cd":"11250550","nm_kor":"고덕1동","nm_eng":"Godeok 1(il)-dong"},

{"cd":"11250560","nm_kor":"고덕2동","nm_eng":"Godeok 2(i)-dong"},

{"cd":"11250720","nm_kor":"암사1동","nm_eng":"Amsa 1(il)-dong"},

{"cd":"11250580","nm_kor":"암사2동","nm_eng":"Amsa 2(i)-dong"},

{"cd":"11250590","nm_kor":"암사3동","nm_eng":"Amsa 3(sam)-dong"},

{"cd":"11250610","nm_kor":"천호1동","nm_eng":"Cheonho 1(il)-dong"},

{"cd":"11250730","nm_kor":"천호2동","nm_eng":"Cheonho 2(i)-dong"},

{"cd":"11250630","nm_kor":"천호3동","nm_eng":"Cheonho 3(sam)-dong"},

{"cd":"11250650","nm_kor":"성내1동","nm_eng":"Seongnae 1(il)-dong"},

{"cd":"11250660","nm_kor":"성내2동","nm_eng":"Seongnae 2(i)-dong"},

{"cd":"11250670","nm_kor":"성내3동","nm_eng":"Seongnae 3(sam)-dong"},

{"cd":"11250740","nm_kor":"길동","nm_eng":"Gil-dong"},

{"cd":"11250700","nm_kor":"둔촌1동","nm_eng":"Dunchon 1(il)-dong"},

{"cd":"11250710","nm_kor":"둔촌2동","nm_eng":"Dunchon 2(i)-dong"},

{"cd":"21000000","nm_kor":"부산광역시","nm_eng":"Busan"},

{"cd":"21010000","nm_kor":"중구","nm_eng":"Jung-gu"},

{"cd":"21010510","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"21010520","nm_kor":"동광동","nm_eng":"Donggwang-dong"},

{"cd":"21010530","nm_kor":"대청동","nm_eng":"Daecheong-dong"},

{"cd":"21010540","nm_kor":"보수동","nm_eng":"Bosu-dong"},

{"cd":"21010560","nm_kor":"부평동","nm_eng":"Bupyeong-dong"},

{"cd":"21010570","nm_kor":"광복동","nm_eng":"Gwangbok-dong"},

{"cd":"21010580","nm_kor":"남포동","nm_eng":"Nampo-dong"},

{"cd":"21010590","nm_kor":"영주1동","nm_eng":"Yeongju 1(il)-dong"},

{"cd":"21010600","nm_kor":"영주2동","nm_eng":"Yeongju 2(i)-dong"},

{"cd":"21020000","nm_kor":"서구","nm_eng":"Seo-gu"},

{"cd":"21020510","nm_kor":"동대신1동","nm_eng":"Dongdaesin 1(il)-dong"},

{"cd":"21020520","nm_kor":"동대신2동","nm_eng":"Dongdaesin 2(i)-dong"},

{"cd":"21020530","nm_kor":"동대신3동","nm_eng":"Dongdaesin 3(sam)-dong"},

{"cd":"21020540","nm_kor":"서대신1동","nm_eng":"Seodaesin 1(il)-dong"},

{"cd":"21020560","nm_kor":"서대신3동","nm_eng":"Seodaesin 3(sam)-dong"},

{"cd":"21020570","nm_kor":"서대신4동","nm_eng":"Seodaesin 4(sa)-dong"},

{"cd":"21020590","nm_kor":"부민동","nm_eng":"Bumin-dong"},

{"cd":"21020610","nm_kor":"아미동","nm_eng":"Ami-dong"},

{"cd":"21020630","nm_kor":"초장동","nm_eng":"Chojang-dong"},

{"cd":"21020640","nm_kor":"충무동","nm_eng":"Chungmu-dong"},

{"cd":"21020650","nm_kor":"남부민1동","nm_eng":"Nambumin 1(il)-dong"},

{"cd":"21020690","nm_kor":"남부민2동","nm_eng":"Nambumin 2(i)-dong"},

{"cd":"21020680","nm_kor":"암남동","nm_eng":"Amnam-dong"},

{"cd":"21030000","nm_kor":"동구","nm_eng":"Dong-gu"},

{"cd":"21030510","nm_kor":"초량1동","nm_eng":"Choryang 1(il)-dong"},

{"cd":"21030520","nm_kor":"초량2동","nm_eng":"Choryang 2(i)-dong"},

{"cd":"21030530","nm_kor":"초량3동","nm_eng":"Choryang 3(sam)-dong"},

{"cd":"21030550","nm_kor":"초량6동","nm_eng":"Choryang 6(yuk)-dong"},

{"cd":"21030560","nm_kor":"수정1동","nm_eng":"Sujeong 1(il)-dong"},

{"cd":"21030570","nm_kor":"수정2동","nm_eng":"Sujeong 2(i)-dong"},

{"cd":"21030590","nm_kor":"수정4동","nm_eng":"Sujeong 4(sa)-dong"},

{"cd":"21030600","nm_kor":"수정5동","nm_eng":"Sujeong 5(o)-dong"},

{"cd":"21030700","nm_kor":"좌천동","nm_eng":"Jwacheon-dong"},

{"cd":"21030710","nm_kor":"범일1동","nm_eng":"Beomil 1(il)-dong"},

{"cd":"21030660","nm_kor":"범일2동","nm_eng":"Beomil 2(i)-dong"},

{"cd":"21030680","nm_kor":"범일5동","nm_eng":"Beomil 5(o)-dong"},

{"cd":"21040000","nm_kor":"영도구","nm_eng":"Yeongdo-gu"},

{"cd":"21040530","nm_kor":"남항동","nm_eng":"Namhang-dong"},

{"cd":"21040540","nm_kor":"영선1동","nm_eng":"Yeongseon 1(il)-dong"},

{"cd":"21040550","nm_kor":"영선2동","nm_eng":"Yeongseon 2(i)-dong"},

{"cd":"21040680","nm_kor":"신선동","nm_eng":"Sinseon-dong"},

{"cd":"21040590","nm_kor":"봉래1동","nm_eng":"Bongnae 1(il)-dong"},

{"cd":"21040690","nm_kor":"봉래2동","nm_eng":"Bongnae 2(i)-dong"},

{"cd":"21040630","nm_kor":"청학1동","nm_eng":"Cheonghak 1(il)-dong"},

{"cd":"21040640","nm_kor":"청학2동","nm_eng":"Cheonghak 2(i)-dong"},

{"cd":"21040650","nm_kor":"동삼1동","nm_eng":"Dongsam 1(il)-dong"},

{"cd":"21040660","nm_kor":"동삼2동","nm_eng":"Dongsam 2(i)-dong"},

{"cd":"21040670","nm_kor":"동삼3동","nm_eng":"Dongsam 3(sam)-dong"},

{"cd":"21050000","nm_kor":"부산진구","nm_eng":"Busanjin-gu"},

{"cd":"21050820","nm_kor":"부전1동","nm_eng":"Bujeon 1(il)-dong"},

{"cd":"21050520","nm_kor":"부전2동","nm_eng":"Bujeon 2(i)-dong"},

{"cd":"21050540","nm_kor":"연지동","nm_eng":"Yeonji-dong"},

{"cd":"21050550","nm_kor":"초읍동","nm_eng":"Choeup-dong"},

{"cd":"21050560","nm_kor":"양정1동","nm_eng":"Yangjeong 1(il)-dong"},

{"cd":"21050570","nm_kor":"양정2동","nm_eng":"Yangjeong 2(i)-dong"},

{"cd":"21050830","nm_kor":"전포1동","nm_eng":"Jeonpo 1(il)-dong"},

{"cd":"21050610","nm_kor":"전포2동","nm_eng":"Jeonpo 2(i)-dong"},

{"cd":"21050640","nm_kor":"부암1동","nm_eng":"Buam 1(il)-dong"},

{"cd":"21050660","nm_kor":"부암3동","nm_eng":"Buam 3(sam)-dong"},

{"cd":"21050800","nm_kor":"당감제1동","nm_eng":"Danggam 1(il)-dong"},

{"cd":"21050680","nm_kor":"당감2동","nm_eng":"Danggam 2(i)-dong"},

{"cd":"21050700","nm_kor":"당감4동","nm_eng":"Danggam 4(sa)-dong"},

{"cd":"21050810","nm_kor":"가야제1동","nm_eng":"Gaya 1(il)-dong"},

{"cd":"21050720","nm_kor":"가야2동","nm_eng":"Gaya 2(i)-dong"},

{"cd":"21050740","nm_kor":"개금1동","nm_eng":"Gaegeum 1(il)-dong"},

{"cd":"21050750","nm_kor":"개금2동","nm_eng":"Gaegeum 2(i)-dong"},

{"cd":"21050760","nm_kor":"개금3동","nm_eng":"Gaegeum 3(sam)-dong"},

{"cd":"21050770","nm_kor":"범천1동","nm_eng":"Beomcheon 1(il)-dong"},

{"cd":"21050840","nm_kor":"범천2동","nm_eng":"Beomcheon 2(i)-dong"},

{"cd":"21060000","nm_kor":"동래구","nm_eng":"Dongnae-gu"},

{"cd":"21060510","nm_kor":"수민동","nm_eng":"Sumin-dong"},

{"cd":"21060520","nm_kor":"복산동","nm_eng":"Boksan-dong"},

{"cd":"21060650","nm_kor":"명륜동","nm_eng":"Myeongnyun-dong"},

{"cd":"21060550","nm_kor":"온천1동","nm_eng":"Oncheon 1(il)-dong"},

{"cd":"21060560","nm_kor":"온천2동","nm_eng":"Oncheon 2(i)-dong"},

{"cd":"21060570","nm_kor":"온천3동","nm_eng":"Oncheon 3(sam)-dong"},

{"cd":"21060580","nm_kor":"사직1동","nm_eng":"Sajik 1(il)-dong"},

{"cd":"21060590","nm_kor":"사직2동","nm_eng":"Sajik 2(i)-dong"},

{"cd":"21060600","nm_kor":"사직3동","nm_eng":"Sajik 3(sam)-dong"},

{"cd":"21060610","nm_kor":"안락1동","nm_eng":"Allak 1(il)-dong"},

{"cd":"21060620","nm_kor":"안락2동","nm_eng":"Allak 2(i)-dong"},

{"cd":"21060630","nm_kor":"명장1동","nm_eng":"Myeongjang 1(il)-dong"},

{"cd":"21060640","nm_kor":"명장2동","nm_eng":"Myeongjang 2(i)-dong"},

{"cd":"21070000","nm_kor":"남구","nm_eng":"Nam-gu"},

{"cd":"21070700","nm_kor":"대연1동","nm_eng":"Daeyeon 1(il)-dong"},

{"cd":"21070530","nm_kor":"대연3동","nm_eng":"Daeyeon 3(sam)-dong"},

{"cd":"21070540","nm_kor":"대연4동","nm_eng":"Daeyeon 4(sa)-dong"},

{"cd":"21070550","nm_kor":"대연5동","nm_eng":"Daeyeon 5(o)-dong"},

{"cd":"21070560","nm_kor":"대연6동","nm_eng":"Daeyeon 6(yuk)-dong"},

{"cd":"21070570","nm_kor":"용호1동","nm_eng":"Yongho 1(il)-dong"},

{"cd":"21070580","nm_kor":"용호2동","nm_eng":"Yongho 2(i)-dong"},

{"cd":"21070590","nm_kor":"용호3동","nm_eng":"Yongho 3(sam)-dong"},

{"cd":"21070600","nm_kor":"용호4동","nm_eng":"Yongho 4(sa)-dong"},

{"cd":"21070610","nm_kor":"용당동","nm_eng":"Yongdang-dong"},

{"cd":"21070620","nm_kor":"감만1동","nm_eng":"Gamman 1(il)-dong"},

{"cd":"21070630","nm_kor":"감만2동","nm_eng":"Gamman 2(i)-dong"},

{"cd":"21070710","nm_kor":"우암동","nm_eng":"Uam-dong"},

{"cd":"21070660","nm_kor":"문현1동","nm_eng":"Munhyeon 1(il)-dong"},

{"cd":"21070670","nm_kor":"문현2동","nm_eng":"Munhyeon 2(i)-dong"},

{"cd":"21070680","nm_kor":"문현3동","nm_eng":"Munhyeon 3(sam)-dong"},

{"cd":"21070690","nm_kor":"문현4동","nm_eng":"Munhyeon 4(sa)-dong"},

{"cd":"21080000","nm_kor":"북구","nm_eng":"Buk-gu"},

{"cd":"21080510","nm_kor":"구포1동","nm_eng":"Gupo 1(il)-dong"},

{"cd":"21080520","nm_kor":"구포2동","nm_eng":"Gupo 2(i)-dong"},

{"cd":"21080530","nm_kor":"구포3동","nm_eng":"Gupo 3(sam)-dong"},

{"cd":"21080540","nm_kor":"금곡동","nm_eng":"Geumgok-dong"},

{"cd":"21080550","nm_kor":"화명1동","nm_eng":"Hwamyeong 1(il)-dong"},

{"cd":"21080620","nm_kor":"화명2동","nm_eng":"Hwamyeong 2(i)-dong"},

{"cd":"21080630","nm_kor":"화명3동","nm_eng":"Hwamyeong 3(sam)-dong"},

{"cd":"21080560","nm_kor":"덕천1동","nm_eng":"Deokcheon 1(il)-dong"},

{"cd":"21080570","nm_kor":"덕천2동","nm_eng":"Deokcheon 2(i)-dong"},

{"cd":"21080580","nm_kor":"덕천3동","nm_eng":"Deokcheon 3(sam)-dong"},

{"cd":"21080590","nm_kor":"만덕1동","nm_eng":"Mandeok 1(il)-dong"},

{"cd":"21080600","nm_kor":"만덕2동","nm_eng":"Mandeok 2(i)-dong"},

{"cd":"21080610","nm_kor":"만덕3동","nm_eng":"Mandeok 3(sam)-dong"},

{"cd":"21090000","nm_kor":"해운대구","nm_eng":"Haeundae-gu"},

{"cd":"21090730","nm_kor":"우1동","nm_eng":"U 1(il)-dong"},

{"cd":"21090740","nm_kor":"우2동","nm_eng":"U 2(i)-dong"},

{"cd":"21090750","nm_kor":"우3동","nm_eng":"U 3(sam)-dong"},

{"cd":"21090530","nm_kor":"중1동","nm_eng":"Jung 1(il)-dong"},

{"cd":"21090540","nm_kor":"중2동","nm_eng":"Jung 2(i)-dong"},

{"cd":"21090660","nm_kor":"좌1동","nm_eng":"Jwa 1(il)-dong"},

{"cd":"21090670","nm_kor":"좌2동","nm_eng":"Jwa 2(i)-dong"},

{"cd":"21090680","nm_kor":"좌3동","nm_eng":"Jwa 3(sam)-dong"},

{"cd":"21090690","nm_kor":"좌4동","nm_eng":"Jwa 4(sa)-dong"},

{"cd":"21090560","nm_kor":"송정동","nm_eng":"Songjeong-dong"},

{"cd":"21090700","nm_kor":"반여1동","nm_eng":"Banyeo 1(il)-dong"},

{"cd":"21090580","nm_kor":"반여2동","nm_eng":"Banyeo 2(i)-dong"},

{"cd":"21090590","nm_kor":"반여3동","nm_eng":"Banyeo 3(sam)-dong"},

{"cd":"21090710","nm_kor":"반여4동","nm_eng":"Banyeo 4(sa)-dong"},

{"cd":"21090720","nm_kor":"반송1동","nm_eng":"Bansong 1(il)-dong"},

{"cd":"21090620","nm_kor":"반송2동","nm_eng":"Bansong 2(i)-dong"},

{"cd":"21090640","nm_kor":"재송1동","nm_eng":"Jaesong 1(il)-dong"},

{"cd":"21090650","nm_kor":"재송2동","nm_eng":"Jaesong 2(i)-dong"},

{"cd":"21100000","nm_kor":"사하구","nm_eng":"Saha-gu"},

{"cd":"21100510","nm_kor":"괴정1동","nm_eng":"Goejeong 1(il)-dong"},

{"cd":"21100520","nm_kor":"괴정2동","nm_eng":"Goejeong 2(i)-dong"},

{"cd":"21100530","nm_kor":"괴정3동","nm_eng":"Goejeong 3(sam)-dong"},

{"cd":"21100540","nm_kor":"괴정4동","nm_eng":"Goejeong 4(sa)-dong"},

{"cd":"21100550","nm_kor":"당리동","nm_eng":"Dangni-dong"},

{"cd":"21100560","nm_kor":"하단1동","nm_eng":"Hadan 1(il)-dong"},

{"cd":"21100570","nm_kor":"하단2동","nm_eng":"Hadan 2(i)-dong"},

{"cd":"21100580","nm_kor":"신평1동","nm_eng":"Sinpyeong 1(il)-dong"},

{"cd":"21100590","nm_kor":"신평2동","nm_eng":"Sinpyeong 2(i)-dong"},

{"cd":"21100600","nm_kor":"장림1동","nm_eng":"Jangnim 1(il)-dong"},

{"cd":"21100610","nm_kor":"장림2동","nm_eng":"Jangnim 2(i)-dong"},

{"cd":"21100620","nm_kor":"다대1동","nm_eng":"Dadae 1(il)-dong"},

{"cd":"21100630","nm_kor":"다대2동","nm_eng":"Dadae 2(i)-dong"},

{"cd":"21100640","nm_kor":"구평동","nm_eng":"Gupyeong-dong"},

{"cd":"21100650","nm_kor":"감천1동","nm_eng":"Gamcheon 1(il)-dong"},

{"cd":"21100660","nm_kor":"감천2동","nm_eng":"Gamcheon 2(i)-dong"},

{"cd":"21110000","nm_kor":"금정구","nm_eng":"Geumjeong-gu"},

{"cd":"21110510","nm_kor":"서1동","nm_eng":"Seo 1(il)-dong"},

{"cd":"21110520","nm_kor":"서2동","nm_eng":"Seo 2(i)-dong"},

{"cd":"21110720","nm_kor":"서3동","nm_eng":"Seo 3(sam)-dong"},

{"cd":"21110730","nm_kor":"금사회동동","nm_eng":"Geumsahoedong-dong"},

{"cd":"21110570","nm_kor":"부곡1동","nm_eng":"Bugok 1(il)-dong"},

{"cd":"21110580","nm_kor":"부곡2동","nm_eng":"Bugok 2(i)-dong"},

{"cd":"21110590","nm_kor":"부곡3동","nm_eng":"Bugok 3(sam)-dong"},

{"cd":"21110600","nm_kor":"부곡4동","nm_eng":"Bugok 4(sa)-dong"},

{"cd":"21110610","nm_kor":"장전1동","nm_eng":"Jangjeon 1(il)-dong"},

{"cd":"21110740","nm_kor":"장전2동","nm_eng":"Jangjeon 2(i)-dong"},

{"cd":"21110640","nm_kor":"선두구동","nm_eng":"Seondugu-dong"},

{"cd":"21110670","nm_kor":"청룡노포동","nm_eng":"Cheongnyongnopo-dong"},

{"cd":"21110680","nm_kor":"남산동","nm_eng":"Namsan-dong"},

{"cd":"21110690","nm_kor":"구서1동","nm_eng":"Guseo 1(il)-dong"},

{"cd":"21110700","nm_kor":"구서2동","nm_eng":"Guseo 2(i)-dong"},

{"cd":"21110710","nm_kor":"금성동","nm_eng":"Geumseong-dong"},

{"cd":"21120000","nm_kor":"강서구","nm_eng":"Gangseo-gu"},

{"cd":"21120510","nm_kor":"대저1동","nm_eng":"Daejeo 1(il)-dong"},

{"cd":"21120520","nm_kor":"대저2동","nm_eng":"Daejeo 2(i)-dong"},

{"cd":"21120530","nm_kor":"강동동","nm_eng":"Gangdong-dong"},

{"cd":"21120590","nm_kor":"명지1동","nm_eng":"Myeongji 1(il)-dong"},

{"cd":"21120600","nm_kor":"명지2동","nm_eng":"Myeongji 2(i)-dong"},

{"cd":"21120550","nm_kor":"가락동","nm_eng":"Garak-dong"},

{"cd":"21120560","nm_kor":"녹산동","nm_eng":"Noksan-dong"},

{"cd":"21120580","nm_kor":"가덕도동","nm_eng":"Gadeokdo-dong"},

{"cd":"21130000","nm_kor":"연제구","nm_eng":"Yeonje-gu"},

{"cd":"21130510","nm_kor":"거제1동","nm_eng":"Geoje 1(il)-dong"},

{"cd":"21130520","nm_kor":"거제2동","nm_eng":"Geoje 2(i)-dong"},

{"cd":"21130530","nm_kor":"거제3동","nm_eng":"Geoje 3(sam)-dong"},

{"cd":"21130540","nm_kor":"거제4동","nm_eng":"Geoje 4(sa)-dong"},

{"cd":"21130550","nm_kor":"연산1동","nm_eng":"Yeonsan 1(il)-dong"},

{"cd":"21130560","nm_kor":"연산2동","nm_eng":"Yeonsan 2(i)-dong"},

{"cd":"21130570","nm_kor":"연산3동","nm_eng":"Yeonsan 3(sam)-dong"},

{"cd":"21130580","nm_kor":"연산4동","nm_eng":"Yeonsan 4(sa)-dong"},

{"cd":"21130590","nm_kor":"연산5동","nm_eng":"Yeonsan 5(o)-dong"},

{"cd":"21130600","nm_kor":"연산6동","nm_eng":"Yeonsan 6(yuk)-dong"},

{"cd":"21130620","nm_kor":"연산8동","nm_eng":"Yeonsan 8(pal)-dong"},

{"cd":"21130630","nm_kor":"연산9동","nm_eng":"Yeonsan 9(gu)-dong"},

{"cd":"21140000","nm_kor":"수영구","nm_eng":"Suyeong-gu"},

{"cd":"21140510","nm_kor":"남천1동","nm_eng":"Namcheon 1(il)-dong"},

{"cd":"21140520","nm_kor":"남천2동","nm_eng":"Namcheon 2(i)-dong"},

{"cd":"21140530","nm_kor":"수영동","nm_eng":"Suyeong-dong"},

{"cd":"21140540","nm_kor":"망미1동","nm_eng":"Mangmi 1(il)-dong"},

{"cd":"21140550","nm_kor":"망미2동","nm_eng":"Mangmi 2(i)-dong"},

{"cd":"21140560","nm_kor":"광안1동","nm_eng":"Gwangan 1(il)-dong"},

{"cd":"21140570","nm_kor":"광안2동","nm_eng":"Gwangan 2(i)-dong"},

{"cd":"21140580","nm_kor":"광안3동","nm_eng":"Gwangan 3(sam)-dong"},

{"cd":"21140590","nm_kor":"광안4동","nm_eng":"Gwangan 4(sa)-dong"},

{"cd":"21140600","nm_kor":"민락동","nm_eng":"Millak-dong"},

{"cd":"21150000","nm_kor":"사상구","nm_eng":"Sasang-gu"},

{"cd":"21150510","nm_kor":"삼락동","nm_eng":"Samnak-dong"},

{"cd":"21150520","nm_kor":"모라1동","nm_eng":"Mora 1(il)-dong"},

{"cd":"21150540","nm_kor":"모라3동","nm_eng":"Mora 3(sam)-dong"},

{"cd":"21150550","nm_kor":"덕포1동","nm_eng":"Deokpo 1(il)-dong"},

{"cd":"21150560","nm_kor":"덕포2동","nm_eng":"Deokpo 2(i)-dong"},

{"cd":"21150570","nm_kor":"괘법동","nm_eng":"Gwaebeop-dong"},

{"cd":"21150650","nm_kor":"감전동","nm_eng":"Gamjeon-dong"},

{"cd":"21150600","nm_kor":"주례1동","nm_eng":"Jurye 1(il)-dong"},

{"cd":"21150610","nm_kor":"주례2동","nm_eng":"Jurye 2(i)-dong"},

{"cd":"21150620","nm_kor":"주례3동","nm_eng":"Jurye 3(sam)-dong"},

{"cd":"21150630","nm_kor":"학장동","nm_eng":"Hakjang-dong"},

{"cd":"21150640","nm_kor":"엄궁동","nm_eng":"Eomgung-dong"},

{"cd":"21510000","nm_kor":"기장군","nm_eng":"Gijang-gun"},

{"cd":"21510110","nm_kor":"기장읍","nm_eng":"Gijang-eup"},

{"cd":"21510120","nm_kor":"장안읍","nm_eng":"Jangan-eup"},

{"cd":"21510130","nm_kor":"정관읍","nm_eng":"Jeonggwan-eup"},

{"cd":"21510111","nm_kor":"일광읍","nm_eng":"Ilgwang-eup"},

{"cd":"21510330","nm_kor":"철마면","nm_eng":"Cheolma-myeon"},

{"cd":"22000000","nm_kor":"대구광역시","nm_eng":"Daegu"},

{"cd":"22010000","nm_kor":"중구","nm_eng":"Jung-gu"},

{"cd":"22010700","nm_kor":"동인동","nm_eng":"Dongin-dong"},

{"cd":"22010540","nm_kor":"삼덕동","nm_eng":"Samdeok-dong"},

{"cd":"22010560","nm_kor":"성내1동","nm_eng":"Seongnae 1(il)-dong"},

{"cd":"22010590","nm_kor":"성내2동","nm_eng":"Seongnae 2(i)-dong"},

{"cd":"22010610","nm_kor":"성내3동","nm_eng":"Seongnae 3(sam)-dong"},

{"cd":"22010620","nm_kor":"대신동","nm_eng":"Daesin-dong"},

{"cd":"22010640","nm_kor":"남산1동","nm_eng":"Namsan 1(il)-dong"},

{"cd":"22010650","nm_kor":"남산2동","nm_eng":"Namsan 2(i)-dong"},

{"cd":"22010660","nm_kor":"남산3동","nm_eng":"Namsan 3(sam)-dong"},

{"cd":"22010670","nm_kor":"남산4동","nm_eng":"Namsan 4(sa)-dong"},

{"cd":"22010680","nm_kor":"대봉1동","nm_eng":"Daebong 1(il)-dong"},

{"cd":"22010690","nm_kor":"대봉2동","nm_eng":"Daebong 2(i)-dong"},

{"cd":"22020000","nm_kor":"동구","nm_eng":"Dong-gu"},

{"cd":"22020510","nm_kor":"신암1동","nm_eng":"Sinam 1(il)-dong"},

{"cd":"22020520","nm_kor":"신암2동","nm_eng":"Sinam 2(i)-dong"},

{"cd":"22020530","nm_kor":"신암3동","nm_eng":"Sinam 3(sam)-dong"},

{"cd":"22020540","nm_kor":"신암4동","nm_eng":"Sinam 4(sa)-dong"},

{"cd":"22020550","nm_kor":"신암5동","nm_eng":"Sinam 5(o)-dong"},

{"cd":"22020560","nm_kor":"신천1.2동","nm_eng":"Sincheon 1.2(ili)-dong"},

{"cd":"22020580","nm_kor":"신천3동","nm_eng":"Sincheon 3(sam)-dong"},

{"cd":"22020590","nm_kor":"신천4동","nm_eng":"Sincheon 4(sa)-dong"},

{"cd":"22020600","nm_kor":"효목1동","nm_eng":"Hyomok 1(il)-dong"},

{"cd":"22020610","nm_kor":"효목2동","nm_eng":"Hyomok 2(i)-dong"},

{"cd":"22020620","nm_kor":"도평동","nm_eng":"Dopyeong-dong"},

{"cd":"22020630","nm_kor":"불로.봉무동","nm_eng":"Bullobongmu-dong"},

{"cd":"22020650","nm_kor":"지저동","nm_eng":"Jijeo-dong"},

{"cd":"22020660","nm_kor":"동촌동","nm_eng":"Dongchon-dong"},

{"cd":"22020680","nm_kor":"방촌동","nm_eng":"Bangchon-dong"},

{"cd":"22020690","nm_kor":"해안동","nm_eng":"Haean-dong"},

{"cd":"22020730","nm_kor":"안심1동","nm_eng":"Ansim 1(il)-dong"},

{"cd":"22020740","nm_kor":"안심2동","nm_eng":"Ansim 2(i)-dong"},

{"cd":"22020760","nm_kor":"안심3동","nm_eng":"Ansim 3(sam)-dong"},

{"cd":"22020770","nm_kor":"안심4동","nm_eng":"Ansim 4(sa)-dong"},

{"cd":"22020780","nm_kor":"혁신동","nm_eng":"hyeoksin-dong"},

{"cd":"22020710","nm_kor":"공산동","nm_eng":"Gongsan-dong"},

{"cd":"22030000","nm_kor":"서구","nm_eng":"Seo-gu"},

{"cd":"22030510","nm_kor":"내당1동","nm_eng":"Naedang 1(il)-dong"},

{"cd":"22030520","nm_kor":"내당2.3동","nm_eng":"Naedang 2.3(isam)-dong"},

{"cd":"22030530","nm_kor":"내당4동","nm_eng":"Naedang 4(sa)-dong"},

{"cd":"22030540","nm_kor":"비산1동","nm_eng":"Bisan 1(il)-dong"},

{"cd":"22030550","nm_kor":"비산2.3동","nm_eng":"Bisan 2.3(isam)-dong"},

{"cd":"22030560","nm_kor":"비산4동","nm_eng":"Bisan 4(sa)-dong"},

{"cd":"22030570","nm_kor":"비산5동","nm_eng":"Bisan 5(o)-dong"},

{"cd":"22030580","nm_kor":"비산6동","nm_eng":"Bisan 6(yuk)-dong"},

{"cd":"22030590","nm_kor":"비산7동","nm_eng":"Bisan 7(chil)-dong"},

{"cd":"22030600","nm_kor":"평리1동","nm_eng":"Pyeongni 1(il)-dong"},

{"cd":"22030610","nm_kor":"평리2동","nm_eng":"Pyeongni 2(i)-dong"},

{"cd":"22030620","nm_kor":"평리3동","nm_eng":"Pyeongni 3(sam)-dong"},

{"cd":"22030630","nm_kor":"평리4동","nm_eng":"Pyeongni 4(sa)-dong"},

{"cd":"22030640","nm_kor":"평리5동","nm_eng":"Pyeongni 5(o)-dong"},

{"cd":"22030650","nm_kor":"평리6동","nm_eng":"Pyeongni 6(yuk)-dong"},

{"cd":"22030660","nm_kor":"상중이동","nm_eng":"Sangjungi-dong"},

{"cd":"22030680","nm_kor":"원대동","nm_eng":"Wondae-dong"},

{"cd":"22040000","nm_kor":"남구","nm_eng":"Nam-gu"},

{"cd":"22040510","nm_kor":"이천동","nm_eng":"Icheon-dong"},

{"cd":"22040530","nm_kor":"봉덕1동","nm_eng":"Bongdeok 1(il)-dong"},

{"cd":"22040540","nm_kor":"봉덕2동","nm_eng":"Bongdeok 2(i)-dong"},

{"cd":"22040550","nm_kor":"봉덕3동","nm_eng":"Bongdeok 3(sam)-dong"},

{"cd":"22040560","nm_kor":"대명1동","nm_eng":"Daemyeong 1(il)-dong"},

{"cd":"22040570","nm_kor":"대명2동","nm_eng":"Daemyeong 2(i)-dong"},

{"cd":"22040580","nm_kor":"대명3동","nm_eng":"Daemyeong 3(sam)-dong"},

{"cd":"22040590","nm_kor":"대명4동","nm_eng":"Daemyeong 4(sa)-dong"},

{"cd":"22040600","nm_kor":"대명5동","nm_eng":"Daemyeong 5(o)-dong"},

{"cd":"22040610","nm_kor":"대명6동","nm_eng":"Daemyeong 6(yuk)-dong"},

{"cd":"22040640","nm_kor":"대명9동","nm_eng":"Daemyeong 9(gu)-dong"},

{"cd":"22040650","nm_kor":"대명10동","nm_eng":"Daemyeong 10(sip)-dong"},

{"cd":"22040660","nm_kor":"대명11동","nm_eng":"Daemyeong 11(sibil)-dong"},

{"cd":"22050000","nm_kor":"북구","nm_eng":"Buk-gu"},

{"cd":"22050510","nm_kor":"고성동","nm_eng":"Goseong-dong"},

{"cd":"22050520","nm_kor":"칠성동","nm_eng":"Chilseong-dong"},

{"cd":"22050550","nm_kor":"침산1동","nm_eng":"Chimsan 1(il)-dong"},

{"cd":"22050560","nm_kor":"침산2동","nm_eng":"Chimsan 2(i)-dong"},

{"cd":"22050570","nm_kor":"침산3동","nm_eng":"Chimsan 3(sam)-dong"},

{"cd":"22050610","nm_kor":"산격1동","nm_eng":"Sangyeok 1(il)-dong"},

{"cd":"22050620","nm_kor":"산격2동","nm_eng":"Sangyeok 2(i)-dong"},

{"cd":"22050630","nm_kor":"산격3동","nm_eng":"Sangyeok 3(sam)-dong"},

{"cd":"22050640","nm_kor":"산격4동","nm_eng":"Sangyeok 4(sa)-dong"},

{"cd":"22050840","nm_kor":"대현동","nm_eng":"Daehyeon-dong"},

{"cd":"22050650","nm_kor":"복현1동","nm_eng":"Bokhyeon 1(il)-dong"},

{"cd":"22050660","nm_kor":"복현2동","nm_eng":"Bokhyeon 2(i)-dong"},

{"cd":"22050700","nm_kor":"검단동","nm_eng":"Geomdan-dong"},

{"cd":"22050710","nm_kor":"무태조야동","nm_eng":"Mutaejoya-dong"},

{"cd":"22050750","nm_kor":"관문동","nm_eng":"Gwanmun-dong"},

{"cd":"22050780","nm_kor":"태전1동","nm_eng":"Taejeon 1(il)-dong"},

{"cd":"22050740","nm_kor":"태전2동","nm_eng":"Taejeon 2(i)-dong"},

{"cd":"22050790","nm_kor":"구암동","nm_eng":"Guam-dong"},

{"cd":"22050770","nm_kor":"관음동","nm_eng":"Gwaneum-dong"},

{"cd":"22050760","nm_kor":"읍내동","nm_eng":"Eupnae-dong"},

{"cd":"22050820","nm_kor":"동천동","nm_eng":"Dongcheon-dong"},

{"cd":"22050810","nm_kor":"노원동","nm_eng":"Nowon-dong"},

{"cd":"22050830","nm_kor":"국우동","nm_eng":"Guku-dong"},

{"cd":"22060000","nm_kor":"수성구","nm_eng":"Suseong-gu"},

{"cd":"22060510","nm_kor":"범어1동","nm_eng":"Beomeo 1(il)-dong"},

{"cd":"22060520","nm_kor":"범어2동","nm_eng":"Beomeo 2(i)-dong"},

{"cd":"22060530","nm_kor":"범어3동","nm_eng":"Beomeo 3(sam)-dong"},

{"cd":"22060540","nm_kor":"범어4동","nm_eng":"Beomeo 4(sa)-dong"},

{"cd":"22060550","nm_kor":"만촌1동","nm_eng":"Manchon 1(il)-dong"},

{"cd":"22060560","nm_kor":"만촌2동","nm_eng":"Manchon 2(i)-dong"},

{"cd":"22060570","nm_kor":"만촌3동","nm_eng":"Manchon 3(sam)-dong"},

{"cd":"22060580","nm_kor":"수성1가동","nm_eng":"Suseong 1(il)-ga-dong"},

{"cd":"22060590","nm_kor":"수성2.3가동","nm_eng":"Suseong 2.3(isam)-ga-dong"},

{"cd":"22060600","nm_kor":"수성4가동","nm_eng":"Suseong 4(sa)-ga-dong"},

{"cd":"22060610","nm_kor":"황금1동","nm_eng":"Hwanggeum 1(il)-dong"},

{"cd":"22060620","nm_kor":"황금2동","nm_eng":"Hwanggeum 2(i)-dong"},

{"cd":"22060630","nm_kor":"중동","nm_eng":"Jung-dong"},

{"cd":"22060640","nm_kor":"상동","nm_eng":"Sang-dong"},

{"cd":"22060650","nm_kor":"파동","nm_eng":"Pa-dong"},

{"cd":"22060660","nm_kor":"두산동","nm_eng":"Dusan-dong"},

{"cd":"22060670","nm_kor":"지산1동","nm_eng":"Jisan 1(il)-dong"},

{"cd":"22060680","nm_kor":"지산2동","nm_eng":"Jisan 2(i)-dong"},

{"cd":"22060690","nm_kor":"범물1동","nm_eng":"Beommul 1(il)-dong"},

{"cd":"22060700","nm_kor":"범물2동","nm_eng":"Beommul 2(i)-dong"},

{"cd":"22060710","nm_kor":"고산1동","nm_eng":"Gosan 1(il)-dong"},

{"cd":"22060720","nm_kor":"고산2동","nm_eng":"Gosan 2(i)-dong"},

{"cd":"22060730","nm_kor":"고산3동","nm_eng":"Gosan 3(sam)-dong"},

{"cd":"22070000","nm_kor":"달서구","nm_eng":"Dalseo-gu"},

{"cd":"22070750","nm_kor":"성당동","nm_eng":"Seongdang-dong"},

{"cd":"22070760","nm_kor":"두류1.2동","nm_eng":"Duryu 1.2(ili)-dong"},

{"cd":"22070550","nm_kor":"두류3동","nm_eng":"Duryu 3(sam)-dong"},

{"cd":"22070570","nm_kor":"감삼동","nm_eng":"Gamsam-dong"},

{"cd":"22070580","nm_kor":"죽전동","nm_eng":"Jukjeon-dong"},

{"cd":"22070590","nm_kor":"장기동","nm_eng":"Janggi-dong"},

{"cd":"22070720","nm_kor":"용산1동","nm_eng":"Yongsan 1(il)-dong"},

{"cd":"22070730","nm_kor":"용산2동","nm_eng":"Yongsan 2(i)-dong"},

{"cd":"22070600","nm_kor":"이곡1동","nm_eng":"Igok 1(il)-dong"},

{"cd":"22070740","nm_kor":"이곡2동","nm_eng":"Igok 2(i)-dong"},

{"cd":"22070610","nm_kor":"신당동","nm_eng":"Sindang-dong"},

{"cd":"22070560","nm_kor":"본리동","nm_eng":"Bolli-dong"},

{"cd":"22070770","nm_kor":"월성1동","nm_eng":"Wolseong 1(il)-dong"},

{"cd":"22070630","nm_kor":"월성2동","nm_eng":"Wolseong 2(i)-dong"},

{"cd":"22070780","nm_kor":"진천동","nm_eng":"Jincheon-dong"},

{"cd":"22070790","nm_kor":"유천동","nm_eng":"Yucheon-dong"},

{"cd":"22070650","nm_kor":"상인1동","nm_eng":"Sangin 1(il)-dong"},

{"cd":"22070660","nm_kor":"상인2동","nm_eng":"Sangin 2(i)-dong"},

{"cd":"22070670","nm_kor":"상인3동","nm_eng":"Sangin 3(sam)-dong"},

{"cd":"22070680","nm_kor":"도원동","nm_eng":"Dowon-dong"},

{"cd":"22070690","nm_kor":"송현1동","nm_eng":"Songhyeon 1(il)-dong"},

{"cd":"22070700","nm_kor":"송현2동","nm_eng":"Songhyeon 2(i)-dong"},

{"cd":"22070710","nm_kor":"본동","nm_eng":"Bon-dong"},

{"cd":"22510000","nm_kor":"달성군","nm_eng":"Dalseong-gun"},

{"cd":"22510110","nm_kor":"화원읍","nm_eng":"Hwawon-eup"},

{"cd":"22510120","nm_kor":"논공읍","nm_eng":"Nongong-eup"},

{"cd":"22510130","nm_kor":"다사읍","nm_eng":"Dasa-eup"},

{"cd":"22510140","nm_kor":"유가읍","nm_eng":"Yuga-eup"},

{"cd":"22510150","nm_kor":"옥포읍","nm_eng":"Okpo-eup"},

{"cd":"22510160","nm_kor":"현풍읍","nm_eng":"Hyeonpung-eup"},

{"cd":"22510310","nm_kor":"가창면","nm_eng":"Gachang-myeon"},

{"cd":"22510320","nm_kor":"하빈면","nm_eng":"Habin-myeon"},

{"cd":"22510360","nm_kor":"구지면","nm_eng":"Guji-myeon"},

{"cd":"23000000","nm_kor":"인천광역시","nm_eng":"Incheon"},

{"cd":"23010000","nm_kor":"중구","nm_eng":"Jung-gu"},

{"cd":"23010520","nm_kor":"연안동","nm_eng":"Yeonan-dong"},

{"cd":"23010530","nm_kor":"신포동","nm_eng":"Sinpo-dong"},

{"cd":"23010540","nm_kor":"신흥동","nm_eng":"Sinheung-dong"},

{"cd":"23010560","nm_kor":"도원동","nm_eng":"Dowon-dong"},

{"cd":"23010570","nm_kor":"율목동","nm_eng":"Yulmok-dong"},

{"cd":"23010580","nm_kor":"동인천동","nm_eng":"Dongincheon-dong"},

{"cd":"23010670","nm_kor":"개항동","nm_eng":"Gaehang-dong"},

{"cd":"23010650","nm_kor":"영종동","nm_eng":"Yeongjong-dong"},

{"cd":"23010660","nm_kor":"영종1동","nm_eng":"Yeongjong 1(il)-dong"},

{"cd":"23010640","nm_kor":"운서동","nm_eng":"unseo-dong"},

{"cd":"23010630","nm_kor":"용유동","nm_eng":"Yongyu-dong"},

{"cd":"23020000","nm_kor":"동구","nm_eng":"Dong-gu"},

{"cd":"23020510","nm_kor":"만석동","nm_eng":"Manseok-dong"},

{"cd":"23020520","nm_kor":"화수1.화평동","nm_eng":"Hwasu 1(il)hwapyeong-dong"},

{"cd":"23020530","nm_kor":"화수2동","nm_eng":"Hwasu 2(i)-dong"},

{"cd":"23020550","nm_kor":"송현1.2동","nm_eng":"Songhyeon 1.2(ili)-dong"},

{"cd":"23020570","nm_kor":"송현3동","nm_eng":"Songhyeon 3(sam)-dong"},

{"cd":"23020580","nm_kor":"송림1동","nm_eng":"Songnim 1(il)-dong"},

{"cd":"23020590","nm_kor":"송림2동","nm_eng":"Songnim 2(i)-dong"},

{"cd":"23020600","nm_kor":"송림3.5동","nm_eng":"Songnim 3.5(samo)-dong"},

{"cd":"23020610","nm_kor":"송림4동","nm_eng":"Songnim 4(sa)-dong"},

{"cd":"23020630","nm_kor":"송림6동","nm_eng":"Songnim 6(yuk)-dong"},

{"cd":"23020640","nm_kor":"금창동","nm_eng":"Geumchang-dong"},

{"cd":"23090000","nm_kor":"미추홀구","nm_eng":"Michuhol-gu"},

{"cd":"23090520","nm_kor":"숭의2동","nm_eng":"Sungui 2(i)-dong"},

{"cd":"23090750","nm_kor":"숭의1.3동","nm_eng":"Sungui 1.3(ilsam)-dong"},

{"cd":"23090540","nm_kor":"숭의4동","nm_eng":"Sungui 4(sa)-dong"},

{"cd":"23090760","nm_kor":"용현1.4동","nm_eng":"Yonghyeon 1.4(ilsa)-dong"},

{"cd":"23090560","nm_kor":"용현2동","nm_eng":"Yonghyeon 2(i)-dong"},

{"cd":"23090570","nm_kor":"용현3동","nm_eng":"Yonghyeon 3(sam)-dong"},

{"cd":"23090590","nm_kor":"용현5동","nm_eng":"Yonghyeon 5(o)-dong"},

{"cd":"23090600","nm_kor":"학익1동","nm_eng":"Hagik 1(il)-dong"},

{"cd":"23090610","nm_kor":"학익2동","nm_eng":"Hagik 2(i)-dong"},

{"cd":"23090620","nm_kor":"도화1동","nm_eng":"Dohwa 1(il)-dong"},

{"cd":"23090770","nm_kor":"도화2.3동","nm_eng":"Dohwa 2.3(isam)-dong"},

{"cd":"23090650","nm_kor":"주안1동","nm_eng":"Juan 1(il)-dong"},

{"cd":"23090660","nm_kor":"주안2동","nm_eng":"Juan 2(i)-dong"},

{"cd":"23090670","nm_kor":"주안3동","nm_eng":"Juan 3(sam)-dong"},

{"cd":"23090680","nm_kor":"주안4동","nm_eng":"Juan 4(sa)-dong"},

{"cd":"23090690","nm_kor":"주안5동","nm_eng":"Juan 5(o)-dong"},

{"cd":"23090700","nm_kor":"주안6동","nm_eng":"Juan 6(yuk)-dong"},

{"cd":"23090710","nm_kor":"주안7동","nm_eng":"Juan 7(chil)-dong"},

{"cd":"23090720","nm_kor":"주안8동","nm_eng":"Juan 8(pal)-dong"},

{"cd":"23090730","nm_kor":"관교동","nm_eng":"Gwangyo-dong"},

{"cd":"23090740","nm_kor":"문학동","nm_eng":"Munhak-dong"},

{"cd":"23040000","nm_kor":"연수구","nm_eng":"Yeonsu-gu"},

{"cd":"23040510","nm_kor":"옥련1동","nm_eng":"Ongnyeon 1(il)-dong"},

{"cd":"23040600","nm_kor":"옥련2동","nm_eng":"Ongnyeon 2(i)-dong"},

{"cd":"23040520","nm_kor":"선학동","nm_eng":"Seonhak-dong"},

{"cd":"23040530","nm_kor":"연수1동","nm_eng":"Yeonsu 1(il)-dong"},

{"cd":"23040540","nm_kor":"연수2동","nm_eng":"Yeonsu 2(i)-dong"},

{"cd":"23040550","nm_kor":"연수3동","nm_eng":"Yeonsu 3(sam)-dong"},

{"cd":"23040560","nm_kor":"청학동","nm_eng":"Cheonghak-dong"},

{"cd":"23040570","nm_kor":"동춘1동","nm_eng":"Dongchun 1(il)-dong"},

{"cd":"23040580","nm_kor":"동춘2동","nm_eng":"Dongchun 2(i)-dong"},

{"cd":"23040590","nm_kor":"동춘3동","nm_eng":"Dongchun 3(sam)-dong"},

{"cd":"23040640","nm_kor":"송도1동","nm_eng":"Songdo 1(il)-dong"},

{"cd":"23040660","nm_kor":"송도2동","nm_eng":"Songdo 2(i)dong"},

{"cd":"23040650","nm_kor":"송도3동","nm_eng":"Songdo 3(sam)dong"},

{"cd":"23040680","nm_kor":"송도4동","nm_eng":"Songdo 4(sa)dong"},

{"cd":"23040690","nm_kor":"송도5동","nm_eng":"Songdo 5(o)dong"},

{"cd":"23050000","nm_kor":"남동구","nm_eng":"Namdong-gu"},

{"cd":"23050510","nm_kor":"구월1동","nm_eng":"Guwol 1(il)-dong"},

{"cd":"23050520","nm_kor":"구월2동","nm_eng":"Guwol 2(i)-dong"},

{"cd":"23050530","nm_kor":"구월3동","nm_eng":"Guwol 3(sam)-dong"},

{"cd":"23050540","nm_kor":"구월4동","nm_eng":"Guwol 4(sa)-dong"},

{"cd":"23050550","nm_kor":"간석1동","nm_eng":"Ganseok 1(il)-dong"},

{"cd":"23050560","nm_kor":"간석2동","nm_eng":"Ganseok 2(i)-dong"},

{"cd":"23050570","nm_kor":"간석3동","nm_eng":"Ganseok 3(sam)-dong"},

{"cd":"23050580","nm_kor":"간석4동","nm_eng":"Ganseok 4(sa)-dong"},

{"cd":"23050590","nm_kor":"만수1동","nm_eng":"Mansu 1(il)-dong"},

{"cd":"23050600","nm_kor":"만수2동","nm_eng":"Mansu 2(i)-dong"},

{"cd":"23050610","nm_kor":"만수3동","nm_eng":"Mansu 3(sam)-dong"},

{"cd":"23050620","nm_kor":"만수4동","nm_eng":"Mansu 4(sa)-dong"},

{"cd":"23050630","nm_kor":"만수5동","nm_eng":"Mansu 5(o)-dong"},

{"cd":"23050640","nm_kor":"만수6동","nm_eng":"Mansu 6(yuk)-dong"},

{"cd":"23050750","nm_kor":"장수서창동","nm_eng":"Jangsuseochang-dong"},

{"cd":"23050760","nm_kor":"서창2동","nm_eng":"Seochang 2(i)-dong"},

{"cd":"23050670","nm_kor":"남촌도림동","nm_eng":"Namchondorim-dong"},

{"cd":"23050720","nm_kor":"논현1동","nm_eng":"Nonhyeon 1(il)-dong"},

{"cd":"23050730","nm_kor":"논현2동","nm_eng":"Nonhyeon 2(i)-dong"},

{"cd":"23050740","nm_kor":"논현고잔동","nm_eng":"Nonhyeongojan-dong"},

{"cd":"23060000","nm_kor":"부평구","nm_eng":"Bupyeong-gu"},

{"cd":"23060510","nm_kor":"부평1동","nm_eng":"Bupyeong 1(il)-dong"},

{"cd":"23060520","nm_kor":"부평2동","nm_eng":"Bupyeong 2(i)-dong"},

{"cd":"23060530","nm_kor":"부평3동","nm_eng":"Bupyeong 3(sam)-dong"},

{"cd":"23060540","nm_kor":"부평4동","nm_eng":"Bupyeong 4(sa)-dong"},

{"cd":"23060550","nm_kor":"부평5동","nm_eng":"Bupyeong 5(o)-dong"},

{"cd":"23060560","nm_kor":"부평6동","nm_eng":"Bupyeong 6(yuk)-dong"},

{"cd":"23060570","nm_kor":"산곡1동","nm_eng":"Sangok 1(il)-dong"},

{"cd":"23060580","nm_kor":"산곡2동","nm_eng":"Sangok 2(i)-dong"},

{"cd":"23060590","nm_kor":"산곡3동","nm_eng":"Sangok 3(sam)-dong"},

{"cd":"23060600","nm_kor":"산곡4동","nm_eng":"Sangok 4(sa)-dong"},

{"cd":"23060610","nm_kor":"청천1동","nm_eng":"Cheongcheon 1(il)-dong"},

{"cd":"23060620","nm_kor":"청천2동","nm_eng":"Cheongcheon 2(i)-dong"},

{"cd":"23060630","nm_kor":"갈산1동","nm_eng":"Galsan 1(il)-dong"},

{"cd":"23060640","nm_kor":"갈산2동","nm_eng":"Galsan 2(i)-dong"},

{"cd":"23060650","nm_kor":"삼산1동","nm_eng":"Samsan 1(il)-dong"},

{"cd":"23060720","nm_kor":"삼산2동","nm_eng":"Samsan 2(i)-dong"},

{"cd":"23060660","nm_kor":"부개1동","nm_eng":"Bugae 1(il)-dong"},

{"cd":"23060670","nm_kor":"부개2동","nm_eng":"Bugae 2(i)-dong"},

{"cd":"23060680","nm_kor":"부개3동","nm_eng":"Bugae 3(sam)-dong"},

{"cd":"23060690","nm_kor":"일신동","nm_eng":"Ilsin-dong"},

{"cd":"23060700","nm_kor":"십정1동","nm_eng":"Sipjeong 1(il)-dong"},

{"cd":"23060710","nm_kor":"십정2동","nm_eng":"Sipjeong 2(i)-dong"},

{"cd":"23070000","nm_kor":"계양구","nm_eng":"Gyeyang-gu"},

{"cd":"23070510","nm_kor":"효성1동","nm_eng":"Hyoseong 1(il)-dong"},

{"cd":"23070520","nm_kor":"효성2동","nm_eng":"Hyoseong 2(i)-dong"},

{"cd":"23070530","nm_kor":"계산1동","nm_eng":"Gyesan 1(il)-dong"},

{"cd":"23070540","nm_kor":"계산2동","nm_eng":"Gyesan 2(i)-dong"},

{"cd":"23070550","nm_kor":"계산3동","nm_eng":"Gyesan 3(sam)-dong"},

{"cd":"23070620","nm_kor":"계산4동","nm_eng":"Gyesan 4(sa)-dong"},

{"cd":"23070560","nm_kor":"작전1동","nm_eng":"Jakjeon 1(il)-dong"},

{"cd":"23070570","nm_kor":"작전2동","nm_eng":"Jakjeon 2(i)-dong"},

{"cd":"23070580","nm_kor":"작전서운동","nm_eng":"Jakjeonseoun-dong"},

{"cd":"23070630","nm_kor":"계양1동","nm_eng":"Gyeyang 1(il)-dong"},

{"cd":"23070610","nm_kor":"계양2동","nm_eng":"Gyeyang 2(i)-dong"},

{"cd":"23070640","nm_kor":"계양3동","nm_eng":"Gyeyang 3(sam)-dong"},

{"cd":"23080000","nm_kor":"서구","nm_eng":"Seo-gu"},

{"cd":"23080510","nm_kor":"검암경서동","nm_eng":"Geomamgyeongseo-dong"},

{"cd":"23080530","nm_kor":"연희동","nm_eng":"Yeonhui-dong"},

{"cd":"23080740","nm_kor":"청라1동","nm_eng":"Cheongna 1(il)-dong"},

{"cd":"23080780","nm_kor":"청라2동","nm_eng":"Cheongna 2(i)-dong"},

{"cd":"23080790","nm_kor":"청라3동","nm_eng":"Cheongna 3(sam)-dong"},

{"cd":"23080540","nm_kor":"가정1동","nm_eng":"Gajeong 1(il)-dong"},

{"cd":"23080550","nm_kor":"가정2동","nm_eng":"Gajeong 2(i)-dong"},

{"cd":"23080560","nm_kor":"가정3동","nm_eng":"Gajeong 3(sam)-dong"},

{"cd":"23080580","nm_kor":"석남1동","nm_eng":"Seongnam 1(il)-dong"},

{"cd":"23080590","nm_kor":"석남2동","nm_eng":"Seongnam 2(i)-dong"},

{"cd":"23080600","nm_kor":"석남3동","nm_eng":"Seongnam 3(sam)-dong"},

{"cd":"23080730","nm_kor":"신현원창동","nm_eng":"Sinhyeonwonchang-dong"},

{"cd":"23080620","nm_kor":"가좌1동","nm_eng":"Gajwa 1(il)-dong"},

{"cd":"23080630","nm_kor":"가좌2동","nm_eng":"Gajwa 2(i)-dong"},

{"cd":"23080640","nm_kor":"가좌3동","nm_eng":"Gajwa 3(sam)-dong"},

{"cd":"23080650","nm_kor":"가좌4동","nm_eng":"Gajwa 4(sa)-dong"},

{"cd":"23080800","nm_kor":"검단동","nm_eng":"Geomdan-dong"},

{"cd":"23080810","nm_kor":"불로대곡동","nm_eng":"Bullodaegok-dong"},

{"cd":"23080870","nm_kor":"원당동","nm_eng":"Wondang-dong"},

{"cd":"23080850","nm_kor":"당하동","nm_eng":"Dangha-dong"},

{"cd":"23080840","nm_kor":"오류왕길동","nm_eng":"Oryuwanggil-dong"},

{"cd":"23080860","nm_kor":"마전동","nm_eng":"Majeon-dong"},

{"cd":"23080880","nm_kor":"아라동","nm_eng":"Ara-dong"},

{"cd":"23510000","nm_kor":"강화군","nm_eng":"Ganghwa-gun"},

{"cd":"23510110","nm_kor":"강화읍","nm_eng":"Ganghwa-eup"},

{"cd":"23510310","nm_kor":"선원면","nm_eng":"Seonwon-myeon"},

{"cd":"23510320","nm_kor":"불은면","nm_eng":"Bureun-myeon"},

{"cd":"23510330","nm_kor":"길상면","nm_eng":"Gilsang-myeon"},

{"cd":"23510340","nm_kor":"화도면","nm_eng":"Hwado-myeon"},

{"cd":"23510350","nm_kor":"양도면","nm_eng":"Yangdo-myeon"},

{"cd":"23510360","nm_kor":"내가면","nm_eng":"Naega-myeon"},

{"cd":"23510370","nm_kor":"하점면","nm_eng":"Hajeom-myeon"},

{"cd":"23510380","nm_kor":"양사면","nm_eng":"Yangsa-myeon"},

{"cd":"23510390","nm_kor":"송해면","nm_eng":"Songhae-myeon"},

{"cd":"23510400","nm_kor":"교동면","nm_eng":"Gyodong-myeon"},

{"cd":"23510410","nm_kor":"삼산면","nm_eng":"Samsan-myeon"},

{"cd":"23510420","nm_kor":"서도면","nm_eng":"Seodo-myeon"},

{"cd":"23520000","nm_kor":"옹진군","nm_eng":"Ongjin-gun"},

{"cd":"23520310","nm_kor":"북도면","nm_eng":"Bukdo-myeon"},

{"cd":"23520330","nm_kor":"백령면","nm_eng":"Baengnyeong-myeon"},

{"cd":"23520340","nm_kor":"대청면","nm_eng":"Daecheong-myeon"},

{"cd":"23520350","nm_kor":"덕적면","nm_eng":"Deokjeok-myeon"},

{"cd":"23520370","nm_kor":"영흥면","nm_eng":"Yeongheung-myeon"},

{"cd":"23520360","nm_kor":"자월면","nm_eng":"Jawol-myeon"},

{"cd":"23520320","nm_kor":"연평면","nm_eng":"Yeonpyeong-myeon"},

{"cd":"24000000","nm_kor":"광주광역시","nm_eng":"Gwangju"},

{"cd":"24010000","nm_kor":"동구","nm_eng":"Dong-gu"},

{"cd":"24010510","nm_kor":"충장동","nm_eng":"Chungjang-dong"},

{"cd":"24010540","nm_kor":"동명동","nm_eng":"Dongmyeong-dong"},

{"cd":"24010560","nm_kor":"계림1동","nm_eng":"Gyerim 1(il)-dong"},

{"cd":"24010580","nm_kor":"계림2동","nm_eng":"Gyerim 2(i)-dong"},

{"cd":"24010590","nm_kor":"산수1동","nm_eng":"Sansu 1(il)-dong"},

{"cd":"24010610","nm_kor":"산수2동","nm_eng":"Sansu 2(i)-dong"},

{"cd":"24010620","nm_kor":"지산1동","nm_eng":"Jisan 1(il)-dong"},

{"cd":"24010630","nm_kor":"지산2동","nm_eng":"Jisan 2(i)-dong"},

{"cd":"24010640","nm_kor":"서남동","nm_eng":"Seonam-dong"},

{"cd":"24010680","nm_kor":"학동","nm_eng":"Hak-dong"},

{"cd":"24010710","nm_kor":"학운동","nm_eng":"Hagun-dong"},

{"cd":"24010720","nm_kor":"지원1동","nm_eng":"Jiwon 1(il)-dong"},

{"cd":"24010730","nm_kor":"지원2동","nm_eng":"Jiwon 2(i)-dong"},

{"cd":"24020000","nm_kor":"서구","nm_eng":"Seo-gu"},

{"cd":"24020510","nm_kor":"양동","nm_eng":"Yang-dong"},

{"cd":"24020530","nm_kor":"양3동","nm_eng":"Yang 3(sam)-dong"},

{"cd":"24020540","nm_kor":"농성1동","nm_eng":"Nongseong 1(il)-dong"},

{"cd":"24020550","nm_kor":"농성2동","nm_eng":"Nongseong 2(i)-dong"},

{"cd":"24020560","nm_kor":"광천동","nm_eng":"Gwangcheon-dong"},

{"cd":"24020570","nm_kor":"유덕동","nm_eng":"Yudeok-dong"},

{"cd":"24020660","nm_kor":"치평동","nm_eng":"Chipyeong-dong"},

{"cd":"24020580","nm_kor":"상무1동","nm_eng":"Sangmu 1(il)-dong"},

{"cd":"24020590","nm_kor":"상무2동","nm_eng":"Sangmu 2(i)-dong"},

{"cd":"24020600","nm_kor":"화정1동","nm_eng":"Hwajeong 1(il)-dong"},

{"cd":"24020610","nm_kor":"화정2동","nm_eng":"Hwajeong 2(i)-dong"},

{"cd":"24020620","nm_kor":"화정3동","nm_eng":"Hwajeong 3(sam)-dong"},

{"cd":"24020630","nm_kor":"화정4동","nm_eng":"Hwajeong 4(sa)-dong"},

{"cd":"24020640","nm_kor":"서창동","nm_eng":"Seochang-dong"},

{"cd":"24020680","nm_kor":"금호1동","nm_eng":"Geumho 1(il)-dong"},

{"cd":"24020690","nm_kor":"금호2동","nm_eng":"Geumho 2(i)-dong"},

{"cd":"24020670","nm_kor":"풍암동","nm_eng":"Pungam-dong"},

{"cd":"24020700","nm_kor":"동천동","nm_eng":"Dongcheon-dong"},

{"cd":"24030000","nm_kor":"남구","nm_eng":"Nam-gu"},

{"cd":"24030510","nm_kor":"양림동","nm_eng":"Yangnim-dong"},

{"cd":"24030520","nm_kor":"방림1동","nm_eng":"Bangnim 1(il)-dong"},

{"cd":"24030530","nm_kor":"방림2동","nm_eng":"Bangnim 2(i)-dong"},

{"cd":"24030680","nm_kor":"봉선1동","nm_eng":"Bongseon 1(il)-dong"},

{"cd":"24030690","nm_kor":"봉선2동","nm_eng":"Bongseon 2(i)-dong"},

{"cd":"24030540","nm_kor":"사직동","nm_eng":"Sajik-dong"},

{"cd":"24030570","nm_kor":"월산동","nm_eng":"Wolsan-dong"},

{"cd":"24030600","nm_kor":"월산4동","nm_eng":"Wolsan 4(sa)-dong"},

{"cd":"24030610","nm_kor":"월산5동","nm_eng":"Wolsan 5(o)-dong"},

{"cd":"24030620","nm_kor":"백운1동","nm_eng":"Baegun 1(il)-dong"},

{"cd":"24030630","nm_kor":"백운2동","nm_eng":"Baegun 2(i)-dong"},

{"cd":"24030640","nm_kor":"주월1동","nm_eng":"Juwol 1(il)-dong"},

{"cd":"24030650","nm_kor":"주월2동","nm_eng":"Juwol 2(i)-dong"},

{"cd":"24030710","nm_kor":"진월동","nm_eng":"Jinwol-dong"},

{"cd":"24030720","nm_kor":"효덕동","nm_eng":"Hyodeok-dong"},

{"cd":"24030670","nm_kor":"송암동","nm_eng":"Songam-dong"},

{"cd":"24030700","nm_kor":"대촌동","nm_eng":"Daechon-dong"},

{"cd":"24040000","nm_kor":"북구","nm_eng":"Buk-gu"},

{"cd":"24040510","nm_kor":"중흥1동","nm_eng":"Jungheung 1(il)-dong"},

{"cd":"24040520","nm_kor":"중흥2동","nm_eng":"Jungheung 2(i)-dong"},

{"cd":"24040530","nm_kor":"중흥3동","nm_eng":"Jungheung 3(sam)-dong"},

{"cd":"24040540","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"24040550","nm_kor":"임동","nm_eng":"Im-dong"},

{"cd":"24040560","nm_kor":"신안동","nm_eng":"Sinan-dong"},

{"cd":"24040570","nm_kor":"용봉동","nm_eng":"Yongbong-dong"},

{"cd":"24040580","nm_kor":"운암1동","nm_eng":"Unam 1(il)-dong"},

{"cd":"24040590","nm_kor":"운암2동","nm_eng":"Unam 2(i)-dong"},

{"cd":"24040600","nm_kor":"운암3동","nm_eng":"Unam 3(sam)-dong"},

{"cd":"24040610","nm_kor":"동림동","nm_eng":"Dongnim-dong"},

{"cd":"24040620","nm_kor":"우산동","nm_eng":"Usan-dong"},

{"cd":"24040630","nm_kor":"풍향동","nm_eng":"Punghyang-dong"},

{"cd":"24040640","nm_kor":"문화동","nm_eng":"Munhwa-dong"},

{"cd":"24040650","nm_kor":"문흥1동","nm_eng":"Munheung 1(il)-dong"},

{"cd":"24040660","nm_kor":"문흥2동","nm_eng":"Munheung 2(i)-dong"},

{"cd":"24040670","nm_kor":"두암1동","nm_eng":"Duam 1(il)-dong"},

{"cd":"24040680","nm_kor":"두암2동","nm_eng":"Duam 2(i)-dong"},

{"cd":"24040690","nm_kor":"두암3동","nm_eng":"Duam 3(sam)-dong"},

{"cd":"24040700","nm_kor":"삼각동","nm_eng":"Samgak-dong"},

{"cd":"24040780","nm_kor":"일곡동","nm_eng":"Ilgok-dong"},

{"cd":"24040710","nm_kor":"매곡동","nm_eng":"Maegok-dong"},

{"cd":"24040720","nm_kor":"오치1동","nm_eng":"Ochi 1(il)-dong"},

{"cd":"24040730","nm_kor":"오치2동","nm_eng":"Ochi 2(i)-dong"},

{"cd":"24040740","nm_kor":"석곡동","nm_eng":"Seokgok-dong"},

{"cd":"24040810","nm_kor":"건국동","nm_eng":"Geonguk-dong"},

{"cd":"24040800","nm_kor":"양산동","nm_eng":"yangsan-dong"},

{"cd":"24040820","nm_kor":"신용동","nm_eng":"Sinyong-dong"},

{"cd":"24050000","nm_kor":"광산구","nm_eng":"Gwangsan-gu"},

{"cd":"24050510","nm_kor":"송정1동","nm_eng":"Songjeong 1(il)-dong"},

{"cd":"24050520","nm_kor":"송정2동","nm_eng":"Songjeong 2(i)-dong"},

{"cd":"24050540","nm_kor":"도산동","nm_eng":"Dosan-dong"},

{"cd":"24050550","nm_kor":"신흥동","nm_eng":"Sinheung-dong"},

{"cd":"24050560","nm_kor":"어룡동","nm_eng":"Eoryong-dong"},

{"cd":"24050580","nm_kor":"우산동","nm_eng":"Usan-dong"},

{"cd":"24050590","nm_kor":"월곡1동","nm_eng":"Wolgok 1(il)-dong"},

{"cd":"24050600","nm_kor":"월곡2동","nm_eng":"Wolgok 2(i)-dong"},

{"cd":"24050610","nm_kor":"비아동","nm_eng":"Bia-dong"},

{"cd":"24050690","nm_kor":"첨단1동","nm_eng":"Cheomdan 1(il)-dong"},

{"cd":"24050700","nm_kor":"첨단2동","nm_eng":"Cheomdan 2(i)-dong"},

{"cd":"24050740","nm_kor":"신가동","nm_eng":"Singa-dong"},

{"cd":"24050710","nm_kor":"운남동","nm_eng":"Unnam-dong"},

{"cd":"24050750","nm_kor":"수완동","nm_eng":"Suwan-dong"},

{"cd":"24050630","nm_kor":"하남동","nm_eng":"Hanam-dong"},

{"cd":"24050640","nm_kor":"임곡동","nm_eng":"Imgok-dong"},

{"cd":"24050650","nm_kor":"동곡동","nm_eng":"Donggok-dong"},

{"cd":"24050660","nm_kor":"평동","nm_eng":"Pyeong-dong"},

{"cd":"24050670","nm_kor":"삼도동","nm_eng":"Samdo-dong"},

{"cd":"24050680","nm_kor":"본량동","nm_eng":"Bolyang-dong"},

{"cd":"24050730","nm_kor":"신창동","nm_eng":"Sinchang-dong"},

{"cd":"25000000","nm_kor":"대전광역시","nm_eng":"Daejeon"},

{"cd":"25010000","nm_kor":"동구","nm_eng":"Dong-gu"},

{"cd":"25010760","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"25010530","nm_kor":"효동","nm_eng":"Hyo-dong"},

{"cd":"25010770","nm_kor":"신인동","nm_eng":"Sinin-dong"},

{"cd":"25010550","nm_kor":"판암1동","nm_eng":"Panam 1(il)-dong"},

{"cd":"25010560","nm_kor":"판암2동","nm_eng":"Panam 2(i)-dong"},

{"cd":"25010570","nm_kor":"용운동","nm_eng":"Yongun-dong"},

{"cd":"25010780","nm_kor":"대동","nm_eng":"Dae-dong"},

{"cd":"25010600","nm_kor":"자양동","nm_eng":"Jayang-dong"},

{"cd":"25010630","nm_kor":"가양1동","nm_eng":"Gayang 1(il)-dong"},

{"cd":"25010640","nm_kor":"가양2동","nm_eng":"Gayang 2(i)-dong"},

{"cd":"25010650","nm_kor":"용전동","nm_eng":"Yongjeon-dong"},

{"cd":"25010790","nm_kor":"성남동","nm_eng":"Seongnam-dong"},

{"cd":"25010680","nm_kor":"홍도동","nm_eng":"Hongdo-dong"},

{"cd":"25010800","nm_kor":"삼성동","nm_eng":"Samseong-dong"},

{"cd":"25010730","nm_kor":"대청동","nm_eng":"Daecheong-dong"},

{"cd":"25010750","nm_kor":"산내동","nm_eng":"Sannae-dong"},

{"cd":"25020000","nm_kor":"중구","nm_eng":"Jung-gu"},

{"cd":"25020510","nm_kor":"은행선화동","nm_eng":"Eunhaengseonhwa-dong"},

{"cd":"25020530","nm_kor":"목동","nm_eng":"Mok-dong"},

{"cd":"25020540","nm_kor":"중촌동","nm_eng":"Jungchon-dong"},

{"cd":"25020550","nm_kor":"대흥동","nm_eng":"Daeheung-dong"},

{"cd":"25020560","nm_kor":"문창동","nm_eng":"Munchang-dong"},

{"cd":"25020570","nm_kor":"석교동","nm_eng":"Seokgyo-dong"},

{"cd":"25020580","nm_kor":"대사동","nm_eng":"Daesa-dong"},

{"cd":"25020590","nm_kor":"부사동","nm_eng":"Busa-dong"},

{"cd":"25020600","nm_kor":"용두동","nm_eng":"Yongdu-dong"},

{"cd":"25020620","nm_kor":"오류동","nm_eng":"Oryu-dong"},

{"cd":"25020630","nm_kor":"태평1동","nm_eng":"Taepyeong 1(il)-dong"},

{"cd":"25020640","nm_kor":"태평2동","nm_eng":"Taepyeong 2(i)-dong"},

{"cd":"25020650","nm_kor":"유천1동","nm_eng":"Yucheon 1(il)-dong"},

{"cd":"25020660","nm_kor":"유천2동","nm_eng":"Yucheon 2(i)-dong"},

{"cd":"25020670","nm_kor":"문화1동","nm_eng":"Munhwa 1(il)-dong"},

{"cd":"25020680","nm_kor":"문화2동","nm_eng":"Munhwa 2(i)-dong"},

{"cd":"25020690","nm_kor":"산성동","nm_eng":"Sanseong-dong"},

{"cd":"25030000","nm_kor":"서구","nm_eng":"Seo-gu"},

{"cd":"25030510","nm_kor":"복수동","nm_eng":"Boksu-dong"},

{"cd":"25030520","nm_kor":"도마1동","nm_eng":"Doma 1(il)-dong"},

{"cd":"25030530","nm_kor":"도마2동","nm_eng":"Doma 2(i)-dong"},

{"cd":"25030540","nm_kor":"정림동","nm_eng":"Jeongnim-dong"},

{"cd":"25030550","nm_kor":"변동","nm_eng":"Byeon-dong"},

{"cd":"25030560","nm_kor":"용문동","nm_eng":"Yongmun-dong"},

{"cd":"25030570","nm_kor":"탄방동","nm_eng":"Tanbang-dong"},

{"cd":"25030610","nm_kor":"괴정동","nm_eng":"Goejeong-dong"},

{"cd":"25030620","nm_kor":"가장동","nm_eng":"Gajang-dong"},

{"cd":"25030630","nm_kor":"내동","nm_eng":"Nae-dong"},

{"cd":"25030640","nm_kor":"갈마1동","nm_eng":"Galma 1(il)-dong"},

{"cd":"25030650","nm_kor":"갈마2동","nm_eng":"Galma 2(i)-dong"},

{"cd":"25030660","nm_kor":"월평1동","nm_eng":"Wolpyeong 1(il)-dong"},

{"cd":"25030670","nm_kor":"월평2동","nm_eng":"Wolpyeong 2(i)-dong"},

{"cd":"25030680","nm_kor":"월평3동","nm_eng":"Wolpyeong 3(sam)-dong"},

{"cd":"25030511","nm_kor":"가수원동","nm_eng":"Gasuwon-dong"},

{"cd":"25030512","nm_kor":"도안동","nm_eng":"Doan-dong"},

{"cd":"25030720","nm_kor":"관저1동","nm_eng":"Gwanjeo 1(il)-dong"},

{"cd":"25030730","nm_kor":"관저2동","nm_eng":"Gwanjeo 2(i)-dong"},

{"cd":"25030710","nm_kor":"기성동","nm_eng":"Giseong-dong"},

{"cd":"25030590","nm_kor":"둔산1동","nm_eng":"Dunsan 1(il)-dong"},

{"cd":"25030600","nm_kor":"둔산2동","nm_eng":"Dunsan 2(i)-dong"},

{"cd":"25030690","nm_kor":"만년동","nm_eng":"Mannyeon-dong"},

{"cd":"25030740","nm_kor":"둔산3동","nm_eng":"Dunsan 3(sam)-dong"},

{"cd":"25040000","nm_kor":"유성구","nm_eng":"Yuseong-gu"},

{"cd":"25040680","nm_kor":"진잠동","nm_eng":"Jinjam-dong"},

{"cd":"25040690","nm_kor":"학하동","nm_eng":"Hakha-dong"},

{"cd":"25040700","nm_kor":"상대동","nm_eng":"Sangdae-dong"},

{"cd":"25040640","nm_kor":"온천1동","nm_eng":"Oncheon 1(il)-dong"},

{"cd":"25040540","nm_kor":"온천2동","nm_eng":"Oncheon 2(i)-dong"},

{"cd":"25040590","nm_kor":"노은1동","nm_eng":"Noeun 1(il)-dong"},

{"cd":"25040660","nm_kor":"노은2동","nm_eng":"Noeun 2(i)-dong"},

{"cd":"25040670","nm_kor":"노은3동","nm_eng":"Noeun 3(sam)-dong"},

{"cd":"25040550","nm_kor":"신성동","nm_eng":"Sinseong-dong"},

{"cd":"25040570","nm_kor":"전민동","nm_eng":"Jeonmin-dong"},

{"cd":"25040610","nm_kor":"구즉동","nm_eng":"Gujeuk-dong"},

{"cd":"25040630","nm_kor":"관평동","nm_eng":"Gwanpyeong-dong"},

{"cd":"25040710","nm_kor":"원신흥동","nm_eng":"Wonsinheung-dong"},

{"cd":"25050000","nm_kor":"대덕구","nm_eng":"Daedeok-gu"},

{"cd":"25050510","nm_kor":"오정동","nm_eng":"Ojeong-dong"},

{"cd":"25050520","nm_kor":"대화동","nm_eng":"Daehwa-dong"},

{"cd":"25050530","nm_kor":"회덕동","nm_eng":"Hoedeok-dong"},

{"cd":"25050540","nm_kor":"비래동","nm_eng":"Birae-dong"},

{"cd":"25050620","nm_kor":"송촌동","nm_eng":"Songchon-dong"},

{"cd":"25050550","nm_kor":"중리동","nm_eng":"Jungni-dong"},

{"cd":"25050580","nm_kor":"신탄진동","nm_eng":"Sintanjin-dong"},

{"cd":"25050590","nm_kor":"석봉동","nm_eng":"Seokbong-dong"},

{"cd":"25050600","nm_kor":"덕암동","nm_eng":"Deogam-dong"},

{"cd":"25050610","nm_kor":"목상동","nm_eng":"Moksang-dong"},

{"cd":"25050560","nm_kor":"법1동","nm_eng":"Beop 1(il)-dong"},

{"cd":"25050570","nm_kor":"법2동","nm_eng":"Beop 2(i)-dong"},

{"cd":"26000000","nm_kor":"울산광역시","nm_eng":"Ulsan"},

{"cd":"26010000","nm_kor":"중구","nm_eng":"Jung-gu"},

{"cd":"26010510","nm_kor":"학성동","nm_eng":"Hakseong-dong"},

{"cd":"26010520","nm_kor":"반구1동","nm_eng":"Bangu 1(il)-dong"},

{"cd":"26010530","nm_kor":"반구2동","nm_eng":"Bangu 2(i)-dong"},

{"cd":"26010540","nm_kor":"복산1동","nm_eng":"Boksan 1(il)-dong"},

{"cd":"26010550","nm_kor":"복산2동","nm_eng":"Boksan 2(i)-dong"},

{"cd":"26010670","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"26010590","nm_kor":"우정동","nm_eng":"Ujeong-dong"},

{"cd":"26010600","nm_kor":"태화동","nm_eng":"Taehwa-dong"},

{"cd":"26010610","nm_kor":"다운동","nm_eng":"Daun-dong"},

{"cd":"26010620","nm_kor":"병영1동","nm_eng":"Byeongyeong 1(il)-dong"},

{"cd":"26010630","nm_kor":"병영2동","nm_eng":"Byeongyeong 2(i)-dong"},

{"cd":"26010640","nm_kor":"약사동","nm_eng":"Yaksa-dong"},

{"cd":"26010660","nm_kor":"성안동","nm_eng":"Seongan-dong"},

{"cd":"26020000","nm_kor":"남구","nm_eng":"Nam-gu"},

{"cd":"26020510","nm_kor":"신정1동","nm_eng":"Sinjeong 1(il)-dong"},

{"cd":"26020520","nm_kor":"신정2동","nm_eng":"Sinjeong 2(i)-dong"},

{"cd":"26020530","nm_kor":"신정3동","nm_eng":"Sinjeong 3(sam)-dong"},

{"cd":"26020540","nm_kor":"신정4동","nm_eng":"Sinjeong 4(sa)-dong"},

{"cd":"26020550","nm_kor":"신정5동","nm_eng":"Sinjeong 5(o)-dong"},

{"cd":"26020560","nm_kor":"달동","nm_eng":"Dal-dong"},

{"cd":"26020570","nm_kor":"삼산동","nm_eng":"Samsan-dong"},

{"cd":"26020580","nm_kor":"삼호동","nm_eng":"Samho-dong"},

{"cd":"26020590","nm_kor":"무거동","nm_eng":"Mugeo-dong"},

{"cd":"26020600","nm_kor":"옥동","nm_eng":"Ok-dong"},

{"cd":"26020620","nm_kor":"대현동","nm_eng":"Daehyeon-dong"},

{"cd":"26020630","nm_kor":"수암동","nm_eng":"Suam-dong"},

{"cd":"26020640","nm_kor":"선암동","nm_eng":"Seonam-dong"},

{"cd":"26020610","nm_kor":"야음장생포동","nm_eng":"Yaeumjangsaengpo-dong"},

{"cd":"26030000","nm_kor":"동구","nm_eng":"Dong-gu"},

{"cd":"26030510","nm_kor":"방어동","nm_eng":"Bangeo-dong"},

{"cd":"26030520","nm_kor":"일산동","nm_eng":"Ilsan-dong"},

{"cd":"26030530","nm_kor":"화정동","nm_eng":"Hwajeong-dong"},

{"cd":"26030540","nm_kor":"대송동","nm_eng":"Daesong-dong"},

{"cd":"26030550","nm_kor":"전하1동","nm_eng":"Jeonha 1(il)-dong"},

{"cd":"26030610","nm_kor":"전하2동","nm_eng":"Jeonha 2(i)-dong"},

{"cd":"26030580","nm_kor":"남목1동","nm_eng":"Nammok 1(il)-dong"},

{"cd":"26030590","nm_kor":"남목2동","nm_eng":"Nammok 2(i)-dong"},

{"cd":"26030600","nm_kor":"남목3동","nm_eng":"Nammok 3(sam)-dong"},

{"cd":"26040000","nm_kor":"북구","nm_eng":"Buk-gu"},

{"cd":"26040510","nm_kor":"농소1동","nm_eng":"Nongso 1(il)-dong"},

{"cd":"26040520","nm_kor":"농소2동","nm_eng":"Nongso 2(i)-dong"},

{"cd":"26040530","nm_kor":"농소3동","nm_eng":"Nongso 3(sam)-dong"},

{"cd":"26040540","nm_kor":"강동동","nm_eng":"Gangdong-dong"},

{"cd":"26040560","nm_kor":"효문동","nm_eng":"Hyomun-dong"},

{"cd":"26040570","nm_kor":"송정동","nm_eng":"Songjeong-dong"},

{"cd":"26040580","nm_kor":"양정동","nm_eng":"Yangjeong-dong"},

{"cd":"26040590","nm_kor":"염포동","nm_eng":"Yeompo-dong"},

{"cd":"26510000","nm_kor":"울주군","nm_eng":"Ulju-gun"},

{"cd":"26510110","nm_kor":"온산읍","nm_eng":"Onsan-eup"},

{"cd":"26510120","nm_kor":"언양읍","nm_eng":"Eonyang-eup"},

{"cd":"26510130","nm_kor":"온양읍","nm_eng":"Onyang-eup"},

{"cd":"26510140","nm_kor":"범서읍","nm_eng":"Beomseo-eup"},

{"cd":"26510150","nm_kor":"청량읍","nm_eng":"Cheongnyang-eup"},

{"cd":"26510160","nm_kor":"삼남읍","nm_eng":"Samnam-eup"},

{"cd":"26510310","nm_kor":"서생면","nm_eng":"Seosaeng-myeon"},

{"cd":"26510340","nm_kor":"웅촌면","nm_eng":"Ungchon-myeon"},

{"cd":"26510360","nm_kor":"두동면","nm_eng":"Dudong-myeon"},

{"cd":"26510370","nm_kor":"두서면","nm_eng":"Duseo-myeon"},

{"cd":"26510380","nm_kor":"상북면","nm_eng":"Sangbuk-myeon"},

{"cd":"26510400","nm_kor":"삼동면","nm_eng":"Samdong-myeon"},

{"cd":"29000000","nm_kor":"세종특별자치시","nm_eng":"Sejong City"},

{"cd":"29010000","nm_kor":"세종특별자치시","nm_eng":"Sejong City"},

{"cd":"29010110","nm_kor":"조치원읍","nm_eng":"Jochiwon-eup"},

{"cd":"29010311","nm_kor":"연기면","nm_eng":"Yeongi-myeon"},

{"cd":"29010312","nm_kor":"연동면","nm_eng":"YeonDong-myeon"},

{"cd":"29010330","nm_kor":"부강면","nm_eng":"Bugang-myeon"},

{"cd":"29010340","nm_kor":"금남면","nm_eng":"Geumnam-myeon"},

{"cd":"29010350","nm_kor":"장군면","nm_eng":"janggun-myeon"},

{"cd":"29010360","nm_kor":"연서면","nm_eng":"YeonSeo-myeon"},

{"cd":"29010370","nm_kor":"전의면","nm_eng":"Jeonui-myeon"},

{"cd":"29010380","nm_kor":"전동면","nm_eng":"Jeondong-myeon"},

{"cd":"29010390","nm_kor":"소정면","nm_eng":"Sojeong-myeon"},

{"cd":"29010610","nm_kor":"한솔동","nm_eng":"Hansol-dong"},

{"cd":"29010511","nm_kor":"새롬동","nm_eng":"Saerom-dong"},

{"cd":"29010690","nm_kor":"도담동","nm_eng":"Dodam-dong"},

{"cd":"29010512","nm_kor":"해밀동","nm_eng":"Haemil-dong"},

{"cd":"29010590","nm_kor":"아름동","nm_eng":"Arum-dong"},

{"cd":"29010560","nm_kor":"종촌동","nm_eng":"Jongchon-dong"},

{"cd":"29010600","nm_kor":"고운동","nm_eng":"Goun-dong"},

{"cd":"29010710","nm_kor":"소담동","nm_eng":"Sodam-dong"},

{"cd":"29010513","nm_kor":"반곡동","nm_eng":"Bangok-dong"},

{"cd":"29010660","nm_kor":"보람동","nm_eng":"Boram-dong"},

{"cd":"29010640","nm_kor":"대평동","nm_eng":"Daepyeong-dong"},

{"cd":"29010680","nm_kor":"다정동","nm_eng":"Dajeong-dong"},

{"cd":"31000000","nm_kor":"경기도","nm_eng":"Gyeonggi-do"},

{"cd":"31010000","nm_kor":"수원시","nm_eng":"Suwon-si"},

{"cd":"31011000","nm_kor":"장안구","nm_eng":"Jangan-gu"},

{"cd":"31011540","nm_kor":"파장동","nm_eng":"Pajang-dong"},

{"cd":"31011550","nm_kor":"율천동","nm_eng":"Yulcheon-dong"},

{"cd":"31011560","nm_kor":"정자1동","nm_eng":"Jeongja 1(il)-dong"},

{"cd":"31011570","nm_kor":"정자2동","nm_eng":"Jeongja 2(i)-dong"},

{"cd":"31011620","nm_kor":"정자3동","nm_eng":"Jeongja 3(sam)-dong"},

{"cd":"31011580","nm_kor":"영화동","nm_eng":"Yeonghwa-dong"},

{"cd":"31011590","nm_kor":"송죽동","nm_eng":"Songjuk-dong"},

{"cd":"31011600","nm_kor":"조원1동","nm_eng":"Jowon 1(il)-dong"},

{"cd":"31011630","nm_kor":"조원2동","nm_eng":"Jowon 2(i)-dong"},

{"cd":"31011610","nm_kor":"연무동","nm_eng":"Yeonmu-dong"},

{"cd":"31012000","nm_kor":"권선구","nm_eng":"Gwonseon-gu"},

{"cd":"31012520","nm_kor":"세류1동","nm_eng":"Seryu 1(il)-dong"},

{"cd":"31012530","nm_kor":"세류2동","nm_eng":"Seryu 2(i)-dong"},

{"cd":"31012540","nm_kor":"세류3동","nm_eng":"Seryu 3(sam)-dong"},

{"cd":"31012550","nm_kor":"평동","nm_eng":"Pyeong-dong"},

{"cd":"31012560","nm_kor":"서둔동","nm_eng":"Seodun-dong"},

{"cd":"31012570","nm_kor":"구운동","nm_eng":"Guun-dong"},

{"cd":"31012650","nm_kor":"금곡동","nm_eng":"Geumgok-dong"},

{"cd":"31012660","nm_kor":"호매실동","nm_eng":"Homaesil-dong"},

{"cd":"31012600","nm_kor":"권선1동","nm_eng":"Gwonseon 1(il)-dong"},

{"cd":"31012640","nm_kor":"권선2동","nm_eng":"Gwonseon 2(i)-dong"},

{"cd":"31012610","nm_kor":"곡선동","nm_eng":"Gokseon-dong"},

{"cd":"31012620","nm_kor":"입북동","nm_eng":"Ipbuk-dong"},

{"cd":"31013000","nm_kor":"팔달구","nm_eng":"Paldal-gu"},

{"cd":"31013670","nm_kor":"매교동","nm_eng":"Maegyo-dong"},

{"cd":"31013680","nm_kor":"매산동","nm_eng":"Maesan-dong"},

{"cd":"31013690","nm_kor":"고등동","nm_eng":"Godeung-dong"},

{"cd":"31013700","nm_kor":"화서1동","nm_eng":"Hwaseo 1(il)-dong"},

{"cd":"31013710","nm_kor":"화서2동","nm_eng":"Hwaseo 2(i)-dong"},

{"cd":"31013530","nm_kor":"지동","nm_eng":"Ji-dong"},

{"cd":"31013540","nm_kor":"우만1동","nm_eng":"Uman 1(il)-dong"},

{"cd":"31013550","nm_kor":"우만2동","nm_eng":"Uman 2(i)-dong"},

{"cd":"31013560","nm_kor":"인계동","nm_eng":"Ingye-dong"},

{"cd":"31013720","nm_kor":"행궁동","nm_eng":"Haenggung-dong"},

{"cd":"31014000","nm_kor":"영통구","nm_eng":"Yeongtong-gu"},

{"cd":"31014510","nm_kor":"매탄1동","nm_eng":"Maetan 1(il)-dong"},

{"cd":"31014520","nm_kor":"매탄2동","nm_eng":"Maetan 2(i)-dong"},

{"cd":"31014530","nm_kor":"매탄3동","nm_eng":"Maetan 3(sam)-dong"},

{"cd":"31014540","nm_kor":"매탄4동","nm_eng":"Maetan 4(sa)-dong"},

{"cd":"31014600","nm_kor":"원천동","nm_eng":"Woncheon-dong"},

{"cd":"31014640","nm_kor":"영통1동","nm_eng":"Yeongtong 1(il)-dong"},

{"cd":"31014650","nm_kor":"영통2동","nm_eng":"Yeongtong 2(i)-dong"},

{"cd":"31014660","nm_kor":"영통3동","nm_eng":"Yeongtong 3(sam)-dong"},

{"cd":"31014670","nm_kor":"망포1동","nm_eng":"Mangpo 1(il)-dong"},

{"cd":"31014680","nm_kor":"망포2동","nm_eng":"Mangpo 2(i)-dong"},

{"cd":"31014620","nm_kor":"광교1동","nm_eng":"Gwoanggyo 1(il)-dong"},

{"cd":"31014630","nm_kor":"광교2동","nm_eng":"Gwoanggyo 2(i)-dong"},

{"cd":"31020000","nm_kor":"성남시","nm_eng":"Seongnam-si"},

{"cd":"31021000","nm_kor":"수정구","nm_eng":"Sujeong-gu"},

{"cd":"31021510","nm_kor":"신흥1동","nm_eng":"Sinheung 1(il)-dong"},

{"cd":"31021520","nm_kor":"신흥2동","nm_eng":"Sinheung 2(i)-dong"},

{"cd":"31021530","nm_kor":"신흥3동","nm_eng":"Sinheung 3(sam)-dong"},

{"cd":"31021540","nm_kor":"태평1동","nm_eng":"Taepyeong 1(il)-dong"},

{"cd":"31021550","nm_kor":"태평2동","nm_eng":"Taepyeong 2(i)-dong"},

{"cd":"31021560","nm_kor":"태평3동","nm_eng":"Taepyeong 3(sam)-dong"},

{"cd":"31021570","nm_kor":"태평4동","nm_eng":"Taepyeong 4(sa)-dong"},

{"cd":"31021580","nm_kor":"수진1동","nm_eng":"Sujin 1(il)-dong"},

{"cd":"31021590","nm_kor":"수진2동","nm_eng":"Sujin 2(i)-dong"},

{"cd":"31021600","nm_kor":"단대동","nm_eng":"Dandae-dong"},

{"cd":"31021610","nm_kor":"산성동","nm_eng":"Sanseong-dong"},

{"cd":"31021620","nm_kor":"양지동","nm_eng":"Yangji-dong"},

{"cd":"31021670","nm_kor":"복정동","nm_eng":"Bokjeong-dong"},

{"cd":"31021680","nm_kor":"위례동","nm_eng":"wirye-dong"},

{"cd":"31021640","nm_kor":"신촌동","nm_eng":"Sinchon-dong"},

{"cd":"31021650","nm_kor":"고등동","nm_eng":"Godeung-dong"},

{"cd":"31021660","nm_kor":"시흥동","nm_eng":"Siheung-dong"},

{"cd":"31022000","nm_kor":"중원구","nm_eng":"Jungwon-gu"},

{"cd":"31022510","nm_kor":"성남동","nm_eng":"Seongnam-dong"},

{"cd":"31022620","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"31022530","nm_kor":"금광1동","nm_eng":"Geumgwang 1(il)-dong"},

{"cd":"31022540","nm_kor":"금광2동","nm_eng":"Geumgwang 2(i)-dong"},

{"cd":"31022550","nm_kor":"은행1동","nm_eng":"Eunhaeng 1(il)-dong"},

{"cd":"31022560","nm_kor":"은행2동","nm_eng":"Eunhaeng 2(i)-dong"},

{"cd":"31022570","nm_kor":"상대원1동","nm_eng":"Sangdaewon 1(il)-dong"},

{"cd":"31022580","nm_kor":"상대원2동","nm_eng":"Sangdaewon 2(i)-dong"},

{"cd":"31022590","nm_kor":"상대원3동","nm_eng":"Sangdaewon 3(sam)-dong"},

{"cd":"31022600","nm_kor":"하대원동","nm_eng":"Hadaewon-dong"},

{"cd":"31022610","nm_kor":"도촌동","nm_eng":"Dochon-dong"},

{"cd":"31023000","nm_kor":"분당구","nm_eng":"Bundang-gu"},

{"cd":"31023510","nm_kor":"분당동","nm_eng":"Bundang-dong"},

{"cd":"31023530","nm_kor":"수내1동","nm_eng":"Sunae 1(il)-dong"},

{"cd":"31023540","nm_kor":"수내2동","nm_eng":"Sunae 2(i)-dong"},

{"cd":"31023520","nm_kor":"수내3동","nm_eng":"Sunae 3(sam)-dong"},

{"cd":"31023780","nm_kor":"정자동","nm_eng":"Jeongja-dong"},

{"cd":"31023770","nm_kor":"정자1동","nm_eng":"Jeongja 1(il)-dong"},

{"cd":"31023550","nm_kor":"정자2동","nm_eng":"Jeongja 2(i)-dong"},

{"cd":"31023560","nm_kor":"정자3동","nm_eng":"Jeongja 3(sam)-dong"},

{"cd":"31023580","nm_kor":"서현1동","nm_eng":"Seohyeon 1(il)-dong"},

{"cd":"31023590","nm_kor":"서현2동","nm_eng":"Seohyeon 2(i)-dong"},

{"cd":"31023600","nm_kor":"이매1동","nm_eng":"Imae 1(il)-dong"},

{"cd":"31023610","nm_kor":"이매2동","nm_eng":"Imae 2(i)-dong"},

{"cd":"31023620","nm_kor":"야탑1동","nm_eng":"Yatap 1(il)-dong"},

{"cd":"31023640","nm_kor":"야탑2동","nm_eng":"Yatap 2(i)-dong"},

{"cd":"31023630","nm_kor":"야탑3동","nm_eng":"Yatap 3(sam)-dong"},

{"cd":"31023750","nm_kor":"판교동","nm_eng":"Pangyo-dong"},

{"cd":"31023740","nm_kor":"삼평동","nm_eng":"Sampyeong-dong"},

{"cd":"31023760","nm_kor":"백현동","nm_eng":"Baekhyeon-dong"},

{"cd":"31023710","nm_kor":"금곡동","nm_eng":"Geumgok-dong"},

{"cd":"31023720","nm_kor":"구미1동","nm_eng":"Gumi 1(il)-dong"},

{"cd":"31023670","nm_kor":"구미동","nm_eng":"Gumi-dong"},

{"cd":"31023680","nm_kor":"운중동","nm_eng":"Unjung-dong"},

{"cd":"31030000","nm_kor":"의정부시","nm_eng":"Uijeongbu-si"},

{"cd":"31030690","nm_kor":"의정부1동","nm_eng":"Uijeongbu 1(il)-dong"},

{"cd":"31030520","nm_kor":"의정부2동","nm_eng":"Uijeongbu 2(i)-dong"},

{"cd":"31030550","nm_kor":"호원1동","nm_eng":"Howon 1(il)-dong"},

{"cd":"31030650","nm_kor":"호원2동","nm_eng":"Howon 2(i)-dong"},

{"cd":"31030560","nm_kor":"장암동","nm_eng":"Jangam-dong"},

{"cd":"31030570","nm_kor":"신곡1동","nm_eng":"Singok 1(il)-dong"},

{"cd":"31030580","nm_kor":"신곡2동","nm_eng":"Singok 2(i)-dong"},

{"cd":"31030590","nm_kor":"송산1동","nm_eng":"Songsan 1(il)-dong"},

{"cd":"31030700","nm_kor":"송산2동","nm_eng":"Songsan 2(i)-dong"},

{"cd":"31030710","nm_kor":"송산3동","nm_eng":"Songsan 3(sam)-dong"},

{"cd":"31030600","nm_kor":"자금동","nm_eng":"Jageum-dong"},

{"cd":"31030680","nm_kor":"가능동","nm_eng":"Ganeung-dong"},

{"cd":"31030670","nm_kor":"흥선동","nm_eng":"Heungsun-dong"},

{"cd":"31030640","nm_kor":"녹양동","nm_eng":"Nogyang-dong"},

{"cd":"31040000","nm_kor":"안양시","nm_eng":"Anyang-si"},

{"cd":"31041000","nm_kor":"만안구","nm_eng":"Manan-gu"},

{"cd":"31041510","nm_kor":"안양1동","nm_eng":"Anyang 1(il)-dong"},

{"cd":"31041520","nm_kor":"안양2동","nm_eng":"Anyang 2(i)-dong"},

{"cd":"31041530","nm_kor":"안양3동","nm_eng":"Anyang 3(sam)-dong"},

{"cd":"31041540","nm_kor":"안양4동","nm_eng":"Anyang 4(sa)-dong"},

{"cd":"31041550","nm_kor":"안양5동","nm_eng":"Anyang 5(o)-dong"},

{"cd":"31041560","nm_kor":"안양6동","nm_eng":"Anyang 6(yuk)-dong"},

{"cd":"31041570","nm_kor":"안양7동","nm_eng":"Anyang 7(chil)-dong"},

{"cd":"31041580","nm_kor":"안양8동","nm_eng":"Anyang 8(pal)-dong"},

{"cd":"31041590","nm_kor":"안양9동","nm_eng":"Anyang 9(gu)-dong"},

{"cd":"31041600","nm_kor":"석수1동","nm_eng":"Seoksu 1(il)-dong"},

{"cd":"31041610","nm_kor":"석수2동","nm_eng":"Seoksu 2(i)-dong"},

{"cd":"31041620","nm_kor":"석수3동","nm_eng":"Seoksu 3(sam)-dong"},

{"cd":"31041630","nm_kor":"박달1동","nm_eng":"Bakdal 1(il)-dong"},

{"cd":"31041640","nm_kor":"박달2동","nm_eng":"Bakdal 2(i)-dong"},

{"cd":"31042","nm_kor":"동안구","nm_eng":"Dongan-gu"},

{"cd":"31042510","nm_kor":"비산1동","nm_eng":"Bisan 1(il)-dong"},

{"cd":"31042520","nm_kor":"비산2동","nm_eng":"Bisan 2(i)-dong"},

{"cd":"31042530","nm_kor":"비산3동","nm_eng":"Bisan 3(sam)-dong"},

{"cd":"31042540","nm_kor":"부흥동","nm_eng":"Buheung-dong"},

{"cd":"31042550","nm_kor":"달안동","nm_eng":"Daran-dong"},

{"cd":"31042560","nm_kor":"관양1동","nm_eng":"Gwanyang 1(il)-dong"},

{"cd":"31042570","nm_kor":"관양2동","nm_eng":"Gwanyang 2(i)-dong"},

{"cd":"31042580","nm_kor":"부림동","nm_eng":"Burim-dong"},

{"cd":"31042590","nm_kor":"평촌동","nm_eng":"Pyeongchon-dong"},

{"cd":"31042600","nm_kor":"평안동","nm_eng":"Pyeongan-dong"},

{"cd":"31042610","nm_kor":"귀인동","nm_eng":"Gwiin-dong"},

{"cd":"31042620","nm_kor":"호계1동","nm_eng":"Hogye 1(il)-dong"},

{"cd":"31042630","nm_kor":"호계2동","nm_eng":"Hogye 2(i)-dong"},

{"cd":"31042640","nm_kor":"호계3동","nm_eng":"Hogye 3(sam)-dong"},

{"cd":"31042650","nm_kor":"범계동","nm_eng":"Beomgye-dong"},

{"cd":"31042660","nm_kor":"신촌동","nm_eng":"Sinchon-dong"},

{"cd":"31042670","nm_kor":"갈산동","nm_eng":"Galsan-dong"},

{"cd":"31050000","nm_kor":"부천시","nm_eng":"Bucheon-si"},

{"cd":"31050870","nm_kor":"심곡동","nm_eng":"Simgok-dong"},

{"cd":"31050880","nm_kor":"부천동","nm_eng":"Bucheon-dong"},

{"cd":"31050890","nm_kor":"중동","nm_eng":"Jung-dong"},

{"cd":"31050900","nm_kor":"신중동","nm_eng":"shinjung-dong"},

{"cd":"31050910","nm_kor":"상동","nm_eng":"Sang-dong"},

{"cd":"31050920","nm_kor":"대산동","nm_eng":"Daesan-dong"},

{"cd":"31050930","nm_kor":"소사본동","nm_eng":"Sosabon-dong"},

{"cd":"31050940","nm_kor":"범안동","nm_eng":"Beoman-dong"},

{"cd":"31050950","nm_kor":"성곡동","nm_eng":"Seonggok-dong"},

{"cd":"31050960","nm_kor":"오정동","nm_eng":"Ojeong-dong"},

{"cd":"31060000","nm_kor":"광명시","nm_eng":"Gwangmyeong-si"},

{"cd":"31060510","nm_kor":"광명1동","nm_eng":"Gwangmyeong 1(il)-dong"},

{"cd":"31060520","nm_kor":"광명2동","nm_eng":"Gwangmyeong 2(i)-dong"},

{"cd":"31060530","nm_kor":"광명3동","nm_eng":"Gwangmyeong 3(sam)-dong"},

{"cd":"31060540","nm_kor":"광명4동","nm_eng":"Gwangmyeong 4(sa)-dong"},

{"cd":"31060550","nm_kor":"광명5동","nm_eng":"Gwangmyeong 5(o)-dong"},

{"cd":"31060560","nm_kor":"광명6동","nm_eng":"Gwangmyeong 6(yuk)-dong"},

{"cd":"31060570","nm_kor":"광명7동","nm_eng":"Gwangmyeong 7(chil)-dong"},

{"cd":"31060580","nm_kor":"철산1동","nm_eng":"Cheolsan 1(il)-dong"},

{"cd":"31060590","nm_kor":"철산2동","nm_eng":"Cheolsan 2(i)-dong"},

{"cd":"31060600","nm_kor":"철산3동","nm_eng":"Cheolsan 3(sam)-dong"},

{"cd":"31060610","nm_kor":"철산4동","nm_eng":"Cheolsan 4(sa)-dong"},

{"cd":"31060620","nm_kor":"하안1동","nm_eng":"Haan 1(il)-dong"},

{"cd":"31060630","nm_kor":"하안2동","nm_eng":"Haan 2(i)-dong"},

{"cd":"31060640","nm_kor":"하안3동","nm_eng":"Haan 3(sam)-dong"},

{"cd":"31060650","nm_kor":"하안4동","nm_eng":"Haan 4(sa)-dong"},

{"cd":"31060660","nm_kor":"소하1동","nm_eng":"Soha 1(il)-dong"},

{"cd":"31060690","nm_kor":"소하2동","nm_eng":"Soha 2(i)-dong"},

{"cd":"31060700","nm_kor":"일직동","nm_eng":"Iljik-dong"},

{"cd":"31060680","nm_kor":"학온동","nm_eng":"Hagon-dong"},

{"cd":"31070000","nm_kor":"평택시","nm_eng":"Pyeongtaek-si"},

{"cd":"31070110","nm_kor":"팽성읍","nm_eng":"Paengseong-eup"},

{"cd":"31070120","nm_kor":"안중읍","nm_eng":"Anjung-eup"},

{"cd":"31070130","nm_kor":"포승읍","nm_eng":"Poseung-eup"},

{"cd":"31070140","nm_kor":"청북읍","nm_eng":"Cheongbuk-eup"},

{"cd":"31070310","nm_kor":"진위면","nm_eng":"Jinwi-myeon"},

{"cd":"31070320","nm_kor":"서탄면","nm_eng":"Seotan-myeon"},

{"cd":"31070330","nm_kor":"고덕면","nm_eng":"Godeok-myeon"},

{"cd":"31070340","nm_kor":"오성면","nm_eng":"Oseong-myeon"},

{"cd":"31070370","nm_kor":"현덕면","nm_eng":"Hyeondeok-myeon"},

{"cd":"31070510","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"31070520","nm_kor":"서정동","nm_eng":"Seojeong-dong"},

{"cd":"31070530","nm_kor":"송탄동","nm_eng":"Songtan-dong"},

{"cd":"31070550","nm_kor":"지산동","nm_eng":"Jisan-dong"},

{"cd":"31070560","nm_kor":"송북동","nm_eng":"Songbuk-dong"},

{"cd":"31070570","nm_kor":"신장1동","nm_eng":"Sinjang 1(il)-dong"},

{"cd":"31070580","nm_kor":"신장2동","nm_eng":"Sinjang 2(i)-dong"},

{"cd":"31070590","nm_kor":"신평동","nm_eng":"Sinpyeong-dong"},

{"cd":"31070600","nm_kor":"원평동","nm_eng":"Wonpyeong-dong"},

{"cd":"31070610","nm_kor":"통복동","nm_eng":"Tongbok-dong"},

{"cd":"31070670","nm_kor":"비전1동","nm_eng":"Bijeon 1(il)-dong"},

{"cd":"31070650","nm_kor":"비전2동","nm_eng":"Bijeon 2(i)-dong"},

{"cd":"31070660","nm_kor":"용이동","nm_eng":"Yongi-dong"},

{"cd":"31070640","nm_kor":"세교동","nm_eng":"Segyo-dong"},

{"cd":"31070680","nm_kor":"동삭동","nm_eng":"Dongsak-dong"},

{"cd":"31070690","nm_kor":"고덕동","nm_eng":"Godeok-dong"},

{"cd":"31080000","nm_kor":"동두천시","nm_eng":"Dongducheon-si"},

{"cd":"31080510","nm_kor":"생연1동","nm_eng":"Saengyeon 1(il)-dong"},

{"cd":"31080520","nm_kor":"생연2동","nm_eng":"Saengyeon 2(i)-dong"},

{"cd":"31080530","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"31080550","nm_kor":"보산동","nm_eng":"Bosan-dong"},

{"cd":"31080560","nm_kor":"불현동","nm_eng":"Bulhyeon-dong"},

{"cd":"31080610","nm_kor":"송내동","nm_eng":"Songnae-dong"},

{"cd":"31080580","nm_kor":"소요동","nm_eng":"Soyo-dong"},

{"cd":"31080600","nm_kor":"상패동","nm_eng":"Sangpae-dong"},

{"cd":"31090000","nm_kor":"안산시","nm_eng":"Ansan-si"},

{"cd":"31091000","nm_kor":"상록구","nm_eng":"Sangnok-gu"},

{"cd":"31091510","nm_kor":"일동","nm_eng":"Il-dong"},

{"cd":"31091740","nm_kor":"이동","nm_eng":"I-dong"},

{"cd":"31091760","nm_kor":"사동","nm_eng":"Sa-dong"},

{"cd":"31091770","nm_kor":"사이동","nm_eng":"Sai-dong"},

{"cd":"31091780","nm_kor":"해양동","nm_eng":"Haeyang-dong"},

{"cd":"31091540","nm_kor":"본오1동","nm_eng":"Bono 1(il)-dong"},

{"cd":"31091550","nm_kor":"본오2동","nm_eng":"Bono 2(i)-dong"},

{"cd":"31091560","nm_kor":"본오3동","nm_eng":"Bono 3(sam)-dong"},

{"cd":"31091570","nm_kor":"부곡동","nm_eng":"Bugok-dong"},

{"cd":"31091580","nm_kor":"월피동","nm_eng":"Wolpi-dong"},

{"cd":"31091620","nm_kor":"성포동","nm_eng":"Seongpo-dong"},

{"cd":"31091710","nm_kor":"반월동","nm_eng":"Banwol-dong"},

{"cd":"31091730","nm_kor":"안산동","nm_eng":"Ansan-dong"},

{"cd":"31092000","nm_kor":"단원구","nm_eng":"Danwon-gu"},

{"cd":"31092590","nm_kor":"와동","nm_eng":"Wa-dong"},

{"cd":"31092740","nm_kor":"고잔동","nm_eng":"Gojan-dong"},

{"cd":"31092750","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"31092730","nm_kor":"호수동","nm_eng":"Hosu-dong"},

{"cd":"31092760","nm_kor":"원곡동","nm_eng":"Wongok-dong"},

{"cd":"31092780","nm_kor":"백운동","nm_eng":"Baekgun-dong"},

{"cd":"31092770","nm_kor":"신길동","nm_eng":"Singil-dong"},

{"cd":"31092660","nm_kor":"초지동","nm_eng":"Choji-dong"},

{"cd":"31092680","nm_kor":"선부1동","nm_eng":"Seonbu 1(il)-dong"},

{"cd":"31092690","nm_kor":"선부2동","nm_eng":"Seonbu 2(i)-dong"},

{"cd":"31092700","nm_kor":"선부3동","nm_eng":"Seonbu 3(sam)-dong"},

{"cd":"31092720","nm_kor":"대부동","nm_eng":"Daebu-dong"},

{"cd":"31100000","nm_kor":"고양시","nm_eng":"Goyang-si"},

{"cd":"31101000","nm_kor":"덕양구","nm_eng":"Deogyang-gu"},

{"cd":"31101510","nm_kor":"주교동","nm_eng":"Jugyo-dong"},

{"cd":"31101520","nm_kor":"원신동","nm_eng":"Wonsin-dong"},

{"cd":"31101511","nm_kor":"흥도동","nm_eng":"Heungdo-dong"},

{"cd":"31101540","nm_kor":"성사1동","nm_eng":"Seongsa 1(il)-dong"},

{"cd":"31101550","nm_kor":"성사2동","nm_eng":"Seongsa 2(i)-dong"},

{"cd":"31101560","nm_kor":"효자동","nm_eng":"Hyoja-dong"},

{"cd":"31101512","nm_kor":"삼송1동","nm_eng":"Samsong 1(il)-dong"},

{"cd":"31101513","nm_kor":"삼송2동","nm_eng":"Samsong 2(i)-dong"},

{"cd":"31101580","nm_kor":"창릉동","nm_eng":"Changneung-dong"},

{"cd":"31101590","nm_kor":"고양동","nm_eng":"Goyang-dong"},

{"cd":"31101600","nm_kor":"관산동","nm_eng":"Gwansan-dong"},

{"cd":"31101610","nm_kor":"능곡동","nm_eng":"Neunggok-dong"},

{"cd":"31101620","nm_kor":"화정1동","nm_eng":"Hwajeong 1(il)-dong"},

{"cd":"31101630","nm_kor":"화정2동","nm_eng":"Hwajeong 2(i)-dong"},

{"cd":"31101640","nm_kor":"행주동","nm_eng":"Haengju-dong"},

{"cd":"31101650","nm_kor":"행신1동","nm_eng":"Haengsin 1(il)-dong"},

{"cd":"31101660","nm_kor":"행신2동","nm_eng":"Haengsin 2(i)-dong"},

{"cd":"31101514","nm_kor":"행신3동","nm_eng":"Haengsin 3(sam)-dong"},

{"cd":"31101515","nm_kor":"행신4동","nm_eng":"Haengsin 4(sa)-dong"},

{"cd":"31101670","nm_kor":"화전동","nm_eng":"Hwajeon-dong"},

{"cd":"31101680","nm_kor":"대덕동","nm_eng":"Daedeok-dong"},

{"cd":"31103000","nm_kor":"일산동구","nm_eng":"Ilsandong-gu"},

{"cd":"31103510","nm_kor":"식사동","nm_eng":"Siksa-dong"},

{"cd":"31103511","nm_kor":"중산1동","nm_eng":"Jungsan 1(il)-dong"},

{"cd":"31103512","nm_kor":"중산2동","nm_eng":"Jungsan 2(i)-dong"},

{"cd":"31103530","nm_kor":"정발산동","nm_eng":"Jeongbalsan-dong"},

{"cd":"31103540","nm_kor":"풍산동","nm_eng":"Pungsan-dong"},

{"cd":"31103550","nm_kor":"백석1동","nm_eng":"Baekseok 1(il)-dong"},

{"cd":"31103610","nm_kor":"백석2동","nm_eng":"Baekseok 2(i)-dong"},

{"cd":"31103560","nm_kor":"마두1동","nm_eng":"Madu 1(il)-dong"},

{"cd":"31103570","nm_kor":"마두2동","nm_eng":"Madu 2(i)-dong"},

{"cd":"31103580","nm_kor":"장항1동","nm_eng":"Baekseok 1(il)-dong"},

{"cd":"31103590","nm_kor":"장항2동","nm_eng":"Baekseok 2(i)-dong"},

{"cd":"31103600","nm_kor":"고봉동","nm_eng":"Gobong-dong"},

{"cd":"31104000","nm_kor":"일산서구","nm_eng":"Ilsanseo-gu"},

{"cd":"31104510","nm_kor":"일산1동","nm_eng":"Ilsan 1(il)-dong"},

{"cd":"31104520","nm_kor":"일산2동","nm_eng":"Ilsan 2(i)-dong"},

{"cd":"31104530","nm_kor":"일산3동","nm_eng":"Ilsan 3(sam)-dong"},

{"cd":"31104511","nm_kor":"탄현1동","nm_eng":"Tanhyeon 1(il)-dong"},

{"cd":"31104512","nm_kor":"탄현2동","nm_eng":"Tanhyeon 2(i)-dong"},

{"cd":"31104550","nm_kor":"주엽1동","nm_eng":"Juyeop 1(il)-dong"},

{"cd":"31104560","nm_kor":"주엽2동","nm_eng":"Juyeop 2(i)-dong"},

{"cd":"31104570","nm_kor":"대화동","nm_eng":"Daehwa-dong"},

{"cd":"31104580","nm_kor":"송포동","nm_eng":"Songpo-dong"},

{"cd":"31104513","nm_kor":"덕이동","nm_eng":"Deoki-dong"},

{"cd":"31104514","nm_kor":"가좌동","nm_eng":"Gajwa-dong"},

{"cd":"31110000","nm_kor":"과천시","nm_eng":"Gwacheon-si"},

{"cd":"31110510","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"31110520","nm_kor":"갈현동","nm_eng":"Galhyeon-dong"},

{"cd":"31110530","nm_kor":"별양동","nm_eng":"Byeoryang-dong"},

{"cd":"31110540","nm_kor":"부림동","nm_eng":"Burim-dong"},

{"cd":"31110550","nm_kor":"과천동","nm_eng":"Gwacheon-dong"},

{"cd":"31110560","nm_kor":"문원동","nm_eng":"Munwon-dong"},

{"cd":"31120000","nm_kor":"구리시","nm_eng":"Guri-si"},

{"cd":"31120510","nm_kor":"갈매동","nm_eng":"Galmae-dong"},

{"cd":"31120520","nm_kor":"동구동","nm_eng":"Donggu-dong"},

{"cd":"31120530","nm_kor":"인창동","nm_eng":"Inchang-dong"},

{"cd":"31120540","nm_kor":"교문1동","nm_eng":"Gyomun 1(il)-dong"},

{"cd":"31120550","nm_kor":"교문2동","nm_eng":"Gyomun 2(i)-dong"},

{"cd":"31120560","nm_kor":"수택1동","nm_eng":"Sutaek 1(il)-dong"},

{"cd":"31120570","nm_kor":"수택2동","nm_eng":"Sutaek 2(i)-dong"},

{"cd":"31120580","nm_kor":"수택3동","nm_eng":"Sutaek 3(sam)-dong"},

{"cd":"31130000","nm_kor":"남양주시","nm_eng":"Namyangju-si"},

{"cd":"31130110","nm_kor":"와부읍","nm_eng":"Wabu-eup"},

{"cd":"31130120","nm_kor":"진접읍","nm_eng":"Jinjeop-eup"},

{"cd":"31130111","nm_kor":"화도읍","nm_eng":"Hwado-eup"},

{"cd":"31130140","nm_kor":"진건읍","nm_eng":"Jingeon-eup"},

{"cd":"31130150","nm_kor":"오남읍","nm_eng":"Onam-eup"},

{"cd":"31130160","nm_kor":"퇴계원읍","nm_eng":"Toegyewon-eup"},

{"cd":"31130310","nm_kor":"별내면","nm_eng":"Byeolnae-myeon"},

{"cd":"31130340","nm_kor":"수동면","nm_eng":"Sudong-myeon"},

{"cd":"31130350","nm_kor":"조안면","nm_eng":"Joan-myeon"},

{"cd":"31130510","nm_kor":"호평동","nm_eng":"Hopyeong-dong"},

{"cd":"31130520","nm_kor":"평내동","nm_eng":"Pyeongnae-dong"},

{"cd":"31130530","nm_kor":"금곡동","nm_eng":"Geumgok-dong"},

{"cd":"31130540","nm_kor":"양정동","nm_eng":"Yangjeong-dong"},

{"cd":"31130580","nm_kor":"다산1동","nm_eng":"Dasan 1(il)-dong"},

{"cd":"31130590","nm_kor":"다산2동","nm_eng":"Dasan 2(i)-dong"},

{"cd":"31130570","nm_kor":"별내동","nm_eng":"Byeolnae-dong"},

{"cd":"31140000","nm_kor":"오산시","nm_eng":"Osan-si"},

{"cd":"31140510","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"31140530","nm_kor":"남촌동","nm_eng":"Namchon-dong"},

{"cd":"31140540","nm_kor":"신장동","nm_eng":"Sinjang-dong"},

{"cd":"31140550","nm_kor":"세마동","nm_eng":"Sema-dong"},

{"cd":"31140560","nm_kor":"초평동","nm_eng":"Chopyeong-dong"},

{"cd":"31140520","nm_kor":"대원동","nm_eng":"Daewon-dong"},

{"cd":"31150000","nm_kor":"시흥시","nm_eng":"Siheung-si"},

{"cd":"31150510","nm_kor":"대야동","nm_eng":"Daeya-dong"},

{"cd":"31150520","nm_kor":"신천동","nm_eng":"Sincheon-dong"},

{"cd":"31150530","nm_kor":"신현동","nm_eng":"Sinhyeon-dong"},

{"cd":"31150540","nm_kor":"은행동","nm_eng":"Eunhaeng-dong"},

{"cd":"31150550","nm_kor":"매화동","nm_eng":"Maehwa-dong"},

{"cd":"31150560","nm_kor":"목감동","nm_eng":"Mokgam-dong"},

{"cd":"31150680","nm_kor":"군자동","nm_eng":"Gunja-dong"},

{"cd":"31150690","nm_kor":"월곶동","nm_eng":"Wolgot-dong"},

{"cd":"31150640","nm_kor":"정왕본동","nm_eng":"Jeongwangbon-dong"},

{"cd":"31150650","nm_kor":"정왕1동","nm_eng":"Jeongwang 1(il)-dong"},

{"cd":"31150610","nm_kor":"정왕2동","nm_eng":"Jeongwang 2(i)-dong"},

{"cd":"31150620","nm_kor":"정왕3동","nm_eng":"Jeongwang 3(sam)-dong"},

{"cd":"31150720","nm_kor":"정왕4동","nm_eng":"Jeongwang 4(sa)-dong"},

{"cd":"31150740","nm_kor":"배곧1동","nm_eng":"Baegot 1(il)-dong"},

{"cd":"31150750","nm_kor":"배곧2동","nm_eng":"Baegot 2(i)-dong"},

{"cd":"31150590","nm_kor":"과림동","nm_eng":"Gwarim-dong"},

{"cd":"31150700","nm_kor":"연성동","nm_eng":"Yeonseong-dong"},

{"cd":"31150710","nm_kor":"장곡동","nm_eng":"Janggok-dong"},

{"cd":"31150670","nm_kor":"능곡동","nm_eng":"Neunggok-dong"},

{"cd":"31160000","nm_kor":"군포시","nm_eng":"Gunpo-si"},

{"cd":"31160510","nm_kor":"군포1동","nm_eng":"Gunpo 1(il)-dong"},

{"cd":"31160520","nm_kor":"군포2동","nm_eng":"Gunpo 2(i)-dong"},

{"cd":"31160540","nm_kor":"산본1동","nm_eng":"Sanbon 1(il)-dong"},

{"cd":"31160550","nm_kor":"산본2동","nm_eng":"Sanbon 2(i)-dong"},

{"cd":"31160560","nm_kor":"금정동","nm_eng":"Geumjeong-dong"},

{"cd":"31160570","nm_kor":"재궁동","nm_eng":"Jaegung-dong"},

{"cd":"31160580","nm_kor":"오금동","nm_eng":"Ogeum-dong"},

{"cd":"31160590","nm_kor":"수리동","nm_eng":"Suri-dong"},

{"cd":"31160600","nm_kor":"궁내동","nm_eng":"Gungnae-dong"},

{"cd":"31160630","nm_kor":"대야동","nm_eng":"Daeya-dong"},

{"cd":"31160610","nm_kor":"광정동","nm_eng":"Gwangjeong-dong"},

{"cd":"31160640","nm_kor":"송부동","nm_eng":"Songbu-dong"},

{"cd":"31170000","nm_kor":"의왕시","nm_eng":"Uiwang-si"},

{"cd":"31170510","nm_kor":"고천동","nm_eng":"Gocheon-dong"},

{"cd":"31170520","nm_kor":"부곡동","nm_eng":"Bugok-dong"},

{"cd":"31170530","nm_kor":"오전동","nm_eng":"Ojeon-dong"},

{"cd":"31170540","nm_kor":"내손1동","nm_eng":"Naeson 1(il)-dong"},

{"cd":"31170550","nm_kor":"내손2동","nm_eng":"Naeson 2(i)-dong"},

{"cd":"31170560","nm_kor":"청계동","nm_eng":"Cheonggye-dong"},

{"cd":"31180000","nm_kor":"하남시","nm_eng":"Hanam-si"},

{"cd":"31180510","nm_kor":"천현동","nm_eng":"Cheonhyeon-dong"},

{"cd":"31180520","nm_kor":"신장1동","nm_eng":"Sinjang 1(il)-dong"},

{"cd":"31180530","nm_kor":"신장2동","nm_eng":"Sinjang 2(i)-dong"},

{"cd":"31180540","nm_kor":"덕풍1동","nm_eng":"Deokpung 1(il)-dong"},

{"cd":"31180550","nm_kor":"덕풍2동","nm_eng":"Deokpung 2(i)-dong"},

{"cd":"31180560","nm_kor":"덕풍3동","nm_eng":"Deokpung 3(sam)-dong"},

{"cd":"31180610","nm_kor":"풍산동","nm_eng":"Pungsan-dong"},

{"cd":"31180660","nm_kor":"감북동","nm_eng":"Gambuk-dong"},

{"cd":"31180670","nm_kor":"감일동","nm_eng":"Gamil-dong"},

{"cd":"31180650","nm_kor":"위례동","nm_eng":"wirye-dong"},

{"cd":"31180590","nm_kor":"춘궁동","nm_eng":"Chungung-dong"},

{"cd":"31180600","nm_kor":"초이동","nm_eng":"Choi-dong"},

{"cd":"31180620","nm_kor":"미사1동","nm_eng":"Misa 1(il)-dong"},

{"cd":"31180630","nm_kor":"미사2동","nm_eng":"Misa 2(i)-dong"},

{"cd":"31190000","nm_kor":"용인시","nm_eng":"Yongin-si"},

{"cd":"31191000","nm_kor":"처인구","nm_eng":"Cheoin-gu"},

{"cd":"31191110","nm_kor":"포곡읍","nm_eng":"Pogok-eup"},

{"cd":"31191120","nm_kor":"모현읍","nm_eng":"Mohyeon-eup"},

{"cd":"31191130","nm_kor":"이동읍","nm_eng":"Idong-eup"},

{"cd":"31191140","nm_kor":"남사읍","nm_eng":"Namsa-eup"},

{"cd":"31191340","nm_kor":"원삼면","nm_eng":"Wonsam-myeon"},

{"cd":"31191350","nm_kor":"백암면","nm_eng":"Baegam-myeon"},

{"cd":"31191360","nm_kor":"양지면","nm_eng":"Yangji-myeon"},

{"cd":"31191510","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"31191550","nm_kor":"역북동","nm_eng":"Yeokbuk-dong"},

{"cd":"31191560","nm_kor":"삼가동","nm_eng":"Samga-dong"},

{"cd":"31191530","nm_kor":"유림동","nm_eng":"Yurim-dong"},

{"cd":"31191540","nm_kor":"동부동","nm_eng":"Dongbu-dong"},

{"cd":"31192000","nm_kor":"기흥구","nm_eng":"Giheung-gu"},

{"cd":"31192610","nm_kor":"신갈동","nm_eng":"Singal-dong"},

{"cd":"31192630","nm_kor":"영덕1동","nm_eng":"Yeongdeok 1(il)-dong"},

{"cd":"31192640","nm_kor":"영덕2동","nm_eng":"Yeongdeok 2(i)-dong"},

{"cd":"31192520","nm_kor":"구갈동","nm_eng":"Gugal-dong"},

{"cd":"31192650","nm_kor":"상갈동","nm_eng":"Sanggal-dong"},

{"cd":"31192660","nm_kor":"보라동","nm_eng":"Bora-dong"},

{"cd":"31192540","nm_kor":"기흥동","nm_eng":"Giheung-dong"},

{"cd":"31192550","nm_kor":"서농동","nm_eng":"Seonong-dong"},

{"cd":"31192560","nm_kor":"구성동","nm_eng":"Guseong-dong"},

{"cd":"31192570","nm_kor":"마북동","nm_eng":"Mabuk-dong"},

{"cd":"31192670","nm_kor":"동백1동","nm_eng":"Dongbaek 1(il)-dong"},

{"cd":"31192680","nm_kor":"동백2동","nm_eng":"Dongbaek 2(i)-dong"},

{"cd":"31192690","nm_kor":"동백3동","nm_eng":"Dongbaek 3(sam)-dong"},

{"cd":"31192600","nm_kor":"상하동","nm_eng":"Sangha-dong"},

{"cd":"31192590","nm_kor":"보정동","nm_eng":"Bojeong-dong"},

{"cd":"31193000","nm_kor":"수지구","nm_eng":"Suji-gu"},

{"cd":"31193510","nm_kor":"풍덕천1동","nm_eng":"Pungdoekcheon 1(il)-dong"},

{"cd":"31193520","nm_kor":"풍덕천2동","nm_eng":"Pungdoekcheon 2(i)-dong"},

{"cd":"31193530","nm_kor":"신봉동","nm_eng":"Sinbong-dong"},

{"cd":"31193600","nm_kor":"죽전1동","nm_eng":"Jukjeon 1(il)-dong"},

{"cd":"31193550","nm_kor":"죽전2동","nm_eng":"Jukjeon 2(i)-dong"},

{"cd":"31193610","nm_kor":"죽전3동","nm_eng":"Jukjeon 3(sam)-dong"},

{"cd":"31193560","nm_kor":"동천동","nm_eng":"Dongcheon-dong"},

{"cd":"31193620","nm_kor":"상현1동","nm_eng":"Sanghyeon 1(il)-dong"},

{"cd":"31193580","nm_kor":"상현2동","nm_eng":"Sanghyeon 2(i)-dong"},

{"cd":"31193630","nm_kor":"상현3동","nm_eng":"Sanghyeon 3(sam)-dong"},

{"cd":"31193590","nm_kor":"성복동","nm_eng":"Seongbok-dong"},

{"cd":"31200000","nm_kor":"파주시","nm_eng":"Paju-si"},

{"cd":"31200110","nm_kor":"문산읍","nm_eng":"Munsan-eup"},

{"cd":"31200120","nm_kor":"파주읍","nm_eng":"Paju-eup"},

{"cd":"31200130","nm_kor":"법원읍","nm_eng":"Beobwon-eup"},

{"cd":"31200150","nm_kor":"조리읍","nm_eng":"Jori-eup"},

{"cd":"31200310","nm_kor":"월롱면","nm_eng":"Wollong-myeon"},

{"cd":"31200320","nm_kor":"탄현면","nm_eng":"Tanhyeon-myeon"},

{"cd":"31200350","nm_kor":"광탄면","nm_eng":"Gwangtan-myeon"},

{"cd":"31200360","nm_kor":"파평면","nm_eng":"Papyeong-myeon"},

{"cd":"31200370","nm_kor":"적성면","nm_eng":"Jeokseong-myeon"},

{"cd":"31200390","nm_kor":"장단면","nm_eng":"Jangdan-myeon"},

{"cd":"31200530","nm_kor":"금촌1동","nm_eng":"Geumchon 1(il)-dong"},

{"cd":"31200520","nm_kor":"금촌2동","nm_eng":"Geumchon 2(i)-dong"},

{"cd":"31200540","nm_kor":"금촌3동","nm_eng":"Geumchon 3(sam)-dong"},

{"cd":"31200550","nm_kor":"교하동","nm_eng":"Gyoha-dong"},

{"cd":"31200560","nm_kor":"운정1동","nm_eng":"Unjeong 1(il)-dong"},

{"cd":"31200570","nm_kor":"운정2동","nm_eng":"Unjeong 2(i)-dong"},

{"cd":"31200580","nm_kor":"운정3동","nm_eng":"Unjeong 3(sam)-dong"},

{"cd":"31210000","nm_kor":"이천시","nm_eng":"Icheon-si"},

{"cd":"31210110","nm_kor":"장호원읍","nm_eng":"Janghowon-eup"},

{"cd":"31210120","nm_kor":"부발읍","nm_eng":"Bubal-eup"},

{"cd":"31210310","nm_kor":"신둔면","nm_eng":"Sindun-myeon"},

{"cd":"31210320","nm_kor":"백사면","nm_eng":"Baeksa-myeon"},

{"cd":"31210330","nm_kor":"호법면","nm_eng":"Hobeop-myeon"},

{"cd":"31210340","nm_kor":"마장면","nm_eng":"Majang-myeon"},

{"cd":"31210350","nm_kor":"대월면","nm_eng":"Daewol-myeon"},

{"cd":"31210360","nm_kor":"모가면","nm_eng":"Moga-myeon"},

{"cd":"31210370","nm_kor":"설성면","nm_eng":"Seolseong-myeon"},

{"cd":"31210380","nm_kor":"율면","nm_eng":"Yul-myeon"},

{"cd":"31210510","nm_kor":"창전동","nm_eng":"Changjeon-dong"},

{"cd":"31210540","nm_kor":"증포동","nm_eng":"jeungpo-dong"},

{"cd":"31210520","nm_kor":"중리동","nm_eng":"Jungni-dong"},

{"cd":"31210530","nm_kor":"관고동","nm_eng":"Gwango-dong"},

{"cd":"31220000","nm_kor":"안성시","nm_eng":"Anseong-si"},

{"cd":"31220110","nm_kor":"공도읍","nm_eng":"Gongdo-eup"},

{"cd":"31220310","nm_kor":"보개면","nm_eng":"Bogae-myeon"},

{"cd":"31220320","nm_kor":"금광면","nm_eng":"Geumgwang-myeon"},

{"cd":"31220330","nm_kor":"서운면","nm_eng":"Seoun-myeon"},

{"cd":"31220340","nm_kor":"미양면","nm_eng":"Miyang-myeon"},

{"cd":"31220350","nm_kor":"대덕면","nm_eng":"Daedeok-myeon"},

{"cd":"31220360","nm_kor":"양성면","nm_eng":"Yangseong-myeon"},

{"cd":"31220380","nm_kor":"원곡면","nm_eng":"Wongok-myeon"},

{"cd":"31220390","nm_kor":"일죽면","nm_eng":"Iljuk-myeon"},

{"cd":"31220400","nm_kor":"죽산면","nm_eng":"Juksan-myeon"},

{"cd":"31220410","nm_kor":"삼죽면","nm_eng":"Samjuk-myeon"},

{"cd":"31220420","nm_kor":"고삼면","nm_eng":"Gosam-myeon"},

{"cd":"31220510","nm_kor":"안성1동","nm_eng":"Anseong 1(il)-dong"},

{"cd":"31220520","nm_kor":"안성2동","nm_eng":"Anseong 2(i)-dong"},

{"cd":"31220530","nm_kor":"안성3동","nm_eng":"Anseong 3(sam)-dong"},

{"cd":"31230000","nm_kor":"김포시","nm_eng":"Gimpo-si"},

{"cd":"31230110","nm_kor":"통진읍","nm_eng":"Tongjin-eup"},

{"cd":"31230120","nm_kor":"고촌읍","nm_eng":"Gochon-eup"},

{"cd":"31230130","nm_kor":"양촌읍","nm_eng":"Yangchon-eup"},

{"cd":"31230340","nm_kor":"대곶면","nm_eng":"Daegot-myeon"},

{"cd":"31230350","nm_kor":"월곶면","nm_eng":"Wolgot-myeon"},

{"cd":"31230360","nm_kor":"하성면","nm_eng":"Haseong-myeon"},

{"cd":"31230610","nm_kor":"김포본동","nm_eng":"Gimpobon-dong"},

{"cd":"31230620","nm_kor":"장기본동","nm_eng":"Janggibon-dong"},

{"cd":"31230530","nm_kor":"사우동","nm_eng":"Sau-dong"},

{"cd":"31230540","nm_kor":"풍무동","nm_eng":"Pungmu-dong"},

{"cd":"31230560","nm_kor":"장기동","nm_eng":"Janggi-dong"},

{"cd":"31230630","nm_kor":"구래동","nm_eng":"Gurae-dong"},

{"cd":"31230640","nm_kor":"마산동","nm_eng":"Masan-dong"},

{"cd":"31230600","nm_kor":"운양동","nm_eng":"Woonyang-dong"},

{"cd":"31240000","nm_kor":"화성시","nm_eng":"Hwaseong-si"},

{"cd":"31240120","nm_kor":"봉담읍","nm_eng":"Bongdam-eup"},

{"cd":"31240130","nm_kor":"우정읍","nm_eng":"Ujeong-eup"},

{"cd":"31240140","nm_kor":"향남읍","nm_eng":"Hyangnam-eup"},

{"cd":"31240150","nm_kor":"남양읍","nm_eng":"Namyang-eup"},

{"cd":"31240310","nm_kor":"매송면","nm_eng":"Maesong-myeon"},

{"cd":"31240330","nm_kor":"비봉면","nm_eng":"Bibong-myeon"},

{"cd":"31240350","nm_kor":"마도면","nm_eng":"Mado-myeon"},

{"cd":"31240360","nm_kor":"송산면","nm_eng":"Songsan-myeon"},

{"cd":"31240370","nm_kor":"서신면","nm_eng":"Seosin-myeon"},

{"cd":"31240380","nm_kor":"팔탄면","nm_eng":"Paltan-myeon"},

{"cd":"31240390","nm_kor":"장안면","nm_eng":"Jangan-myeon"},

{"cd":"31240420","nm_kor":"양감면","nm_eng":"Yanggam-myeon"},

{"cd":"31240430","nm_kor":"정남면","nm_eng":"Jeongnam-myeon"},

{"cd":"31240670","nm_kor":"새솔동","nm_eng":"Saesol-dong"},

{"cd":"31240520","nm_kor":"진안동","nm_eng":"Jinan-dong"},

{"cd":"31240530","nm_kor":"병점1동","nm_eng":"Beyngjeom 1(il)-dong"},

{"cd":"31240540","nm_kor":"병점2동","nm_eng":"Beyngjeom 2(i)-dong"},

{"cd":"31240550","nm_kor":"반월동","nm_eng":"Banwol-dong"},

{"cd":"31240560","nm_kor":"기배동","nm_eng":"Gibae-dong"},

{"cd":"31240570","nm_kor":"화산동","nm_eng":"Hwasan-dong"},

{"cd":"31240610","nm_kor":"동탄1동","nm_eng":"Dongtan 1(il)-dong"},

{"cd":"31240600","nm_kor":"동탄2동","nm_eng":"Dongtan 2(i)-dong"},

{"cd":"31240620","nm_kor":"동탄3동","nm_eng":"Dongtan 3(sam)-dong"},

{"cd":"31240640","nm_kor":"동탄4동","nm_eng":"Dongtan 4(sa)-dong"},

{"cd":"31240650","nm_kor":"동탄5동","nm_eng":"Dongtan 5(o)-dong"},

{"cd":"31240700","nm_kor":"동탄6동","nm_eng":"Dongtan 6(yuk)-dong"},

{"cd":"31240690","nm_kor":"동탄7동","nm_eng":"Dongtan 7(chil)-dong"},

{"cd":"31240710","nm_kor":"동탄8동","nm_eng":"Dongtan 8(pal)-dong"},

{"cd":"31250000","nm_kor":"광주시","nm_eng":"Gwangju-si"},

{"cd":"31250110","nm_kor":"오포읍","nm_eng":"Opo-eup"},

{"cd":"31250120","nm_kor":"초월읍","nm_eng":"Chowol-eup"},

{"cd":"31250140","nm_kor":"곤지암읍","nm_eng":"gonjiam-eup"},

{"cd":"31250340","nm_kor":"도척면","nm_eng":"Docheok-myeon"},

{"cd":"31250350","nm_kor":"퇴촌면","nm_eng":"Toechon-myeon"},

{"cd":"31250360","nm_kor":"남종면","nm_eng":"Namjong-myeon"},

{"cd":"31250380","nm_kor":"남한산성면","nm_eng":"Namhansanseong-myeon"},

{"cd":"31250540","nm_kor":"경안동","nm_eng":"Gyeongan-dong"},

{"cd":"31250550","nm_kor":"송정동","nm_eng":"Songjeong-dong"},

{"cd":"31250560","nm_kor":"쌍령동","nm_eng":"Ssangnyeong-dong"},

{"cd":"31250570","nm_kor":"탄벌동","nm_eng":"Tanbeol-dong"},

{"cd":"31250580","nm_kor":"광남1동","nm_eng":"Gwangnam 1(il)-dong"},

{"cd":"31250590","nm_kor":"광남2동","nm_eng":"Gwangnam 2(i)-dong"},

{"cd":"31260000","nm_kor":"양주시","nm_eng":"Yangju-si"},

{"cd":"31260110","nm_kor":"백석읍","nm_eng":"Baekseok-eup"},

{"cd":"31260310","nm_kor":"은현면","nm_eng":"Eunhyeon-myeon"},

{"cd":"31260320","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"31260330","nm_kor":"광적면","nm_eng":"Gwangjeok-myeon"},

{"cd":"31260340","nm_kor":"장흥면","nm_eng":"Jangheung-myeon"},

{"cd":"31260510","nm_kor":"양주1동","nm_eng":"Yangju 1(il)-dong"},

{"cd":"31260520","nm_kor":"양주2동","nm_eng":"Yangju 2(i)-dong"},

{"cd":"31260530","nm_kor":"회천1동","nm_eng":"Hoecheon 1(il)-dong"},

{"cd":"31260540","nm_kor":"회천2동","nm_eng":"Hoecheon 2(i)-dong"},

{"cd":"31260550","nm_kor":"회천3동","nm_eng":"Hoecheon 3(sam)-dong"},

{"cd":"31260560","nm_kor":"회천4동","nm_eng":"Hoecheon 4(sa)-dong"},

{"cd":"31270000","nm_kor":"포천시","nm_eng":"Pocheon-si"},

{"cd":"31270110","nm_kor":"소흘읍","nm_eng":"Sohol-eup"},

{"cd":"31270310","nm_kor":"군내면","nm_eng":"Gunnae-myeon"},

{"cd":"31270320","nm_kor":"내촌면","nm_eng":"Naechon-myeon"},

{"cd":"31270330","nm_kor":"가산면","nm_eng":"Gasan-myeon"},

{"cd":"31270340","nm_kor":"신북면","nm_eng":"Sinbuk-myeon"},

{"cd":"31270350","nm_kor":"창수면","nm_eng":"Changsu-myeon"},

{"cd":"31270360","nm_kor":"영중면","nm_eng":"Yeongjung-myeon"},

{"cd":"31270370","nm_kor":"일동면","nm_eng":"Ildong-myeon"},

{"cd":"31270380","nm_kor":"이동면","nm_eng":"Idong-myeon"},

{"cd":"31270390","nm_kor":"영북면","nm_eng":"Yeongbuk-myeon"},

{"cd":"31270400","nm_kor":"관인면","nm_eng":"Gwanin-myeon"},

{"cd":"31270410","nm_kor":"화현면","nm_eng":"Hwahyeon-myeon"},

{"cd":"31270510","nm_kor":"포천동","nm_eng":"Pocheon-dong"},

{"cd":"31270520","nm_kor":"선단동","nm_eng":"Seondan-dong"},

{"cd":"31280000","nm_kor":"여주시","nm_eng":"Yeoju-si"},

{"cd":"31280110","nm_kor":"가남읍","nm_eng":"Ganam-eup"},

{"cd":"31280310","nm_kor":"점동면","nm_eng":"Jeomdong-myeon"},

{"cd":"31280330","nm_kor":"흥천면","nm_eng":"Heungcheon-myeon"},

{"cd":"31280340","nm_kor":"금사면","nm_eng":"Geumsa-myeon"},

{"cd":"31280390","nm_kor":"세종대왕면","nm_eng":"Sejongdaewang-myeon"},

{"cd":"31280360","nm_kor":"대신면","nm_eng":"Daesin-myeon"},

{"cd":"31280370","nm_kor":"북내면","nm_eng":"Bungnae-myeon"},

{"cd":"31280380","nm_kor":"강천면","nm_eng":"Gangcheon-myeon"},

{"cd":"31280350","nm_kor":"산북면","nm_eng":"Sanbuk-myeon"},

{"cd":"31280510","nm_kor":"여흥동","nm_eng":"Yeoheung-dong"},

{"cd":"31280520","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"31280530","nm_kor":"오학동","nm_eng":"Ohak-dong"},

{"cd":"31550000","nm_kor":"연천군","nm_eng":"Yeoncheon-gun"},

{"cd":"31550110","nm_kor":"연천읍","nm_eng":"Yeoncheon-eup"},

{"cd":"31550120","nm_kor":"전곡읍","nm_eng":"Jeongok-eup"},

{"cd":"31550310","nm_kor":"군남면","nm_eng":"Gunnam-myeon"},

{"cd":"31550320","nm_kor":"청산면","nm_eng":"Cheongsan-myeon"},

{"cd":"31550330","nm_kor":"백학면","nm_eng":"Baekhak-myeon"},

{"cd":"31550340","nm_kor":"미산면","nm_eng":"Misan-myeon"},

{"cd":"31550350","nm_kor":"왕징면","nm_eng":"Wangjing-myeon"},

{"cd":"31550360","nm_kor":"신서면","nm_eng":"Sinseo-myeon"},

{"cd":"31550370","nm_kor":"중면","nm_eng":"Jung-myeon"},

{"cd":"31550380","nm_kor":"장남면","nm_eng":"Jangnam-myeon"},

{"cd":"31570000","nm_kor":"가평군","nm_eng":"Gapyeong-gun"},

{"cd":"31570110","nm_kor":"가평읍","nm_eng":"Gapyeong-eup"},

{"cd":"31570310","nm_kor":"설악면","nm_eng":"Seorak-myeon"},

{"cd":"31570320","nm_kor":"청평면","nm_eng":"Cheongpyeong-myeon"},

{"cd":"31570330","nm_kor":"상면","nm_eng":"Sang-myeon"},

{"cd":"31570360","nm_kor":"조종면","nm_eng":"Jojong-myeon"},

{"cd":"31570350","nm_kor":"북면","nm_eng":"Buk-myeon"},

{"cd":"31580000","nm_kor":"양평군","nm_eng":"Yangpyeong-gun"},

{"cd":"31580110","nm_kor":"양평읍","nm_eng":"Yangpyeong-eup"},

{"cd":"31580310","nm_kor":"강상면","nm_eng":"Gangsang-myeon"},

{"cd":"31580320","nm_kor":"강하면","nm_eng":"Gangha-myeon"},

{"cd":"31580330","nm_kor":"양서면","nm_eng":"Yangseo-myeon"},

{"cd":"31580340","nm_kor":"옥천면","nm_eng":"Okcheon-myeon"},

{"cd":"31580350","nm_kor":"서종면","nm_eng":"Seojong-myeon"},

{"cd":"31580360","nm_kor":"단월면","nm_eng":"Danwol-myeon"},

{"cd":"31580370","nm_kor":"청운면","nm_eng":"Cheongun-myeon"},

{"cd":"31580380","nm_kor":"양동면","nm_eng":"Yangdong-myeon"},

{"cd":"31580390","nm_kor":"지평면","nm_eng":"Jipyeong-myeon"},

{"cd":"31580400","nm_kor":"용문면","nm_eng":"Yongmun-myeon"},

{"cd":"31580410","nm_kor":"개군면","nm_eng":"Gaegun-myeon"},

{"cd":"32000000","nm_kor":"강원도","nm_eng":"Gangwon-do"},

{"cd":"32010000","nm_kor":"춘천시","nm_eng":"Chuncheon-si"},

{"cd":"32010110","nm_kor":"신북읍","nm_eng":"Sinbuk-eup"},

{"cd":"32010310","nm_kor":"동면","nm_eng":"Dong-myeon"},

{"cd":"32010320","nm_kor":"동산면","nm_eng":"Dongsan-myeon"},

{"cd":"32010330","nm_kor":"신동면","nm_eng":"Sindong-myeon"},

{"cd":"32010350","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"32010370","nm_kor":"서면","nm_eng":"Seo-myeon"},

{"cd":"32010380","nm_kor":"사북면","nm_eng":"Sabuk-myeon"},

{"cd":"32010390","nm_kor":"북산면","nm_eng":"Buksan-myeon"},

{"cd":"32010340","nm_kor":"동내면","nm_eng":"Dongnae-myeon"},

{"cd":"32010360","nm_kor":"남산면","nm_eng":"Namsan-myeon"},

{"cd":"32010520","nm_kor":"교동","nm_eng":"Gyo-dong"},

{"cd":"32010530","nm_kor":"조운동","nm_eng":"Jowun-dong"},

{"cd":"32010540","nm_kor":"약사명동","nm_eng":"Yaksamyeong-dong"},

{"cd":"32010570","nm_kor":"근화동","nm_eng":"Geunhwa-dong"},

{"cd":"32010580","nm_kor":"소양동","nm_eng":"Soyang-dong"},

{"cd":"32010600","nm_kor":"후평1동","nm_eng":"Hupyeong 1(il)-dong"},

{"cd":"32010610","nm_kor":"후평2동","nm_eng":"Hupyeong 2(i)-dong"},

{"cd":"32010620","nm_kor":"후평3동","nm_eng":"Hupyeong 3(sam)-dong"},

{"cd":"32010630","nm_kor":"효자1동","nm_eng":"Hyoja 1(il)-dong"},

{"cd":"32010640","nm_kor":"효자2동","nm_eng":"Hyoja 2(i)-dong"},

{"cd":"32010650","nm_kor":"효자3동","nm_eng":"Hyoja 3(sam)-dong"},

{"cd":"32010660","nm_kor":"석사동","nm_eng":"Seoksa-dong"},

{"cd":"32010670","nm_kor":"퇴계동","nm_eng":"Toegye-dong"},

{"cd":"32010680","nm_kor":"강남동","nm_eng":"Gangnam-dong"},

{"cd":"32010710","nm_kor":"신사우동","nm_eng":"Sinsau-dong"},

{"cd":"32020000","nm_kor":"원주시","nm_eng":"Wonju-si"},

{"cd":"32020110","nm_kor":"문막읍","nm_eng":"Munmak-eup"},

{"cd":"32020310","nm_kor":"소초면","nm_eng":"Socho-myeon"},

{"cd":"32020320","nm_kor":"호저면","nm_eng":"Hojeo-myeon"},

{"cd":"32020330","nm_kor":"지정면","nm_eng":"Jijeong-myeon"},

{"cd":"32020340","nm_kor":"부론면","nm_eng":"Buron-myeon"},

{"cd":"32020350","nm_kor":"귀래면","nm_eng":"Gwirae-myeon"},

{"cd":"32020360","nm_kor":"흥업면","nm_eng":"Heungeop-myeon"},

{"cd":"32020370","nm_kor":"판부면","nm_eng":"Panbu-myeon"},

{"cd":"32020380","nm_kor":"신림면","nm_eng":"Sillim-myeon"},

{"cd":"32020510","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"32020520","nm_kor":"원인동","nm_eng":"Wonin-dong"},

{"cd":"32020530","nm_kor":"개운동","nm_eng":"Gaeun-dong"},

{"cd":"32020540","nm_kor":"명륜1동","nm_eng":"Myeongnyun 1(il)-dong"},

{"cd":"32020550","nm_kor":"명륜2동","nm_eng":"Myeongnyun 2(i)-dong"},

{"cd":"32020560","nm_kor":"단구동","nm_eng":"Dangu-dong"},

{"cd":"32020570","nm_kor":"일산동","nm_eng":"Ilsan-dong"},

{"cd":"32020580","nm_kor":"학성동","nm_eng":"Hakseong-dong"},

{"cd":"32020600","nm_kor":"단계동","nm_eng":"Dangye-dong"},

{"cd":"32020610","nm_kor":"우산동","nm_eng":"Usan-dong"},

{"cd":"32020620","nm_kor":"태장1동","nm_eng":"Taejang 1(il)-dong"},

{"cd":"32020630","nm_kor":"태장2동","nm_eng":"Taejang 2(i)-dong"},

{"cd":"32020640","nm_kor":"봉산동","nm_eng":"Bongsan-dong"},

{"cd":"32020660","nm_kor":"행구동","nm_eng":"Haenggu-dong"},

{"cd":"32020670","nm_kor":"무실동","nm_eng":"Musil-dong"},

{"cd":"32020680","nm_kor":"반곡관설동","nm_eng":"Bangokgwanseol-dong"},

{"cd":"32030000","nm_kor":"강릉시","nm_eng":"Gangneung-si"},

{"cd":"32030110","nm_kor":"주문진읍","nm_eng":"Jumunjin-eup"},

{"cd":"32030310","nm_kor":"성산면","nm_eng":"Seongsan-myeon"},

{"cd":"32030320","nm_kor":"왕산면","nm_eng":"Wangsan-myeon"},

{"cd":"32030330","nm_kor":"구정면","nm_eng":"Gujeong-myeon"},

{"cd":"32030340","nm_kor":"강동면","nm_eng":"Gangdong-myeon"},

{"cd":"32030350","nm_kor":"옥계면","nm_eng":"Okgye-myeon"},

{"cd":"32030360","nm_kor":"사천면","nm_eng":"Sacheon-myeon"},

{"cd":"32030370","nm_kor":"연곡면","nm_eng":"Yeongok-myeon"},

{"cd":"32030510","nm_kor":"홍제동","nm_eng":"Hongje-dong"},

{"cd":"32030520","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"32030540","nm_kor":"옥천동","nm_eng":"Okcheon-dong"},

{"cd":"32030550","nm_kor":"교1동","nm_eng":"Gyo 1(il)-dong"},

{"cd":"32030560","nm_kor":"교2동","nm_eng":"Gyo 2(i)-dong"},

{"cd":"32030570","nm_kor":"포남1동","nm_eng":"Ponam 1(il)-dong"},

{"cd":"32030580","nm_kor":"포남2동","nm_eng":"Ponam 2(i)-dong"},

{"cd":"32030590","nm_kor":"초당동","nm_eng":"Chodang-dong"},

{"cd":"32030600","nm_kor":"송정동","nm_eng":"Songjeong-dong"},

{"cd":"32030610","nm_kor":"내곡동","nm_eng":"Naegok-dong"},

{"cd":"32030620","nm_kor":"강남동","nm_eng":"Gangnam-dong"},

{"cd":"32030650","nm_kor":"성덕동","nm_eng":"Seongdeok-dong"},

{"cd":"32030670","nm_kor":"경포동","nm_eng":"Gyeongpo-dong"},

{"cd":"32040000","nm_kor":"동해시","nm_eng":"Donghae-si"},

{"cd":"32040510","nm_kor":"천곡동","nm_eng":"Cheongok-dong"},

{"cd":"32040520","nm_kor":"송정동","nm_eng":"Songjeong-dong"},

{"cd":"32040530","nm_kor":"북삼동","nm_eng":"Buksam-dong"},

{"cd":"32040540","nm_kor":"부곡동","nm_eng":"Bugok-dong"},

{"cd":"32040550","nm_kor":"동호동","nm_eng":"Dongho-dong"},

{"cd":"32040570","nm_kor":"발한동","nm_eng":"Balhan-dong"},

{"cd":"32040590","nm_kor":"묵호동","nm_eng":"Mukho-dong"},

{"cd":"32040600","nm_kor":"북평동","nm_eng":"Bukpyeong-dong"},

{"cd":"32040630","nm_kor":"망상동","nm_eng":"Mangsang-dong"},

{"cd":"32040650","nm_kor":"삼화동","nm_eng":"Samhwa-dong"},

{"cd":"32050000","nm_kor":"태백시","nm_eng":"Taebaek-si"},

{"cd":"32050510","nm_kor":"황지동","nm_eng":"Hwangji-dong"},

{"cd":"32050520","nm_kor":"황연동","nm_eng":"Hwangyeon-dong"},

{"cd":"32050530","nm_kor":"삼수동","nm_eng":"Samsu-dong"},

{"cd":"32050540","nm_kor":"상장동","nm_eng":"Sangjang-dong"},

{"cd":"32050620","nm_kor":"문곡소도동","nm_eng":"Mungoksodo-dong"},

{"cd":"32050560","nm_kor":"장성동","nm_eng":"Jangseong-dong"},

{"cd":"32050550","nm_kor":"구문소동","nm_eng":"Gumunso-dong"},

{"cd":"32050580","nm_kor":"철암동","nm_eng":"Cheoram-dong"},

{"cd":"32060000","nm_kor":"속초시","nm_eng":"Sokcho-si"},

{"cd":"32060510","nm_kor":"영랑동","nm_eng":"Yeongnang-dong"},

{"cd":"32060520","nm_kor":"동명동","nm_eng":"Dongmyeong-dong"},

{"cd":"32060540","nm_kor":"금호동","nm_eng":"Geumho-dong"},

{"cd":"32060560","nm_kor":"교동","nm_eng":"Gyo-dong"},

{"cd":"32060570","nm_kor":"노학동","nm_eng":"Nohak-dong"},

{"cd":"32060580","nm_kor":"조양동","nm_eng":"Joyang-dong"},

{"cd":"32060590","nm_kor":"청호동","nm_eng":"Cheongho-dong"},

{"cd":"32060600","nm_kor":"대포동","nm_eng":"Daepo-dong"},

{"cd":"32070000","nm_kor":"삼척시","nm_eng":"Samcheok-si"},

{"cd":"32070110","nm_kor":"도계읍","nm_eng":"Dogye-eup"},

{"cd":"32070120","nm_kor":"원덕읍","nm_eng":"Wondeok-eup"},

{"cd":"32070310","nm_kor":"근덕면","nm_eng":"Geundeok-myeon"},

{"cd":"32070320","nm_kor":"하장면","nm_eng":"Hajang-myeon"},

{"cd":"32070330","nm_kor":"노곡면","nm_eng":"Nogok-myeon"},

{"cd":"32070340","nm_kor":"미로면","nm_eng":"Miro-myeon"},

{"cd":"32070350","nm_kor":"가곡면","nm_eng":"Gagok-myeon"},

{"cd":"32070360","nm_kor":"신기면","nm_eng":"Singi-myeon"},

{"cd":"32070510","nm_kor":"남양동","nm_eng":"Namyang-dong"},

{"cd":"32070530","nm_kor":"교동","nm_eng":"Gyo-dong"},

{"cd":"32070540","nm_kor":"정라동","nm_eng":"Jeongna-dong"},

{"cd":"32070520","nm_kor":"성내동","nm_eng":"Seongnae-dong"},

{"cd":"32510000","nm_kor":"홍천군","nm_eng":"Hongcheon-gun"},

{"cd":"32510110","nm_kor":"홍천읍","nm_eng":"Hongcheon-eup"},

{"cd":"32510310","nm_kor":"화촌면","nm_eng":"Hwachon-myeon"},

{"cd":"32510320","nm_kor":"두촌면","nm_eng":"Duchon-myeon"},

{"cd":"32510330","nm_kor":"내촌면","nm_eng":"Naechon-myeon"},

{"cd":"32510340","nm_kor":"서석면","nm_eng":"Seoseok-myeon"},

{"cd":"32510400","nm_kor":"영귀미면","nm_eng":"Yeonggwimi-myeon"},

{"cd":"32510360","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"32510370","nm_kor":"서면","nm_eng":"Seo-myeon"},

{"cd":"32510380","nm_kor":"북방면","nm_eng":"Bukbang-myeon"},

{"cd":"32510390","nm_kor":"내면","nm_eng":"Nae-myeon"},

{"cd":"32520000","nm_kor":"횡성군","nm_eng":"Hoengseong-gun"},

{"cd":"32520110","nm_kor":"횡성읍","nm_eng":"Hoengseong-eup"},

{"cd":"32520310","nm_kor":"우천면","nm_eng":"Ucheon-myeon"},

{"cd":"32520320","nm_kor":"안흥면","nm_eng":"Anheung-myeon"},

{"cd":"32520330","nm_kor":"둔내면","nm_eng":"Dunnae-myeon"},

{"cd":"32520340","nm_kor":"갑천면","nm_eng":"Gapcheon-myeon"},

{"cd":"32520350","nm_kor":"청일면","nm_eng":"Cheongil-myeon"},

{"cd":"32520360","nm_kor":"공근면","nm_eng":"Gonggeun-myeon"},

{"cd":"32520370","nm_kor":"서원면","nm_eng":"Seowon-myeon"},

{"cd":"32520380","nm_kor":"강림면","nm_eng":"Gangnim-myeon"},

{"cd":"32530000","nm_kor":"영월군","nm_eng":"Yeongwol-gun"},

{"cd":"32530110","nm_kor":"영월읍","nm_eng":"Yeongwol-eup"},

{"cd":"32530120","nm_kor":"상동읍","nm_eng":"Sangdong-eup"},

{"cd":"32530410","nm_kor":"산솔면","nm_eng":"Sansol-myeon"},

{"cd":"32530380","nm_kor":"김삿갓면","nm_eng":"Gimsatgat-myeon"},

{"cd":"32530330","nm_kor":"북면","nm_eng":"Buk-myeon"},

{"cd":"32530340","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"32530390","nm_kor":"한반도면","nm_eng":"Hanbando-myeon"},

{"cd":"32530360","nm_kor":"주천면","nm_eng":"Jucheon-myeon"},

{"cd":"32530400","nm_kor":"무릉도원면","nm_eng":"Muneungdowon-myeon"},

{"cd":"32540000","nm_kor":"평창군","nm_eng":"Pyeongchang-gun"},

{"cd":"32540110","nm_kor":"평창읍","nm_eng":"Pyeongchang-eup"},

{"cd":"32540310","nm_kor":"미탄면","nm_eng":"Mitan-myeon"},

{"cd":"32540320","nm_kor":"방림면","nm_eng":"Bangnim-myeon"},

{"cd":"32540330","nm_kor":"대화면","nm_eng":"Daehwa-myeon"},

{"cd":"32540340","nm_kor":"봉평면","nm_eng":"Bongpyeong-myeon"},

{"cd":"32540350","nm_kor":"용평면","nm_eng":"Yongpyeong-myeon"},

{"cd":"32540360","nm_kor":"진부면","nm_eng":"Jinbu-myeon"},

{"cd":"32540370","nm_kor":"대관령면","nm_eng":"Daegwallyeong-myeon"},

{"cd":"32550000","nm_kor":"정선군","nm_eng":"Jeongseon-gun"},

{"cd":"32550110","nm_kor":"정선읍","nm_eng":"Jeongseon-eup"},

{"cd":"32550120","nm_kor":"고한읍","nm_eng":"Gohan-eup"},

{"cd":"32550130","nm_kor":"사북읍","nm_eng":"Sabuk-eup"},

{"cd":"32550140","nm_kor":"신동읍","nm_eng":"Sindong-eup"},

{"cd":"32550320","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"32550340","nm_kor":"북평면","nm_eng":"Bukpyeong-myeon"},

{"cd":"32550350","nm_kor":"임계면","nm_eng":"Imgye-myeon"},

{"cd":"32550360","nm_kor":"화암면","nm_eng":"Hwaam-myeon"},

{"cd":"32550370","nm_kor":"여량면","nm_eng":"Yeoryang-myeon"},

{"cd":"32560000","nm_kor":"철원군","nm_eng":"Cheorwon-gun"},

{"cd":"32560110","nm_kor":"철원읍","nm_eng":"Cheorwon-eup"},

{"cd":"32560120","nm_kor":"김화읍","nm_eng":"Gimhwa-eup"},

{"cd":"32560130","nm_kor":"갈말읍","nm_eng":"Galmal-eup"},

{"cd":"32560140","nm_kor":"동송읍","nm_eng":"Dongsong-eup"},

{"cd":"32560310","nm_kor":"서면","nm_eng":"Seo-myeon"},

{"cd":"32560320","nm_kor":"근남면","nm_eng":"Geunnam-myeon"},

{"cd":"32560210","nm_kor":"근북면","nm_eng":"Geunbuk-myeon"},

{"cd":"32560260","nm_kor":"근동면","nm_eng":"Geundong-myeon"},

{"cd":"32560270","nm_kor":"원동면","nm_eng":"Wondong-myeon"},

{"cd":"32560280","nm_kor":"원남면","nm_eng":"Wonnam-myeon"},

{"cd":"32560290","nm_kor":"임남면","nm_eng":"Imnam-myeon"},

{"cd":"32570000","nm_kor":"화천군","nm_eng":"Hwacheon-gun"},

{"cd":"32570110","nm_kor":"화천읍","nm_eng":"Hwacheon-eup"},

{"cd":"32570310","nm_kor":"간동면","nm_eng":"Gandong-myeon"},

{"cd":"32570320","nm_kor":"하남면","nm_eng":"Hanam-myeon"},

{"cd":"32570330","nm_kor":"상서면","nm_eng":"Sangseo-myeon"},

{"cd":"32570340","nm_kor":"사내면","nm_eng":"Sanae-myeon"},

{"cd":"32580000","nm_kor":"양구군","nm_eng":"Yanggu-gun"},

{"cd":"32580110","nm_kor":"양구읍","nm_eng":"Yanggu-eup"},

{"cd":"32580350","nm_kor":"국토정중앙면","nm_eng":"Guktojeongjungang-myeon"},

{"cd":"32580320","nm_kor":"동면","nm_eng":"Dong-myeon"},

{"cd":"32580330","nm_kor":"방산면","nm_eng":"Bangsan-myeon"},

{"cd":"32580340","nm_kor":"해안면","nm_eng":"Haean-myeon"},

{"cd":"32590000","nm_kor":"인제군","nm_eng":"Inje-gun"},

{"cd":"32590110","nm_kor":"인제읍","nm_eng":"Inje-eup"},

{"cd":"32590310","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"32590320","nm_kor":"북면","nm_eng":"Buk-myeon"},

{"cd":"32590330","nm_kor":"기린면","nm_eng":"Girin-myeon"},

{"cd":"32590340","nm_kor":"서화면","nm_eng":"Seohwa-myeon"},

{"cd":"32590350","nm_kor":"상남면","nm_eng":"Sangnam-myeon"},

{"cd":"32600000","nm_kor":"고성군","nm_eng":"Goseong-gun"},

{"cd":"32600110","nm_kor":"간성읍","nm_eng":"Ganseong-eup"},

{"cd":"32600120","nm_kor":"거진읍","nm_eng":"Geojin-eup"},

{"cd":"32600310","nm_kor":"현내면","nm_eng":"Hyeonnae-myeon"},

{"cd":"32600320","nm_kor":"죽왕면","nm_eng":"Jugwang-myeon"},

{"cd":"32600330","nm_kor":"토성면","nm_eng":"Toseong-myeon"},

{"cd":"32600260","nm_kor":"수동면","nm_eng":"Sudong-myeon"},

{"cd":"32610000","nm_kor":"양양군","nm_eng":"Yangyang-gun"},

{"cd":"32610110","nm_kor":"양양읍","nm_eng":"Yangyang-eup"},

{"cd":"32610310","nm_kor":"서면","nm_eng":"Seo-myeon"},

{"cd":"32610320","nm_kor":"손양면","nm_eng":"Sonyang-myeon"},

{"cd":"32610330","nm_kor":"현북면","nm_eng":"Hyeonbuk-myeon"},

{"cd":"32610340","nm_kor":"현남면","nm_eng":"Hyeonnam-myeon"},

{"cd":"32610350","nm_kor":"강현면","nm_eng":"Ganghyeon-myeon"},

{"cd":"33000000","nm_kor":"충청북도","nm_eng":"Chungcheongbuk-do"},

{"cd":"33040000","nm_kor":"청주시","nm_eng":"Cheongju-si"},

{"cd":"33041000","nm_kor":"상당구","nm_eng":"Sangdang-gu"},

{"cd":"33041310","nm_kor":"낭성면","nm_eng":"Nangseong-myeon"},

{"cd":"33041320","nm_kor":"미원면","nm_eng":"Miwon-myeon"},

{"cd":"33041330","nm_kor":"가덕면","nm_eng":"Gadeok-myeon"},

{"cd":"33041340","nm_kor":"남일면","nm_eng":"Namil-myeon"},

{"cd":"33041350","nm_kor":"문의면","nm_eng":"Munui-myeon"},

{"cd":"33041510","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"33041520","nm_kor":"성안동","nm_eng":"Seongan-dong"},

{"cd":"33041530","nm_kor":"탑대성동","nm_eng":"Tapdaeseong-dong"},

{"cd":"33041540","nm_kor":"영운동","nm_eng":"Yeongun-dong"},

{"cd":"33041550","nm_kor":"금천동","nm_eng":"Geumcheon-dong"},

{"cd":"33041560","nm_kor":"용담.명암.산성동","nm_eng":"Yongdammyeongamsanseong-dong"},

{"cd":"33041570","nm_kor":"용암1동","nm_eng":"Yongam 1(il)-dong"},

{"cd":"33041580","nm_kor":"용암2동","nm_eng":"Yongam 2(I)-dong"},

{"cd":"33042000","nm_kor":"서원구","nm_eng":"Seowon-gu"},

{"cd":"33042310","nm_kor":"남이면","nm_eng":"Nami-myeon"},

{"cd":"33042320","nm_kor":"현도면","nm_eng":"Hyeondo-myeon"},

{"cd":"33042510","nm_kor":"사직1동","nm_eng":"Sajik 1(il)-dong"},

{"cd":"33042520","nm_kor":"사직2동","nm_eng":"Sajik 2(i)-dong"},

{"cd":"33042530","nm_kor":"사창동","nm_eng":"Sachang-dong"},

{"cd":"33042540","nm_kor":"모충동","nm_eng":"Mochung-dong"},

{"cd":"33042550","nm_kor":"산남동","nm_eng":"Sannam-dong"},

{"cd":"33042560","nm_kor":"분평동","nm_eng":"Bunpyeong-dong"},

{"cd":"33042570","nm_kor":"수곡1동","nm_eng":"Sugok 1(il)-dong"},

{"cd":"33042580","nm_kor":"수곡2동","nm_eng":"Sugok 2(i)-dong"},

{"cd":"33042590","nm_kor":"성화.개신.죽림동","nm_eng":"Seonghwagaesinjungnim-dong"},

{"cd":"33043000","nm_kor":"흥덕구","nm_eng":"Heungdeok-gu"},

{"cd":"33043110","nm_kor":"오송읍","nm_eng":"Osong-eup"},

{"cd":"33043310","nm_kor":"강내면","nm_eng":"Gangnae-myeon"},

{"cd":"33043320","nm_kor":"옥산면","nm_eng":"Oksan-myeon"},

{"cd":"33043510","nm_kor":"운천.신봉동","nm_eng":"Uncheonsinbong-dong"},

{"cd":"33043520","nm_kor":"복대1동","nm_eng":"Bokdae 1(il)-dong"},

{"cd":"33043530","nm_kor":"복대2동","nm_eng":"Bokdae 2(i)-dong"},

{"cd":"33043540","nm_kor":"가경동","nm_eng":"Gagyeong-dong"},

{"cd":"33043550","nm_kor":"봉명1동","nm_eng":"Bongmyeong 1(il)-dong"},

{"cd":"33043560","nm_kor":"봉명2.송정동","nm_eng":"Bongmyeong 2(i)songjeong-dong"},

{"cd":"33043570","nm_kor":"강서1동","nm_eng":"Gangseo 1(il)-dong"},

{"cd":"33043580","nm_kor":"강서2동","nm_eng":"Gangseo 2(i)-dong"},

{"cd":"33044000","nm_kor":"청원구","nm_eng":"Cheongwon-gu"},

{"cd":"33044110","nm_kor":"내수읍","nm_eng":"Naesu-eup"},

{"cd":"33044120","nm_kor":"오창읍","nm_eng":"Ochang-eup"},

{"cd":"33044310","nm_kor":"북이면","nm_eng":"Bugi-myeon"},

{"cd":"33044520","nm_kor":"우암동","nm_eng":"Uam-dong"},

{"cd":"33044530","nm_kor":"내덕1동","nm_eng":"Naedeok 1(il)-dong"},

{"cd":"33044540","nm_kor":"내덕2동","nm_eng":"Naedeok 2(i)-dong"},

{"cd":"33044550","nm_kor":"율량.사천동","nm_eng":"Yullyangsacheon-dong"},

{"cd":"33044510","nm_kor":"오근장동","nm_eng":"Ogeunjang-dong"},

{"cd":"33020000","nm_kor":"충주시","nm_eng":"Chungju-si"},

{"cd":"33020110","nm_kor":"주덕읍","nm_eng":"Judeok-eup"},

{"cd":"33020310","nm_kor":"살미면","nm_eng":"Salmi-myeon"},

{"cd":"33020320","nm_kor":"수안보면","nm_eng":"Suanbo-myeon"},

{"cd":"33020430","nm_kor":"대소원면","nm_eng":"Daesowon-myeon"},

{"cd":"33020340","nm_kor":"신니면","nm_eng":"Sinni-myeon"},

{"cd":"33020350","nm_kor":"노은면","nm_eng":"Noeun-myeon"},

{"cd":"33020360","nm_kor":"앙성면","nm_eng":"Angseong-myeon"},

{"cd":"33020440","nm_kor":"중앙탑면","nm_eng":"Jungangtap-myeon"},

{"cd":"33020380","nm_kor":"금가면","nm_eng":"Geumga-myeon"},

{"cd":"33020390","nm_kor":"동량면","nm_eng":"Dongnyang-myeon"},

{"cd":"33020400","nm_kor":"산척면","nm_eng":"Sancheok-myeon"},

{"cd":"33020410","nm_kor":"엄정면","nm_eng":"Eomjeong-myeon"},

{"cd":"33020420","nm_kor":"소태면","nm_eng":"Sotae-myeon"},

{"cd":"33020510","nm_kor":"성내.충인동","nm_eng":"Seongnaechungin-dong"},

{"cd":"33020530","nm_kor":"교현.안림동","nm_eng":"Gyohyeonalim-dong"},

{"cd":"33020540","nm_kor":"교현2동","nm_eng":"Gyohyeon 2(i)-dong"},

{"cd":"33020550","nm_kor":"용산동","nm_eng":"Yongsan-dong"},

{"cd":"33020560","nm_kor":"지현동","nm_eng":"Jihyeon-dong"},

{"cd":"33020570","nm_kor":"문화동","nm_eng":"Munhwa-dong"},

{"cd":"33020580","nm_kor":"호암.직동","nm_eng":"Hoamjik-dong"},

{"cd":"33020600","nm_kor":"달천동","nm_eng":"Dalcheon-dong"},

{"cd":"33020610","nm_kor":"봉방동","nm_eng":"Bongbang-dong"},

{"cd":"33020620","nm_kor":"칠금.금릉동","nm_eng":"Chilgeumgeumneung-dong"},

{"cd":"33020630","nm_kor":"연수동","nm_eng":"Yeonsu-dong"},

{"cd":"33020640","nm_kor":"목행.용탄동","nm_eng":"Mokhaengyongtan-dong"},

{"cd":"33030000","nm_kor":"제천시","nm_eng":"Jecheon-si"},

{"cd":"33030110","nm_kor":"봉양읍","nm_eng":"Bongyang-eup"},

{"cd":"33030310","nm_kor":"금성면","nm_eng":"Geumseong-myeon"},

{"cd":"33030320","nm_kor":"청풍면","nm_eng":"Cheongpung-myeon"},

{"cd":"33030330","nm_kor":"수산면","nm_eng":"Susan-myeon"},

{"cd":"33030340","nm_kor":"덕산면","nm_eng":"Deoksan-myeon"},

{"cd":"33030350","nm_kor":"한수면","nm_eng":"Hansu-myeon"},

{"cd":"33030360","nm_kor":"백운면","nm_eng":"Baegun-myeon"},

{"cd":"33030370","nm_kor":"송학면","nm_eng":"Songhak-myeon"},

{"cd":"33030510","nm_kor":"교동","nm_eng":"Gyo-dong"},

{"cd":"33030730","nm_kor":"의림지동","nm_eng":"Uilimji-dong"},

{"cd":"33030740","nm_kor":"중앙동","nm_eng":"jungang-dong"},

{"cd":"33030700","nm_kor":"남현동","nm_eng":"Namhyeon-dong"},

{"cd":"33030710","nm_kor":"영서동","nm_eng":"Yeongseo-dong"},

{"cd":"33030560","nm_kor":"용두동","nm_eng":"Yongdu-dong"},

{"cd":"33030720","nm_kor":"신백동","nm_eng":"Sinbaek-dong"},

{"cd":"33030590","nm_kor":"청전동","nm_eng":"Cheongjeon-dong"},

{"cd":"33030600","nm_kor":"화산동","nm_eng":"Hwasan-dong"},

{"cd":"33520000","nm_kor":"보은군","nm_eng":"Boeun-gun"},

{"cd":"33520110","nm_kor":"보은읍","nm_eng":"Boeun-eup"},

{"cd":"33520310","nm_kor":"속리산면","nm_eng":"Songnisan-myeon"},

{"cd":"33520320","nm_kor":"장안면","nm_eng":"Jangan-myeon"},

{"cd":"33520330","nm_kor":"마로면","nm_eng":"Maro-myeon"},

{"cd":"33520340","nm_kor":"탄부면","nm_eng":"Tanbu-myeon"},

{"cd":"33520350","nm_kor":"삼승면","nm_eng":"Samseung-myeon"},

{"cd":"33520360","nm_kor":"수한면","nm_eng":"Suhan-myeon"},

{"cd":"33520370","nm_kor":"회남면","nm_eng":"Hoenam-myeon"},

{"cd":"33520380","nm_kor":"회인면","nm_eng":"Hoein-myeon"},

{"cd":"33520390","nm_kor":"내북면","nm_eng":"Naebuk-myeon"},

{"cd":"33520400","nm_kor":"산외면","nm_eng":"Sanoe-myeon"},

{"cd":"33530000","nm_kor":"옥천군","nm_eng":"Okcheon-gun"},

{"cd":"33530110","nm_kor":"옥천읍","nm_eng":"Okcheon-eup"},

{"cd":"33530310","nm_kor":"동이면","nm_eng":"Dongi-myeon"},

{"cd":"33530320","nm_kor":"안남면","nm_eng":"Annam-myeon"},

{"cd":"33530330","nm_kor":"안내면","nm_eng":"Annae-myeon"},

{"cd":"33530340","nm_kor":"청성면","nm_eng":"Cheongseong-myeon"},

{"cd":"33530350","nm_kor":"청산면","nm_eng":"Cheongsan-myeon"},

{"cd":"33530360","nm_kor":"이원면","nm_eng":"Iwon-myeon"},

{"cd":"33530370","nm_kor":"군서면","nm_eng":"Gunseo-myeon"},

{"cd":"33530380","nm_kor":"군북면","nm_eng":"Gunbuk-myeon"},

{"cd":"33540000","nm_kor":"영동군","nm_eng":"Yeongdong-gun"},

{"cd":"33540110","nm_kor":"영동읍","nm_eng":"Yeongdong-eup"},

{"cd":"33540310","nm_kor":"용산면","nm_eng":"Yongsan-myeon"},

{"cd":"33540320","nm_kor":"황간면","nm_eng":"Hwanggan-myeon"},

{"cd":"33540330","nm_kor":"추풍령면","nm_eng":"Chupungnyeong-myeon"},

{"cd":"33540340","nm_kor":"매곡면","nm_eng":"Maegok-myeon"},

{"cd":"33540350","nm_kor":"상촌면","nm_eng":"Sangchon-myeon"},

{"cd":"33540360","nm_kor":"양강면","nm_eng":"Yanggang-myeon"},

{"cd":"33540370","nm_kor":"용화면","nm_eng":"Yonghwa-myeon"},

{"cd":"33540380","nm_kor":"학산면","nm_eng":"Haksan-myeon"},

{"cd":"33540390","nm_kor":"양산면","nm_eng":"Yangsan-myeon"},

{"cd":"33540400","nm_kor":"심천면","nm_eng":"Simcheon-myeon"},

{"cd":"33590000","nm_kor":"증평군","nm_eng":"Jeungpyeong-gun"},

{"cd":"33590140","nm_kor":"증평읍","nm_eng":"Jeungpyeong-eup"},

{"cd":"33590310","nm_kor":"도안면","nm_eng":"Doan-myeon"},

{"cd":"33550000","nm_kor":"진천군","nm_eng":"Jincheon-gun"},

{"cd":"33550110","nm_kor":"진천읍","nm_eng":"Jincheon-eup"},

{"cd":"33550120","nm_kor":"덕산읍","nm_eng":"Deoksan-eup"},

{"cd":"33550320","nm_kor":"초평면","nm_eng":"Chopyeong-myeon"},

{"cd":"33550330","nm_kor":"문백면","nm_eng":"Munbaek-myeon"},

{"cd":"33550340","nm_kor":"백곡면","nm_eng":"Baekgok-myeon"},

{"cd":"33550350","nm_kor":"이월면","nm_eng":"Iwol-myeon"},

{"cd":"33550360","nm_kor":"광혜원면","nm_eng":"Gwanghyewon-myeon"},

{"cd":"33560000","nm_kor":"괴산군","nm_eng":"Goesan-gun"},

{"cd":"33560110","nm_kor":"괴산읍","nm_eng":"Goesan-eup"},

{"cd":"33560310","nm_kor":"감물면","nm_eng":"Gammul-myeon"},

{"cd":"33560320","nm_kor":"장연면","nm_eng":"Jangyeon-myeon"},

{"cd":"33560330","nm_kor":"연풍면","nm_eng":"Yeonpung-myeon"},

{"cd":"33560340","nm_kor":"칠성면","nm_eng":"Chilseong-myeon"},

{"cd":"33560350","nm_kor":"문광면","nm_eng":"Mungwang-myeon"},

{"cd":"33560360","nm_kor":"청천면","nm_eng":"Cheongcheon-myeon"},

{"cd":"33560370","nm_kor":"청안면","nm_eng":"Cheongan-myeon"},

{"cd":"33560380","nm_kor":"사리면","nm_eng":"Sari-myeon"},

{"cd":"33560390","nm_kor":"소수면","nm_eng":"Sosu-myeon"},

{"cd":"33560400","nm_kor":"불정면","nm_eng":"Buljeong-myeon"},

{"cd":"33570000","nm_kor":"음성군","nm_eng":"Eumseong-gun"},

{"cd":"33570110","nm_kor":"음성읍","nm_eng":"Eumseong-eup"},

{"cd":"33570120","nm_kor":"금왕읍","nm_eng":"Geumwang-eup"},

{"cd":"33570310","nm_kor":"소이면","nm_eng":"Soi-myeon"},

{"cd":"33570320","nm_kor":"원남면","nm_eng":"Wonnam-myeon"},

{"cd":"33570330","nm_kor":"맹동면","nm_eng":"Maengdong-myeon"},

{"cd":"33570340","nm_kor":"대소면","nm_eng":"Daeso-myeon"},

{"cd":"33570350","nm_kor":"삼성면","nm_eng":"Samseong-myeon"},

{"cd":"33570360","nm_kor":"생극면","nm_eng":"Saenggeuk-myeon"},

{"cd":"33570370","nm_kor":"감곡면","nm_eng":"Gamgok-myeon"},

{"cd":"33580000","nm_kor":"단양군","nm_eng":"Danyang-gun"},

{"cd":"33580110","nm_kor":"단양읍","nm_eng":"Danyang-eup"},

{"cd":"33580120","nm_kor":"매포읍","nm_eng":"Maepo-eup"},

{"cd":"33580320","nm_kor":"대강면","nm_eng":"Daegang-myeon"},

{"cd":"33580330","nm_kor":"가곡면","nm_eng":"Gagok-myeon"},

{"cd":"33580340","nm_kor":"영춘면","nm_eng":"Yeongchun-myeon"},

{"cd":"33580350","nm_kor":"어상천면","nm_eng":"Eosangcheon-myeon"},

{"cd":"33580360","nm_kor":"적성면","nm_eng":"Jeokseong-myeon"},

{"cd":"33580310","nm_kor":"단성면","nm_eng":"Danseong-myeon"},

{"cd":"34000000","nm_kor":"충청남도","nm_eng":"Chungcheongnam-do"},

{"cd":"34010000","nm_kor":"천안시","nm_eng":"Cheonan-si"},

{"cd":"34011000","nm_kor":"동남구","nm_eng":"Dongnam-gu"},

{"cd":"34011110","nm_kor":"목천읍","nm_eng":"Mokcheon-eup"},

{"cd":"34011310","nm_kor":"풍세면","nm_eng":"Pungse-myeon"},

{"cd":"34011320","nm_kor":"광덕면","nm_eng":"Gwangdeok-myeon"},

{"cd":"34011330","nm_kor":"북면","nm_eng":"Buk-myeon"},

{"cd":"34011340","nm_kor":"성남면","nm_eng":"Seongnam-myeon"},

{"cd":"34011350","nm_kor":"수신면","nm_eng":"Susin-myeon"},

{"cd":"34011360","nm_kor":"병천면","nm_eng":"Byeongcheon-myeon"},

{"cd":"34011370","nm_kor":"동면","nm_eng":"Dong-myeon"},

{"cd":"34011510","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"34011520","nm_kor":"문성동","nm_eng":"Munseong-dong"},

{"cd":"34011530","nm_kor":"원성1동","nm_eng":"Wonseong 1(il)-dong"},

{"cd":"34011540","nm_kor":"원성2동","nm_eng":"Wonseong 2(i)-dong"},

{"cd":"34011550","nm_kor":"봉명동","nm_eng":"Bongmyeong-dong"},

{"cd":"34011560","nm_kor":"일봉동","nm_eng":"Ilbong-dong"},

{"cd":"34011570","nm_kor":"신방동","nm_eng":"Sinbang-dong"},

{"cd":"34011580","nm_kor":"청룡동","nm_eng":"Cheongnyong-dong"},

{"cd":"34011590","nm_kor":"신안동","nm_eng":"Sinan-dong"},

{"cd":"34012000","nm_kor":"서북구","nm_eng":"Sebuk-gu"},

{"cd":"34012110","nm_kor":"성환읍","nm_eng":"Seonghwan-eup"},

{"cd":"34012120","nm_kor":"성거읍","nm_eng":"Seonggeo-eup"},

{"cd":"34012130","nm_kor":"직산읍","nm_eng":"Jiksan-eup"},

{"cd":"34012310","nm_kor":"입장면","nm_eng":"Ipjang-myeon"},

{"cd":"34012510","nm_kor":"성정1동","nm_eng":"Seongjeong 1(il)-dong"},

{"cd":"34012520","nm_kor":"성정2동","nm_eng":"Seongjeong 2(i)-dong"},

{"cd":"34012530","nm_kor":"쌍용1동","nm_eng":"Ssangyong 1(il)-dong"},

{"cd":"34012540","nm_kor":"쌍용2동","nm_eng":"Ssangyong 2(i)-dong"},

{"cd":"34012550","nm_kor":"쌍용3동","nm_eng":"Ssangyong 3(sam)-dong"},

{"cd":"34012580","nm_kor":"백석동","nm_eng":"Baekseok-dong"},

{"cd":"34012620","nm_kor":"불당1동","nm_eng":"Buldang 1(il)-dong"},

{"cd":"34012630","nm_kor":"불당2동","nm_eng":"Buldang 2(i)-dong"},

{"cd":"34012600","nm_kor":"부성1동","nm_eng":"Buseong 1(il)-dong"},

{"cd":"34012610","nm_kor":"부성2동","nm_eng":"Buseong 2(i)-dong"},

{"cd":"34020000","nm_kor":"공주시","nm_eng":"Gongju-si"},

{"cd":"34020110","nm_kor":"유구읍","nm_eng":"Yugu-eup"},

{"cd":"34020310","nm_kor":"이인면","nm_eng":"Iin-myeon"},

{"cd":"34020320","nm_kor":"탄천면","nm_eng":"Tancheon-myeon"},

{"cd":"34020330","nm_kor":"계룡면","nm_eng":"Gyeryong-myeon"},

{"cd":"34020340","nm_kor":"반포면","nm_eng":"Banpo-myeon"},

{"cd":"34020360","nm_kor":"의당면","nm_eng":"Uidang-myeon"},

{"cd":"34020370","nm_kor":"정안면","nm_eng":"Jeongan-myeon"},

{"cd":"34020380","nm_kor":"우성면","nm_eng":"Useong-myeon"},

{"cd":"34020390","nm_kor":"사곡면","nm_eng":"Sagok-myeon"},

{"cd":"34020400","nm_kor":"신풍면","nm_eng":"Sinpung-myeon"},

{"cd":"34020510","nm_kor":"중학동","nm_eng":"Junghak-dong"},

{"cd":"34020580","nm_kor":"웅진동","nm_eng":"Ungjin-dong"},

{"cd":"34020550","nm_kor":"금학동","nm_eng":"Geumhak-dong"},

{"cd":"34020560","nm_kor":"옥룡동","nm_eng":"Ongnyong-dong"},

{"cd":"34020570","nm_kor":"신관동","nm_eng":"Singwan-dong"},

{"cd":"34020590","nm_kor":"월송동","nm_eng":"wolsong-dong"},

{"cd":"34030000","nm_kor":"보령시","nm_eng":"Boryeong-si"},

{"cd":"34030110","nm_kor":"웅천읍","nm_eng":"Ungcheon-eup"},

{"cd":"34030310","nm_kor":"주포면","nm_eng":"Jupo-myeon"},

{"cd":"34030330","nm_kor":"오천면","nm_eng":"Ocheon-myeon"},

{"cd":"34030340","nm_kor":"천북면","nm_eng":"Cheonbuk-myeon"},

{"cd":"34030350","nm_kor":"청소면","nm_eng":"Cheongso-myeon"},

{"cd":"34030360","nm_kor":"청라면","nm_eng":"Cheongna-myeon"},

{"cd":"34030370","nm_kor":"남포면","nm_eng":"Nampo-myeon"},

{"cd":"34030380","nm_kor":"주산면","nm_eng":"Jusan-myeon"},

{"cd":"34030390","nm_kor":"미산면","nm_eng":"Misan-myeon"},

{"cd":"34030400","nm_kor":"성주면","nm_eng":"Seongju-myeon"},

{"cd":"34030320","nm_kor":"주교면","nm_eng":"Jugyo-myeon"},

{"cd":"34030510","nm_kor":"대천1동","nm_eng":"Daecheon 1(il)-dong"},

{"cd":"34030520","nm_kor":"대천2동","nm_eng":"Daecheon 2(i)-dong"},

{"cd":"34030530","nm_kor":"대천3동","nm_eng":"Daecheon 3(sam)-dong"},

{"cd":"34030540","nm_kor":"대천4동","nm_eng":"Daecheon4(sa)-dong"},

{"cd":"34030560","nm_kor":"대천5동","nm_eng":"Daecheon 5(o)-dong"},

{"cd":"34040000","nm_kor":"아산시","nm_eng":"Asan-si"},

{"cd":"34040110","nm_kor":"염치읍","nm_eng":"Yeomchi-eup"},

{"cd":"34040120","nm_kor":"배방읍","nm_eng":"Baebang-eup"},

{"cd":"34040310","nm_kor":"송악면 ","nm_eng":"Songak-myeon"},

{"cd":"34040330","nm_kor":"탕정면","nm_eng":"Tangjeong-myeon"},

{"cd":"34040340","nm_kor":"음봉면","nm_eng":"Eumbong-myeon"},

{"cd":"34040350","nm_kor":"둔포면","nm_eng":"Dunpo-myeon"},

{"cd":"34040360","nm_kor":"영인면","nm_eng":"Yeongin-myeon"},

{"cd":"34040370","nm_kor":"인주면","nm_eng":"Inju-myeon"},

{"cd":"34040380","nm_kor":"선장면","nm_eng":"Seonjang-myeon"},

{"cd":"34040390","nm_kor":"도고면","nm_eng":"Dogo-myeon"},

{"cd":"34040400","nm_kor":"신창면","nm_eng":"Sinchang-myeon"},

{"cd":"34040510","nm_kor":"온양1동","nm_eng":"Onyang 1(il)-dong"},

{"cd":"34040520","nm_kor":"온양2동","nm_eng":"Onyang 2(i)-dong"},

{"cd":"34040530","nm_kor":"온양3동","nm_eng":"Onyang 3(sam)-dong"},

{"cd":"34040540","nm_kor":"온양4동","nm_eng":"Onyang 4(sa)-dong"},

{"cd":"34040550","nm_kor":"온양5동","nm_eng":"Onyang 5(o)-dong"},

{"cd":"34040560","nm_kor":"온양6동","nm_eng":"Onyang 6(yuk)-dong"},

{"cd":"34050000","nm_kor":"서산시","nm_eng":"Seosan-si"},

{"cd":"34050110","nm_kor":"대산읍","nm_eng":"Daesan-eup"},

{"cd":"34050310","nm_kor":"인지면","nm_eng":"Inji-myeon"},

{"cd":"34050320","nm_kor":"부석면","nm_eng":"Buseok-myeon"},

{"cd":"34050330","nm_kor":"팔봉면","nm_eng":"Palbong-myeon"},

{"cd":"34050340","nm_kor":"지곡면","nm_eng":"Jigok-myeon"},

{"cd":"34050350","nm_kor":"성연면","nm_eng":"Seongyeon-myeon"},

{"cd":"34050360","nm_kor":"음암면","nm_eng":"Eumam-myeon"},

{"cd":"34050370","nm_kor":"운산면","nm_eng":"Unsan-myeon"},

{"cd":"34050380","nm_kor":"해미면","nm_eng":"Haemi-myeon"},

{"cd":"34050390","nm_kor":"고북면","nm_eng":"Gobuk-myeon"},

{"cd":"34050510","nm_kor":"부춘동","nm_eng":"Buchun-dong"},

{"cd":"34050520","nm_kor":"동문1동","nm_eng":"Dongmun 1(il)-dong"},

{"cd":"34050530","nm_kor":"동문2동","nm_eng":"Dongmun 2(i)-dong"},

{"cd":"34050540","nm_kor":"수석동","nm_eng":"Suseok-dong"},

{"cd":"34050550","nm_kor":"석남동 ","nm_eng":"Seongnam-dong"},

{"cd":"34060000","nm_kor":"논산시","nm_eng":"Nonsan-si"},

{"cd":"34060110","nm_kor":"강경읍","nm_eng":"Ganggyeong-eup"},

{"cd":"34060120","nm_kor":"연무읍","nm_eng":"Yeonmu-eup"},

{"cd":"34060310","nm_kor":"성동면","nm_eng":"Seongdong-myeon"},

{"cd":"34060320","nm_kor":"광석면","nm_eng":"Gwangseok-myeon"},

{"cd":"34060330","nm_kor":"노성면","nm_eng":"Noseong-myeon"},

{"cd":"34060340","nm_kor":"상월면","nm_eng":"Sangwol-myeon"},

{"cd":"34060350","nm_kor":"부적면","nm_eng":"Bujeok-myeon"},

{"cd":"34060360","nm_kor":"연산면","nm_eng":"Yeonsan-myeon"},

{"cd":"34060370","nm_kor":"벌곡면","nm_eng":"Beolgok-myeon"},

{"cd":"34060380","nm_kor":"양촌면","nm_eng":"Yangchon-myeon"},

{"cd":"34060390","nm_kor":"가야곡면","nm_eng":"Gayagok-myeon"},

{"cd":"34060400","nm_kor":"은진면","nm_eng":"Eunjin-myeon"},

{"cd":"34060410","nm_kor":"채운면","nm_eng":"Chaeun-myeon"},

{"cd":"34060510","nm_kor":"취암동","nm_eng":"Chwiam-dong"},

{"cd":"34060520","nm_kor":"부창동","nm_eng":"Buchang-dong"},

{"cd":"34070000","nm_kor":"계룡시","nm_eng":"Gyeryong-si"},

{"cd":"34070310","nm_kor":"두마면","nm_eng":"Duma-myeon"},

{"cd":"34070330","nm_kor":"엄사면","nm_eng":"Eomsa-myeon"},

{"cd":"34070340","nm_kor":"신도안면","nm_eng":"Sindoan_myeon"},

{"cd":"34070510","nm_kor":"금암동","nm_eng":"Geumam-dong"},

{"cd":"34080000","nm_kor":"당진시","nm_eng":"Dangjin-si"},

{"cd":"34080110","nm_kor":"합덕읍","nm_eng":"Hapdeok-eup"},

{"cd":"34080120","nm_kor":"송악읍","nm_eng":"Songak-eup"},

{"cd":"34080310","nm_kor":"고대면","nm_eng":"Godae-myeon"},

{"cd":"34080320","nm_kor":"석문면","nm_eng":"Seongmun-myeon"},

{"cd":"34080330","nm_kor":"대호지면","nm_eng":"Daehoji-myeon"},

{"cd":"34080340","nm_kor":"정미면","nm_eng":"Jeongmi-myeon"},

{"cd":"34080350","nm_kor":"면천면","nm_eng":"Myeoncheon-myeon"},

{"cd":"34080360","nm_kor":"순성면","nm_eng":"Sunseong-myeon"},

{"cd":"34080370","nm_kor":"우강면","nm_eng":"Ugang-myeon"},

{"cd":"34080380","nm_kor":"신평면","nm_eng":"Sinpyeong-myeon"},

{"cd":"34080390","nm_kor":"송산면","nm_eng":"Songsan-myeon"},

{"cd":"34080510","nm_kor":"당진1동","nm_eng":"Dangjin 1(il)-dong"},

{"cd":"34080520","nm_kor":"당진2동","nm_eng":"Dangjin 2(i)-dong"},

{"cd":"34080530","nm_kor":"당진3동","nm_eng":"Dangjin 3(sam)-dong"},

{"cd":"34510000","nm_kor":"금산군","nm_eng":"Geumsan-gun"},

{"cd":"34510110","nm_kor":"금산읍","nm_eng":"Geumsan-eup"},

{"cd":"34510310","nm_kor":"금성면","nm_eng":"Geumseong-myeon"},

{"cd":"34510320","nm_kor":"제원면","nm_eng":"Jewon-myeon"},

{"cd":"34510330","nm_kor":"부리면","nm_eng":"Buri-myeon"},

{"cd":"34510340","nm_kor":"군북면","nm_eng":"Gunbuk-myeon"},

{"cd":"34510350","nm_kor":"남일면","nm_eng":"Namil-myeon"},

{"cd":"34510360","nm_kor":"남이면","nm_eng":"Nami-myeon"},

{"cd":"34510370","nm_kor":"진산면","nm_eng":"Jinsan-myeon"},

{"cd":"34510380","nm_kor":"복수면","nm_eng":"Boksu-myeon"},

{"cd":"34510390","nm_kor":"추부면","nm_eng":"Chubu-myeon"},

{"cd":"34530000","nm_kor":"부여군","nm_eng":"Buyeo-gun"},

{"cd":"34530110","nm_kor":"부여읍","nm_eng":"Buyeo-eup"},

{"cd":"34530310","nm_kor":"규암면","nm_eng":"Gyuam-myeon"},

{"cd":"34530320","nm_kor":"은산면","nm_eng":"Eunsan-myeon"},

{"cd":"34530330","nm_kor":"외산면","nm_eng":"Oesan-myeon"},

{"cd":"34530340","nm_kor":"내산면","nm_eng":"Naesan-myeon"},

{"cd":"34530350","nm_kor":"구룡면","nm_eng":"Guryong-myeon"},

{"cd":"34530360","nm_kor":"홍산면","nm_eng":"Hongsan-myeon"},

{"cd":"34530370","nm_kor":"옥산면","nm_eng":"Oksan-myeon"},

{"cd":"34530380","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"34530390","nm_kor":"충화면","nm_eng":"Chunghwa-myeon"},

{"cd":"34530400","nm_kor":"양화면","nm_eng":"Yanghwa-myeon"},

{"cd":"34530410","nm_kor":"임천면","nm_eng":"Imcheon-myeon"},

{"cd":"34530420","nm_kor":"장암면","nm_eng":"Jangam-myeon"},

{"cd":"34530430","nm_kor":"세도면","nm_eng":"Sedo-myeon"},

{"cd":"34530440","nm_kor":"석성면","nm_eng":"Seokseong-myeon"},

{"cd":"34530450","nm_kor":"초촌면","nm_eng":"Chochon-myeon"},

{"cd":"34540000","nm_kor":"서천군","nm_eng":"Seocheon-gun"},

{"cd":"34540110","nm_kor":"장항읍","nm_eng":"Janghang-eup"},

{"cd":"34540120","nm_kor":"서천읍","nm_eng":"Seocheon-eup"},

{"cd":"34540310","nm_kor":"마서면","nm_eng":"Maseo-myeon"},

{"cd":"34540320","nm_kor":"화양면","nm_eng":"Hwayang-myeon"},

{"cd":"34540330","nm_kor":"기산면","nm_eng":"Gisan-myeon"},

{"cd":"34540340","nm_kor":"한산면","nm_eng":"Hansan-myeon"},

{"cd":"34540350","nm_kor":"마산면","nm_eng":"Masan-myeon"},

{"cd":"34540360","nm_kor":"시초면","nm_eng":"Sicho-myeon"},

{"cd":"34540370","nm_kor":"문산면","nm_eng":"Munsan-myeon"},

{"cd":"34540380","nm_kor":"판교면","nm_eng":"Pangyo-myeon"},

{"cd":"34540390","nm_kor":"종천면","nm_eng":"Jongcheon-myeon"},

{"cd":"34540400","nm_kor":"비인면","nm_eng":"Biin-myeon"},

{"cd":"34540410","nm_kor":"서면","nm_eng":"Seo-myeon"},

{"cd":"34550000","nm_kor":"청양군","nm_eng":"Cheongyang-gun"},

{"cd":"34550110","nm_kor":"청양읍","nm_eng":"Cheongyang-eup"},

{"cd":"34550310","nm_kor":"운곡면","nm_eng":"Ungok-myeon"},

{"cd":"34550320","nm_kor":"대치면","nm_eng":"Daechi-myeon"},

{"cd":"34550330","nm_kor":"정산면","nm_eng":"Jeongsan-myeon"},

{"cd":"34550340","nm_kor":"목면","nm_eng":"Mok-myeon"},

{"cd":"34550350","nm_kor":"청남면","nm_eng":"Cheongnam-myeon"},

{"cd":"34550360","nm_kor":"장평면","nm_eng":"Jangpyeong-myeon"},

{"cd":"34550370","nm_kor":"남양면","nm_eng":"Namyang-myeon"},

{"cd":"34550380","nm_kor":"화성면","nm_eng":"Hwaseong-myeon"},

{"cd":"34550390","nm_kor":"비봉면","nm_eng":"Bibong-myeon"},

{"cd":"34560000","nm_kor":"홍성군","nm_eng":"Hongseong-gun"},

{"cd":"34560110","nm_kor":"홍성읍","nm_eng":"Hongseong-eup"},

{"cd":"34560120","nm_kor":"광천읍","nm_eng":"Gwangcheon-eup"},

{"cd":"34560130","nm_kor":"홍북읍","nm_eng":"Hongbuk-eup"},

{"cd":"34560320","nm_kor":"금마면","nm_eng":"Geumma-myeon"},

{"cd":"34560330","nm_kor":"홍동면","nm_eng":"Hongdong-myeon"},

{"cd":"34560340","nm_kor":"장곡면","nm_eng":"Janggok-myeon"},

{"cd":"34560350","nm_kor":"은하면","nm_eng":"Eunha-myeon"},

{"cd":"34560360","nm_kor":"결성면","nm_eng":"Gyeolseong-myeon"},

{"cd":"34560370","nm_kor":"서부면","nm_eng":"Seobu-myeon"},

{"cd":"34560380","nm_kor":"갈산면","nm_eng":"Galsan-myeon"},

{"cd":"34560390","nm_kor":"구항면","nm_eng":"Guhang-myeon"},

{"cd":"34570000","nm_kor":"예산군","nm_eng":"Yesan-gun"},

{"cd":"34570110","nm_kor":"예산읍","nm_eng":"Yesan-eup"},

{"cd":"34570120","nm_kor":"삽교읍","nm_eng":"Sapgyo-eup"},

{"cd":"34570310","nm_kor":"대술면","nm_eng":"Daesul-myeon"},

{"cd":"34570320","nm_kor":"신양면","nm_eng":"Sinyang-myeon"},

{"cd":"34570330","nm_kor":"광시면","nm_eng":"Gwangsi-myeon"},

{"cd":"34570340","nm_kor":"대흥면","nm_eng":"Daeheung-myeon"},

{"cd":"34570350","nm_kor":"응봉면","nm_eng":"Eungbong-myeon"},

{"cd":"34570360","nm_kor":"덕산면","nm_eng":"Deoksan-myeon"},

{"cd":"34570370","nm_kor":"봉산면","nm_eng":"Bongsan-myeon"},

{"cd":"34570380","nm_kor":"고덕면","nm_eng":"Godeok-myeon"},

{"cd":"34570390","nm_kor":"신암면","nm_eng":"Sinam-myeon"},

{"cd":"34570400","nm_kor":"오가면","nm_eng":"Oga-myeon"},

{"cd":"34580000","nm_kor":"태안군","nm_eng":"Taean-gun"},

{"cd":"34580110","nm_kor":"태안읍","nm_eng":"Taean-eup"},

{"cd":"34580120","nm_kor":"안면읍","nm_eng":"Anmyeon-eup"},

{"cd":"34580310","nm_kor":"고남면","nm_eng":"Gonam-myeon"},

{"cd":"34580320","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"34580330","nm_kor":"근흥면","nm_eng":"Geunheung-myeon"},

{"cd":"34580340","nm_kor":"소원면","nm_eng":"Sowon-myeon"},

{"cd":"34580350","nm_kor":"원북면","nm_eng":"Wonbuk-myeon"},

{"cd":"34580360","nm_kor":"이원면","nm_eng":"Iwon-myeon"},

{"cd":"35000000","nm_kor":"전라북도","nm_eng":"Jeollabuk-do"},

{"cd":"35010000","nm_kor":"전주시","nm_eng":"Jeonju-si"},

{"cd":"35011000","nm_kor":"완산구","nm_eng":"Wansan-gu"},

{"cd":"35011740","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"35011750","nm_kor":"풍남동","nm_eng":"Pungnam-dong"},

{"cd":"35011760","nm_kor":"노송동","nm_eng":"Nosong-dong"},

{"cd":"35011770","nm_kor":"완산동","nm_eng":"Wansan-dong"},

{"cd":"35011600","nm_kor":"동서학동","nm_eng":"Dongseohak-dong"},

{"cd":"35011610","nm_kor":"서서학동","nm_eng":"Seoseohak-dong"},

{"cd":"35011620","nm_kor":"중화산1동","nm_eng":"Junghwasan 1(il)-dong"},

{"cd":"35011630","nm_kor":"중화산2동","nm_eng":"Junghwasan 2(i)-dong"},

{"cd":"35011660","nm_kor":"서신동","nm_eng":"Seosin-dong"},

{"cd":"35011640","nm_kor":"평화1동","nm_eng":"Pyeonghwa 1(il)-dong"},

{"cd":"35011650","nm_kor":"평화2동","nm_eng":"Pyeonghwa 2(i)-dong"},

{"cd":"35011670","nm_kor":"삼천1동","nm_eng":"Samcheon 1(il)-dong"},

{"cd":"35011680","nm_kor":"삼천2동","nm_eng":"Samcheon 2(i)-dong"},

{"cd":"35011690","nm_kor":"삼천3동","nm_eng":"Samcheon 3(sam)-dong"},

{"cd":"35011700","nm_kor":"효자1동","nm_eng":"Hyoja 1(il)-dong"},

{"cd":"35011710","nm_kor":"효자2동","nm_eng":"Hyoja 2(i)-dong"},

{"cd":"35011720","nm_kor":"효자3동","nm_eng":"Hyoja 3(sam)-dong"},

{"cd":"35011780","nm_kor":"효자4동","nm_eng":"Hyoja 4(sa)-dong"},

{"cd":"35011790","nm_kor":"효자5동","nm_eng":"Hyoja 5(o)-dong"},

{"cd":"35012000","nm_kor":"덕진구","nm_eng":"Deokjin-gu"},

{"cd":"35012690","nm_kor":"진북동","nm_eng":"Jinbuk-dong"},

{"cd":"35012540","nm_kor":"인후1동","nm_eng":"Inhu 1(il)-dong"},

{"cd":"35012550","nm_kor":"인후2동","nm_eng":"Inhu 2(i)-dong"},

{"cd":"35012560","nm_kor":"인후3동","nm_eng":"Inhu 3(sam)-dong"},

{"cd":"35012570","nm_kor":"덕진동","nm_eng":"Deokjin-dong"},

{"cd":"35012580","nm_kor":"금암1동","nm_eng":"Geumam 1(il)-dong"},

{"cd":"35012590","nm_kor":"금암2동","nm_eng":"Geumam 2(i)-dong"},

{"cd":"35012600","nm_kor":"팔복동","nm_eng":"Palbok-dong"},

{"cd":"35012610","nm_kor":"우아1동","nm_eng":"Ua 1(il)-dong"},

{"cd":"35012620","nm_kor":"우아2동","nm_eng":"Ua 2(i)-dong"},

{"cd":"35012630","nm_kor":"호성동","nm_eng":"Hoseong-dong"},

{"cd":"35012650","nm_kor":"송천1동","nm_eng":"Songcheon 1(il)-dong"},

{"cd":"35012660","nm_kor":"송천2동","nm_eng":"Songcheon 2(i)-dong"},

{"cd":"35012670","nm_kor":"조촌동","nm_eng":"Jochon-dong"},

{"cd":"35012710","nm_kor":"여의동","nm_eng":"Yeoui-dong"},

{"cd":"35012700","nm_kor":"혁신동","nm_eng":"Hyeoksin-dong"},

{"cd":"35020000","nm_kor":"군산시","nm_eng":"Gunsan-si"},

{"cd":"35020110","nm_kor":"옥구읍","nm_eng":"Okgu-eup"},

{"cd":"35020310","nm_kor":"옥산면","nm_eng":"Oksan-myeon"},

{"cd":"35020320","nm_kor":"회현면","nm_eng":"Hoehyeon-myeon"},

{"cd":"35020330","nm_kor":"임피면","nm_eng":"Impi-myeon"},

{"cd":"35020340","nm_kor":"서수면","nm_eng":"Seosu-myeon"},

{"cd":"35020350","nm_kor":"대야면","nm_eng":"Daeya-myeon"},

{"cd":"35020360","nm_kor":"개정면","nm_eng":"Gaejeong-myeon"},

{"cd":"35020370","nm_kor":"성산면","nm_eng":"Seongsan-myeon"},

{"cd":"35020380","nm_kor":"나포면","nm_eng":"Napo-myeon"},

{"cd":"35020390","nm_kor":"옥도면","nm_eng":"Okdo-myeon"},

{"cd":"35020400","nm_kor":"옥서면","nm_eng":"Okseo-myeon"},

{"cd":"35020510","nm_kor":"해신동","nm_eng":"Haesin-dong"},

{"cd":"35020530","nm_kor":"월명동","nm_eng":"Wolmyeong-dong"},

{"cd":"35020550","nm_kor":"신풍동","nm_eng":"Sinpung-dong"},

{"cd":"35020560","nm_kor":"삼학동","nm_eng":"Samhak-dong"},

{"cd":"35020600","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"35020640","nm_kor":"흥남동","nm_eng":"Heungnam-dong"},

{"cd":"35020650","nm_kor":"조촌동","nm_eng":"Jochon-dong"},

{"cd":"35020660","nm_kor":"경암동","nm_eng":"Gyeongam-dong"},

{"cd":"35020670","nm_kor":"구암동","nm_eng":"Guam-dong"},

{"cd":"35020680","nm_kor":"개정동","nm_eng":"Gaejeong-dong"},

{"cd":"35020690","nm_kor":"수송동","nm_eng":"Susong-dong"},

{"cd":"35020700","nm_kor":"나운1동","nm_eng":"Naun 1(il)-dong"},

{"cd":"35020710","nm_kor":"나운2동","nm_eng":"Naun 2(i)-dong"},

{"cd":"35020740","nm_kor":"나운3동","nm_eng":"Naun 3(sam)-dong"},

{"cd":"35020720","nm_kor":"소룡동","nm_eng":"Soryong-dong"},

{"cd":"35020730","nm_kor":"미성동","nm_eng":"Miseong-dong"},

{"cd":"35030000","nm_kor":"익산시","nm_eng":"Iksan-si"},

{"cd":"35030110","nm_kor":"함열읍","nm_eng":"Hamyeol-eup"},

{"cd":"35030310","nm_kor":"오산면","nm_eng":"Osan-myeon"},

{"cd":"35030320","nm_kor":"황등면","nm_eng":"Hwangdeung-myeon"},

{"cd":"35030330","nm_kor":"함라면","nm_eng":"Hamna-myeon"},

{"cd":"35030340","nm_kor":"웅포면","nm_eng":"Ungpo-myeon"},

{"cd":"35030350","nm_kor":"성당면","nm_eng":"Seongdang-myeon"},

{"cd":"35030360","nm_kor":"용안면","nm_eng":"Yongan-myeon"},

{"cd":"35030370","nm_kor":"낭산면","nm_eng":"Nangsan-myeon"},

{"cd":"35030380","nm_kor":"망성면","nm_eng":"Mangseong-myeon"},

{"cd":"35030390","nm_kor":"여산면","nm_eng":"Yeosan-myeon"},

{"cd":"35030400","nm_kor":"금마면","nm_eng":"Geumma-myeon"},

{"cd":"35030410","nm_kor":"왕궁면","nm_eng":"Wanggung-myeon"},

{"cd":"35030420","nm_kor":"춘포면","nm_eng":"Chunpo-myeon"},

{"cd":"35030430","nm_kor":"삼기면","nm_eng":"Samgi-myeon"},

{"cd":"35030440","nm_kor":"용동면","nm_eng":"Yongdong-myeon"},

{"cd":"35030510","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"35030530","nm_kor":"평화동","nm_eng":"Pyeonghwa-dong"},

{"cd":"35030550","nm_kor":"인화동","nm_eng":"Inhwa-dong"},

{"cd":"35030570","nm_kor":"동산동","nm_eng":"Dongsan-dong"},

{"cd":"35030580","nm_kor":"마동","nm_eng":"Ma-dong"},

{"cd":"35030590","nm_kor":"남중동","nm_eng":"Namjung-dong"},

{"cd":"35030610","nm_kor":"모현동","nm_eng":"Mohyeon-dong"},

{"cd":"35030620","nm_kor":"송학동","nm_eng":"Songhak-dong"},

{"cd":"35030660","nm_kor":"영등1동","nm_eng":"Yeongdeung 1(il)-dong"},

{"cd":"35030710","nm_kor":"영등2동","nm_eng":"Yeongdeung 2(i)-dong"},

{"cd":"35030720","nm_kor":"어양동","nm_eng":"Eoyang-dong"},

{"cd":"35030650","nm_kor":"신동","nm_eng":"Sin-dong"},

{"cd":"35030690","nm_kor":"팔봉동","nm_eng":"Palbong-dong"},

{"cd":"35030700","nm_kor":"삼성동","nm_eng":"Samseong-dong"},

{"cd":"35040000","nm_kor":"정읍시","nm_eng":"Jeongeup-si"},

{"cd":"35040110","nm_kor":"신태인읍","nm_eng":"Sintaein-eup"},

{"cd":"35040310","nm_kor":"북면","nm_eng":"Buk-myeon"},

{"cd":"35040320","nm_kor":"입암면","nm_eng":"Ibam-myeon"},

{"cd":"35040330","nm_kor":"소성면","nm_eng":"Soseong-myeon"},

{"cd":"35040340","nm_kor":"고부면","nm_eng":"Gobu-myeon"},

{"cd":"35040350","nm_kor":"영원면","nm_eng":"Yeongwon-myeon"},

{"cd":"35040360","nm_kor":"덕천면","nm_eng":"Deokcheon-myeon"},

{"cd":"35040370","nm_kor":"이평면","nm_eng":"Ipyeong-myeon"},

{"cd":"35040380","nm_kor":"정우면","nm_eng":"Jeongu-myeon"},

{"cd":"35040390","nm_kor":"태인면","nm_eng":"Taein-myeon"},

{"cd":"35040400","nm_kor":"감곡면","nm_eng":"Gamgok-myeon"},

{"cd":"35040410","nm_kor":"옹동면","nm_eng":"Ongdong-myeon"},

{"cd":"35040420","nm_kor":"칠보면","nm_eng":"Chilbo-myeon"},

{"cd":"35040430","nm_kor":"산내면","nm_eng":"Sannae-myeon"},

{"cd":"35040440","nm_kor":"산외면","nm_eng":"Sanoe-myeon"},

{"cd":"35040510","nm_kor":"수성동","nm_eng":"Suseong-dong"},

{"cd":"35040520","nm_kor":"장명동","nm_eng":"Jangmyeong-dong"},

{"cd":"35040530","nm_kor":"내장상동","nm_eng":"Naejangsang-dong"},

{"cd":"35040540","nm_kor":"시기동","nm_eng":"Sigi-dong"},

{"cd":"35040600","nm_kor":"초산동","nm_eng":"Chosan-dong"},

{"cd":"35040570","nm_kor":"연지동","nm_eng":"Yeonji-dong"},

{"cd":"35040580","nm_kor":"농소동","nm_eng":"Nongso-dong"},

{"cd":"35040590","nm_kor":"상교동","nm_eng":"Sanggyo-dong"},

{"cd":"35050000","nm_kor":"남원시","nm_eng":"Namwon-si"},

{"cd":"35050110","nm_kor":"운봉읍","nm_eng":"Unbong-eup"},

{"cd":"35050310","nm_kor":"주천면","nm_eng":"Jucheon-myeon"},

{"cd":"35050320","nm_kor":"수지면","nm_eng":"Suji-myeon"},

{"cd":"35050330","nm_kor":"송동면","nm_eng":"Songdong-myeon"},

{"cd":"35050340","nm_kor":"주생면","nm_eng":"Jusaeng-myeon"},

{"cd":"35050350","nm_kor":"금지면","nm_eng":"Geumji-myeon"},

{"cd":"35050360","nm_kor":"대강면","nm_eng":"Daegang-myeon"},

{"cd":"35050370","nm_kor":"대산면","nm_eng":"Daesan-myeon"},

{"cd":"35050380","nm_kor":"사매면","nm_eng":"Samae-myeon"},

{"cd":"35050390","nm_kor":"덕과면","nm_eng":"Deokgwa-myeon"},

{"cd":"35050400","nm_kor":"보절면","nm_eng":"Bojeol-myeon"},

{"cd":"35050410","nm_kor":"산동면","nm_eng":"Sandong-myeon"},

{"cd":"35050420","nm_kor":"이백면","nm_eng":"Ibaek-myeon"},

{"cd":"35050440","nm_kor":"아영면","nm_eng":"Ayeong-myeon"},

{"cd":"35050450","nm_kor":"산내면","nm_eng":"Sannae-myeon"},

{"cd":"35050430","nm_kor":"인월면","nm_eng":"Inwol-myeon"},

{"cd":"35050510","nm_kor":"동충동","nm_eng":"Dongchung-dong"},

{"cd":"35050520","nm_kor":"죽항동","nm_eng":"Jukhang-dong"},

{"cd":"35050540","nm_kor":"노암동","nm_eng":"Noam-dong"},

{"cd":"35050550","nm_kor":"금동","nm_eng":"Geum-dong"},

{"cd":"35050560","nm_kor":"왕정동","nm_eng":"Wangjeong-dong"},

{"cd":"35050570","nm_kor":"향교동","nm_eng":"Hyanggyo-dong"},

{"cd":"35050590","nm_kor":"도통동","nm_eng":"Dotong-dong"},

{"cd":"35060000","nm_kor":"김제시","nm_eng":"Gimje-si"},

{"cd":"35060110","nm_kor":"만경읍","nm_eng":"Mangyeong-eup"},

{"cd":"35060310","nm_kor":"죽산면","nm_eng":"Juksan-myeon"},

{"cd":"35060320","nm_kor":"백산면","nm_eng":"Baeksan-myeon"},

{"cd":"35060330","nm_kor":"용지면","nm_eng":"Yongji-myeon"},

{"cd":"35060340","nm_kor":"백구면","nm_eng":"Baekgu-myeon"},

{"cd":"35060350","nm_kor":"부량면","nm_eng":"Buryang-myeon"},

{"cd":"35060360","nm_kor":"공덕면","nm_eng":"Gongdeok-myeon"},

{"cd":"35060370","nm_kor":"청하면","nm_eng":"Cheongha-myeon"},

{"cd":"35060380","nm_kor":"성덕면","nm_eng":"Seongdeok-myeon"},

{"cd":"35060390","nm_kor":"진봉면","nm_eng":"Jinbong-myeon"},

{"cd":"35060400","nm_kor":"금구면","nm_eng":"Geumgu-myeon"},

{"cd":"35060410","nm_kor":"봉남면","nm_eng":"Bongnam-myeon"},

{"cd":"35060420","nm_kor":"황산면","nm_eng":"Hwangsan-myeon"},

{"cd":"35060430","nm_kor":"금산면","nm_eng":"Geumsan-myeon"},

{"cd":"35060440","nm_kor":"광활면","nm_eng":"Gwanghwal-myeon"},

{"cd":"35060510","nm_kor":"요촌동","nm_eng":"Yochon-dong"},

{"cd":"35060520","nm_kor":"신풍동","nm_eng":"Sinpung-dong"},

{"cd":"35060540","nm_kor":"검산동","nm_eng":"Geomsan-dong"},

{"cd":"35060580","nm_kor":"교월동","nm_eng":"Gyowol-dong"},

{"cd":"35510000","nm_kor":"완주군","nm_eng":"Wanju-gun"},

{"cd":"35510110","nm_kor":"삼례읍","nm_eng":"Samnye-eup"},

{"cd":"35510120","nm_kor":"봉동읍","nm_eng":"Bongdong-eup"},

{"cd":"35510130","nm_kor":"용진읍","nm_eng":"Yongjin-eup"},

{"cd":"35510320","nm_kor":"상관면","nm_eng":"Sanggwan-myeon"},

{"cd":"35510330","nm_kor":"이서면","nm_eng":"Iseo-myeon"},

{"cd":"35510340","nm_kor":"소양면","nm_eng":"Soyang-myeon"},

{"cd":"35510350","nm_kor":"구이면","nm_eng":"Gui-myeon"},

{"cd":"35510360","nm_kor":"고산면","nm_eng":"Gosan-myeon"},

{"cd":"35510370","nm_kor":"비봉면","nm_eng":"Bibong-myeon"},

{"cd":"35510380","nm_kor":"운주면","nm_eng":"Unju-myeon"},

{"cd":"35510390","nm_kor":"화산면","nm_eng":"Hwasan-myeon"},

{"cd":"35510400","nm_kor":"동상면","nm_eng":"Dongsang-myeon"},

{"cd":"35510410","nm_kor":"경천면","nm_eng":"Gyeongcheon-myeon"},

{"cd":"35520000","nm_kor":"진안군","nm_eng":"Jinan-gun"},

{"cd":"35520110","nm_kor":"진안읍","nm_eng":"Jinan-eup"},

{"cd":"35520310","nm_kor":"용담면","nm_eng":"Yongdam-myeon"},

{"cd":"35520320","nm_kor":"안천면","nm_eng":"Ancheon-myeon"},

{"cd":"35520330","nm_kor":"동향면","nm_eng":"Donghyang-myeon"},

{"cd":"35520340","nm_kor":"상전면","nm_eng":"Sangjeon-myeon"},

{"cd":"35520350","nm_kor":"백운면","nm_eng":"Baegun-myeon"},

{"cd":"35520360","nm_kor":"성수면","nm_eng":"Seongsu-myeon"},

{"cd":"35520370","nm_kor":"마령면","nm_eng":"Maryeong-myeon"},

{"cd":"35520380","nm_kor":"부귀면","nm_eng":"Bugwi-myeon"},

{"cd":"35520390","nm_kor":"정천면","nm_eng":"Jeongcheon-myeon"},

{"cd":"35520400","nm_kor":"주천면","nm_eng":"Jucheon-myeon"},

{"cd":"35530000","nm_kor":"무주군","nm_eng":"Muju-gun"},

{"cd":"35530110","nm_kor":"무주읍","nm_eng":"Muju-eup"},

{"cd":"35530310","nm_kor":"무풍면","nm_eng":"Mupung-myeon"},

{"cd":"35530320","nm_kor":"설천면","nm_eng":"Seolcheon-myeon"},

{"cd":"35530330","nm_kor":"적상면","nm_eng":"Jeoksang-myeon"},

{"cd":"35530340","nm_kor":"안성면","nm_eng":"Anseong-myeon"},

{"cd":"35530350","nm_kor":"부남면","nm_eng":"Bunam-myeon"},

{"cd":"35540000","nm_kor":"장수군","nm_eng":"Jangsu-gun"},

{"cd":"35540110","nm_kor":"장수읍","nm_eng":"Jangsu-eup"},

{"cd":"35540310","nm_kor":"산서면","nm_eng":"Sanseo-myeon"},

{"cd":"35540320","nm_kor":"번암면","nm_eng":"Beonam-myeon"},

{"cd":"35540330","nm_kor":"장계면","nm_eng":"Janggye-myeon"},

{"cd":"35540340","nm_kor":"천천면","nm_eng":"Cheoncheon-myeon"},

{"cd":"35540350","nm_kor":"계남면","nm_eng":"Gyenam-myeon"},

{"cd":"35540360","nm_kor":"계북면","nm_eng":"Gyebuk-myeon"},

{"cd":"35550000","nm_kor":"임실군","nm_eng":"Imsil-gun"},

{"cd":"35550110","nm_kor":"임실읍","nm_eng":"Imsil-eup"},

{"cd":"35550310","nm_kor":"청웅면","nm_eng":"Cheongung-myeon"},

{"cd":"35550320","nm_kor":"운암면","nm_eng":"Unam-myeon"},

{"cd":"35550330","nm_kor":"신평면","nm_eng":"Sinpyeong-myeon"},

{"cd":"35550340","nm_kor":"성수면","nm_eng":"Seongsu-myeon"},

{"cd":"35550350","nm_kor":"오수면","nm_eng":"Osu-myeon"},

{"cd":"35550360","nm_kor":"신덕면","nm_eng":"Sindeok-myeon"},

{"cd":"35550370","nm_kor":"삼계면","nm_eng":"Samgye-myeon"},

{"cd":"35550380","nm_kor":"관촌면","nm_eng":"Gwanchon-myeon"},

{"cd":"35550390","nm_kor":"강진면","nm_eng":"Gangjin-myeon"},

{"cd":"35550400","nm_kor":"덕치면","nm_eng":"Deokchi-myeon"},

{"cd":"35550410","nm_kor":"지사면","nm_eng":"Jisa-myeon"},

{"cd":"35560000","nm_kor":"순창군","nm_eng":"Sunchang-gun"},

{"cd":"35560110","nm_kor":"순창읍","nm_eng":"Sunchang-eup"},

{"cd":"35560310","nm_kor":"인계면","nm_eng":"Ingye-myeon"},

{"cd":"35560320","nm_kor":"동계면","nm_eng":"Donggye-myeon"},

{"cd":"35560350","nm_kor":"풍산면","nm_eng":"Pungsan-myeon"},

{"cd":"35560360","nm_kor":"금과면","nm_eng":"Geumgwa-myeon"},

{"cd":"35560370","nm_kor":"팔덕면","nm_eng":"Paldeok-myeon"},

{"cd":"35560390","nm_kor":"쌍치면","nm_eng":"Ssangchi-myeon"},

{"cd":"35560380","nm_kor":"복흥면","nm_eng":"Bokheung-myeon"},

{"cd":"35560330","nm_kor":"적성면","nm_eng":"Jeokseong-myeon"},

{"cd":"35560340","nm_kor":"유등면","nm_eng":"Yudeung-myeon"},

{"cd":"35560400","nm_kor":"구림면","nm_eng":"Gurim-myeon"},

{"cd":"35570000","nm_kor":"고창군","nm_eng":"Gochang-gun"},

{"cd":"35570110","nm_kor":"고창읍","nm_eng":"Gochang-eup"},

{"cd":"35570310","nm_kor":"고수면","nm_eng":"Gosu-myeon"},

{"cd":"35570320","nm_kor":"아산면","nm_eng":"Asan-myeon"},

{"cd":"35570330","nm_kor":"무장면","nm_eng":"Mujang-myeon"},

{"cd":"35570340","nm_kor":"공음면","nm_eng":"Gongeum-myeon"},

{"cd":"35570350","nm_kor":"상하면","nm_eng":"Sangha-myeon"},

{"cd":"35570360","nm_kor":"해리면","nm_eng":"Haeri-myeon"},

{"cd":"35570370","nm_kor":"성송면","nm_eng":"Seongsong-myeon"},

{"cd":"35570380","nm_kor":"대산면","nm_eng":"Daesan-myeon"},

{"cd":"35570390","nm_kor":"심원면","nm_eng":"Simwon-myeon"},

{"cd":"35570400","nm_kor":"흥덕면","nm_eng":"Heungdeok-myeon"},

{"cd":"35570410","nm_kor":"성내면","nm_eng":"Seongnae-myeon"},

{"cd":"35570420","nm_kor":"신림면","nm_eng":"Sillim-myeon"},

{"cd":"35570430","nm_kor":"부안면","nm_eng":"Buan-myeon"},

{"cd":"35580000","nm_kor":"부안군","nm_eng":"Buan-gun"},

{"cd":"35580110","nm_kor":"부안읍","nm_eng":"Buan-eup"},

{"cd":"35580310","nm_kor":"주산면","nm_eng":"Jusan-myeon"},

{"cd":"35580320","nm_kor":"동진면","nm_eng":"Dongjin-myeon"},

{"cd":"35580330","nm_kor":"행안면","nm_eng":"Haengan-myeon"},

{"cd":"35580340","nm_kor":"계화면","nm_eng":"Gyehwa-myeon"},

{"cd":"35580350","nm_kor":"보안면","nm_eng":"Boan-myeon"},

{"cd":"35580360","nm_kor":"변산면","nm_eng":"Byeonsan-myeon"},

{"cd":"35580370","nm_kor":"진서면","nm_eng":"Jinseo-myeon"},

{"cd":"35580380","nm_kor":"백산면","nm_eng":"Baeksan-myeon"},

{"cd":"35580390","nm_kor":"상서면","nm_eng":"Sangseo-myeon"},

{"cd":"35580400","nm_kor":"하서면","nm_eng":"Haseo-myeon"},

{"cd":"35580410","nm_kor":"줄포면","nm_eng":"Julpo-myeon"},

{"cd":"35580420","nm_kor":"위도면","nm_eng":"Wido-myeon"},

{"cd":"36000000","nm_kor":"전라남도","nm_eng":"Jeollanam-do"},

{"cd":"36010000","nm_kor":"목포시","nm_eng":"Mokpo-si"},

{"cd":"36010510","nm_kor":"용당1동","nm_eng":"Yongdang 1(il)-dong"},

{"cd":"36010520","nm_kor":"용당2동","nm_eng":"Yongdang 2(i)-dong"},

{"cd":"36010530","nm_kor":"연동","nm_eng":"Yeon-dong"},

{"cd":"36010550","nm_kor":"산정동","nm_eng":"Sanjeong-dong"},

{"cd":"36010560","nm_kor":"연산동","nm_eng":"Yeonsan-dong"},

{"cd":"36010570","nm_kor":"원산동","nm_eng":"Wonsan-dong"},

{"cd":"36010580","nm_kor":"대성동","nm_eng":"Daeseong-dong"},

{"cd":"36010600","nm_kor":"목원동","nm_eng":"Mokwon-dong"},

{"cd":"36010620","nm_kor":"동명동","nm_eng":"Dongmyeong-dong"},

{"cd":"36010630","nm_kor":"삼학동","nm_eng":"Samhak-dong"},

{"cd":"36010640","nm_kor":"만호동","nm_eng":"Manho-dong"},

{"cd":"36010650","nm_kor":"유달동","nm_eng":"Yudal-dong"},

{"cd":"36010670","nm_kor":"죽교동","nm_eng":"Jukgyo-dong"},

{"cd":"36010680","nm_kor":"북항동","nm_eng":"Bukhang-dong"},

{"cd":"36010690","nm_kor":"용해동","nm_eng":"Yonghae-dong"},

{"cd":"36010700","nm_kor":"이로동","nm_eng":"Iro-dong"},

{"cd":"36010710","nm_kor":"상동","nm_eng":"Sang-dong"},

{"cd":"36010720","nm_kor":"하당동","nm_eng":"Hadang-dong"},

{"cd":"36010730","nm_kor":"신흥동","nm_eng":"Sinheung-dong"},

{"cd":"36010740","nm_kor":"삼향동","nm_eng":"Samhyang-dong"},

{"cd":"36010750","nm_kor":"옥암동","nm_eng":"Ogam-dong"},

{"cd":"36010760","nm_kor":"부흥동","nm_eng":"Buheung-dong"},

{"cd":"36010770","nm_kor":"부주동","nm_eng":"Buju-dong"},

{"cd":"36020000","nm_kor":"여수시","nm_eng":"Yeosu-si"},

{"cd":"36020110","nm_kor":"돌산읍","nm_eng":"Dolsan-eup"},

{"cd":"36020310","nm_kor":"소라면","nm_eng":"Sora-myeon"},

{"cd":"36020320","nm_kor":"율촌면","nm_eng":"Yulchon-myeon"},

{"cd":"36020330","nm_kor":"화양면","nm_eng":"Hwayang-myeon"},

{"cd":"36020340","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"36020350","nm_kor":"화정면","nm_eng":"Hwajeong-myeon"},

{"cd":"36020360","nm_kor":"삼산면","nm_eng":"Samsan-myeon"},

{"cd":"36020510","nm_kor":"동문동","nm_eng":"Dongmun-dong"},

{"cd":"36020520","nm_kor":"한려동","nm_eng":"Hallyeo-dong"},

{"cd":"36020530","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"36020540","nm_kor":"충무동","nm_eng":"Chungmu-dong"},

{"cd":"36020550","nm_kor":"광림동","nm_eng":"Gwangnim-dong"},

{"cd":"36020560","nm_kor":"서강동","nm_eng":"Seogang-dong"},

{"cd":"36020570","nm_kor":"대교동","nm_eng":"Daegyo-dong"},

{"cd":"36020580","nm_kor":"국동","nm_eng":"Guk-dong"},

{"cd":"36020590","nm_kor":"월호동","nm_eng":"Wolho-dong"},

{"cd":"36020600","nm_kor":"여서동","nm_eng":"Yeoseo-dong"},

{"cd":"36020610","nm_kor":"문수동","nm_eng":"Munsu-dong"},

{"cd":"36020620","nm_kor":"미평동","nm_eng":"Mipyeong-dong"},

{"cd":"36020630","nm_kor":"둔덕동","nm_eng":"Dundeok-dong"},

{"cd":"36020640","nm_kor":"만덕동","nm_eng":"Mandeok-dong"},

{"cd":"36020650","nm_kor":"쌍봉동","nm_eng":"Ssangbong-dong"},

{"cd":"36020660","nm_kor":"시전동","nm_eng":"Sijeon-dong"},

{"cd":"36020670","nm_kor":"여천동","nm_eng":"Yeocheon-dong"},

{"cd":"36020680","nm_kor":"주삼동","nm_eng":"Jusam-dong"},

{"cd":"36020690","nm_kor":"삼일동","nm_eng":"Samil-dong"},

{"cd":"36020700","nm_kor":"묘도동","nm_eng":"Myodo-dong"},

{"cd":"36030000","nm_kor":"순천시","nm_eng":"Suncheon-si"},

{"cd":"36030110","nm_kor":"승주읍","nm_eng":"Seungju-eup"},

{"cd":"36030370","nm_kor":"해룡면","nm_eng":"Haeryong-myeon"},

{"cd":"36030380","nm_kor":"서면","nm_eng":"Seo-myeon"},

{"cd":"36030390","nm_kor":"황전면","nm_eng":"Hwangjeon-myeon"},

{"cd":"36030400","nm_kor":"월등면","nm_eng":"Woldeung-myeon"},

{"cd":"36030310","nm_kor":"주암면","nm_eng":"Juam-myeon"},

{"cd":"36030320","nm_kor":"송광면","nm_eng":"Songgwang-myeon"},

{"cd":"36030330","nm_kor":"외서면","nm_eng":"Oeseo-myeon"},

{"cd":"36030340","nm_kor":"낙안면","nm_eng":"Nagan-myeon"},

{"cd":"36030350","nm_kor":"별량면","nm_eng":"Byeollyang-myeon"},

{"cd":"36030360","nm_kor":"상사면","nm_eng":"Sangsa-myeon"},

{"cd":"36030510","nm_kor":"향동","nm_eng":"Hyang-dong"},

{"cd":"36030540","nm_kor":"매곡동","nm_eng":"Maegok-dong"},

{"cd":"36030550","nm_kor":"삼산동","nm_eng":"Samsan-dong"},

{"cd":"36030560","nm_kor":"조곡동","nm_eng":"Jogok-dong"},

{"cd":"36030570","nm_kor":"덕연동","nm_eng":"Deogyeon-dong"},

{"cd":"36030580","nm_kor":"풍덕동","nm_eng":"Pungdeok-dong"},

{"cd":"36030590","nm_kor":"남제동","nm_eng":"Namje-dong"},

{"cd":"36030600","nm_kor":"저전동","nm_eng":"Jeojeon-dong"},

{"cd":"36030610","nm_kor":"장천동","nm_eng":"Jangcheon-dong"},

{"cd":"36030620","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"36030630","nm_kor":"도사동","nm_eng":"Dosa-dong"},

{"cd":"36030660","nm_kor":"왕조1동","nm_eng":"Wangjo 1(il)dong"},

{"cd":"36030670","nm_kor":"왕조2동","nm_eng":"Wangjo 2(i)dong"},

{"cd":"36040000","nm_kor":"나주시","nm_eng":"Naju-si"},

{"cd":"36040110","nm_kor":"남평읍","nm_eng":"Nampyeong-eup"},

{"cd":"36040310","nm_kor":"세지면","nm_eng":"Seji-myeon"},

{"cd":"36040320","nm_kor":"왕곡면","nm_eng":"Wanggok-myeon"},

{"cd":"36040330","nm_kor":"반남면","nm_eng":"Bannam-myeon"},

{"cd":"36040340","nm_kor":"공산면","nm_eng":"Gongsan-myeon"},

{"cd":"36040350","nm_kor":"동강면","nm_eng":"Donggang-myeon"},

{"cd":"36040360","nm_kor":"다시면","nm_eng":"Dasi-myeon"},

{"cd":"36040370","nm_kor":"문평면","nm_eng":"Munpyeong-myeon"},

{"cd":"36040380","nm_kor":"노안면","nm_eng":"Noan-myeon"},

{"cd":"36040390","nm_kor":"금천면","nm_eng":"Geumcheon-myeon"},

{"cd":"36040400","nm_kor":"산포면","nm_eng":"Sanpo-myeon"},

{"cd":"36040410","nm_kor":"다도면","nm_eng":"Dado-myeon"},

{"cd":"36040420","nm_kor":"봉황면","nm_eng":"Bonghwang-myeon"},

{"cd":"36040510","nm_kor":"송월동","nm_eng":"Songwol-dong"},

{"cd":"36040520","nm_kor":"영강동","nm_eng":"Yeonggang-dong"},

{"cd":"36040540","nm_kor":"금남동","nm_eng":"Geumnam-dong"},

{"cd":"36040550","nm_kor":"성북동","nm_eng":"Seongbuk-dong"},

{"cd":"36040580","nm_kor":"영산동","nm_eng":"Yeongsan-dong"},

{"cd":"36040600","nm_kor":"이창동","nm_eng":"Ichang-dong"},

{"cd":"36040610","nm_kor":"빛가람동","nm_eng":"Bitgaram-dong"},

{"cd":"36060000","nm_kor":"광양시","nm_eng":"Gwangyang-si"},

{"cd":"36060110","nm_kor":"광양읍","nm_eng":"Gwangyang-eup"},

{"cd":"36060310","nm_kor":"봉강면","nm_eng":"Bonggang-myeon"},

{"cd":"36060320","nm_kor":"옥룡면","nm_eng":"Ongnyong-myeon"},

{"cd":"36060330","nm_kor":"옥곡면","nm_eng":"Okgok-myeon"},

{"cd":"36060340","nm_kor":"진상면","nm_eng":"Jinsang-myeon"},

{"cd":"36060350","nm_kor":"진월면","nm_eng":"Jinwol-myeon"},

{"cd":"36060360","nm_kor":"다압면","nm_eng":"Daap-myeon"},

{"cd":"36060510","nm_kor":"골약동","nm_eng":"Golyak-dong"},

{"cd":"36060530","nm_kor":"중마동","nm_eng":"Jungma-dong"},

{"cd":"36060540","nm_kor":"광영동","nm_eng":"Gwangyeong-dong"},

{"cd":"36060560","nm_kor":"금호동","nm_eng":"Geumho-dong"},

{"cd":"36060550","nm_kor":"태인동","nm_eng":"Taein-dong"},

{"cd":"36510000","nm_kor":"담양군","nm_eng":"Damyang-gun"},

{"cd":"36510110","nm_kor":"담양읍","nm_eng":"Damyang-eup"},

{"cd":"36510310","nm_kor":"봉산면","nm_eng":"Bongsan-myeon"},

{"cd":"36510320","nm_kor":"고서면","nm_eng":"Goseo-myeon"},

{"cd":"36510420","nm_kor":"가사문학면","nm_eng":"Gasamunhak-myeon"},

{"cd":"36510340","nm_kor":"창평면","nm_eng":"Changpyeong-myeon"},

{"cd":"36510350","nm_kor":"대덕면","nm_eng":"Daedeok-myeon"},

{"cd":"36510360","nm_kor":"무정면","nm_eng":"Mujeong-myeon"},

{"cd":"36510370","nm_kor":"금성면","nm_eng":"Geumseong-myeon"},

{"cd":"36510380","nm_kor":"용면","nm_eng":"Yong-myeon"},

{"cd":"36510390","nm_kor":"월산면","nm_eng":"Wolsan-myeon"},

{"cd":"36510400","nm_kor":"수북면","nm_eng":"Subuk-myeon"},

{"cd":"36510410","nm_kor":"대전면","nm_eng":"Daejeon-myeon"},

{"cd":"36520000","nm_kor":"곡성군","nm_eng":"Gokseong-gun"},

{"cd":"36520110","nm_kor":"곡성읍","nm_eng":"Gokseong-eup"},

{"cd":"36520310","nm_kor":"오곡면","nm_eng":"Ogok-myeon"},

{"cd":"36520320","nm_kor":"삼기면","nm_eng":"Samgi-myeon"},

{"cd":"36520330","nm_kor":"석곡면","nm_eng":"Seokgok-myeon"},

{"cd":"36520340","nm_kor":"목사동면","nm_eng":"Moksadong-myeon"},

{"cd":"36520350","nm_kor":"죽곡면","nm_eng":"Jukgok-myeon"},

{"cd":"36520360","nm_kor":"고달면","nm_eng":"Godal-myeon"},

{"cd":"36520370","nm_kor":"옥과면","nm_eng":"Okgwa-myeon"},

{"cd":"36520380","nm_kor":"입면","nm_eng":"Ip-myeon"},

{"cd":"36520390","nm_kor":"겸면","nm_eng":"Gyeom-myeon"},

{"cd":"36520400","nm_kor":"오산면","nm_eng":"Osan-myeon"},

{"cd":"36530000","nm_kor":"구례군","nm_eng":"Gurye-gun"},

{"cd":"36530110","nm_kor":"구례읍","nm_eng":"Gurye-eup"},

{"cd":"36530310","nm_kor":"문척면","nm_eng":"Muncheok-myeon"},

{"cd":"36530320","nm_kor":"간전면","nm_eng":"Ganjeon-myeon"},

{"cd":"36530330","nm_kor":"토지면","nm_eng":"Toji-myeon"},

{"cd":"36530340","nm_kor":"마산면","nm_eng":"Masan-myeon"},

{"cd":"36530350","nm_kor":"광의면","nm_eng":"Gwangui-myeon"},

{"cd":"36530360","nm_kor":"용방면","nm_eng":"Yongbang-myeon"},

{"cd":"36530370","nm_kor":"산동면","nm_eng":"Sandong-myeon"},

{"cd":"36550000","nm_kor":"고흥군","nm_eng":"Goheung-gun"},

{"cd":"36550110","nm_kor":"고흥읍","nm_eng":"Goheung-eup"},

{"cd":"36550120","nm_kor":"도양읍","nm_eng":"Doyang-eup"},

{"cd":"36550310","nm_kor":"풍양면","nm_eng":"Pungyang-myeon"},

{"cd":"36550320","nm_kor":"도덕면","nm_eng":"Dodeok-myeon"},

{"cd":"36550330","nm_kor":"금산면","nm_eng":"Geumsan-myeon"},

{"cd":"36550340","nm_kor":"도화면","nm_eng":"Dohwa-myeon"},

{"cd":"36550350","nm_kor":"포두면","nm_eng":"Podu-myeon"},

{"cd":"36550360","nm_kor":"봉래면","nm_eng":"Bongnae-myeon"},

{"cd":"36550380","nm_kor":"점암면","nm_eng":"Jeomam-myeon"},

{"cd":"36550400","nm_kor":"과역면","nm_eng":"Gwayeok-myeon"},

{"cd":"36550410","nm_kor":"남양면","nm_eng":"Namyang-myeon"},

{"cd":"36550420","nm_kor":"동강면","nm_eng":"Donggang-myeon"},

{"cd":"36550430","nm_kor":"대서면","nm_eng":"Daeseo-myeon"},

{"cd":"36550440","nm_kor":"두원면","nm_eng":"Duwon-myeon"},

{"cd":"36550390","nm_kor":"영남면","nm_eng":"Yeongnam-myeon"},

{"cd":"36550370","nm_kor":"동일면","nm_eng":"Dongil-myeon"},

{"cd":"36560000","nm_kor":"보성군","nm_eng":"Boseong-gun"},

{"cd":"36560110","nm_kor":"보성읍","nm_eng":"Boseong-eup"},

{"cd":"36560120","nm_kor":"벌교읍","nm_eng":"Beolgyo-eup"},

{"cd":"36560310","nm_kor":"노동면","nm_eng":"Nodong-myeon"},

{"cd":"36560320","nm_kor":"미력면","nm_eng":"Miryeok-myeon"},

{"cd":"36560330","nm_kor":"겸백면","nm_eng":"Gyeombaek-myeon"},

{"cd":"36560340","nm_kor":"율어면","nm_eng":"Yureo-myeon"},

{"cd":"36560350","nm_kor":"복내면","nm_eng":"Bongnae-myeon"},

{"cd":"36560360","nm_kor":"문덕면","nm_eng":"Mundeok-myeon"},

{"cd":"36560370","nm_kor":"조성면","nm_eng":"Joseong-myeon"},

{"cd":"36560380","nm_kor":"득량면","nm_eng":"Deungnyang-myeon"},

{"cd":"36560390","nm_kor":"회천면","nm_eng":"Hoecheon-myeon"},

{"cd":"36560400","nm_kor":"웅치면","nm_eng":"Ungchi-myeon"},

{"cd":"36570000","nm_kor":"화순군","nm_eng":"Hwasun-gun"},

{"cd":"36570110","nm_kor":"화순읍","nm_eng":"Hwasun-eup"},

{"cd":"36570310","nm_kor":"한천면","nm_eng":"Hancheon-myeon"},

{"cd":"36570320","nm_kor":"춘양면","nm_eng":"Chunyang-myeon"},

{"cd":"36570330","nm_kor":"청풍면","nm_eng":"Cheongpung-myeon"},

{"cd":"36570340","nm_kor":"이양면","nm_eng":"Iyang-myeon"},

{"cd":"36570350","nm_kor":"능주면","nm_eng":"Neungju-myeon"},

{"cd":"36570360","nm_kor":"도곡면","nm_eng":"Dogok-myeon"},

{"cd":"36570370","nm_kor":"도암면","nm_eng":"Doam-myeon"},

{"cd":"36570380","nm_kor":"이서면","nm_eng":"Iseo-myeon"},

{"cd":"36570430","nm_kor":"백아면","nm_eng":"Baega-myeon"},

{"cd":"36570400","nm_kor":"동복면","nm_eng":"Dongbok-myeon"},

{"cd":"36570440","nm_kor":"사평면","nm_eng":"Sapyeong-myeon"},

{"cd":"36570420","nm_kor":"동면","nm_eng":"Dong-myeon"},

{"cd":"36580000","nm_kor":"장흥군","nm_eng":"Jangheung-gun"},

{"cd":"36580110","nm_kor":"장흥읍","nm_eng":"Jangheung-eup"},

{"cd":"36580120","nm_kor":"관산읍","nm_eng":"Gwansan-eup"},

{"cd":"36580130","nm_kor":"대덕읍","nm_eng":"Daedeok-eup"},

{"cd":"36580310","nm_kor":"용산면","nm_eng":"Yongsan-myeon"},

{"cd":"36580320","nm_kor":"안양면","nm_eng":"Anyang-myeon"},

{"cd":"36580330","nm_kor":"장동면","nm_eng":"Jangdong-myeon"},

{"cd":"36580340","nm_kor":"장평면","nm_eng":"Jangpyeong-myeon"},

{"cd":"36580350","nm_kor":"유치면","nm_eng":"Yuchi-myeon"},

{"cd":"36580360","nm_kor":"부산면","nm_eng":"Busan-myeon"},

{"cd":"36580370","nm_kor":"회진면","nm_eng":"Hoejin-myeon"},

{"cd":"36590000","nm_kor":"강진군","nm_eng":"Gangjin-gun"},

{"cd":"36590110","nm_kor":"강진읍","nm_eng":"Gangjin-eup"},

{"cd":"36590310","nm_kor":"군동면","nm_eng":"Gundong-myeon"},

{"cd":"36590320","nm_kor":"칠량면","nm_eng":"Chillyang-myeon"},

{"cd":"36590330","nm_kor":"대구면","nm_eng":"Daegu-myeon"},

{"cd":"36590350","nm_kor":"도암면","nm_eng":"Doam-myeon"},

{"cd":"36590360","nm_kor":"신전면","nm_eng":"Sinjeon-myeon"},

{"cd":"36590370","nm_kor":"성전면","nm_eng":"Seongjeon-myeon"},

{"cd":"36590380","nm_kor":"작천면","nm_eng":"Jakcheon-myeon"},

{"cd":"36590390","nm_kor":"병영면","nm_eng":"Byeongyeong-myeon"},

{"cd":"36590400","nm_kor":"옴천면","nm_eng":"Omcheon-myeon"},

{"cd":"36590340","nm_kor":"마량면","nm_eng":"Maryang-myeon"},

{"cd":"36600000","nm_kor":"해남군","nm_eng":"Haenam-gun"},

{"cd":"36600110","nm_kor":"해남읍","nm_eng":"Haenam-eup"},

{"cd":"36600310","nm_kor":"삼산면","nm_eng":"Samsan-myeon"},

{"cd":"36600320","nm_kor":"화산면","nm_eng":"Hwasan-myeon"},

{"cd":"36600330","nm_kor":"현산면","nm_eng":"Hyeonsan-myeon"},

{"cd":"36600340","nm_kor":"송지면","nm_eng":"Songji-myeon"},

{"cd":"36600350","nm_kor":"북평면","nm_eng":"Bukpyeong-myeon"},

{"cd":"36600360","nm_kor":"북일면","nm_eng":"Bugil-myeon"},

{"cd":"36600370","nm_kor":"옥천면","nm_eng":"Okcheon-myeon"},

{"cd":"36600380","nm_kor":"계곡면","nm_eng":"Gyegok-myeon"},

{"cd":"36600390","nm_kor":"마산면","nm_eng":"Masan-myeon"},

{"cd":"36600400","nm_kor":"황산면","nm_eng":"Hwangsan-myeon"},

{"cd":"36600410","nm_kor":"산이면","nm_eng":"Sani-myeon"},

{"cd":"36600420","nm_kor":"문내면","nm_eng":"Munnae-myeon"},

{"cd":"36600430","nm_kor":"화원면","nm_eng":"Hwawon-myeon"},

{"cd":"36610000","nm_kor":"영암군","nm_eng":"Yeongam-gun"},

{"cd":"36610110","nm_kor":"영암읍","nm_eng":"Yeongam-eup"},

{"cd":"36610120","nm_kor":"삼호읍","nm_eng":"Samho-eup"},

{"cd":"36610310","nm_kor":"덕진면","nm_eng":"Deokjin-myeon"},

{"cd":"36610320","nm_kor":"금정면","nm_eng":"Geumjeong-myeon"},

{"cd":"36610330","nm_kor":"신북면","nm_eng":"Sinbuk-myeon"},

{"cd":"36610340","nm_kor":"시종면","nm_eng":"Sijong-myeon"},

{"cd":"36610350","nm_kor":"도포면","nm_eng":"Dopo-myeon"},

{"cd":"36610360","nm_kor":"군서면","nm_eng":"Gunseo-myeon"},

{"cd":"36610370","nm_kor":"서호면","nm_eng":"Seoho-myeon"},

{"cd":"36610380","nm_kor":"학산면","nm_eng":"Haksan-myeon"},

{"cd":"36610390","nm_kor":"미암면","nm_eng":"Miam-myeon"},

{"cd":"36620000","nm_kor":"무안군","nm_eng":"Muan-gun"},

{"cd":"36620110","nm_kor":"무안읍","nm_eng":"Muan-eup"},

{"cd":"36620120","nm_kor":"일로읍","nm_eng":"Illo-eup"},

{"cd":"36620130","nm_kor":"삼향읍","nm_eng":"Samhyang-eup"},

{"cd":"36620320","nm_kor":"몽탄면","nm_eng":"Mongtan-myeon"},

{"cd":"36620330","nm_kor":"청계면","nm_eng":"Cheonggye-myeon"},

{"cd":"36620340","nm_kor":"현경면","nm_eng":"Hyeongyeong-myeon"},

{"cd":"36620350","nm_kor":"망운면","nm_eng":"Mangun-myeon"},

{"cd":"36620360","nm_kor":"해제면","nm_eng":"Haeje-myeon"},

{"cd":"36620370","nm_kor":"운남면","nm_eng":"Unnam-myeon"},

{"cd":"36630000","nm_kor":"함평군","nm_eng":"Hampyeong-gun"},

{"cd":"36630110","nm_kor":"함평읍","nm_eng":"Hampyeong-eup"},

{"cd":"36630310","nm_kor":"손불면","nm_eng":"Sonbul-myeon"},

{"cd":"36630320","nm_kor":"신광면","nm_eng":"Singwang-myeon"},

{"cd":"36630330","nm_kor":"학교면","nm_eng":"Hakgyo-myeon"},

{"cd":"36630340","nm_kor":"엄다면","nm_eng":"Eomda-myeon"},

{"cd":"36630350","nm_kor":"대동면","nm_eng":"Daedong-myeon"},

{"cd":"36630360","nm_kor":"나산면","nm_eng":"Nasan-myeon"},

{"cd":"36630370","nm_kor":"해보면","nm_eng":"Haebo-myeon"},

{"cd":"36630380","nm_kor":"월야면","nm_eng":"Worya-myeon"},

{"cd":"36640000","nm_kor":"영광군","nm_eng":"Yeonggwang-gun"},

{"cd":"36640110","nm_kor":"영광읍","nm_eng":"Yeonggwang-eup"},

{"cd":"36640120","nm_kor":"백수읍","nm_eng":"Baeksu-eup"},

{"cd":"36640130","nm_kor":"홍농읍","nm_eng":"Hongnong-eup"},

{"cd":"36640310","nm_kor":"대마면","nm_eng":"Daema-myeon"},

{"cd":"36640320","nm_kor":"묘량면","nm_eng":"Myoryang-myeon"},

{"cd":"36640330","nm_kor":"불갑면","nm_eng":"Bulgap-myeon"},

{"cd":"36640340","nm_kor":"군서면","nm_eng":"Gunseo-myeon"},

{"cd":"36640350","nm_kor":"군남면","nm_eng":"Gunnam-myeon"},

{"cd":"36640360","nm_kor":"염산면","nm_eng":"Yeomsan-myeon"},

{"cd":"36640370","nm_kor":"법성면","nm_eng":"Beopseong-myeon"},

{"cd":"36640380","nm_kor":"낙월면","nm_eng":"Nagwol-myeon"},

{"cd":"36650000","nm_kor":"장성군","nm_eng":"Jangseong-gun"},

{"cd":"36650110","nm_kor":"장성읍","nm_eng":"Jangseong-eup"},

{"cd":"36650310","nm_kor":"진원면","nm_eng":"Jinwon-myeon"},

{"cd":"36650320","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"36650330","nm_kor":"동화면","nm_eng":"Donghwa-myeon"},

{"cd":"36650340","nm_kor":"삼서면","nm_eng":"Samseo-myeon"},

{"cd":"36650350","nm_kor":"삼계면","nm_eng":"Samgye-myeon"},

{"cd":"36650360","nm_kor":"황룡면","nm_eng":"Hwangnyong-myeon"},

{"cd":"36650370","nm_kor":"서삼면","nm_eng":"Seosam-myeon"},

{"cd":"36650380","nm_kor":"북일면","nm_eng":"Bugil-myeon"},

{"cd":"36650390","nm_kor":"북이면","nm_eng":"Bugi-myeon"},

{"cd":"36650400","nm_kor":"북하면","nm_eng":"Bukha-myeon"},

{"cd":"36660000","nm_kor":"완도군","nm_eng":"Wando-gun"},

{"cd":"36660110","nm_kor":"완도읍","nm_eng":"Wando-eup"},

{"cd":"36660120","nm_kor":"금일읍","nm_eng":"Geumil-eup"},

{"cd":"36660130","nm_kor":"노화읍","nm_eng":"Nohwa-eup"},

{"cd":"36660310","nm_kor":"군외면","nm_eng":"Gunoe-myeon"},

{"cd":"36660320","nm_kor":"신지면","nm_eng":"Sinji-myeon"},

{"cd":"36660330","nm_kor":"고금면","nm_eng":"Gogeum-myeon"},

{"cd":"36660340","nm_kor":"약산면","nm_eng":"Yaksan-myeon"},

{"cd":"36660350","nm_kor":"청산면","nm_eng":"Cheongsan-myeon"},

{"cd":"36660360","nm_kor":"소안면","nm_eng":"Soan-myeon"},

{"cd":"36660370","nm_kor":"금당면","nm_eng":"Geumdang-myeon"},

{"cd":"36660380","nm_kor":"보길면","nm_eng":"Bogil-myeon"},

{"cd":"36660390","nm_kor":"생일면","nm_eng":"Saengil-myeon"},

{"cd":"36670000","nm_kor":"진도군","nm_eng":"Jindo-gun"},

{"cd":"36670110","nm_kor":"진도읍","nm_eng":"Jindo-eup"},

{"cd":"36670310","nm_kor":"군내면","nm_eng":"Gunnae-myeon"},

{"cd":"36670320","nm_kor":"고군면","nm_eng":"Gogun-myeon"},

{"cd":"36670330","nm_kor":"의신면","nm_eng":"Uisin-myeon"},

{"cd":"36670340","nm_kor":"임회면","nm_eng":"Imhoe-myeon"},

{"cd":"36670350","nm_kor":"지산면","nm_eng":"Jisan-myeon"},

{"cd":"36670360","nm_kor":"조도면","nm_eng":"Jodo-myeon"},

{"cd":"36680000","nm_kor":"신안군","nm_eng":"Sinan-gun"},

{"cd":"36680110","nm_kor":"지도읍","nm_eng":"Jido-eup"},

{"cd":"36680120","nm_kor":"압해읍","nm_eng":"Aphae-eup"},

{"cd":"36680310","nm_kor":"증도면","nm_eng":"Jeungdo-myeon"},

{"cd":"36680320","nm_kor":"임자면","nm_eng":"Imja-myeon"},

{"cd":"36680330","nm_kor":"자은면","nm_eng":"Jaeun-myeon"},

{"cd":"36680340","nm_kor":"비금면","nm_eng":"Bigeum-myeon"},

{"cd":"36680350","nm_kor":"도초면","nm_eng":"Docho-myeon"},

{"cd":"36680360","nm_kor":"흑산면","nm_eng":"Heuksan-myeon"},

{"cd":"36680370","nm_kor":"하의면","nm_eng":"Haui-myeon"},

{"cd":"36680380","nm_kor":"신의면","nm_eng":"Sinui-myeon"},

{"cd":"36680390","nm_kor":"장산면","nm_eng":"Jangsan-myeon"},

{"cd":"36680400","nm_kor":"안좌면","nm_eng":"Anjwa-myeon"},

{"cd":"36680410","nm_kor":"팔금면","nm_eng":"Palgeum-myeon"},

{"cd":"36680420","nm_kor":"암태면","nm_eng":"Amtae-myeon"},

{"cd":"37000000","nm_kor":"경상북도","nm_eng":"Gyeongsangbuk-do"},

{"cd":"37010000","nm_kor":"포항시","nm_eng":"Pohang-si"},

{"cd":"37011000","nm_kor":"남구","nm_eng":"Nam-gu"},

{"cd":"37011110","nm_kor":"구룡포읍","nm_eng":"Guryongpo-eup"},

{"cd":"37011120","nm_kor":"연일읍","nm_eng":"Yeonil-eup"},

{"cd":"37011130","nm_kor":"오천읍","nm_eng":"Ocheon-eup"},

{"cd":"37011310","nm_kor":"대송면","nm_eng":"Daesong-myeon"},

{"cd":"37011320","nm_kor":"동해면","nm_eng":"Donghae-myeon"},

{"cd":"37011330","nm_kor":"장기면","nm_eng":"Janggi-myeon"},

{"cd":"37011350","nm_kor":"호미곶면","nm_eng":"Homigot-myeon"},

{"cd":"37011600","nm_kor":"상대동","nm_eng":"Sangdae-dong"},

{"cd":"37011610","nm_kor":"해도동","nm_eng":"Haedo-dong"},

{"cd":"37011550","nm_kor":"송도동","nm_eng":"Songdo-dong"},

{"cd":"37011560","nm_kor":"청림동","nm_eng":"Cheongnim-dong"},

{"cd":"37011570","nm_kor":"제철동","nm_eng":"Jecheol-dong"},

{"cd":"37011580","nm_kor":"효곡동","nm_eng":"Hyogok-dong"},

{"cd":"37011590","nm_kor":"대이동","nm_eng":"Daei-dong"},

{"cd":"37012000","nm_kor":"북구","nm_eng":"Buk-gu"},

{"cd":"37012110","nm_kor":"흥해읍","nm_eng":"Heunghae-eup"},

{"cd":"37012310","nm_kor":"신광면","nm_eng":"Singwang-myeon"},

{"cd":"37012320","nm_kor":"청하면","nm_eng":"Cheongha-myeon"},

{"cd":"37012330","nm_kor":"송라면","nm_eng":"Songna-myeon"},

{"cd":"37012340","nm_kor":"기계면","nm_eng":"Gigye-myeon"},

{"cd":"37012350","nm_kor":"죽장면","nm_eng":"Jukjang-myeon"},

{"cd":"37012360","nm_kor":"기북면","nm_eng":"Gibuk-myeon"},

{"cd":"37012670","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"37012580","nm_kor":"양학동","nm_eng":"Yanghak-dong"},

{"cd":"37012680","nm_kor":"죽도동","nm_eng":"Jukdo-dong"},

{"cd":"37012610","nm_kor":"용흥동","nm_eng":"Yongheung-dong"},

{"cd":"37012630","nm_kor":"우창동","nm_eng":"Uchang-dong"},

{"cd":"37012640","nm_kor":"두호동","nm_eng":"Duho-dong"},

{"cd":"37012650","nm_kor":"장량동","nm_eng":"Jangnyang-dong"},

{"cd":"37012660","nm_kor":"환여동","nm_eng":"Hwanyeo-dong"},

{"cd":"37020000","nm_kor":"경주시","nm_eng":"Gyeongju-si"},

{"cd":"37020110","nm_kor":"감포읍","nm_eng":"Gampo-eup"},

{"cd":"37020120","nm_kor":"안강읍","nm_eng":"Angang-eup"},

{"cd":"37020130","nm_kor":"건천읍","nm_eng":"Geoncheon-eup"},

{"cd":"37020140","nm_kor":"외동읍","nm_eng":"Oedong-eup"},

{"cd":"37020390","nm_kor":"문무대왕면","nm_eng":"Munmudaewang-myeon"},

{"cd":"37020320","nm_kor":"양남면","nm_eng":"Yangnam-myeon"},

{"cd":"37020330","nm_kor":"내남면","nm_eng":"Naenam-myeon"},

{"cd":"37020340","nm_kor":"산내면","nm_eng":"Sannae-myeon"},

{"cd":"37020350","nm_kor":"서면","nm_eng":"Seo-myeon"},

{"cd":"37020360","nm_kor":"현곡면","nm_eng":"Hyeongok-myeon"},

{"cd":"37020370","nm_kor":"강동면","nm_eng":"Gangdong-myeon"},

{"cd":"37020380","nm_kor":"천북면","nm_eng":"Cheonbuk-myeon"},

{"cd":"37020510","nm_kor":"중부동","nm_eng":"Jungbu-dong"},

{"cd":"37020680","nm_kor":"황오동","nm_eng":"Hwango-dong"},

{"cd":"37020550","nm_kor":"성건동","nm_eng":"Seonggeon-dong"},

{"cd":"37020690","nm_kor":"황남동","nm_eng":"Hwangnam-dong"},

{"cd":"37020590","nm_kor":"선도동","nm_eng":"Seondo-dong"},

{"cd":"37020580","nm_kor":"월성동","nm_eng":"Wolseong-dong"},

{"cd":"37020620","nm_kor":"용강동","nm_eng":"Yonggang-dong"},

{"cd":"37020630","nm_kor":"황성동","nm_eng":"Hwangseong-dong"},

{"cd":"37020640","nm_kor":"동천동","nm_eng":"Dongcheon-dong"},

{"cd":"37020660","nm_kor":"불국동","nm_eng":"Bulguk-dong"},

{"cd":"37020670","nm_kor":"보덕동","nm_eng":"Bodeok-dong"},

{"cd":"37030000","nm_kor":"김천시","nm_eng":"Gimcheon-si"},

{"cd":"37030110","nm_kor":"아포읍","nm_eng":"Apo-eup"},

{"cd":"37030310","nm_kor":"농소면","nm_eng":"Nongso-myeon"},

{"cd":"37030320","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"37030330","nm_kor":"개령면","nm_eng":"Gaeryeong-myeon"},

{"cd":"37030340","nm_kor":"감문면","nm_eng":"Gammun-myeon"},

{"cd":"37030350","nm_kor":"어모면","nm_eng":"Eomo-myeon"},

{"cd":"37030360","nm_kor":"봉산면","nm_eng":"Bongsan-myeon"},

{"cd":"37030370","nm_kor":"대항면","nm_eng":"Daehang-myeon"},

{"cd":"37030380","nm_kor":"감천면","nm_eng":"Gamcheon-myeon"},

{"cd":"37030390","nm_kor":"조마면","nm_eng":"Joma-myeon"},

{"cd":"37030400","nm_kor":"구성면","nm_eng":"Guseong-myeon"},

{"cd":"37030410","nm_kor":"지례면","nm_eng":"Jirye-myeon"},

{"cd":"37030420","nm_kor":"부항면","nm_eng":"Buhang-myeon"},

{"cd":"37030430","nm_kor":"대덕면","nm_eng":"Daedeok-myeon"},

{"cd":"37030440","nm_kor":"증산면","nm_eng":"Jeungsan-myeon"},

{"cd":"37030600","nm_kor":"자산동","nm_eng":"Jasan-dong"},

{"cd":"37030610","nm_kor":"평화남산동","nm_eng":"Pyeonghwanamsan-dong"},

{"cd":"37030550","nm_kor":"양금동","nm_eng":"Yanggeum-dong"},

{"cd":"37030560","nm_kor":"대신동","nm_eng":"Daesin-dong"},

{"cd":"37030580","nm_kor":"대곡동","nm_eng":"Daegok-dong"},

{"cd":"37030590","nm_kor":"지좌동","nm_eng":"Jijwa-dong"},

{"cd":"37030620","nm_kor":"율곡동","nm_eng":"Yulgok-dong"},

{"cd":"37040000","nm_kor":"안동시","nm_eng":"Andong-si"},

{"cd":"37040110","nm_kor":"풍산읍","nm_eng":"Pungsan-eup"},

{"cd":"37040310","nm_kor":"와룡면","nm_eng":"Waryong-myeon"},

{"cd":"37040320","nm_kor":"북후면","nm_eng":"Bukhu-myeon"},

{"cd":"37040330","nm_kor":"서후면","nm_eng":"Seohu-myeon"},

{"cd":"37040340","nm_kor":"풍천면","nm_eng":"Pungcheon-myeon"},

{"cd":"37040350","nm_kor":"일직면","nm_eng":"Iljik-myeon"},

{"cd":"37040360","nm_kor":"남후면","nm_eng":"Namhu-myeon"},

{"cd":"37040370","nm_kor":"남선면","nm_eng":"Namseon-myeon"},

{"cd":"37040380","nm_kor":"임하면","nm_eng":"Imha-myeon"},

{"cd":"37040390","nm_kor":"길안면","nm_eng":"Giran-myeon"},

{"cd":"37040400","nm_kor":"임동면","nm_eng":"Imdong-myeon"},

{"cd":"37040410","nm_kor":"예안면","nm_eng":"Yean-myeon"},

{"cd":"37040420","nm_kor":"도산면","nm_eng":"Dosan-myeon"},

{"cd":"37040430","nm_kor":"녹전면","nm_eng":"Nokjeon-myeon"},

{"cd":"37040510","nm_kor":"중구동","nm_eng":"Junggu-dong"},

{"cd":"37040520","nm_kor":"명륜동","nm_eng":"Myeongnyun-dong"},

{"cd":"37040540","nm_kor":"용상동","nm_eng":"Yongsang-dong"},

{"cd":"37040620","nm_kor":"서구동","nm_eng":"Seogu-dong"},

{"cd":"37040560","nm_kor":"태화동","nm_eng":"Taehwa-dong"},

{"cd":"37040580","nm_kor":"평화동","nm_eng":"Pyeonghwa-dong"},

{"cd":"37040590","nm_kor":"안기동","nm_eng":"Angi-dong"},

{"cd":"37040600","nm_kor":"옥동","nm_eng":"Ok-dong"},

{"cd":"37040610","nm_kor":"송하동","nm_eng":"Songha-dong"},

{"cd":"37040630","nm_kor":"강남동","nm_eng":"Gangnam-dong"},

{"cd":"37050000","nm_kor":"구미시","nm_eng":"Gumi-si"},

{"cd":"37050110","nm_kor":"선산읍","nm_eng":"Seonsan-eup"},

{"cd":"37050120","nm_kor":"고아읍","nm_eng":"Goa-eup"},

{"cd":"37050130","nm_kor":"산동읍","nm_eng":"Sandong-eup"},

{"cd":"37050310","nm_kor":"무을면","nm_eng":"Mueul-myeon"},

{"cd":"37050320","nm_kor":"옥성면","nm_eng":"Okseong-myeon"},

{"cd":"37050330","nm_kor":"도개면","nm_eng":"Dogae-myeon"},

{"cd":"37050340","nm_kor":"해평면","nm_eng":"Haepyeong-myeon"},

{"cd":"37050360","nm_kor":"장천면","nm_eng":"Jangcheon-myeon"},

{"cd":"37050510","nm_kor":"송정동","nm_eng":"Songjeong-dong"},

{"cd":"37050750","nm_kor":"원평동","nm_eng":"Wonpyeong-dong"},

{"cd":"37050550","nm_kor":"도량동","nm_eng":"Doryang-dong"},

{"cd":"37050560","nm_kor":"지산동","nm_eng":"Jisan-dong"},

{"cd":"37050570","nm_kor":"선주원남동","nm_eng":"Seonjuwonnam-dong"},

{"cd":"37050590","nm_kor":"형곡1동","nm_eng":"Hyeonggok 1(il)-dong"},

{"cd":"37050600","nm_kor":"형곡2동","nm_eng":"Hyeonggok 2(i)-dong"},

{"cd":"37050610","nm_kor":"신평1동","nm_eng":"Sinpyeong 1(il)-dong"},

{"cd":"37050620","nm_kor":"신평2동","nm_eng":"Sinpyeong 2(i)-dong"},

{"cd":"37050730","nm_kor":"비산동","nm_eng":"Bisan-dong"},

{"cd":"37050660","nm_kor":"광평동","nm_eng":"Gwangpyeong-dong"},

{"cd":"37050670","nm_kor":"상모사곡동","nm_eng":"Sangmosagok-dong"},

{"cd":"37050690","nm_kor":"임오동","nm_eng":"Imo-dong"},

{"cd":"37050700","nm_kor":"인동동","nm_eng":"Indong-dong"},

{"cd":"37050710","nm_kor":"진미동","nm_eng":"Jinmi-dong"},

{"cd":"37050720","nm_kor":"양포동","nm_eng":"Yangpo-dong"},

{"cd":"37050740","nm_kor":"공단동","nm_eng":"Gongdan-dong"},

{"cd":"37060000","nm_kor":"영주시","nm_eng":"Yeongju-si"},

{"cd":"37060110","nm_kor":"풍기읍","nm_eng":"Punggi-eup"},

{"cd":"37060310","nm_kor":"이산면","nm_eng":"Isan-myeon"},

{"cd":"37060320","nm_kor":"평은면","nm_eng":"Pyeongeun-myeon"},

{"cd":"37060330","nm_kor":"문수면","nm_eng":"Munsu-myeon"},

{"cd":"37060340","nm_kor":"장수면","nm_eng":"Jangsu-myeon"},

{"cd":"37060350","nm_kor":"안정면","nm_eng":"Anjeong-myeon"},

{"cd":"37060360","nm_kor":"봉현면","nm_eng":"Bonghyeon-myeon"},

{"cd":"37060370","nm_kor":"순흥면","nm_eng":"Sunheung-myeon"},

{"cd":"37060380","nm_kor":"단산면","nm_eng":"Dansan-myeon"},

{"cd":"37060390","nm_kor":"부석면","nm_eng":"Buseok-myeon"},

{"cd":"37060510","nm_kor":"상망동","nm_eng":"Sangmang-dong"},

{"cd":"37060530","nm_kor":"하망동","nm_eng":"Hamang-dong"},

{"cd":"37060550","nm_kor":"영주1동","nm_eng":"Yeongju 1(il)-dong"},

{"cd":"37060580","nm_kor":"영주2동","nm_eng":"Yeongju 2(i)-dong"},

{"cd":"37060590","nm_kor":"휴천1동","nm_eng":"Hyucheon 1(il)-dong"},

{"cd":"37060600","nm_kor":"휴천2동","nm_eng":"Hyucheon 2(i)-dong"},

{"cd":"37060610","nm_kor":"휴천3동","nm_eng":"Hyucheon 3(sam)-dong"},

{"cd":"37060620","nm_kor":"가흥1동","nm_eng":"Gaheung 1(il)-dong"},

{"cd":"37060630","nm_kor":"가흥2동","nm_eng":"Gaheung 2(i)-dong"},

{"cd":"37070000","nm_kor":"영천시","nm_eng":"Yeongcheon-si"},

{"cd":"37070110","nm_kor":"금호읍","nm_eng":"Geumho-eup"},

{"cd":"37070310","nm_kor":"청통면","nm_eng":"Cheongtong-myeon"},

{"cd":"37070320","nm_kor":"신녕면","nm_eng":"Sinnyeong-myeon"},

{"cd":"37070330","nm_kor":"화산면","nm_eng":"Hwasan-myeon"},

{"cd":"37070340","nm_kor":"화북면","nm_eng":"Hwabuk-myeon"},

{"cd":"37070350","nm_kor":"화남면","nm_eng":"Hwanam-myeon"},

{"cd":"37070360","nm_kor":"자양면","nm_eng":"Jayang-myeon"},

{"cd":"37070370","nm_kor":"임고면","nm_eng":"Imgo-myeon"},

{"cd":"37070380","nm_kor":"고경면","nm_eng":"Gogyeong-myeon"},

{"cd":"37070390","nm_kor":"북안면","nm_eng":"Bugan-myeon"},

{"cd":"37070400","nm_kor":"대창면","nm_eng":"Daechang-myeon"},

{"cd":"37070510","nm_kor":"동부동","nm_eng":"Dongbu-dong"},

{"cd":"37070520","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"37070530","nm_kor":"서부동","nm_eng":"Seobu-dong"},

{"cd":"37070540","nm_kor":"완산동","nm_eng":"Wansan-dong"},

{"cd":"37070550","nm_kor":"남부동","nm_eng":"Nambu-dong"},

{"cd":"37080000","nm_kor":"상주시","nm_eng":"Sangju-si"},

{"cd":"37080110","nm_kor":"함창읍","nm_eng":"Hamchang-eup"},

{"cd":"37080320","nm_kor":"중동면","nm_eng":"Jungdong-myeon"},

{"cd":"37080480","nm_kor":"사벌국면","nm_eng":"Sabeolguk-myeon"},

{"cd":"37080330","nm_kor":"낙동면","nm_eng":"Nakdong-myeon"},

{"cd":"37080340","nm_kor":"청리면","nm_eng":"Cheongni-myeon"},

{"cd":"37080350","nm_kor":"공성면","nm_eng":"Gongseong-myeon"},

{"cd":"37080360","nm_kor":"외남면","nm_eng":"Oenam-myeon"},

{"cd":"37080370","nm_kor":"내서면","nm_eng":"Naeseo-myeon"},

{"cd":"37080380","nm_kor":"모동면","nm_eng":"Modong-myeon"},

{"cd":"37080390","nm_kor":"모서면","nm_eng":"Moseo-myeon"},

{"cd":"37080400","nm_kor":"화동면","nm_eng":"Hwadong-myeon"},

{"cd":"37080410","nm_kor":"화서면","nm_eng":"Hwaseo-myeon"},

{"cd":"37080420","nm_kor":"화북면","nm_eng":"Hwabuk-myeon"},

{"cd":"37080430","nm_kor":"외서면","nm_eng":"Oeseo-myeon"},

{"cd":"37080440","nm_kor":"은척면","nm_eng":"Euncheok-myeon"},

{"cd":"37080450","nm_kor":"공검면","nm_eng":"Gonggeom-myeon"},

{"cd":"37080460","nm_kor":"이안면","nm_eng":"Ian-myeon"},

{"cd":"37080470","nm_kor":"화남면","nm_eng":"Hwanam-myeon"},

{"cd":"37080520","nm_kor":"남원동","nm_eng":"Namwon-dong"},

{"cd":"37080530","nm_kor":"북문동","nm_eng":"Bungmun-dong"},

{"cd":"37080540","nm_kor":"계림동","nm_eng":"Gyerim-dong"},

{"cd":"37080550","nm_kor":"동문동","nm_eng":"Dongmun-dong"},

{"cd":"37080560","nm_kor":"동성동","nm_eng":"Dongseong-dong"},

{"cd":"37080570","nm_kor":"신흥동","nm_eng":"Sinheung-dong"},

{"cd":"37090000","nm_kor":"문경시","nm_eng":"Mungyeong-si"},

{"cd":"37090110","nm_kor":"문경읍","nm_eng":"Mungyeong-eup"},

{"cd":"37090120","nm_kor":"가은읍","nm_eng":"Gaeun-eup"},

{"cd":"37090310","nm_kor":"영순면","nm_eng":"Yeongsun-myeon"},

{"cd":"37090320","nm_kor":"산양면","nm_eng":"Sanyang-myeon"},

{"cd":"37090330","nm_kor":"호계면","nm_eng":"Hogye-myeon"},

{"cd":"37090340","nm_kor":"산북면","nm_eng":"Sanbuk-myeon"},

{"cd":"37090350","nm_kor":"동로면","nm_eng":"Dongno-myeon"},

{"cd":"37090360","nm_kor":"마성면","nm_eng":"Maseong-myeon"},

{"cd":"37090370","nm_kor":"농암면","nm_eng":"Nongam-myeon"},

{"cd":"37090570","nm_kor":"점촌1동","nm_eng":"Jeomchon 1(il)-dong"},

{"cd":"37090580","nm_kor":"점촌2동","nm_eng":"Jeomchon 2(i)-dong"},

{"cd":"37090590","nm_kor":"점촌3동","nm_eng":"Jeomchon 3(sam)-dong"},

{"cd":"37090600","nm_kor":"점촌4동","nm_eng":"Jeomchon 4(sa)-dong"},

{"cd":"37090610","nm_kor":"점촌5동","nm_eng":"Jeomchon 5(o)-dong"},

{"cd":"37100000","nm_kor":"경산시","nm_eng":"Gyeongsan-si"},

{"cd":"37100110","nm_kor":"하양읍","nm_eng":"Hayang-eup"},

{"cd":"37100120","nm_kor":"진량읍","nm_eng":"Jillyang-eup"},

{"cd":"37100130","nm_kor":"압량읍","nm_eng":"Amnyang-eup"},

{"cd":"37100310","nm_kor":"와촌면","nm_eng":"Wachon-myeon"},

{"cd":"37100320","nm_kor":"자인면","nm_eng":"Jain-myeon"},

{"cd":"37100330","nm_kor":"용성면","nm_eng":"Yongseong-myeon"},

{"cd":"37100340","nm_kor":"남산면","nm_eng":"Namsan-myeon"},

{"cd":"37100360","nm_kor":"남천면","nm_eng":"Namcheon-myeon"},

{"cd":"37100560","nm_kor":"중방동","nm_eng":"Jungbang-dong"},

{"cd":"37100510","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"37100540","nm_kor":"남부동","nm_eng":"Nambu-dong"},

{"cd":"37100530","nm_kor":"서부1동","nm_eng":"Seobu 1(il)-dong"},

{"cd":"37100570","nm_kor":"서부2동","nm_eng":"Seobu 2(i)-dong"},

{"cd":"37100550","nm_kor":"북부동","nm_eng":"Bukbu-dong"},

{"cd":"37100520","nm_kor":"동부동","nm_eng":"Dongbu-dong"},

{"cd":"37510000","nm_kor":"군위군","nm_eng":"Gunwi-gun"},

{"cd":"37510110","nm_kor":"군위읍","nm_eng":"Gunwi-eup"},

{"cd":"37510310","nm_kor":"소보면","nm_eng":"Sobo-myeon"},

{"cd":"37510320","nm_kor":"효령면","nm_eng":"Hyoryeong-myeon"},

{"cd":"37510330","nm_kor":"부계면","nm_eng":"Bugye-myeon"},

{"cd":"37510340","nm_kor":"우보면","nm_eng":"Ubo-myeon"},

{"cd":"37510350","nm_kor":"의흥면","nm_eng":"Uiheung-myeon"},

{"cd":"37510360","nm_kor":"산성면","nm_eng":"Sanseong-myeon"},

{"cd":"37510380","nm_kor":"삼국유사면","nm_eng":"Samgugyusa-myeon"},

{"cd":"37520000","nm_kor":"의성군","nm_eng":"Uiseong-gun"},

{"cd":"37520110","nm_kor":"의성읍","nm_eng":"Uiseong-eup"},

{"cd":"37520310","nm_kor":"단촌면","nm_eng":"Danchon-myeon"},

{"cd":"37520320","nm_kor":"점곡면","nm_eng":"Jeomgok-myeon"},

{"cd":"37520330","nm_kor":"옥산면","nm_eng":"Oksan-myeon"},

{"cd":"37520340","nm_kor":"사곡면","nm_eng":"Sagok-myeon"},

{"cd":"37520350","nm_kor":"춘산면","nm_eng":"Chunsan-myeon"},

{"cd":"37520360","nm_kor":"가음면","nm_eng":"Gaeum-myeon"},

{"cd":"37520370","nm_kor":"금성면","nm_eng":"Geumseong-myeon"},

{"cd":"37520380","nm_kor":"봉양면","nm_eng":"Bongyang-myeon"},

{"cd":"37520390","nm_kor":"비안면","nm_eng":"Bian-myeon"},

{"cd":"37520400","nm_kor":"구천면","nm_eng":"Gucheon-myeon"},

{"cd":"37520410","nm_kor":"단밀면","nm_eng":"Danmil-myeon"},

{"cd":"37520420","nm_kor":"단북면","nm_eng":"Danbuk-myeon"},

{"cd":"37520430","nm_kor":"안계면","nm_eng":"Angye-myeon"},

{"cd":"37520440","nm_kor":"다인면","nm_eng":"Dain-myeon"},

{"cd":"37520450","nm_kor":"신평면","nm_eng":"Sinpyeong-myeon"},

{"cd":"37520460","nm_kor":"안평면","nm_eng":"Anpyeong-myeon"},

{"cd":"37520470","nm_kor":"안사면","nm_eng":"Ansa-myeon"},

{"cd":"37530000","nm_kor":"청송군","nm_eng":"Cheongsong-gun"},

{"cd":"37530110","nm_kor":"청송읍","nm_eng":"Cheongsong-eup"},

{"cd":"37530380","nm_kor":"주왕산면","nm_eng":"Juwangsan-myeon"},

{"cd":"37530320","nm_kor":"부남면","nm_eng":"Bunam-myeon"},

{"cd":"37530330","nm_kor":"현동면","nm_eng":"Hyeondong-myeon"},

{"cd":"37530340","nm_kor":"현서면","nm_eng":"Hyeonseo-myeon"},

{"cd":"37530350","nm_kor":"안덕면","nm_eng":"Andeok-myeon"},

{"cd":"37530360","nm_kor":"파천면","nm_eng":"Pacheon-myeon"},

{"cd":"37530370","nm_kor":"진보면","nm_eng":"Jinbo-myeon"},

{"cd":"37540000","nm_kor":"영양군","nm_eng":"Yeongyang-gun"},

{"cd":"37540110","nm_kor":"영양읍","nm_eng":"Yeongyang-eup"},

{"cd":"37540310","nm_kor":"입암면","nm_eng":"Ibam-myeon"},

{"cd":"37540320","nm_kor":"청기면","nm_eng":"Cheonggi-myeon"},

{"cd":"37540330","nm_kor":"일월면","nm_eng":"Irwol-myeon"},

{"cd":"37540340","nm_kor":"수비면","nm_eng":"Subi-myeon"},

{"cd":"37540350","nm_kor":"석보면","nm_eng":"Seokbo-myeon"},

{"cd":"37550000","nm_kor":"영덕군","nm_eng":"Yeongdeok-gun"},

{"cd":"37550110","nm_kor":"영덕읍","nm_eng":"Yeongdeok-eup"},

{"cd":"37550310","nm_kor":"강구면","nm_eng":"Ganggu-myeon"},

{"cd":"37550320","nm_kor":"남정면","nm_eng":"Namjeong-myeon"},

{"cd":"37550330","nm_kor":"달산면","nm_eng":"Dalsan-myeon"},

{"cd":"37550340","nm_kor":"지품면","nm_eng":"Jipum-myeon"},

{"cd":"37550350","nm_kor":"축산면","nm_eng":"Chuksan-myeon"},

{"cd":"37550360","nm_kor":"영해면","nm_eng":"Yeonghae-myeon"},

{"cd":"37550370","nm_kor":"병곡면","nm_eng":"Byeonggok-myeon"},

{"cd":"37550380","nm_kor":"창수면","nm_eng":"Changsu-myeon"},

{"cd":"37560000","nm_kor":"청도군","nm_eng":"Cheongdo-gun"},

{"cd":"37560110","nm_kor":"화양읍","nm_eng":"Hwayang-eup"},

{"cd":"37560120","nm_kor":"청도읍","nm_eng":"Cheongdo-eup"},

{"cd":"37560310","nm_kor":"각남면","nm_eng":"Gangnam-myeon"},

{"cd":"37560320","nm_kor":"풍각면","nm_eng":"Punggak-myeon"},

{"cd":"37560330","nm_kor":"각북면","nm_eng":"Gakbuk-myeon"},

{"cd":"37560340","nm_kor":"이서면","nm_eng":"Iseo-myeon"},

{"cd":"37560350","nm_kor":"운문면","nm_eng":"Unmun-myeon"},

{"cd":"37560360","nm_kor":"금천면","nm_eng":"Geumcheon-myeon"},

{"cd":"37560370","nm_kor":"매전면","nm_eng":"Maejeon-myeon"},

{"cd":"37570000","nm_kor":"고령군","nm_eng":"Goryeong-gun"},

{"cd":"37570120","nm_kor":"대가야읍","nm_eng":"Daegaya-eup"},

{"cd":"37570310","nm_kor":"덕곡면","nm_eng":"Deokgok-myeon"},

{"cd":"37570320","nm_kor":"운수면","nm_eng":"Unsu-myeon"},

{"cd":"37570330","nm_kor":"성산면","nm_eng":"Seongsan-myeon"},

{"cd":"37570340","nm_kor":"다산면","nm_eng":"Dasan-myeon"},

{"cd":"37570350","nm_kor":"개진면","nm_eng":"Gaejin-myeon"},

{"cd":"37570360","nm_kor":"우곡면","nm_eng":"Ugok-myeon"},

{"cd":"37570370","nm_kor":"쌍림면","nm_eng":"Ssangnim-myeon"},

{"cd":"37580000","nm_kor":"성주군","nm_eng":"Seongju-gun"},

{"cd":"37580110","nm_kor":"성주읍","nm_eng":"Seongju-eup"},

{"cd":"37580310","nm_kor":"선남면","nm_eng":"Seonnam-myeon"},

{"cd":"37580320","nm_kor":"용암면","nm_eng":"Yongam-myeon"},

{"cd":"37580330","nm_kor":"수륜면","nm_eng":"Suryun-myeon"},

{"cd":"37580340","nm_kor":"가천면","nm_eng":"Gacheon-myeon"},

{"cd":"37580350","nm_kor":"금수면","nm_eng":"Geumsu-myeon"},

{"cd":"37580360","nm_kor":"대가면","nm_eng":"Daega-myeon"},

{"cd":"37580370","nm_kor":"벽진면","nm_eng":"Byeokjin-myeon"},

{"cd":"37580380","nm_kor":"초전면","nm_eng":"Chojeon-myeon"},

{"cd":"37580390","nm_kor":"월항면","nm_eng":"Wolhang-myeon"},

{"cd":"37590000","nm_kor":"칠곡군","nm_eng":"Chilgok-gun"},

{"cd":"37590110","nm_kor":"왜관읍","nm_eng":"Waegwan-eup"},

{"cd":"37590120","nm_kor":"북삼읍","nm_eng":"Buksam-eup"},

{"cd":"37590130","nm_kor":"석적읍","nm_eng":"Seokjeok-eup"},

{"cd":"37590310","nm_kor":"지천면","nm_eng":"Jicheon-myeon"},

{"cd":"37590320","nm_kor":"동명면","nm_eng":"Dongmyeong-myeon"},

{"cd":"37590330","nm_kor":"가산면","nm_eng":"Gasan-myeon"},

{"cd":"37590360","nm_kor":"약목면","nm_eng":"Yangmok-myeon"},

{"cd":"37590370","nm_kor":"기산면","nm_eng":"Gisan-myeon"},

{"cd":"37600000","nm_kor":"예천군","nm_eng":"Yecheon-gun"},

{"cd":"37600110","nm_kor":"예천읍","nm_eng":"Yecheon-eup"},

{"cd":"37600310","nm_kor":"용문면","nm_eng":"Yongmun-myeon"},

{"cd":"37600340","nm_kor":"감천면","nm_eng":"Gamcheon-myeon"},

{"cd":"37600350","nm_kor":"보문면","nm_eng":"Bomun-myeon"},

{"cd":"37600360","nm_kor":"호명면","nm_eng":"Homyeong-myeon"},

{"cd":"37600370","nm_kor":"유천면","nm_eng":"Yucheon-myeon"},

{"cd":"37600380","nm_kor":"용궁면","nm_eng":"Yonggung-myeon"},

{"cd":"37600390","nm_kor":"개포면","nm_eng":"Gaepo-myeon"},

{"cd":"37600400","nm_kor":"지보면","nm_eng":"Jibo-myeon"},

{"cd":"37600410","nm_kor":"풍양면","nm_eng":"Pungyang-myeon"},

{"cd":"37600420","nm_kor":"효자면","nm_eng":"Hyoja-myeon"},

{"cd":"37600430","nm_kor":"은풍면","nm_eng":"Eunpung-myeon"},

{"cd":"37610000","nm_kor":"봉화군","nm_eng":"Bonghwa-gun"},

{"cd":"37610110","nm_kor":"봉화읍","nm_eng":"Bonghwa-eup"},

{"cd":"37610310","nm_kor":"물야면","nm_eng":"Murya-myeon"},

{"cd":"37610320","nm_kor":"봉성면","nm_eng":"Bongseong-myeon"},

{"cd":"37610330","nm_kor":"법전면","nm_eng":"Beopjeon-myeon"},

{"cd":"37610340","nm_kor":"춘양면","nm_eng":"Chunyang-myeon"},

{"cd":"37610350","nm_kor":"소천면","nm_eng":"Socheon-myeon"},

{"cd":"37610370","nm_kor":"재산면","nm_eng":"Jaesan-myeon"},

{"cd":"37610380","nm_kor":"명호면","nm_eng":"Myeongho-myeon"},

{"cd":"37610390","nm_kor":"상운면","nm_eng":"Sangun-myeon"},

{"cd":"37610360","nm_kor":"석포면","nm_eng":"Seokpo-myeon"},

{"cd":"37620000","nm_kor":"울진군","nm_eng":"Uljin-gun"},

{"cd":"37620110","nm_kor":"울진읍","nm_eng":"Uljin-eup"},

{"cd":"37620120","nm_kor":"평해읍","nm_eng":"Pyeonghae-eup"},

{"cd":"37620310","nm_kor":"북면","nm_eng":"Buk-myeon"},

{"cd":"37620330","nm_kor":"근남면","nm_eng":"Geunnam-myeon"},

{"cd":"37620350","nm_kor":"기성면","nm_eng":"Giseong-myeon"},

{"cd":"37620360","nm_kor":"온정면","nm_eng":"Onjeong-myeon"},

{"cd":"37620370","nm_kor":"죽변면","nm_eng":"Jukbyeon-myeon"},

{"cd":"37620380","nm_kor":"후포면","nm_eng":"Hupo-myeon"},

{"cd":"37620390","nm_kor":"금강송면","nm_eng":"Geumgangsong-myeon"},

{"cd":"37620400","nm_kor":"매화면","nm_eng":"maehwa-myeon"},

{"cd":"37630000","nm_kor":"울릉군","nm_eng":"Ulleung-gun"},

{"cd":"37630110","nm_kor":"울릉읍","nm_eng":"Ulleung-eup"},

{"cd":"37630310","nm_kor":"서면","nm_eng":"Seo-myeon"},

{"cd":"37630320","nm_kor":"북면","nm_eng":"Buk-myeon"},

{"cd":"38000000","nm_kor":"경상남도","nm_eng":"Gyeongsangnam-do"},

{"cd":"38110000","nm_kor":"창원시","nm_eng":"Changwon-si"},

{"cd":"38111000","nm_kor":"의창구","nm_eng":"Uichang-gu"},

{"cd":"38111110","nm_kor":"동읍","nm_eng":"Dong-eup"},

{"cd":"38111310","nm_kor":"북면","nm_eng":"Buk-myeon"},

{"cd":"38111320","nm_kor":"대산면","nm_eng":"Daesan-myeon"},

{"cd":"38111510","nm_kor":"의창동","nm_eng":"Uichang-dong"},

{"cd":"38111520","nm_kor":"팔룡동","nm_eng":"Pallyong-dong"},

{"cd":"38111530","nm_kor":"명곡동","nm_eng":"Myeonggok-dong"},

{"cd":"38111540","nm_kor":"봉림동","nm_eng":"Bongnim-dong"},

{"cd":"38112000","nm_kor":"성산구","nm_eng":"seongsan-gu"},

{"cd":"38112510","nm_kor":"반송동","nm_eng":"Bansong-dong"},

{"cd":"38112580","nm_kor":"용지동","nm_eng":"Yongji-dong"},

{"cd":"38112520","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"38112530","nm_kor":"상남동","nm_eng":"Sangnam-dong"},

{"cd":"38112540","nm_kor":"사파동","nm_eng":"Sapa-dong"},

{"cd":"38112550","nm_kor":"가음정동","nm_eng":"Gaeumjeong-dong"},

{"cd":"38112560","nm_kor":"성주동","nm_eng":"Seongju-dong"},

{"cd":"38112570","nm_kor":"웅남동","nm_eng":"Ungnam-dong"},

{"cd":"38113000","nm_kor":"마산합포구","nm_eng":"Masanhappo-gu"},

{"cd":"38113310","nm_kor":"구산면","nm_eng":"Gusan-myeon"},

{"cd":"38113320","nm_kor":"진동면","nm_eng":"Jindong-myeon"},

{"cd":"38113330","nm_kor":"진북면","nm_eng":"Jinbuk-myeon"},

{"cd":"38113340","nm_kor":"진전면","nm_eng":"Jinjeon-myeon"},

{"cd":"38113510","nm_kor":"현동","nm_eng":"Hyeon-dong"},

{"cd":"38113520","nm_kor":"가포동","nm_eng":"Gapo-dong"},

{"cd":"38113530","nm_kor":"월영동","nm_eng":"Woryeong-dong"},

{"cd":"38113540","nm_kor":"문화동","nm_eng":"Munhwa-dong"},

{"cd":"38113660","nm_kor":"반월중앙동","nm_eng":"Banwol-jungang-dong"},

{"cd":"38113570","nm_kor":"완월동","nm_eng":"Wanwol-dong"},

{"cd":"38113580","nm_kor":"자산동","nm_eng":"Jasan-dong"},

{"cd":"38113680","nm_kor":"교방동","nm_eng":"Gyobang-dong"},

{"cd":"38113670","nm_kor":"오동동","nm_eng":"Odong-dong"},

{"cd":"38113640","nm_kor":"합포동","nm_eng":"Happo-dong"},

{"cd":"38113650","nm_kor":"산호동","nm_eng":"Sanho-dong"},

{"cd":"38114000","nm_kor":"마산회원구","nm_eng":"Masanhoewon-gu"},

{"cd":"38114110","nm_kor":"내서읍","nm_eng":"Naeseo-eup"},

{"cd":"38114510","nm_kor":"회원1동","nm_eng":"Hoewon 1(il)-dong"},

{"cd":"38114520","nm_kor":"회원2동","nm_eng":"Hoewon 2(i)-dong"},

{"cd":"38114630","nm_kor":"석전동","nm_eng":"Seokjeon -dong"},

{"cd":"38114550","nm_kor":"회성동","nm_eng":"Hoeseong-dong"},

{"cd":"38114560","nm_kor":"양덕1동","nm_eng":"Yangdeok 1(il)-dong"},

{"cd":"38114570","nm_kor":"양덕2동","nm_eng":"Yangdeok 2(i)-dong"},

{"cd":"38114580","nm_kor":"합성1동","nm_eng":"Hapseong 1(il)-dong"},

{"cd":"38114590","nm_kor":"합성2동","nm_eng":"Hapseong 2(i)-dong"},

{"cd":"38114600","nm_kor":"구암1동","nm_eng":"Guam 1(il)-dong"},

{"cd":"38114610","nm_kor":"구암2동","nm_eng":"Guam 2(i)-dong"},

{"cd":"38114620","nm_kor":"봉암동","nm_eng":"Bongam-dong"},

{"cd":"38115000","nm_kor":"진해구","nm_eng":"Jinhae-gu"},

{"cd":"38115660","nm_kor":"충무동","nm_eng":"Chungmu-dong"},

{"cd":"38115540","nm_kor":"여좌동","nm_eng":"Yeojwa-dong"},

{"cd":"38115550","nm_kor":"태백동","nm_eng":"Taebaek-dong"},

{"cd":"38115560","nm_kor":"경화동","nm_eng":"Gyeonghwa-dong"},

{"cd":"38115570","nm_kor":"병암동","nm_eng":"Byeongam-dong"},

{"cd":"38115580","nm_kor":"석동","nm_eng":"Seok-dong"},

{"cd":"38115590","nm_kor":"이동","nm_eng":"I-dong"},

{"cd":"38115600","nm_kor":"자은동","nm_eng":"Jaeun-dong"},

{"cd":"38115610","nm_kor":"덕산동","nm_eng":"Deoksan-dong"},

{"cd":"38115620","nm_kor":"풍호동","nm_eng":"Pungho-dong"},

{"cd":"38115630","nm_kor":"웅천동","nm_eng":"Ungcheon-dong"},

{"cd":"38115640","nm_kor":"웅동1동","nm_eng":"Ungdong 1(il)-dong"},

{"cd":"38115650","nm_kor":"웅동2동","nm_eng":"Ungdong 2(i)-dong"},

{"cd":"38030000","nm_kor":"진주시","nm_eng":"Jinju-si"},

{"cd":"38030110","nm_kor":"문산읍","nm_eng":"Munsan-eup"},

{"cd":"38030310","nm_kor":"내동면","nm_eng":"Naedong-myeon"},

{"cd":"38030320","nm_kor":"정촌면","nm_eng":"Jeongchon-myeon"},

{"cd":"38030330","nm_kor":"금곡면","nm_eng":"Geumgok-myeon"},

{"cd":"38030340","nm_kor":"진성면","nm_eng":"Jinseong-myeon"},

{"cd":"38030350","nm_kor":"일반성면","nm_eng":"Ilbanseong-myeon"},

{"cd":"38030360","nm_kor":"이반성면","nm_eng":"Ibanseong-myeon"},

{"cd":"38030370","nm_kor":"사봉면","nm_eng":"Sabong-myeon"},

{"cd":"38030380","nm_kor":"지수면","nm_eng":"Jisu-myeon"},

{"cd":"38030390","nm_kor":"대곡면","nm_eng":"Daegok-myeon"},

{"cd":"38030400","nm_kor":"금산면","nm_eng":"Geumsan-myeon"},

{"cd":"38030410","nm_kor":"집현면","nm_eng":"Jiphyeon-myeon"},

{"cd":"38030420","nm_kor":"미천면","nm_eng":"Micheon-myeon"},

{"cd":"38030430","nm_kor":"명석면","nm_eng":"Myeongseok-myeon"},

{"cd":"38030440","nm_kor":"대평면","nm_eng":"Daepyeong-myeon"},

{"cd":"38030450","nm_kor":"수곡면","nm_eng":"Sugok-myeon"},

{"cd":"38030720","nm_kor":"천전동","nm_eng":"cheonjeon-dong"},

{"cd":"38030730","nm_kor":"성북동","nm_eng":"Seongbuk-dong"},

{"cd":"38030740","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"38030750","nm_kor":"상봉동","nm_eng":"Sangbong_dong"},

{"cd":"38030770","nm_kor":"상대동","nm_eng":"Sangdae-dong"},

{"cd":"38030780","nm_kor":"하대동","nm_eng":"Hadae-dong"},

{"cd":"38030650","nm_kor":"상평동","nm_eng":"Sangpyeong-dong"},

{"cd":"38030660","nm_kor":"초장동","nm_eng":"Chojang-dong"},

{"cd":"38030670","nm_kor":"평거동","nm_eng":"Pyeonggeo-dong"},

{"cd":"38030680","nm_kor":"신안동","nm_eng":"Sinan-dong"},

{"cd":"38030690","nm_kor":"이현동","nm_eng":"Ihyeon-dong"},

{"cd":"38030700","nm_kor":"판문동","nm_eng":"Panmun-dong"},

{"cd":"38030710","nm_kor":"가호동","nm_eng":"Gahoe-dong"},

{"cd":"38030760","nm_kor":"충무공동","nm_eng":"Chungmugong-dong"},

{"cd":"38050000","nm_kor":"통영시","nm_eng":"Tongyeong-si"},

{"cd":"38050110","nm_kor":"산양읍","nm_eng":"Sanyang-eup"},

{"cd":"38050310","nm_kor":"용남면","nm_eng":"Yongnam-myeon"},

{"cd":"38050320","nm_kor":"도산면","nm_eng":"Dosan-myeon"},

{"cd":"38050330","nm_kor":"광도면","nm_eng":"Gwangdo-myeon"},

{"cd":"38050340","nm_kor":"욕지면","nm_eng":"Yokji-myeon"},

{"cd":"38050350","nm_kor":"한산면","nm_eng":"Hansan-myeon"},

{"cd":"38050360","nm_kor":"사량면","nm_eng":"Saryang-myeon"},

{"cd":"38050620","nm_kor":"도천동","nm_eng":"Docheon-dong"},

{"cd":"38050520","nm_kor":"명정동","nm_eng":"Myeongjeong-dong"},

{"cd":"38050530","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"38050540","nm_kor":"정량동","nm_eng":"Jeongnyang-dong"},

{"cd":"38050550","nm_kor":"북신동","nm_eng":"Buksin-dong"},

{"cd":"38050630","nm_kor":"미수동","nm_eng":"Misu-dong"},

{"cd":"38050640","nm_kor":"봉평동","nm_eng":"Bongpyeong-dong"},

{"cd":"38050560","nm_kor":"무전동","nm_eng":"Mujeon-dong"},

{"cd":"38060000","nm_kor":"사천시","nm_eng":"Sacheon-si"},

{"cd":"38060110","nm_kor":"사천읍","nm_eng":"Sacheon-eup"},

{"cd":"38060310","nm_kor":"정동면","nm_eng":"Jeongdong-myeon"},

{"cd":"38060320","nm_kor":"사남면","nm_eng":"Sanam-myeon"},

{"cd":"38060330","nm_kor":"용현면","nm_eng":"Yonghyeon-myeon"},

{"cd":"38060340","nm_kor":"축동면","nm_eng":"Chukdong-myeon"},

{"cd":"38060350","nm_kor":"곤양면","nm_eng":"Gonyang-myeon"},

{"cd":"38060360","nm_kor":"곤명면","nm_eng":"Gonmyeong-myeon"},

{"cd":"38060370","nm_kor":"서포면","nm_eng":"Seopo-myeon"},

{"cd":"38060510","nm_kor":"동서동","nm_eng":"Dongseo-dong"},

{"cd":"38060520","nm_kor":"선구동","nm_eng":"Seongu-dong"},

{"cd":"38060530","nm_kor":"동서금동","nm_eng":"Dongseogeum-dong"},

{"cd":"38060550","nm_kor":"벌용동","nm_eng":"Beollyong-dong"},

{"cd":"38060570","nm_kor":"향촌동","nm_eng":"Hyangchon-dong"},

{"cd":"38060590","nm_kor":"남양동","nm_eng":"Namyang-dong"},

{"cd":"38070000","nm_kor":"김해시","nm_eng":"Gimhae-si"},

{"cd":"38070110","nm_kor":"진영읍","nm_eng":"Jinyeong-eup"},

{"cd":"38070320","nm_kor":"주촌면","nm_eng":"Juchon-myeon"},

{"cd":"38070330","nm_kor":"진례면","nm_eng":"Jillye-myeon"},

{"cd":"38070340","nm_kor":"한림면","nm_eng":"Hallim-myeon"},

{"cd":"38070350","nm_kor":"생림면","nm_eng":"Saengnim-myeon"},

{"cd":"38070360","nm_kor":"상동면","nm_eng":"Sangdong-myeon"},

{"cd":"38070370","nm_kor":"대동면","nm_eng":"Daedong-myeon"},

{"cd":"38070510","nm_kor":"동상동","nm_eng":"Dongsang-dong"},

{"cd":"38070520","nm_kor":"회현동","nm_eng":"Hoehyeon-dong"},

{"cd":"38070530","nm_kor":"부원동","nm_eng":"Buwon-dong"},

{"cd":"38070540","nm_kor":"내외동","nm_eng":"Naeoe-dong"},

{"cd":"38070550","nm_kor":"북부동","nm_eng":"Bukbu-dong"},

{"cd":"38070560","nm_kor":"칠산서부동","nm_eng":"Chilsanseobu-dong"},

{"cd":"38070580","nm_kor":"활천동","nm_eng":"Hwalcheon-dong"},

{"cd":"38070590","nm_kor":"삼안동","nm_eng":"Saman-dong"},

{"cd":"38070600","nm_kor":"불암동","nm_eng":"Buram-dong"},

{"cd":"38070610","nm_kor":"장유1동","nm_eng":"Jangyu 1(il)-dong"},

{"cd":"38070620","nm_kor":"장유2동","nm_eng":"Jangyu 2(i)-dong"},

{"cd":"38070630","nm_kor":"장유3동","nm_eng":"Jangyu 3(sam)-dong"},

{"cd":"38080000","nm_kor":"밀양시","nm_eng":"Miryang-si"},

{"cd":"38080110","nm_kor":"삼랑진읍","nm_eng":"Samnangjin-eup"},

{"cd":"38080120","nm_kor":"하남읍","nm_eng":"Hanam-eup"},

{"cd":"38080310","nm_kor":"부북면","nm_eng":"Bubuk-myeon"},

{"cd":"38080320","nm_kor":"상동면","nm_eng":"Sangdong-myeon"},

{"cd":"38080330","nm_kor":"산외면","nm_eng":"Sanoe-myeon"},

{"cd":"38080340","nm_kor":"산내면","nm_eng":"Sannae-myeon"},

{"cd":"38080350","nm_kor":"단장면","nm_eng":"Danjang-myeon"},

{"cd":"38080360","nm_kor":"상남면","nm_eng":"Sangnam-myeon"},

{"cd":"38080370","nm_kor":"초동면","nm_eng":"Chodong-myeon"},

{"cd":"38080380","nm_kor":"무안면","nm_eng":"Muan-myeon"},

{"cd":"38080390","nm_kor":"청도면","nm_eng":"Cheongdo-myeon"},

{"cd":"38080510","nm_kor":"내일동","nm_eng":"Naeil-dong"},

{"cd":"38080520","nm_kor":"내이동","nm_eng":"Naei-dong"},

{"cd":"38080540","nm_kor":"삼문동","nm_eng":"Sammun-dong"},

{"cd":"38080550","nm_kor":"가곡동","nm_eng":"Gagok-dong"},

{"cd":"38080530","nm_kor":"교동","nm_eng":"Gyo-dong"},

{"cd":"38090000","nm_kor":"거제시","nm_eng":"Geoje-si"},

{"cd":"38090310","nm_kor":"일운면","nm_eng":"Irun-myeon"},

{"cd":"38090320","nm_kor":"동부면","nm_eng":"Dongbu-myeon"},

{"cd":"38090330","nm_kor":"남부면","nm_eng":"Nambu-myeon"},

{"cd":"38090340","nm_kor":"거제면","nm_eng":"Geoje-myeon"},

{"cd":"38090350","nm_kor":"둔덕면","nm_eng":"Dundeok-myeon"},

{"cd":"38090360","nm_kor":"사등면","nm_eng":"Sadeung-myeon"},

{"cd":"38090370","nm_kor":"연초면","nm_eng":"Yeoncho-myeon"},

{"cd":"38090380","nm_kor":"하청면","nm_eng":"Hacheong-myeon"},

{"cd":"38090390","nm_kor":"장목면","nm_eng":"Jangmok-myeon"},

{"cd":"38090610","nm_kor":"장승포동","nm_eng":"Jangseungpo-dong"},

{"cd":"38090530","nm_kor":"능포동","nm_eng":"Neungpo-dong"},

{"cd":"38090540","nm_kor":"아주동","nm_eng":"Aju-dong"},

{"cd":"38090550","nm_kor":"옥포1동","nm_eng":"Okpo 1(il)-dong"},

{"cd":"38090560","nm_kor":"옥포2동","nm_eng":"Okpo 2(i)-dong"},

{"cd":"38090570","nm_kor":"장평동","nm_eng":"Jangpyeong-dong"},

{"cd":"38090580","nm_kor":"고현동","nm_eng":"Gohyeon-dong"},

{"cd":"38090590","nm_kor":"상문동","nm_eng":"Sangmun-dong"},

{"cd":"38090600","nm_kor":"수양동","nm_eng":"Suyang-dong"},

{"cd":"38100000","nm_kor":"양산시","nm_eng":"Yangsan-si"},

{"cd":"38100120","nm_kor":"물금읍","nm_eng":"Mulgeum-eup"},

{"cd":"38100310","nm_kor":"동면","nm_eng":"Dong-myeon"},

{"cd":"38100320","nm_kor":"원동면","nm_eng":"Wondong-myeon"},

{"cd":"38100330","nm_kor":"상북면","nm_eng":"Sangbuk-myeon"},

{"cd":"38100340","nm_kor":"하북면","nm_eng":"Habuk-myeon"},

{"cd":"38100580","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"38100590","nm_kor":"양주동","nm_eng":"Yangju-dong"},

{"cd":"38100520","nm_kor":"삼성동","nm_eng":"Samseong-dong"},

{"cd":"38100530","nm_kor":"강서동","nm_eng":"Gangseo-dong"},

{"cd":"38100540","nm_kor":"서창동","nm_eng":"Seochang-dong"},

{"cd":"38100550","nm_kor":"소주동","nm_eng":"Soju-dong"},

{"cd":"38100560","nm_kor":"평산동","nm_eng":"Pyeongsan-dong"},

{"cd":"38100570","nm_kor":"덕계동","nm_eng":"Deokgye-dong"},

{"cd":"38510000","nm_kor":"의령군","nm_eng":"Uiryeong-gun"},

{"cd":"38510110","nm_kor":"의령읍","nm_eng":"Uiryeong-eup"},

{"cd":"38510310","nm_kor":"가례면","nm_eng":"Garye-myeon"},

{"cd":"38510320","nm_kor":"칠곡면","nm_eng":"Chilgok-myeon"},

{"cd":"38510330","nm_kor":"대의면","nm_eng":"Daeui-myeon"},

{"cd":"38510340","nm_kor":"화정면","nm_eng":"Hwajeong-myeon"},

{"cd":"38510350","nm_kor":"용덕면","nm_eng":"Yongdeok-myeon"},

{"cd":"38510360","nm_kor":"정곡면","nm_eng":"Jeonggok-myeon"},

{"cd":"38510370","nm_kor":"지정면","nm_eng":"Jijeong-myeon"},

{"cd":"38510380","nm_kor":"낙서면","nm_eng":"Nakseo-myeon"},

{"cd":"38510390","nm_kor":"부림면","nm_eng":"Burim-myeon"},

{"cd":"38510400","nm_kor":"봉수면","nm_eng":"Bongsu-myeon"},

{"cd":"38510410","nm_kor":"궁류면","nm_eng":"Gungnyu-myeon"},

{"cd":"38510420","nm_kor":"유곡면","nm_eng":"Yugok-myeon"},

{"cd":"38520000","nm_kor":"함안군","nm_eng":"Haman-gun"},

{"cd":"38520110","nm_kor":"가야읍","nm_eng":"Gaya-eup"},

{"cd":"38520120","nm_kor":"칠원읍","nm_eng":"Chirwon-eup"},

{"cd":"38520310","nm_kor":"함안면","nm_eng":"Haman-myeon"},

{"cd":"38520320","nm_kor":"군북면","nm_eng":"Gunbuk-myeon"},

{"cd":"38520330","nm_kor":"법수면","nm_eng":"Beopsu-myeon"},

{"cd":"38520340","nm_kor":"대산면","nm_eng":"Daesan-myeon"},

{"cd":"38520350","nm_kor":"칠서면","nm_eng":"Chilseo-myeon"},

{"cd":"38520360","nm_kor":"칠북면","nm_eng":"Chilbuk-myeon"},

{"cd":"38520380","nm_kor":"산인면","nm_eng":"Sanin-myeon"},

{"cd":"38520390","nm_kor":"여항면","nm_eng":"Yeohang-myeon"},

{"cd":"38530000","nm_kor":"창녕군","nm_eng":"Changnyeong-gun"},

{"cd":"38530110","nm_kor":"창녕읍","nm_eng":"Changnyeong-eup"},

{"cd":"38530120","nm_kor":"남지읍","nm_eng":"Namji-eup"},

{"cd":"38530310","nm_kor":"고암면","nm_eng":"Goam-myeon"},

{"cd":"38530320","nm_kor":"성산면","nm_eng":"Seongsan-myeon"},

{"cd":"38530330","nm_kor":"대합면","nm_eng":"Daehap-myeon"},

{"cd":"38530340","nm_kor":"이방면","nm_eng":"Ibang-myeon"},

{"cd":"38530350","nm_kor":"유어면","nm_eng":"Yueo-myeon"},

{"cd":"38530360","nm_kor":"대지면","nm_eng":"Daeji-myeon"},

{"cd":"38530370","nm_kor":"계성면","nm_eng":"Gyeseong-myeon"},

{"cd":"38530380","nm_kor":"영산면","nm_eng":"Yeongsan-myeon"},

{"cd":"38530390","nm_kor":"장마면","nm_eng":"Jangma-myeon"},

{"cd":"38530400","nm_kor":"도천면","nm_eng":"Docheon-myeon"},

{"cd":"38530410","nm_kor":"길곡면","nm_eng":"Gilgok-myeon"},

{"cd":"38530420","nm_kor":"부곡면","nm_eng":"Bugok-myeon"},

{"cd":"38540000","nm_kor":"고성군","nm_eng":"Goseong-gun"},

{"cd":"38540110","nm_kor":"고성읍","nm_eng":"Goseong-eup"},

{"cd":"38540310","nm_kor":"삼산면","nm_eng":"Samsan-myeon"},

{"cd":"38540320","nm_kor":"하일면","nm_eng":"Hail-myeon"},

{"cd":"38540330","nm_kor":"하이면","nm_eng":"Hai-myeon"},

{"cd":"38540340","nm_kor":"상리면","nm_eng":"Sangni-myeon"},

{"cd":"38540350","nm_kor":"대가면","nm_eng":"Daega-myeon"},

{"cd":"38540360","nm_kor":"영현면","nm_eng":"Yeonghyeon-myeon"},

{"cd":"38540370","nm_kor":"영오면","nm_eng":"Yeongo-myeon"},

{"cd":"38540380","nm_kor":"개천면","nm_eng":"Gaecheon-myeon"},

{"cd":"38540390","nm_kor":"구만면","nm_eng":"Guman-myeon"},

{"cd":"38540400","nm_kor":"회화면","nm_eng":"Hoehwa-myeon"},

{"cd":"38540410","nm_kor":"마암면","nm_eng":"Maam-myeon"},

{"cd":"38540420","nm_kor":"동해면","nm_eng":"Donghae-myeon"},

{"cd":"38540430","nm_kor":"거류면","nm_eng":"Georyu-myeon"},

{"cd":"38550000","nm_kor":"남해군","nm_eng":"Namhae-gun"},

{"cd":"38550110","nm_kor":"남해읍","nm_eng":"Namhae-eup"},

{"cd":"38550310","nm_kor":"이동면","nm_eng":"Idong-myeon"},

{"cd":"38550320","nm_kor":"상주면","nm_eng":"Sangju-myeon"},

{"cd":"38550330","nm_kor":"삼동면","nm_eng":"Samdong-myeon"},

{"cd":"38550340","nm_kor":"미조면","nm_eng":"Mijo-myeon"},

{"cd":"38550350","nm_kor":"남면","nm_eng":"Nam-myeon"},

{"cd":"38550360","nm_kor":"서면","nm_eng":"Seo-myeon"},

{"cd":"38550370","nm_kor":"고현면","nm_eng":"Gohyeon-myeon"},

{"cd":"38550380","nm_kor":"설천면","nm_eng":"Seolcheon-myeon"},

{"cd":"38550390","nm_kor":"창선면","nm_eng":"Changseon-myeon"},

{"cd":"38560000","nm_kor":"하동군","nm_eng":"Hadong-gun"},

{"cd":"38560110","nm_kor":"하동읍","nm_eng":"Hadong-eup"},

{"cd":"38560310","nm_kor":"화개면","nm_eng":"Hwagae-myeon"},

{"cd":"38560320","nm_kor":"악양면","nm_eng":"Agyang-myeon"},

{"cd":"38560330","nm_kor":"적량면","nm_eng":"Jeongnyang-myeon"},

{"cd":"38560340","nm_kor":"횡천면","nm_eng":"Hoengcheon-myeon"},

{"cd":"38560350","nm_kor":"고전면","nm_eng":"Gojeon-myeon"},

{"cd":"38560360","nm_kor":"금남면","nm_eng":"Geumnam-myeon"},

{"cd":"38560380","nm_kor":"진교면","nm_eng":"Jingyo-myeon"},

{"cd":"38560390","nm_kor":"양보면","nm_eng":"Yangbo-myeon"},

{"cd":"38560400","nm_kor":"북천면","nm_eng":"Bukcheon-myeon"},

{"cd":"38560410","nm_kor":"청암면","nm_eng":"Cheongam-myeon"},

{"cd":"38560420","nm_kor":"옥종면","nm_eng":"Okjong-myeon"},

{"cd":"38560370","nm_kor":"금성면","nm_eng":"Geumseong-myeon"},

{"cd":"38570000","nm_kor":"산청군","nm_eng":"Sancheong-gun"},

{"cd":"38570110","nm_kor":"산청읍","nm_eng":"Sancheong-eup"},

{"cd":"38570310","nm_kor":"차황면","nm_eng":"Chahwang-myeon"},

{"cd":"38570320","nm_kor":"오부면","nm_eng":"Obu-myeon"},

{"cd":"38570330","nm_kor":"생초면","nm_eng":"Saengcho-myeon"},

{"cd":"38570340","nm_kor":"금서면","nm_eng":"Geumseo-myeon"},

{"cd":"38570350","nm_kor":"삼장면","nm_eng":"Samjang-myeon"},

{"cd":"38570360","nm_kor":"시천면","nm_eng":"Sicheon-myeon"},

{"cd":"38570370","nm_kor":"단성면","nm_eng":"Danseong-myeon"},

{"cd":"38570380","nm_kor":"신안면","nm_eng":"Sinan-myeon"},

{"cd":"38570390","nm_kor":"생비량면","nm_eng":"Saengbiryang-myeon"},

{"cd":"38570400","nm_kor":"신등면","nm_eng":"Sindeung-myeon"},

{"cd":"38580000","nm_kor":"함양군","nm_eng":"Hamyang-gun"},

{"cd":"38580110","nm_kor":"함양읍","nm_eng":"Hamyang-eup"},

{"cd":"38580310","nm_kor":"마천면","nm_eng":"Macheon-myeon"},

{"cd":"38580320","nm_kor":"휴천면","nm_eng":"Hyucheon-myeon"},

{"cd":"38580330","nm_kor":"유림면","nm_eng":"Yurim-myeon"},

{"cd":"38580340","nm_kor":"수동면","nm_eng":"Sudong-myeon"},

{"cd":"38580350","nm_kor":"지곡면","nm_eng":"Jigok-myeon"},

{"cd":"38580360","nm_kor":"안의면","nm_eng":"Anui-myeon"},

{"cd":"38580370","nm_kor":"서하면","nm_eng":"Seoha-myeon"},

{"cd":"38580380","nm_kor":"서상면","nm_eng":"Seosang-myeon"},

{"cd":"38580390","nm_kor":"백전면","nm_eng":"Baekjeon-myeon"},

{"cd":"38580400","nm_kor":"병곡면","nm_eng":"Byeonggok-myeon"},

{"cd":"38590000","nm_kor":"거창군","nm_eng":"Geochang-gun"},

{"cd":"38590110","nm_kor":"거창읍","nm_eng":"Geochang-eup"},

{"cd":"38590310","nm_kor":"주상면","nm_eng":"Jusang-myeon"},

{"cd":"38590320","nm_kor":"웅양면","nm_eng":"Ungyang-myeon"},

{"cd":"38590330","nm_kor":"고제면","nm_eng":"Goje-myeon"},

{"cd":"38590340","nm_kor":"북상면","nm_eng":"Buksang-myeon"},

{"cd":"38590350","nm_kor":"위천면","nm_eng":"Wicheon-myeon"},

{"cd":"38590360","nm_kor":"마리면","nm_eng":"Mari-myeon"},

{"cd":"38590370","nm_kor":"남상면","nm_eng":"Namsang-myeon"},

{"cd":"38590380","nm_kor":"남하면","nm_eng":"Namha-myeon"},

{"cd":"38590390","nm_kor":"신원면","nm_eng":"Sinwon-myeon"},

{"cd":"38590400","nm_kor":"가조면","nm_eng":"Gajo-myeon"},

{"cd":"38590410","nm_kor":"가북면","nm_eng":"Gabuk-myeon"},

{"cd":"38600000","nm_kor":"합천군","nm_eng":"Hapcheon-gun"},

{"cd":"38600110","nm_kor":"합천읍","nm_eng":"Hapcheon-eup"},

{"cd":"38600310","nm_kor":"봉산면","nm_eng":"Bongsan-myeon"},

{"cd":"38600320","nm_kor":"묘산면","nm_eng":"Myosan-myeon"},

{"cd":"38600330","nm_kor":"가야면","nm_eng":"Gaya-myeon"},

{"cd":"38600340","nm_kor":"야로면","nm_eng":"Yaro-myeon"},

{"cd":"38600350","nm_kor":"율곡면","nm_eng":"Yulgok-myeon"},

{"cd":"38600360","nm_kor":"초계면","nm_eng":"Chogye-myeon"},

{"cd":"38600370","nm_kor":"쌍책면","nm_eng":"Ssangchaek-myeon"},

{"cd":"38600380","nm_kor":"덕곡면","nm_eng":"Deokgok-myeon"},

{"cd":"38600390","nm_kor":"청덕면","nm_eng":"Cheongdeok-myeon"},

{"cd":"38600400","nm_kor":"적중면","nm_eng":"Jeokjung-myeon"},

{"cd":"38600410","nm_kor":"대양면","nm_eng":"Daeyang-myeon"},

{"cd":"38600420","nm_kor":"쌍백면","nm_eng":"Ssangbaek-myeon"},

{"cd":"38600430","nm_kor":"삼가면","nm_eng":"Samga-myeon"},

{"cd":"38600440","nm_kor":"가회면","nm_eng":"Gahoe-myeon"},

{"cd":"38600450","nm_kor":"대병면","nm_eng":"Daebyeong-myeon"},

{"cd":"38600460","nm_kor":"용주면","nm_eng":"Yongju-myeon"},

{"cd":"39000000","nm_kor":"제주특별자치도","nm_eng":"Jeju"},

{"cd":"39010000","nm_kor":"제주시","nm_eng":"Jeju-si"},

{"cd":"39010110","nm_kor":"한림읍","nm_eng":"Hallim-eup"},

{"cd":"39010120","nm_kor":"애월읍","nm_eng":"Aewol-eup"},

{"cd":"39010130","nm_kor":"구좌읍","nm_eng":"Gujwa-eup"},

{"cd":"39010140","nm_kor":"조천읍","nm_eng":"Jocheon-eup"},

{"cd":"39010310","nm_kor":"한경면","nm_eng":"Hangyeong-myeon"},

{"cd":"39010320","nm_kor":"추자면","nm_eng":"Chuja-myeon"},

{"cd":"39010330","nm_kor":"우도면","nm_eng":"Udo-myeon"},

{"cd":"39010510","nm_kor":"일도1동","nm_eng":"Ildo 1(il)-dong"},

{"cd":"39010520","nm_kor":"일도2동","nm_eng":"Ildo 2(i)-dong"},

{"cd":"39010530","nm_kor":"이도1동","nm_eng":"Ido 1(il)-dong"},

{"cd":"39010540","nm_kor":"이도2동","nm_eng":"Ido 2(i)-dong"},

{"cd":"39010550","nm_kor":"삼도1동","nm_eng":"Samdo 1(il)-dong"},

{"cd":"39010560","nm_kor":"삼도2동","nm_eng":"Samdo 2(i)-dong"},

{"cd":"39010570","nm_kor":"용담1동","nm_eng":"Yongdam 1(il)-dong"},

{"cd":"39010580","nm_kor":"용담2동","nm_eng":"Yongdam 2(i)-dong"},

{"cd":"39010590","nm_kor":"건입동","nm_eng":"Geonip-dong"},

{"cd":"39010600","nm_kor":"화북동","nm_eng":"Hwabuk-dong"},

{"cd":"39010610","nm_kor":"삼양동","nm_eng":"Samyang-dong"},

{"cd":"39010620","nm_kor":"봉개동","nm_eng":"Bonggae-dong"},

{"cd":"39010630","nm_kor":"아라동","nm_eng":"Ara-dong"},

{"cd":"39010640","nm_kor":"오라동","nm_eng":"Ora-dong"},

{"cd":"39010650","nm_kor":"연동","nm_eng":"Yeon-dong"},

{"cd":"39010660","nm_kor":"노형동","nm_eng":"Nohyeong-dong"},

{"cd":"39010670","nm_kor":"외도동","nm_eng":"Oedo-dong"},

{"cd":"39010680","nm_kor":"이호동","nm_eng":"Iho-dong"},

{"cd":"39010690","nm_kor":"도두동","nm_eng":"Dodu-dong"},

{"cd":"39020000","nm_kor":"서귀포시","nm_eng":"Seogwipo-si"},

{"cd":"39020110","nm_kor":"대정읍","nm_eng":"Daejeong-eup"},

{"cd":"39020120","nm_kor":"남원읍","nm_eng":"Namwon-eup"},

{"cd":"39020130","nm_kor":"성산읍","nm_eng":"Seongsan-eup"},

{"cd":"39020310","nm_kor":"안덕면","nm_eng":"Andeok-myeon"},

{"cd":"39020320","nm_kor":"표선면","nm_eng":"Pyoseon-myeon"},

{"cd":"39020510","nm_kor":"송산동","nm_eng":"Songsan-dong"},

{"cd":"39020520","nm_kor":"정방동","nm_eng":"Jeongbang-dong"},

{"cd":"39020530","nm_kor":"중앙동","nm_eng":"Jungang-dong"},

{"cd":"39020540","nm_kor":"천지동","nm_eng":"Cheonji-dong"},

{"cd":"39020550","nm_kor":"효돈동","nm_eng":"Hyodon-dong"},

{"cd":"39020560","nm_kor":"영천동","nm_eng":"Yeongcheon-dong"},

{"cd":"39020570","nm_kor":"동홍동","nm_eng":"Donghong-dong"},

{"cd":"39020580","nm_kor":"서홍동","nm_eng":"Seohong-dong"},

{"cd":"39020590","nm_kor":"대륜동","nm_eng":"Daeryun-dong"},

{"cd":"39020600","nm_kor":"대천동","nm_eng":"Daecheon-dong"},

{"cd":"39020610","nm_kor":"중문동","nm_eng":"Jungmun-dong"},

{"cd":"39020620","nm_kor":"예래동","nm_eng":"Yerae-dong"},

] 

``` javascript
    let option = {
        fieldMatch : {
            id : function(row, idx) { return row.cd },
            nm : function(row, idx) { return row.nm_kor + " (" + row.cd + ", " + row.nm_eng + ", " + idx.toString() + ")" },
            depth : function(row, idx) {
                if (row.cd.substring(2) == '000000') {
                    return 0
                } else if (row.cd.substring(4) == '0000') {
                    return 1
                } else if (row.cd.substring(5) == '000') {
                    return 2
                } else {
                    return 3
                }
            }
        }
    }

    const ret = list.wiseTreeView(option, json)
    console.log("done: " + ret.totalCount)
```   
    
    (샘플2)
      
``` javascript      
    const json = [
        { nm : "A", depth : 0 },
        { nm : "A1", depth : 1 },
        { nm : "A11", depth : 2 },
        { nm : "A12", depth : 2 },
        { nm : "A13", depth : 2 },
        { nm : "A131", depth : 3 },
        { nm : "A21", depth : 2 },
    ]

    const option = { }
    const ret = list.wiseTreeView(option, json)
    console.log("done: " + ret.totalCount) 
```

    (샘플3)

``` javascript
    const json = [
        { path : "A" },
        { path : "A/A1" },
        { path : "A/A1/A11", text1 : "라라라", text2 : "abcd" },
        { path : "A/A1/A12" },
        { path : "A/A13" },
        { path : "A/A13/A131" },
        { path : "A/A21" },
        { path : "B" },
        { path : "B/B1" },
    ]

    const option = { }
    const ret = list.wiseTreeView(option, json)
    console.log("done: " + ret.totalCount)
```

    (샘플4)

``` javascript
    const json = [
        { nm : "A", depth : 0 },
        { nm : "A1", depth : 1 },
        { nm : "A11", depth : 2 },
        { nm : "A12", depth : 2 },
        { nm : "A13", depth : 2 },
        { nm : "A131", depth : 3 },
        { nm : "A21", depth : 2 },
    ]

    const option = {
        customRow : function(row1, row2, idx) {
            debugger
            let _html = "<div style='font-size:14px;line-height:25px;font-weight:bold'>" + row2.nm + "</div>"
            _html += " <div id=state_" + row2.idx + " style='font-size:12px;color:darkgreen;line-height:15px'>id:" + (row2.id + " ===== depth:" + row2.depth) + "</div>"
            return _html
        },
    }

    const ret = list.wiseTreeView(option, json)
    console.log("done: " + ret.totalCount) 
```

* API 설명
 
  1. wiseTreeView가 json array에서 읽어 들이는 (정해진) 기본 필드(키)는 아래와 같습니다.
     { id : 0, nm : "AAA", path : "AAA", depth : 0, memcnt : 9 (하위노드갯수), text1 : "라라라", text2 : "abcd" } 

  2. 만일, json array에 위에 해당하는 필드가 없으면 option중에 fieldMatch 함수로 매핑하면 됩니다 : 샘플1 참조 

  3. 또는, 다음과 같이 일부 필드만 있어도 트리를 그려줍니다.
      - nm, depth만 있어도 구현 가능 : 샘플2 참조
      - path만 있어도 구현 가능 : 샘플3의 option.pathSeparator 기본값은 "/"인데 "/"으로 split해서 depth가 구해짐 

  4. depth를 function()으로 처리해서 구현 가능 : 샘플1 참조 

  5. 노드내 html로 처리해서 구현 가능 : 샘플4 참조 

  6. option (알파벳순. 기본값도 표시한 것임)
      - backColorChildSel = "lightsteelblue" : Child 노드 선택시 색상
      - backColorParent = "ivory" : Parent 노드 색상
      - customRow : 사용자가 원하는 대로 노드내 html을 넣을 수 있는 function
      - expand = 0 : TreeView가 표시될 때 기본적으로 펼쳐질 depth
      - fieldMatch : wiseTreeView가 json array에서 읽어 들이는 기본 필드(키)가 없을 뎡우 거기에 맞춰 매핑하는 함수
      - showCheckbox = false : 노드 왼쪽에 선택 가능하게 하는 체크박스 show 여부
      - showChildImg = false : Child 노드 왼쪽에 이미지 표시 여부
      - showParentImg = false : Parent 노드 왼쪽에 이미지 표시 여부
      - idToClick : json array에서 읽어 들이는 기본 필드(키)중 id에 해당하는 값을 idToClick에 입력시 해당 값이 있는 노드 클릭이벤트를 트리거함
      - idToScroll : json array에서 읽어 들이는 기본 필드(키)중 id에 해당하는 값을 idToScroll에 입력시 해당 값이 있는 노드까지 스크롤해 보여줌
      - imgChild = "doc.png" : Child 노드 이미지 파일
      - imgCheckbox = "selecton.png" : 체크박스 이미지 파일
      - imgCollapse = "minus.png" : 접기 이미지 파일
      - imgExpand = "plus.png" : 펼치기 이미지 파일
      - imgParent = "folder.png" : Parent 노드 이미지 파일
      - imgPath : 이미지를 가져오는 기본 경로
      - indent = 20 : 각 depth간에 인덴트
      - pathSeparator = "/" : json array에서 읽어 들이는 기본 필드(키)중 path에 해당하는 값을 split할 델리미터
      - rowHeight = "45px" : 노드 높이
      - showMemberCount = false : json array에서 읽어 들이는 기본 필드(키)중 memcnt가 있는 경우 memcnt show 여부 

  7. Event 처리

``` javascript
     list.off("wiseTreeOnCheck").on("wiseTreeOnCheck", function(e, data) {     
          debugger          
     })

     list.off("wiseTreeOnClick").on("wiseTreeOnClick", function(e, data) {      
          debugger          
          if (data.row2.type == "child") alert(data.row2.idx)          
      }) 

      list.off("wiseTreeNodeShown").on("wiseTreeNodeShown", function(e, data) {      
          debugger //펼칠 때 해당 노드에 이미지 표시 등 작업이 필요할 경우 사용          
      })

      list.off("wiseTreeNodeHidden").on("wiseTreeNodeHidden", function(e, data) {      
          debugger //접을 때 해당 노드 관련 처리가 필요할 경우 사용          
      })
```

  8. properties & methods

      예) const ret = list.wiseTreeView(option, json); debugger
      - ret.jsonArr
      - ret.totalCount
      - ret.childCount
      - ret.collapse(targetDepth)
      - ret.collapseAll()
      - ret.expand(targetDepth)
      - ret.expandAll()
      - ret.getText(idx)
      - ret.getText1(idx)
      - ret.getText2(idx)
      - ret.setNodeLeftImage(idx, src, width, height, ignoreIfSrcExists)
        트리 가져온 후 루프 돌면서 비동기로 이미지 추가시 사용. ignoreIfSrcExists : true시 기존 이미지 있어도 무조건 replace
 
  9. callback 지원

``` javascript
      list.wiseTreeView(option, json, function(ret) {
          console.log("done: " + ret.totalCount)          
      })
```

  10. async/await 지원            

``` javascript
      const ret = await list.wiseTreeViewAsync(option, json)      
      console.log("done: " + ret.totalCount) 
```

끝.
