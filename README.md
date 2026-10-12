# REAL Jellybeans

[nanotech/jellybeans.vim](https://github.com/nanotech/jellybeans.vim)의 색을 최대한 그대로 옮긴 VS Code 다크 테마입니다.

## 기존 Jellybeans 테마(DimitarNonov)와 다른 점

- **터미널 16색이 제대로 구분됩니다.** 기존 테마는 `ansiBlack`과 `ansiWhite`가 같은 색(`#e8e8d3`)이고 Bright 색이 일반 색과 전부 같아서, tmux 상태바·htop·fzf 등이 깨졌습니다.
- **문법 색을 vim 하이라이트 그룹 기준으로 맞췄습니다.** Type `#ffb964`, Structure/PreProc `#8fbfdc`, StorageClass `#c59f6f`, Delimiter `#668799`, StringDelimiter `#556633`, Identifier `#c6b6ee`, Title `#70b950` 등.
- **UI 색 버그를 고쳤습니다.** 알림 정보/경고 아이콘 색 뒤바뀜, 초록색 경고, 디버깅 중에도 바뀌지 않는 상태바, 보이지 않는 선택 영역·현재 줄 강조.

## 팔레트

| vim 그룹 | 색 | VS Code 적용 |
| --- | --- | --- |
| Normal | `#e8e8d3` / bg `#151515` | 기본 글자/배경 |
| Comment | `#888888` italic | 주석 |
| Constant | `#cf6a4c` | 숫자, 상수, 불리언 |
| String | `#99ad6a` | 문자열 |
| StringDelimiter | `#556633` | 따옴표 |
| Special | `#799d6a` | 이스케이프, 엔티티 |
| Identifier | `#c6b6ee` | self/this, 문자열 보간 |
| Statement | `#8197bf` | 키워드, 태그 |
| Structure / Operator / PreProc | `#8fbfdc` | 연산자, class/struct, import, 데코레이터 |
| StorageClass | `#c59f6f` | static/const 등 수식어, CSS 속성 |
| Type | `#ffb964` | 타입, 클래스 이름 |
| Function | `#fad07a` | 함수 |
| Delimiter | `#668799` | 괄호, 구분자 |
| Title | `#70b950` bold | 마크다운 제목 |

jellybeans.vim에는 터미널 16색 정의가 없어서, 일반 8색은 위 팔레트에서 가져오고 Bright 8색은 각 색을 흰색 쪽으로 30% 섞어 만들었습니다. 검정은 배경과 구분되도록 `#3b3b3b`, 밝은 검정은 주석 색 `#888888`입니다.

## 설치

```sh
npx @vscode/vsce package
code --install-extension real-jellybeans-theme-*.vsix
```

그다음 `Preferences: Color Theme`에서 **REAL Jellybeans**를 고릅니다.

## 라이선스

MIT. 색 팔레트는 MIT 라이선스인 [jellybeans.vim](https://github.com/nanotech/jellybeans.vim)(NanoTech)에서 가져왔습니다.
