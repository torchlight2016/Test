---
layout: post
title: "광고 ID(Advertising ID)"
---

Google Play로 부터의 앱이 삭제되었다는 메일이 왔다.

<h4>
xxx 을(를) 검토한 결과 정책 위반으로 Google Play에서 앱이 삭제되었습니다. 귀하의 앱은 정책을 따르는 업데이트를 제출할 때까지 사용자에게 제공되지 않습니다.
귀하의 앱은 Android 광고 ID 사용 및 개발자 배포 계약의 4.8 조항을 위반하였습니다.
</h4>

2년 동안 문제없었으나 구글의 개인정보 보호정책에 변경된거 같다.
한달전쯤 관련 메일이 왔었는데 무시했더니 앱이 삭제되었다.

<span style="color:red">Firebase Analytics 라이브러리에서 광고 ID를 수집하고 있어 문제가 되었다.</span> 
<br>

해결방법은 수집하지 않거나 앱의 스토어 페이지에서 개인정보 취급방침 URL을 기입하면 해결된다.

[Firebase Analytics 수집 중지](https://firebase.google.com/support/guides/disable-analytics?hl=ko)하기 위해 androidmanifest.xml에 아래 코드를 추가한다.

{% highlight ruby %}
<meta-data android:name="firebase_analytics_collection_enabled" android:value="false" /> 
{% endhighlight %}





