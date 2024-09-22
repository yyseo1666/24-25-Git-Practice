# 🔥 [LV200] Git을 사용한 협업의 시작

**시나리오:**
"맛집 지도" 프로젝트가 순조롭게 진행되고 있습니다! 이제 본인의 작업물을 다른 팀원들과 공유해볼까요?

## ✨ 1단계: Issue 
팀 프로젝트인만큼 서로 어떠한 작업을 할당받고 진행하는지 파악해야겠죠?

그리고 다른 팀원과의 conflict를 방지하기 위한 효율적인 PR 방법을 알아봅시다!

### 🚤 1.1 Issue가 무엇일까?
Issue(이슈)는 프로젝트 진행 시 작업의 새로 추가될 기능, 버그 수정, 리팩토링, 개선 기능 등등 모든 것들이 될 수 있습니다! 

본인이 할당한 일에 대해 이슈를 등록 후 진행합니다.

### 🚤 1.2 Issue 생성하는 두 가지 방법 - 첫번째

**Issue 탭 이용하기:**

<img width="900" alt="스크린샷 2024-09-22 오후 6 03 04" src="https://github.com/user-attachments/assets/797d8ad5-2ec2-474f-b36e-435380f49576">

위의 사진 보이시나요?
레포지토리 탭바에 Issue 탭에 들어가줍니다!

Issue 창에 들어간 후, 오른쪽 윗 부분의 `New Issue` 버튼을 클릭해봅시다!

<img width="900" alt="스크린샷 2024-09-22 오후 8 08 38" src="https://github.com/user-attachments/assets/9c11568f-89c1-4bfe-8899-50b5e1b0d2a6">

`Add a Title` 부분에는 본인이 할당한 작업의 제목을,

`Add a description` 부분에는 본인이 할당한 작업의 내용을 간단하게 작성해주시면 됩니다.

<br>

이해를 돕기 위해 제가 실제로 진행했던 프로젝트의 Issue 중 한 가지를 가져왔습니다.

<br>
<img width="900" alt="스크린샷 2024-09-22 오후 8 15 48" src="https://github.com/user-attachments/assets/249eb0c6-c380-4d83-be1c-95c84a1ea548">

<br>

**🫡 여기서 잠깐! 오른쪽을 주목하세요** 

`Assignees`: Assignee는 이 이슈를 해결할 책임이 있는, 말 그대로 담당자입니다.

`Labels`: 팀 내에서 정한 여러 Labels가 존재할 것입니다. (ex. Feat, Network, Design) 그 중 각 이슈에 맞는 Labels를 달아 주시면 됩니다.

`Projects`: 프로젝트가 있을 경우 해당 프로젝트를 선택해 주시면 됩니다. 

`Milestone`: 프로젝트의 큰 목표나 일정과 관련된 이슈들을 묶어서 관리하는 기능입니다. Label과 Assignee를 부여해도 각 기능별 서로 유사한 이슈들이 존재하기 때문에 이 기능을 이용해 이슈들을 그룹화합니다.

`Development`: 이 이슈와 연관된 브랜치 및 PR을 선택해 주시면 됩니다. 

- 브랜치 생성 방법: 원하는 브랜치 이름을 작성 + `Create branch {브랜치 이름} from main` 

  원격 저장소에서 생성한 브랜치를 로컬 저장소에 불러오는 방법!

  ```bash
  git fetch
  ```

<br>
