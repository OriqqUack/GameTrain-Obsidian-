---
태그: 공부
설명: 인프런 2d게임 공부
작성 날짜: "[[2023-09-24]]"
수정된 날짜: "[[2023-10-01]]"
---

---

## 맵 개선

[[AsyncOperation]] 


## UI 개선

1. 팝업인지 씬인지 구별
2. 씬에 바로 올리는 것이 아닌 UI -> Image 를 클릭해서 Image를 만들고 거기에 Sprite를 덮어 주자.
3. UI가 작동하는지 확인하는 절차
	1.  UI의 *RayCast*가 켜져 있거나 불필요한 UI의 RayCast가 꺼져있는지 확인.
	2. Hierachy창에 *EventSystem* 존재 유무 확인.
4. UI는 자동화가 되는 게 편하다. 강의에선 *SetInfo(), RefreshUI()* 를 통해서 관리함.
5. UI를 그리기 위한 스크립트와 데이터 스크립트를 따로 만들어라. UI_GameScene <> GameManager. 지금은 규모가 작아서  GameManger에서 다 관리하지만 규모가 커지면 Invetory 처럼 각각 만들어서 데이터 관리를 해야한다.
6. 자시만의 규칙을 만들어라. ex) UI는 따로 스크립트를 파고 
	