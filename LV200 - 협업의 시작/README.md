# 🔥 [LV200] Git을 사용한 협업의 시작

**시나리오:**
"맛집 지도" 프로젝트가 순조롭게 진행되고 있습니다! 이제 본인의 작업물을 다른 팀원들과 공유해볼까요?

## ✨ 1단계: Issue 
팀 프로젝트인만큼 서로 어떠한 작업을 할당받고 진행하는지 파악해야겠죠?

그리고 다른 팀원과의 효율적인 협업을 위한 Issue 등록 방법을 알아봅시다!

### 🚤 1.1 Issue가 무엇일까?
Issue(이슈)는 프로젝트 진행 시 작업의 새로 추가될 기능, 버그 수정, 리팩토링, 개선 기능 등등 모든 것들이 될 수 있습니다! 

본인이 할당한 일에 대해 이슈를 등록 후 진행합니다.

### 🚤 1.2 Issue 생성하는 두 가지 방법 - 첫번째

**Issue 탭 이용하기:**

<img width="800" alt="스크린샷 2024-09-22 오후 6 03 04" src="https://github.com/user-attachments/assets/797d8ad5-2ec2-474f-b36e-435380f49576">

위의 사진 보이시나요?
레포지토리 탭바에서 Issue 탭에 들어갑니다!

Issue 창에 들어간 후, 오른쪽 윗 부분의 `New Issue` 버튼을 클릭해봅시다!

<img width="800" alt="스크린샷 2024-09-22 오후 8 08 38" src="https://github.com/user-attachments/assets/9c11568f-89c1-4bfe-8899-50b5e1b0d2a6">

`Add a Title` 부분에는 본인이 할당한 작업의 제목을,

`Add a description` 부분에는 본인이 할당한 작업의 내용을 간단하게 작성해주시면 됩니다.

<br>

이해를 돕기 위해 제가 실제로 진행했던 프로젝트의 Issue 중 한 가지를 가져왔습니다.

<br>
<img width="800" alt="스크린샷 2024-09-22 오후 8 15 48" src="https://github.com/user-attachments/assets/249eb0c6-c380-4d83-be1c-95c84a1ea548">

<br>

**🫡 여기서 잠깐! 오른쪽을 주목하세요** 

`Assignees`: Assignee는 이 이슈를 해결할 책임이 있는, 말 그대로 담당자입니다.

`Labels`: 팀 내에서 정한 여러 Labels가 존재할 것입니다. (ex. Feat, Bug / Feat는 새로운 기능 개발, Bug는 버그 수정을 의미합니다.) 그 중 각 이슈에 맞는 Label를 달아 주시면 됩니다.

Ex)

<img width="800" alt="스크린샷 2024-10-02 오후 4 32 08" src="https://github.com/user-attachments/assets/88fa4089-28dd-4609-89d0-4465e87ec9a7">

`Projects`: 프로젝트가 있을 경우 해당 프로젝트를 선택해 주시면 됩니다. 

`Milestone`: 프로젝트의 큰 목표나 일정과 관련된 이슈들을 묶어서 관리하는 기능입니다. Label과 Assignee를 부여해도 각 기능별 서로 유사한 이슈들이 존재하기 때문에 이 기능을 이용해 이슈들을 그룹화합니다.

`Development`: 이 이슈와 연관된 브랜치 및 PR을 선택해 주시면 됩니다. 

- 브랜치 생성 방법: 원하는 브랜치 이름을 작성 + `Create branch {브랜치 이름} from main` 

  원격 저장소에서 생성한 브랜치를 로컬 저장소에 불러오는 방법!

  ```bash
  git fetch
  ```

<br>

### 🚤 1.3 Issue 닫기
처음 Issue를 생성하셨다면 `Open` 되어있을텐데요,

<img width="800" alt="스크린샷 2024-09-22 오후 9 00 07" src="https://github.com/user-attachments/assets/2e691152-15c8-4a74-9711-3c9451ec4104">

아래 `Close Issue` 버튼을 통해 `Close`로 상태를 변경해주시면 됩니다.

성공적으로 merge 되었거나, 작업이 완료되었을 때 이슈를 닫습니다. 

닫은 Issue들은 따로 보관되고, 혹시 실수로 닫았을 경우에도 다시 `Open` 상태로 변경할 수 있습니다!

<br>

## ✨ 2단계: PR
다음으로는 다른 팀원과의 conflict를 방지하기 위한 효율적인 PR 방법을 알아봅시다!

### 🚤 2.1 PR(Pull Request)은 무엇일까?

PR(Pull Request)은 **브랜치에서 작업한 내용을 다른 브랜치로 Merge 하기 위한 요청입니다.**  

프로젝트 진행 시 할당된 작업을 새로운 브랜치를 생성해서 작업한 후 Main 브랜치에 반영하기 전, 다른 팀원들에게 리뷰를 요청하는 과정에서 사용됩니다. 

PR을 통해 다른 팀원들에게 코드 리뷰를 받고 conflict를 미리 방지할 수 있습니다!

### 🚤 2.2 PR(Pull Request) 과정

PR 과정을 알아볼까요?

1. 로컬 브랜치 작업: 새로운 작업을 위한 브랜치를 생성하고 로컬에서 작업을 완료합니다.

2. Commit & Push: 작업이 끝난 후 변경 사항을 커밋하고 푸시합니다.

