---
title: 로컬로 Git 리포지토리 설정
description: 이 문서에서는 포크 및 복제 프로세스를 포함하여, 로컬 Git 리포지토리를 만들고 Adobe 설명서에 기여하는 지침을 제공합니다.
exl-id: 679c07a2-030b-4a30-ba14-7780f88dae11
source-git-commit: a3c283c5c0d181beacc566262743528d5ff9f7d2
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 98%

---

# 로컬로 설명서를 위한 Git 리포지토리 설정

이 문서에서는 Adobe 설명서에 기여하기 위해 로컬 컴퓨터에서 Git 리포지토리를 설정하는 절차를 설명합니다. 기여자는 로컬로 복제된 리포지토리를 사용하여 새 문서를 추가하거나, 기존 문서에 대한 주요 편집 작업을 수행하거나, 아트워크를 변경할 수 있습니다.

>[!IMPORTANT]
>부분 변경 사항만 문서에 적용하는 경우에는 이 문서의 절차를 완료하지 *않아도 됩니다*. 브라우저에서 편집 아이콘을 클릭하고 텍스트를 편집할 수 있습니다.

## 개요

Adobe 설명서에 기여하기 위해 읽기/쓰기 권한이 생기도록 적절한 리포지토리를 고유한 GitHub 계정에 포크할 수 있습니다. 그런 다음 해당 설명서 리포지토리를 복제하여 로컬에서 Markdown 파일을 만들고 편집할 수 있습니다. 그런 다음 가져오기 요청을 사용하여 변경 사항을 읽기 전용 중앙 공유 리포지토리에 병합(제출)합니다.

* 적절한 리포지토리 결정
* GitHub 계정에 리포지토리 포크
* 복제된 파일에 대한 로컬 폴더 선택
* 로컬 컴퓨터에 리포지토리 복제
* 업스트림 원격 값 구성

## 리포지토리 결정

제안된 변경 사항을 저장할 수 있는 읽기/쓰기 권한이 생기도록 적절한 리포지토리를 고유한 GitHub 계정에 포크합니다. [!UICONTROL Adobe Experience Cloud] 설명서는 [github.com](https://www.github.com/adobedocs)의 여러 저장소에 있습니다.

1. 어떤 리포지토리를 사용할지 잘 모른다면 웹 브라우저를 사용하여 해당 문서를 방문합니다. 문서의 오른쪽 상단에 있는 **편집** 링크(연필 아이콘)를 선택합니다. (편집 링크가 보이지 않는다면 해당 내용은 Github에서 아직 사용할 수 없습니다.)

Adobe 설명서에 기여하기 위해 해당 설명서 리포지토리를 복제하여 로컬에서 Markdown 파일을 만들고 편집할 수 있습니다. 그런 다음 가져오기 요청을 사용하여 변경 사항을 읽기 전용 중앙 공유 리포지토리에 병합합니다.

<!---
![GitHub Triangle](/assets/git-and-github-initial-setup.png)

If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]
-->

## 리포지토리 포크

GitHub 웹 사이트를 통해 적절한 리포지토리를 사용하여 고유한 GitHub 계정에 리포지토리 포크를 만듭니다.

모든 주 문서 리포지토리는 읽기 전용 액세스를 제공하므로 개인 포크가 필요합니다. 이것은 리포지토리의 내용을 직접 변경할 수는 없음을 의미합니다. 변경하려면 가져오기 요청(PR)을 포크에서 주 리포지토리로 제출해야 합니다. 이 프로세스를 용이하게 하려면 우선 쓰기 액세스 권한이 있는 리포지토리의 사용자 소유 복사본이 필요합니다. GitHub *포크*&#x200B;를 이 작업에 사용할 수 있습니다.

1. 주 리포지토리의 GitHub 페이지로 이동하여 오른쪽 상단의 **포크** 버튼을 클릭합니다.

   ![GitHub 포크](assets/fork-simple.png)

1. 메시지가 표시되면 포크를 만들어야 하는 대상으로 GitHub 계정 타일을 선택합니다. 이 메시지는 GitHub 계정 내에서 포크라고 하는 리포지토리의 복사본을 만듭니다.

1. 기억하고 입력하기 쉬운 폴더 이름을 선택합니다.

   일부 리포지토리는 클 수 있습니다. 사용 가능한 디스크 공간이 있는 위치를 선택하십시오.

   >[!NOTE]
   >
   >다른 Git 리포지토리 폴더 위치 안에 중첩된 로컬 폴더 경로는 선택하지 마십시오. 복제된 Git 폴더를 서로 인접하여 저장하는 것은 허용되지만 서로의 내부에 Git 폴더가 중첩되면 파일 추적 오류가 발생합니다.

## 리포지토리의 로컬 복제 생성

포크된 리포지토리를 복제하면 컴퓨터에 파일의 사본이 다운로드됩니다. 준비가 되면 로컬 드라이브에서 편집한 내용을 서버의 포크된 리포지토리에 푸시할 수 있습니다. 그런 다음 가져오기 요청을 제출하여 편집 업스트림을 주 리포지토리에 병합할 수 있습니다.

이 절차에서는 GitHub Desktop을 사용하고 있다고 가정합니다. 다른 클라이언트를 사용 중이라면 적절하게 조정하십시오.

1. **복제 또는 다운로드**&#x200B;를 클릭한 다음 **데스크탑에서 열기**&#x200B;를 선택하여 리포지토리의 사본을 현재 디렉터리에 있는 컴퓨터로 가져옵니다.

   ![저장소 복제](assets/clone-pulldown.png)

1. GitHub Desktop을 사용하여 로컬 파일을 포크된 리포지토리와 계속 동기화할 수 있습니다.

자세한 내용은 [GitHub Desktop 설명서](https://help.github.com/desktop/)를 참조하십시오.
