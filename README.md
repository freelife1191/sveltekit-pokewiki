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