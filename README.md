# 포켓몬 위키 웹사이트 만들기

1. 웹개발의 프로세스
2. 스벨트, 스벨트킷의 테크닉
    - page route, api route, SSR(서버 사이드 렌더링)
    - svelte store, reactivity, 검색, 필터링
3. 디자인: tailwindcss(css framework) 사용법

- 포켓몬 API: https://pokeapi.co/
    - https://pokeapi.co/api/v2/pokemon

## 1. 프로젝트 셋업

- tailwindcss svelteKit: https://tailwindcss.com/docs/guides/sveltekit

tailwindcss 설치
```bash
$ npm install -D tailwindcss postcss autoprefixer
$ npx tailwindcss init -p
```

## 2. 사이트 초반 작업

- 타이틀
- 메인페이지 꾸미기
- 네비게이션
- About 페이지

## 3. poke API 에서 데이터 가져오기

- poke API: https://pokeapi.co/api/v2/pokemon

아래의 SvelteKit Loading Data를 사용하지 않고 [Promise.all()](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Promise/all) 사용
- Loading Data: https://kit.svelte.dev/docs/load

Store에 데이터를 저장하여 모든 컴포넌트에서 사용할 수 있도록 구현
![store](attachments/20231031084650.png)

150개의 Poketmon 데이터 가져오기
```JSON
GET https://pokeapi.co/api/v2/pokemon?limit=150
```