# MetaLand

MetaLand is integrated metaverse platform, which includes minecraft server, auth, web services.

# Architecture
![image](https://user-images.githubusercontent.com/20203944/158025473-8eb2e274-b6e1-436c-ad5b-2ee3e03a3a75.png)

* 마인크래프트 서버는 PaperMC를 사용합니다.
* Dynmap과 LuckPerms는 마인크래프트 서버 플러그인이며, PaperMC에 의존적으로 로드됩니다.

# MetaLand Accounts
MetaLand 플랫폼에서 통합 인증으로 사용되는 서버입니다.

# MetaLand Plaza
마인크래프트 메타버스 창작물을 기반으로 한 다양한 서비스가 제공되는 서버입니다.

# MetaLand Web
웹 인터페이스로 제공되며 MetaLand Accounts, MetaLand Plaza 기능을 사용할 수 있습니다.

# 1. 프로젝트 개요

## 1-1. 프로젝트 소개
![image](https://user-images.githubusercontent.com/20203944/158054197-1bf044f2-cdd9-4525-8be9-aa3aa154048f.png)

MetaLand는 마인크래프트 기반의 가상 캠퍼스 창작물을 기반으로 한 다양한 서비스를 제공하는 플랫폼입니다.

본 프로젝트는 가상 캠퍼스 창작자와 일반 유저들에게 마인크래프트 서버와 웹 사이트를 제공합니다.

# 2. 컨벤션

## 2-1. 프로젝트 명명법

본 프로젝트는 `metaland` 입니다. 아래의 규칙들로 서브 프로젝트들의 이름을 명명합니다.

* 프로젝트 이름은 모두 lowercase로
* `metaland-` 접두사를 붙인다.
* 약어가 필요한 경우 `mtl` 사용 (`metaland` -> `mtl`)

> 예시) 인증 서버 프로젝트의 이름은 `metaland-accounts`

* GitHub의 레포지토리 이름은 위의 규칙대로 생성합니다.
* 대시(`-`) 사용이 불가능한 파이썬에서는 언더스코어(`_`) 를 대신 사용합니다.
* 패키지명으로 사용하기에 너무 길다면 약어 `mtl`을 사용합니다.

> 예시) `metaland-accounts` -> `mtl_accounts`

## 2-1. Git Workflow
기능, 버그 수정, 문서 작성은 모두 별도 브랜치에서 작업하고, 이를 PR로 만들어 메인 브랜치인 `main`에 병합하는 것으로 한다.

아래 순서에 따라 작업한다.

1. 추가할 기능에 대한 이슈 생성
2. 이슈의 성격에 따라 브랜치 생성 (`feat`, `fix`, `refactor`)
3. 브랜치에서 커밋한 후 GitHub로 `push`
4. `Create Pull Request` 로 PR 생성
5. `Merge Pull Request` 로 `main` 에 병합
6. 완료된 브랜치는 삭제

> 간단한 수정 또는 리팩터링의 경우 이슈를 생성하지 않고 바로 브랜치를 만들어 작업할 수 있다.

## 2-2. 브랜치 이름 컨벤션
브랜치 이름은 cebab case로 작성하는 것을 원칙으로 한다.

* `feat/#ISSUE-feature-description`: 기능 추가 브랜치
* `fix/#ISSUE-fix-description`: 버그 수정 브랜치
* `refactor/#ISSUE-refactor-description`: 리팩터링 브랜치
* `docs/docs-description`: 문서 브랜치

> 해당되는 이슈가 없다면 #ISSUE는 생략할 수 있다.

## 2-3. 커밋 이름 컨벤션
커밋도 브랜치와 마찬가지로 성격에 따라 구분하여 `feat`, `fix`, `refactot`, `docs` 등을 붙인다.

* `feat: commit message`: 기능 추가 커밋
* `fix: commit message`: 버그 수정 커밋
* `refactor: commit message`: 리팩터링 커밋
* `docs: commit message`: 문서 커밋
* `style: commit message`: 코드 포맷팅, 세미콜론 누락, 코드 변경이 없는 경우
* `test: commit message`: 테스트 코드, 리펙토링 테스트 코드 추가
* `chore: commit message`: 빌드 업무 수정, 패키지 매니저 수정