3. PR 생성: 상단 탭의 Issue 옆에 있는 Pull Request를 열어 다른 대상 브랜치에(ex. main 브랜치) 작업 내용을 merge 할 수 있도록 요청합니다.

4. Review: 팀원들이 PR을 통해 코드리뷰나 변경사항에 대해 코멘트를 달며 리뷰를 진행합니다.

5. Merge: 리뷰가 완료되고 다른 팀원들의 승인이나 동의가 있을 경우 PR을 merge 시킵니다. merge 후에는 작업한 브랜치를 삭제할 수 있습니다.

6. 이슈 닫기: 이슈를 등록하였을 경우 이슈도 Close 상태로 바꾸어줍니다.

### 🚤 1.2 PR(Pull Request) 템플릿

PR 템플릿이란?

PR을 생성할 때 프로젝트 팀원들이 따르는 일관된 양식입니다.

보통 프로젝트 개발 시작 전 PR 템플릿 논의 후 동일한 템플릿을 사용해 PR을 날립니다!

템플릿은 다양하기에 자유롭게 정하셔도 괜찮습니다. 보통 PR 템플릿에는 작업한 내용, 변경 사항, 테스트 방법 등이 포함됩니다!

이해를 돕기 위해 제가 실제로 진행했던 프로젝트의 PR 중 한 가지를 가져왔습니다. (위에서 보여드린 Issue에 대한 PR입니다!)

이런식으로 PR 내용을 적어주시면 됩니다.

<br>

<img width="800" alt="스크린샷 2024-09-22 오후 9 14 45" src="https://github.com/user-attachments/assets/23916b91-2d75-4b69-b04e-bed93669972b">

<hr>

다음은 PR 템플릿 예시입니다!

<br>

```bash
## What is this PR? 👀
PR 개요 및 내용을 적어주세요.
<br><br/>

## Changes 📃
변경 사항을 적어주세요.
<br><br/>

## Screenshot (optional) 📷
스크린샷이 있다면 첨부해주세요.
<br><br/>

## Additional & Attention points(optional) 🔥
주의할 점이나 리뷰어가 집중해서 봐야하는 부분이 있다면 작성해주세요.
<br><br/>
```

<br>

## ✨ 3단계: Commit Message Convention
다음으로 깃허브 협업 시 커밋 메시지를 더욱 효율적이게 사용하는 방법을 알아볼까요?

### 🚤 3.1 Commit Message Convention은 무엇일까?

Commit Message Convention 이란?

Git을 사용하여 협업할 때에 프로젝트 참여자들이 통일된 커밋 메시지 양식을 지켜 작성하기 위한 일종의 규칙입니다.

일반적으로 관습적인 Commit Message Convention이 있지만, 프로젝트마다 바꾸어서 사용하기도 합니다!

### 🚤 3.2 Commit Message Convention의 중요성

그럼 이러한 규칙이 왜 중요할까요?

Commit Message는 코드의 변경 사항을 요약하여 한 눈에 알아볼수 있게 하는 역할을 합니다.

이 때 프로젝트 참여자마다 각기 다른 방식으로 커밋 메시지를 작성하게 되면 가독성이 떨어지고, 효율적인 프로젝트 관리와 협업이 어렵습니다.

따라서 일관된 커밋 메시지를 사용하여 가독성 및 커뮤니케이션의 효율성을 높일 수 있습니다!

### 🚤 3.3 Commit Message Convention 기본 양식
- 기본 포맷
```bash
<type>(optional: scope): <subject>

// feat(login): 로그인 기능 추가

<body>

// 이 커밋은 로그인 기능을 구현했습니다

<footer> #Issue number

// Closes #45
```

1) 타입(Type)
타입은 이 커밋이 어떤 종류의 작업을 했는지를 나타냅니다. 아래는 Commit Type의 예시입니다.

`feat`: 새로운 기능 추가

`fix`: 버그 수정

`docs`: 문서 관련 변경

`refactor`: 코드 리팩토링 

`test`: 테스트 추가 또는 수정

2) 스코프(Scope) (옵션)
스코프는 변경된 부분의 모듈이나 기능을 명시하는 선택적 요소입니다.

예를 들어 login, api 등 구체적인 내용을 표시할 수 있습니다.

4) 제목(Subject)
제목은 커밋의 핵심 내용을 요약하는 부분입니다.

👻 하지만! 일반적으로는 <type>: <subject>의 형식으로만 간단하게 작성합니다.

```bash
<type>: <subject>  // feat: 로그인 기능 추가
```

### 🚤 3.4 Gitmoji 

커밋 메시지 type을 글자로 작성하지 않고 Gitmoji를 사용하는 경우도 있습니다.

깃모지(Gitmoji)는 깃 커밋 메시지에 이모지를 사용하여 커밋의 목적을 직관적으로 표현하는 방식입니다. 

이해를 돕기 위해 제가 실제로 진행했던 프로젝트의 커밋 메시지들을 가져왔습니다.

<img width="800" alt="스크린샷 2024-09-27 오후 3 23 49" src="https://github.com/user-attachments/assets/cd3b0525-181c-4869-b7de-03e43e5fbade">

<hr>

참고 사이트 첨부해놓을테니 한 번 둘러보시면 좋습니다!

https://gitmoji-js.netlify.app/

<br>
