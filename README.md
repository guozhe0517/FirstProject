- // 웹페이지 띄우기
Uri uri = Uri.parse("http://www.google.com");
Intent it  = new Intent(Intent.ACTION_VIEW,uri);
startActivity(it);

- // 구글맵 띄우기
Uri uri = Uri.parse("geo:38.899533,-77.036476");
Intent it = new Intent(Intent.Action_VIEW,uri);
startActivity(it); 


- // 구글 길찾기 띄우기
Uri uri = Uri.parse("http://maps.google.com/maps?f=d&saddr=출발지주소&daddr=도착지주소&hl=ko");
Intent it = new Intent(Intent.ACTION_VIEW,URI);
startActivity(it);


- // 전화 걸기
Uri uri = Uri.parse("tel:xxxxxx");
Intent it = new Intent(Intent.ACTION_DIAL, uri);  
startActivity(it);  

- 
Uri uri = Uri.parse("tel.xxxxxx");
Intent it = new Intent(Intent.ACTION_CALL,uri);
// 퍼미션을 잊지 마세요. <uses-permission id="android.permission.CALL_PHONE" />


- // SMS/MMS 발송
Intent it = new Intent(Intent.ACTION_VIEW);   
it.putExtra("sms_body", "The SMS text");   
it.setType("vnd.android-dir/mms-sms");   
startActivity(it);  


- // SMS 발송
Uri uri = Uri.parse("smsto:0800000123");   
Intent it = new Intent(Intent.ACTION_SENDTO, uri);   
it.putExtra("sms_body", "The SMS text");   
startActivity(it);  


- // MMS 발송
Uri uri = Uri.parse("content://media/external/images/media/23");   
Intent it = new Intent(Intent.ACTION_SEND);   
it.putExtra("sms_body", "some text");   
it.putExtra(Intent.EXTRA_STREAM, uri);   
it.setType("image/png");   
startActivity(it); 


- // 이메일 발송
Uri uri = Uri.parse("mailto:xxx@abc.com");
Intent it = new Intent(Intent.ACTION_SENDTO, uri);
startActivity(it);


Intent it = new Intent(Intent.ACTION_SEND);   
it.putExtra(Intent.EXTRA_EMAIL, "me@abc.com");   
it.putExtra(Intent.EXTRA_TEXT, "The email body text");   
it.setType("text/plain");   
startActivity(Intent.createChooser(it, "Choose Email Client"));  


Intent it = new Intent(Intent.ACTION_SEND);     
String[] tos = {"me@abc.com"};     
String[] ccs = {"you@abc.com"};     
it.putExtra(Intent.EXTRA_EMAIL, tos);     
it.putExtra(Intent.EXTRA_CC, ccs);     
it.putExtra(Intent.EXTRA_TEXT, "The email body text");     
it.putExtra(Intent.EXTRA_SUBJECT, "The email subject text");     
it.setType("message/rfc822");     
startActivity(Intent.createChooser(it, "Choose Email Client"));   


- // extra 추가하기
Intent it = new Intent(Intent.ACTION_SEND);   
it.putExtra(Intent.EXTRA_SUBJECT, "The email subject text");   
it.putExtra(Intent.EXTRA_STREAM, "file:///sdcard/mysong.mp3");   
sendIntent.setType("audio/mp3");   
startActivity(Intent.createChooser(it, "Choose Email Client"));


- // 미디어파일 플레이 하기
Intent it = new Intent(Intent.ACTION_VIEW);
Uri uri = Uri.parse("file:///sdcard/song.mp3");
it.setDataAndType(uri, "audio/mp3");
startActivity(it);


Uri uri = Uri.withAppendedPath(
  MediaStore.Audio.Media.INTERNAL_CONTENT_URI, "1");   
Intent it = new Intent(Intent.ACTION_VIEW, uri);   
startActivity(it);  


- // 설치 어플 제거
Uri uri = Uri.fromParts("package", strPackageName, null);   
Intent it = new Intent(Intent.ACTION_DELETE, uri);   
startActivity(it);


- // APK파일을 통해 제거하기
Uri uninstallUri = Uri.fromParts("package", "xxx", null);
returnIt = new Intent(Intent.ACTION_DELETE, uninstallUri);


- // APK파일 설치
Uri installUri = Uri.fromParts("package", "xxx", null);
returnIt = new Intent(Intent.ACTION_PACKAGE_ADDED, installUri);


- // 음악 파일 재생
Uri playUri = Uri.parse("file:///sdcard/download/everything.mp3");
returnIt = new Intent(Intent.ACTION_VIEW, playUri);


- // 첨부파일을 추가하여 메일 보내기
Intent it = new Intent(Intent.ACTION_SEND);  
it.putExtra(Intent.EXTRA_SUBJECT, "The email subject text");  
it.putExtra(Intent.EXTRA_STREAM, "file:///sdcard/eoe.mp3");  
sendIntent.setType("audio/mp3");  
startActivity(Intent.createChooser(it, "Choose Email Client"));


- // 마켓에서 어플리케이션 검색
Uri uri = Uri.parse("market://search?q=pname:pkg_name");  
Intent it = new Intent(Intent.ACTION_VIEW, uri);  
startActivity(it);  
- // 패키지명은 어플리케이션의 전체 패키지명을 입력해야 합니다.


- // 마켓 어플리케이션 상세 화면
Uri uri = Uri.parse("market://details?id=어플리케이션아이디");  
Intent it = new Intent(Intent.ACTION_VIEW, uri);  
startActivity(it);
- // 아이디의 경우 마켓 퍼블리싱사이트의 어플을 선택후에 URL을 확인해보면 알 수 있습니다.


- // 구글 검색
Intent intent = new Intent();
intent.setAction(Intent.ACTION_WEB_SEARCH);
intent.putExtra(SearchManager.QUERY,"searchString")
startActivity(intent);
