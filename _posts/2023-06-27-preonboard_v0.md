---
title: "💫 7월 프리온보딩 사전과제"
categories:
  - FE
tags:
  - frontend
  - 7월 프리온보딩 - 직접 만져보는 Next.js 해부학 교실 사전과제
author_profile: true
comments: true
search: true
toc: true
toc_label: "사전과제"
toc_icon: "minus"
toc_sticky: true
---

{% capture notice-2 %}

# CSR(Client-side Rendering)이란 ❓

- Javascript를 사용하여 브라우저에서 직접 페이지를 렌더링하는 것
- 모든 논리, 데이터 검색, 템플릿 및 라우팅은 서버가 아닌 클라이언트에서 처리
  {% endcapture %}

<div class="notice">{{ notice-2 | markdownify }}</div>

## 🔶 CSR(Client-side Rendering) 작동

![Unsplash]({{ site.url }}{{ site.baseurl }}/assets/images/CSRexecutes.png)
{: .full-csr}

<!-- <img class="align-left" style = "margin-right : 30px; margin-bottom : 50px;" src="{{ site.url }}{{ site.baseurl }}/assets/images/CSRexecutes.png" alt="">
{% capture notice-2 %}
1.  서버는 클라이언트에 응답을 보낸다.
2.  브라우저는 JS를 렌더링
3.  브라우저는 JS를 실행
4.  페이지(화면) 표시
  {% endcapture %}

<div class="left-box">{{ notice-2 | markdownify }}</div>
<br/> -->

## 🔸 CSR(Client-side Rendering) 단점

🌟 느린 초기 로드 시간

- 각종 자원을 다운로드한 후에 브라우저에서 렌더링하기 때문이다.

🌟 낮은 SEO

- SEO란❓<br/>
  웹사이트의 기술적 구조, 콘텐츠 관련성 및 링크 인기도를 최적화하는데 사용되는 프로세스로 페이지를 더 쉽게 찾을 수 있고, 검색에서 더 관련성 있고 인기 있으며 검색엔진에서 순위를 높일 수 있다.
- 검색엔진이 해당 페이지로 처음 접하였을 경우 빈 페이지이므로 이해할 수 없다. 현재는 JS도 실행할 수 있는 구글 크롤러와 같은 검색엔진이 등장하고 있지만 아직은 많은 검색엔진에서 지원되지 않는다.

🌟 페이지가 완전히 로드될 때까지 캐싱이 불가능하다.

- SSR은 사용자 정보를 서버 측에 세션으로 관리하지만 CSR은 쿠키 말고는 사용자 정보를 저장할 공간이 마땅치 않다.

## 🔸 CSR(Client-side Rendering) 장점

🌟 후속 페이지 로드 시간이 빠르다.

- 이미 지원 스크립트가 사전에 로드되어 있으므로 로드 시간이 줄어든다.

🌟 서버 호출 시마다 전체 UI를 로드할 필요가 없다.

- 필요하고 변경된 데이터만 받아올 수 있어 서버의 부담을 줄일 수 있다.

{% capture notice-2 %}

# SSR(Server-side Rendering)이란 ❓

- 서버에서 렌더링을 작업하는 방식, 전통적인 웹 애플리케이션 렌더링 방식으로 사용자가 웹 페이지를 접근할 때, 서버에 각각의 페이지에 대한 요청을 하며 서버에서 HTML 및 JS 파일 등을 모두 다운로드하여 화면에 표출
- 초기 로딩 속도가 빠르며 SEO 점수가 높다.
- 변경이 필요할 때마다 서버에 지속적으로 요청해야 하므로 서버에 부담이 된다.
  {% endcapture %}

<div class="notice">{{ notice-2 | markdownify }}</div>

✅ 한가지로 구성하기 보다는 SSR과 CSR 등 적절히 활용하여 구성하는 것이 가장 좋은 방법이다.

{% capture notice-2 %}

# SPA(Single Page Application)이란 ❓

- Single Page Application으로 단일 페이지로 구성
- 비교적 배포가 간단하며 native app과 유사한 ux를 제공
- 새로운 페이지 요청 시 갱신에 필요한 데이터만을 받아 페이지 갱신
- 전체적으로 서버에 부담이 줄어듦
  {% endcapture %}

<div class="notice notice-my">{{ notice-2 | markdownify }}</div>
## 🔶 SPA(Single Page Application) 단점

- 초기 구동속도가 느림
- SEO가 낮다.
- 보안에 문제가 있다.

## ✅ SPA(Single Page Application)로 구성된 웹 앱에서 SSR(Server-side Rendering)이 필요한 이유

🌟 검색엔진 최적화 이슈를 해결할 수 있다.

- 서버에서 렌더링 된 페이지를 사용하면 검색 엔진 크롤러가 웹 페이지의 콘텐츠와 태크를 쉽게 읽을 수 있게 하여, 웹사이트의 검색 엔진 순위를 향상시킬 수 있다.

🌟 초기 로딩 시간을 줄일 수 있다.

- 사용자는 서버가 클라이언트에게 완전히 렌더링 된 페이지를 전송하기 때문에 사용자가 페이지와 상호 작용을 시작하기 전에 애플리케이션이 로딩되어야 하는 시간을 줄일 수 있다.

🌟 사용자 경험이 개선된다

- 사용자에게 빈 화면이나 로딩 화면을 보여주는 대신 완전히 렌더링 된 화면을 즉시 보여줄 수 있고 사이트 방문자가 빠른 시간 내에 원하는 정보를 찾을 수 있게 된다.

# Next.js project에서 yarn start를 실행한다면 ❓

`yarn start`전에 `yarn build`로 먼저 nextjs 애플리케이션 빌드를 실행

빌드 후 `yarn start`실행시 `package.json`에서 `next start`가 실행

```json
"scripts": {
"dev": "next",
"build": "next build",
"start": "next start"
},
```

**next.js/packages/next/src/cli/next-start** 파일실행하면 startServer가 실행되어

```js
await startServer({
  dir,
  isDev: false,
  hostname: host,
  port,
  keepAliveTimeout,
  useWorkers: !!config.experimental.appDir,
});
```

최종적으로 **next.js/packages/next/src/server/lib/start-server** 파일실행이 실행된다.

```js
const server = http.createServer(async (req, res) => {
  try {
    if (handlersPromise) {
      await handlersPromise;
      handlersPromise = undefined;
    }
    sockets.add(res);
    res.on("close", () => sockets.delete(res));
    await requestHandler(req, res);
  } catch (err) {
    res.statusCode = 500;
    res.end("Internal Server Error");
    Log.error(`Failed to handle request for ${req.url}`);
    console.error(err);
  }
});
```

위 파일이 다 실행되면 결론적으로 [localhost:3000](http://localhost:3000) 서버가 실행된다.

# 과제를 하며 느낀점 ❗️

처음에 사전과제를 보고는 이해를 하지 못했다. 그래서 깃 소스도 엄청 둘러보고 블로그도 찾으며 노력했지만 결국 갈피를 잡지 못한 체 과제 제출 기한이 다가와 제출해버렸다.
그리고 첫 강의에서 당연히 그렇게 하는 게 아니라는 강사님의 말씀에 다시 깃 소스를 뜯어보고 강사님의 말씀을 떠올려가며 아름아름 소스를 찾았다.
맞는 정답인지는 모르지만 차근차근 따라가다 보니 모든 소스를 다 알진 못하더라고 이거 일 거 같은 소스들이 보였고 서버가 그렇게 실행되는 것으로 확인하였다.
{:.notice--info}
