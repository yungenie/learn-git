# Git


# Branch
## 브랜치는 버전의 분기
<img width="452" height="333" alt="2" src="https://github.com/user-attachments/assets/2c5a0da0-b205-471d-ac2f-d7ed9e1cb555" />


### 브랜치로 버전의 분기를 관리하는 방법
1. 브랜치를 나눈다.
2. 각자의 브랜치에서 작업한다.
3. (필요하다면) 나눈 브랜치를 합친다.
<img width="644" height="401" alt="스크린샷 2025-07-29 오후 10 51 10" src="https://github.com/user-attachments/assets/1e47a883-4957-431d-8b48-744b78daf279" />

### 브랜치 Head ⭐️
- 생성되어 있는 브랜치로부터 새로운 브랜치를 생성할때 source 뿐만 아니라 기반이 되는 브랜치의 git history(git commit & merge 내역)도 가져온다.
- 만약 Head가 되는 브랜치(A)가 devleop에 merge 전 상태의 브랜치를 기반으로 새로운 브랜치(B)를 따게 되면 devleop에 PR 올릴때 반영되지 않은 source(A)까지 diff에 포함된다.
  - diff가 뜨는 이유는 A브랜치 내역이 develop에 반영이 안된 상태에서 새로운 브랜치를 땄기 때문에, 해당 시점의 history를 갖고 있어서 B브랜치의 기능만 올라가는게 아니라 A브랜치의 수정된 소스까지 포함되어 보인다.
  - 문제를 해결하기 위해서는 A브랜치를 먼저 develop에 반영을 하고나서, B브랜치는 develop을 merge해서 최신화를 받은 후 PR을 올리면 diff에 포함되지 않는다.  

# Stash
- 아직 마무리하지 않은 작업을 스택에 잠시 저장할 수 있도록 하는 기능이다.
- Souretree를 통해 UI에서 간편하게 스태시를 할 수 있음. 브랜치 별로 가능함. 
- 스태시를 하면 commit하지 않은 수정 사항을 잠시 저장하고, 수정하기 전 source로 되돌릴 수도 있다. (옵션 존재함.)
- 그 이후 수정한 내역의 소스를 다시 적용하고 싶은 경우 저장 내역(치워두기)에서 스태시 적용하면 수정한 내역으로 적용할 수 있다. (원하는 버전으로 적용 가능함)
