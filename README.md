# HEAD

HTML head 태그 모음 (특별히 meta 태그!)

## 내용

- [최소 권장사항](#최소-권장사항)
- [태그들](#태그들)
- [메타 태그들](#메타-태그들)
  - [사용하지 않기를 권고하는 메타 태그들](#사용하지-않기를-권고하는-메타-태그들)
- [링크 태그들](#링크-태그들)
  - [사용하지 않기를 권고하는 링크 태그들](#사용하지-않기를-권고하는-링크-태그들)
  - [파비콘](#파비콘)
- [소셜](#소셜)
  - [페이스북 / 오픈 그래프](#페이스북---오픈-그래프)
  - [페이스북 / 인스턴트 아티클](#페이스북--인스턴트-아티클)
  - [트위터](#트위터)
  - [Google+ / Schema.org](#google--schemaorg)
  - [OEmbed](#oembed)
- [브라우저 / 플랫폼](#브라우저--플랫폼)
  - [애플 iOS](#애플-ios)
  - [애플 사파리](#애플-사파리)
  - [구글 안드로이드](#구글-안드로이드)
  - [구글 크롬](#구글-크롬)
  - [인터넷 익스플로러](#인터넷-익스플로러)
  - [인터넷 익스플로러 (사용하면 안되는 레거시들)](#인터넷-익스플로러-사용하면-안되는-레거시들)
  - [360 브라우저](#360-브라우저)
  - [UC 모바일 브라우저](#uc-모바일-브라우저)
  - [QQ 모바일 브라우저](#qq-모바일-브라우저)
- [앱 링크](#앱-링크)
- [알림](#알림)
  - [성능](#성능)
- [다른 자원들](#다른-자원들)
- [관련 프로젝트들](#관련-프로젝트들)
- [기여](#기여)

## 최소 권장사항

웹사이트가 기본적으로 반드시 가져야 할 태그들

```html
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Page Title</title>
```

## 태그들

``` html
<!-- 문서 제목 -->
<title>페이지 제목</title>

<!-- 문서내에 있는 상대 주소의 루트가 될 Base 주소 -->
<base href="https://example.com/page.html">

<!-- 외부 CSS 파일 -->
<link rel="stylesheet" href="styles.css">

<!-- 인라인 CSS -->
<style>
  /* ... */
</style>

<!-- 자바스크립트 -->
<script src="script.js"></script>
```

## 메타 태그들

``` html
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<!-- 위의 3개 태그는 *반드시* head의 첫번째에 와야함. 다른 head 태그들은 반드시 이 태그들 *이후에* 와야한다.  -->
<meta name="application-name" content="Application 이름">
<meta name="description" content="150자 이내의 페이지 설명">
<meta name="subject" content="웹사이트 주제">
<meta name="robots" content="index,follow,noodp">
<meta name="googlebot" content="index,follow">
<meta name="google" content="nositelinkssearchbox">
<meta name="google-site-verification" content="verification_token">
<meta name="generator" content="program">
<meta name="abstract" content="">
<meta name="topic" content="">
<meta name="summary" content="">
<meta name="classification" content="business">
<meta name="url" content="https://example.com/">
<meta name="identifier-URL" content="https://example.com/">
<meta name="directory" content="submission">
<meta name="category" content="">
<meta name="coverage" content="Worldwide">
<meta name="distribution" content="Global">
<meta name="rating" content="General">
<meta name="referrer" content="never">
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

<!-- 핸드폰 번호 자동 감지 및 포매팅 기능 해제  -->
<meta name="format-detection" content="telephone=no">

<!-- 위치 정보 태그 -->
<meta name="ICBM" content="latitude, longitude" />
<meta name="geo.position" content="latitude;longitude" />
<meta name="geo.region" content="country[-state]" /><!-- 국가 코드 (ISO 3166-1): 필수, 주(state) 코드 (ISO 3166-2): 선택; eg. content="US" / content="US-NY" -->
<meta name="geo.placename" content="city/town" /><!-- eg. content="New York City" -->
```

- [ICBM on Wikipedia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- [Geotagging on Wikipedia](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)

### 사용하지 않기를 권고하는 메타 태그들
아래 메타 태그들은 사용하지 맙시다.

```html
<!-- 문서에서 사용하는 언어를 명시하지만 잘 지원이 안됩니다. 그러니 <html lang=""> 형태로 사용합시다. -->
<meta name="language" content="en">

<!-- 구글하고 빙은 이 태그를 스팸으로 간주한답니다. -->
<meta name="keywords" content="your,keywords,here,comma,separated,no,spaces">

<!-- 현재 어떤 검색엔진에서도 이 태그를 사용한다는 정보가 없습니다. -->
<meta name="revised" content="Sunday, July 18th, 2010, 5:15 pm">

<!-- to 스팸 봇: 내 멜 주소를 가져가서 스팸에 쓰세요. 읭??? -->
<meta name="reply-to" content="email@example.com">

<!-- <link rel="author"> 형태나 humans.txt 파일 형태로 사용합시다. -->
<meta name="author" content="name, email@example.com">
<meta name="designer" content="">
<meta name="owner" content="">

<!-- to 검색 봇: 특정 기간 이후에 우리 페이지 다시 방문해줘. -->
<!-- RE: 싫어요~ 언제 방문할지는 제 맘입니다~ 랜덤이죠! -->
<meta name="revisit-after" content="7 days">

<!-- 구글이 이거 쓰지 말라고 아주 강하게 권고하네요. 서버측에서 redirect 설정합시다. -->
<meta http-equiv="refresh" content="300;url=https://example.com/">

<!-- 캐시 제어 -->
<!-- 서버측에서 설정합시다 :) -->
<meta http-equiv="Expires" content="0">
<meta http-equiv="Pragma" content="no-cache">
<meta http-equiv="Cache-Control" content="no-cache">
```

## 링크 태그들

``` html
<link rel="copyright" href="copyright.html">
<link rel="stylesheet" href="https://example.com/styles.css">
<link rel="alternate" href="https://feeds.feedburner.com/martini" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">
<link rel="alternate" href="https://es.example.com/" hreflang="es">
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">
<link rel="archives" href="https://example.com/2003/05/" title="May 2003">
<link rel="index" href="https://example.com/" title="DeWitt Clinton">
<link rel="start" href="https://example.com/photos/pattern_recognition_1_about/" title="Pattern Recognition 1">
<link rel="prev" href="https://example.com/opensearch/opensearch-and-openid-a-sure-way-to-get-my-attention/" title="OpenSearch and OpenID? A sure way to get my attention.">
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">
<link rel="self" type="application/atom+xml" href="https://example.com/atomFeed.php?page=3">
<link rel="first" href="https://example.com/atomFeed.php">
<link rel="next" href="https://example.com/atomFeed.php?page=4">
<link rel="previous" href="https://example.com/atomFeed.php?page=2">
<link rel="last" href="https://example.com/atomFeed.php?page=147">
<link rel="shortlink" href="https://example.com/?p=43625">
<link rel="canonical" href="https://example.com/2010/06/9-things-to-do-before-entering-social-media.html">
<link rel="amphtml" href="https://www.example.com/url/to/amp-version.html">
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">
<link rel="pingback" href="https://example.com/xmlrpc.php">
<link rel="webmention" href="https://example.com/webmention">
<link rel="manifest" href="manifest.json">
<link rel="author" href="humans.txt">
<link rel="import" href="component.html">

<!-- Prefetching, preloading, prebrowsing -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="subresource" href="styles.css">
<link rel="preload" href="image.png">
```

- [Prefetching, Preloading, Prebrowsing](https://css-tricks.com/prefetching-preloading-prebrowsing)

### 사용하지 않기를 권고하는 링크 태그들
아래 링크 태그들은 사용하지 맙시다.

```html
<link rel="shortcut icon" href="path/to/favicon.ico">
```

### 파비콘

``` html
<!-- IE 10 이하 버전에서는 -->
<!-- 링크 제공하지 말고 favicon.ico 파일을 루트 폴더에 둡시다. -->

<!-- IE 11, Chrome, Firefox, Safari, Opera -->
<link rel="icon" href="path/to/favicon-16.png" sizes="16x16" type="image/png">
<link rel="icon" href="path/to/favicon-32.png" sizes="32x32" type="image/png">
<link rel="icon" href="path/to/favicon-48.png" sizes="48x48" type="image/png">
<link rel="icon" href="path/to/favicon-62.png" sizes="62x62" type="image/png">
<link rel="icon" href="path/to/favicon-192.png" sizes="192x192" type="image/png">
```

- [All About Favicons (And Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/)

## 소셜

### 페이스북 / 오픈 그래프

``` html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
```

- [Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup)
- [Open Graph protocol](http://ogp.me/)

### 페이스북 / 인스턴트 아티클

``` html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- 아티클은 페이스북의 인스턴트 아티클을 말함 -->
<!-- 아티클의 웹 버전 주소 -->
<link rel="canonical" href="http://example.com/article.html">

<!-- 아티클에 사용된 스타일 -->
<meta property="fb:article_style" content="myarticlestyle">
```

- [Facebook Instant Articles: Creating Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- [Instant Articles: Format Reference](https://developers.facebook.com/docs/instant-articles/reference)

### 트위터

``` html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

- [Twitter Cards: Getting Started Guide](https://dev.twitter.com/cards/getting-started)
- [Twitter Card Validator](https://dev.twitter.com/docs/cards/validation/validator)

### Google+ / Schema.org

``` html
<link href="https://plus.google.com/+YourPage" rel="publisher">
<meta itemprop="name" content="Content Title">
<meta itemprop="description" content="Content description less than 200 characters">
<meta itemprop="image" content="https://example.com/image.jpg">
```

### OEmbed

``` html
<link rel="alternate" type="application/json+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- [oEmbed format](http://oembed.com/)

## 브라우저 / 플랫폼


### 애플 iOS

``` html
<!-- 스마트 앱 배너 -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- 핸드폰 번호 자동 감지 및 포매팅 기능 해제  -->
<meta name="format-detection" content="telephone=no">

<!-- 홈 스크린에 추가 -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- 터치 아이콘 -->
<link rel="apple-touch-icon" href="path/to/apple-touch-icon.png">
<link rel="apple-touch-icon-precomposed" href="path/to/apple-touch-icon-precomposed.png">
<!-- 대부분의 경우, head 안에 180x180px 크기의 아이콘 한개면 충분하다. -->
<!-- 만약 art-direction을 사용하거나 기기별로 다른 콘텐츠를 보여주고 싶다면, 아이콘을 여러개 추가하면 된다 -->

<!-- 시작(start-up) 이미지 -->
<link rel="apple-touch-startup-image" href="path/to/startup.png">
```

- [Apple Meta Tags](https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

### 애플 사파리

```html
<!-- 핀 표시한 사이트 (pinned site) -->
<link rel="mask-icon" href="path/to/icon.svg" color="red">
```

### 구글 안드로이드

``` html
<meta name="theme-color" content="#E64545">

<!-- 홈 스크린에 추가 -->
<meta name="mobile-web-app-capable" content="yes">
```

- [Install to Home Screen](https://developer.chrome.com/multidevice/android/installtohomescreen)

### 구글 크롬

``` html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- 번역 기능 해제 -->
<meta name="google" value="notranslate">
```

### 인터넷 익스플로러

``` html
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta http-equiv="cleartype" content="on">
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- 윈도우 폰 내 IE 10 링크 하이라이팅 기능 해제 -->
<meta name="msapplication-tap-highlight" content="no">

<!-- 핀 표시한 사이트 -->
<meta name="application-name" content="Contoso Pinned Site Caption">
<meta name="msapplication-tooltip" content="Example Tooltip Text">
<meta name="msapplication-starturl" content="/">

<meta name="msapplication-config" content="http://example.com/browserconfig.xml">

<meta name="msapplication-allowDomainApiCalls" content="true">
<meta name="msapplication-allowDomainMetaTags" content="true">
<meta name="msapplication-badge" content="frequency=30; polling-uri=http://example.com/id45453245/polling.xml">
<meta name="msapplication-navbutton-color" content="#FF3300">
<meta name="msapplication-notification" content="frequency=60;polling-uri=http://example.com/livetile">
<meta name="msapplication-square150x150logo" content="path/to/logo.png">
<meta name="msapplication-square310x310logo" content="path/to/largelogo.png">
<meta name="msapplication-square70x70logo" content="path/to/tinylogo.png">
<meta name="msapplication-wide310x150logo" content="path/to/widelogo.png">
<meta name="msapplication-task" content="name=Check Order Status;action-uri=./orderStatus.aspx?src=IE9;icon-uri=./favicon.ico">
<meta name="msapplication-task-seperator" content="1">
<meta name="msapplication-TileColor" content="#FF3300">
<meta name="msapplication-TileImage" content="path/to/tileimage.jpg">
<meta name="msapplication-window" content="width=1024;height=768">
```

- [Adapting your webkit optimized site for IE 10](https://blogs.windows.com/buildingapps/2012/11/15/adapting-your-webkit-optimized-site-for-internet-explorer-10/)

### 인터넷 익스플로러 (사용하면 안되는 레거시들)

``` html
<!-- Disable the image toolbar when you mouse over images in IE 6 (https://msdn.microsoft.com/en-us/library/ms532986(v=vs.85).aspx) -->
<meta http-equiv="imagetoolbar" content="no">

<!-- Disable Windows theming to form inputs/buttons (https://support.microsoft.com/en-us/kb/322240) -->
<meta name="MSThemeCompatible" content="no">

<!-- Disable a feature that only appeared on IE 6 beta (https://stackoverflow.com/q/2167301) -->
<meta name="MSSmartTagsPreventParsing" content="true">

<!-- Interpage Transitions (https://msdn.microsoft.com/en-us/library/ms532847(v=vs.85).aspx) -->
<meta http-equiv="Page-Enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="Page-Exit" content="revealtrans(duration=3,transition=12)">
<meta http-equiv="Site-Enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="Site-Exit" content="revealtrans(duration=3,transition=12)">
```

### 360 브라우저

``` html
<!-- 렌더링 엔진 순서대로 표시 -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### UC 모바일 브라우저

``` html
<!-- 특정 방향으로 스크린 잠금 -->
<meta name="screen-orientation" content="landscape/portrait">
<!-- 이 페이지 풀스크린으로 표시 -->
<meta name="full-screen" content="yes">
<!-- "text mode"여도 이미지 표시 강제 -->
<meta name="imagemode" content="force">
<!-- 페이지를 "application mode"로 실행 (풀스크린,제스처 금지, etc.) -->
<meta name="browsermode" content="application">
<!-- 페이지를 "night mode"로 실행 제한 -->
<meta name="nightmode" content="disable">
<!-- 데이터 소모를 줄이기 위해 페이지 Simplify -->
<meta name="layoutmode" content="fitscreen">
<!-- Disable the UC browser's feature of "scaling font up when there are many words in this page" -->
<meta name="wap-font-scale" content="no">
```

- [UC Browser Docs](http://www.uc.cn/download/UCBrowser_U3_API.doc)

### QQ 모바일 브라우저

``` html
<!-- 특정 방향으로 스크린 잠금 -->
<meta name="x5-orientation" content="landscape/portrait">
<!-- 이 페이지 풀스크린으로 표시 -->
<meta name="x5-fullscreen" content="true">
<!-- 페이지를 "application mode"로 실행 (풀스크린, etc.) -->
<meta name="x5-page-mode" content="app">
```

## 앱 링크

``` html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">
<!-- 안드로이드 -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">
<!-- 웹 Fallback -->
<meta property="al:web:url" content="http://applinks.org/documentation">
```

- [App Links Docs](http://applinks.org/documentation/)

## 알림

### 성능
`href` 속성을 태그의 첫번째 속성으로 지정하면 GZIP 기능을 사용할 때 압축 성능이 향상 된다. 왜냐하면 `href` 속성은 `a`, `base`, `link` 태그에서 사용되기 때문이다.

Example:
```
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700" rel="stylesheet">
```

## 다른 자원들

- [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

## 관련 프로젝트들

- [html-head-snippets](https://github.com/joshbuchea/atom-html-head-snippets) - `HEAD` 스니핏을 위한 아톰 패키지
- [head-it](https://github.com/hemanth/head-it) - `HEAD` 스니핏을 위한 CLI 인터페이스

## 번역

- [일본어](http://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)

## 기여

수정이나 추가를 제안하고 싶으면 이슈나 풀리퀘를 해주세요.

풀리퀘는 다음 순서대로 해주세요:
 - 하나의 태그나 관련된 태그 내용을 한번에 수정해주세요
 - 속성은 쌍따옴표로 감싸주세요
 - 스스로 닫는 태그는 문장 마지막에 슬래시는 사용하지 말아주세요. HTML5 스펙에 해당 사항은 선택이라고 나와있어요.
 - 수정한 내용에 대해서는 문서를 포함하는 걸 고려해주세요.

## 기여자들

[우리 짱 멋진 기여자들을 확인해보세요](https://github.com/joshbuchea/HEAD/graphs/contributors).

## 저자

**[Josh Buchea](http://joshbuchea.com/)**

## 라이센스

[CC0 License](LICENSE)

![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")
