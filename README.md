# xmayocatx2<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8"%>
<!DOCTYPE html><html><head><meta charset="UTF-8"><meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0, user-scalable=no">
<title>간단한 지도 표시하기</title>
<script type="text/javascript" src="https://openapi.map.naver.com/openapi/v3/maps.js?clientId=N42oA4gGPK53TokQ9Vui"></script>
<script>
var HOME_PATH = window.HOME_PATH || '.';var la_map = new naver.maps.LatLng(37.4989960, 127.032849),
map = new naver.maps.Map('map', {center: la_map, zoom: 10}),
marker = new naver.maps.Marker({map: map,position: la_map});
var contentString = [
'<div class="iw_inner">',
'<h3>LaLaLa&Ding</h3>',
'<p>서울특별시 강남구 테헤란로14길 6 | 서울특별시 강남구 역삼동 823-24 남도빌딩 2층, 3층<br/>',
'교육기관 &gt; 세미프로젝트<br/>',
'<a href="https://www.iei.or.kr/main/main.kh" target="_blank">www.semitest.go.kr/</a>',
'</p>',
'</div>'].join('');
var infowindow = new naver.maps.InfoWindow({content: contentString,maxWidth: 140,
backgroundColor: "#eee", borderColor: "#2db400",borderWidth: 5,anchorSize: new naver.maps.Size(30, 30),
anchorSkew: true,anchorColor: "#eee",pixelOffset: new naver.maps.Point(20, -20)});
naver.maps.Event.addListener(marker, "click", function(e) {
if (infowindow.getMap()) {infowindow.close();
} else {infowindow.open(map, marker);
}});
</script>
</head>
<body>
<div id="map" style="width: 100%; height: 400px;"></div>
<script>var mapOptions = {center: new naver.maps.LatLng(37.3595704, 127.105399),zoom: 10};
var map = new naver.maps.Map('map', mapOptions);
</script>
</body>
</html>
