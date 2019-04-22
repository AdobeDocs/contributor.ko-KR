---
title: Adobe 설명서에 대한 기여자 안내서
seo-title: Adobe Experience Cloud 기술 설명서에 대한 기고자 가이드 개요
description: 이 안내서에서는 Adobe 설명서 사이트에 제안과 추가 사항을 제공하는 방법에 대해 설명합니다.
seo-description: 이 안내서에서는 [!UICONTROL Adobe Experience Cloud] 기술 설명서에 기여할 수 있는 방법에
  대해 설명합니다.
translation-type: tm+mt
source-git-commit: 4d8d741544e5fefe6d186e75ce4157ea127d5b16

---


# Adobe 설명서에 대한 기고자 가이드 개요

## 공동 작업 문서 소개

2019 년 Adobe Experience Cloud에 대한 기술 문서 및 역량 강화 컨텐츠는 Adobe Experience Manager, Analytics, Launch 및 Target를 비롯한 Github, Markdown 및 Adobe Experience Cloud 솔루션을 활용하여 오픈 소스 원칙을 기반으로 한 새로운 플랫폼으로 전환하고 있습니다.

이 오픈 소스 모델은 컨텐츠 품질을 향상시키고 고객, 설명서 팀 및 제품 팀 간의 커뮤니케이션을 향상시켜줍니다. 모든 페이지에서 컨텐츠 유용성을 평가하고, 문제를 기록하며, 컨텐츠 제안을 Git 풀 요청 (PRS) 로 제공할 수 있습니다. Adobe 설명서 팀은 매일 기여 및 문제를 모니터링하고 필요에 따라 업데이트, 수정 및 조정을 수행합니다.

## 협업 설명서 작업

이 자료의 사용자인 경우 - 직원, 파트너, 고객 또는 잠재 고객인 경우와 상관없이, 귀하는 몇 가지 간단한 방법으로 이 문서에 기여 선택할 수 있습니다.

* 페이지의 유용성 평가
* 특정 페이지에 대한 문제 기록
* 에셋 및 코드 샘플이 포함된 전체 아티클을 작성하여 전체 아티클을 작성해 보세요.

이 안내서에서는 이 자료 세트에 상호 작용하고 기여할 수 있는 방법을 개괄적으로 설명합니다.

<!--
> [!IMPORTANT]
> All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](../code-of-conduct.md) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Contributing](../contributing.md) article.
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [Adobe Documentation Terms of Use](https://www.adobe.com/legal/terms.html). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.
--->

## 기존 문서의 빠른 편집

빠른 편집은 문서의 사소한 오류와 누락을 수정하는 좋은 방법입니다. 문서에 아래와 같이 [편집] 단추가 표시되는 경우 직접 빠른 수정 작업을 할 수 있습니다. 문서를 편집할 때, 끌어오기 요청(PR)을 제출하여 수정/제안을 Adobe에 제출하십시오. 그러면 Adobe에서 제안을 조사하고, 승인하고, 게시할 수 있습니다.

1. 수락 가능한 경우 [Contributor License Agreement (CLA)](http://opensource.adobe.com/cla.html) 에 서명합니다.

   Adobe CLA를 한 번만 제출하면 됩니다.
1. 오른쪽 열의 **을 클릭하여 GitHub의 Markdown 소스 파일로 이동합니다.`Edit this page`**
1. 연필 아이콘을 클릭하여 아티클을 편집합니다.

   > [!NOTE]
   > 연필 아이콘이 회색으로 표시된다면 GitHub 계정에 로그인하거나 새 계정을 만들어야 합니다.

   ![연필 아이콘 위치](assets/edit-icon.png)

1. 웹 편집기에서 변경 작업을 수행합니다. **변경 내용 미리 보기** 탭을 클릭하여 변경 내용의 서식을 확인할 수 있습니다.
1. 변경 작업을 수행한 후 페이지 하단으로 스크롤합니다. 다음 그림과 같이 PR의 제목과 설명을 입력하고 **파일 변경 제안**을 클릭합니다.

   ![변경 제안](assets/submit-pull-request.png)

   >[!NOTE] Contributor License Agreement (CLA) 에 서명하는 데 대한 확인 오류 메시지가 표시되면 **세부** 정보를 클릭하여 사용권 계약을 엽니다. 수락 가능한 경우 계약서에 서명합니다. 그런 다음 가져오기 요청을 닫았다가 열고 계속합니다.

이게 전부입니다. 감사합니다. 설명서 팀 멤버가 끌어오기 요청을 검토하고 병합하게 됩니다.

## 문제 기록

한 내용에 있는 문제에 대해 Adobe에 알리는 또 다른 간단한 방법은 '문제를 기록'하는 것입니다.

1. 한 내용에 문제가 있는 것을 발견하면 페이지의 오른쪽 하단에 있는 `Log an Issue` 링크를 클릭합니다. 아래 그림을 참조하십시오.

   ![](assets/git_log_issue.png)

   > [!NOTE]
   > 문제를 기록하려면 GitHub 계정에 로그인하거나 새 계정을 만들어야 합니다.

   이 링크를 클릭하면 Github 문제 인터페이스를 사용하여 Adobe에 빠른 티켓을 기록할 수 있습니다.

1. 문제가 있는 페이지의 URL은 설명 필드에 자동으로 채워집니다. 제목을 입력하고 문제에 대한 간단한 설명을 작성한 다음 *새 문제 제출*을 클릭합니다.

   ![](assets/git_issue_example.png)

발행물을 제출하면 이 페이지에 대해 작업을 수행할 수 있는 컨텐츠 팀에 직접 알립니다. Adobe는 내용을 업데이트하면 Github 문제 인터페이스로 사용자에게 알리게 되며, 업데이트 또는 종료되면 이 인터페이스에서 이메일로 사용자에게 알려줍니다.

## GitHub 권한 이해

Github 편집 UI는 리포지토리 권한에 맞게 조정됩니다. 대상 리포지토리에 대한 쓰기 권한이 없는 기여자의 경우 이전 이미지가 정확합니다. GitHub는 해당 계정의 대상 리포지토리의 포크를 자동으로 만듭니다. 대상 리포지토리에 대한 쓰기 권한이 있는 경우 GitHub는 대상 리포지토리에 새 분기를 만듭니다.

Adobe는 쓰기 권한이 있는 기여자의 경우에도 모든 변경 내용에 대해 끌어오기 요청을 사용합니다. 대부분의 리포지토리에는 보호되는 `master` 분기가 있으므로 업데이트는 끌어오기 요청으로 제출되어야 합니다.

브라우저 내 편집 환경은 변경 내용이 적거나 자주 변경하지 않는 경우 적합합니다. 크게 기여하거나 고급 Git 기능을 사용하는 경우 [리포지토리를 포크하고 로컬에서 작업](setup/full-workflow.md)해야 합니다.

## 피드백 제공

Adobe의 솔루션만큼 큰 솔루션 세트를 사용할 때 설명서는 항상 진행 중인 작업입니다. 오류를 발견하면 문제를 기록하고, 자료에 대한 제안이 있으면 알려주십시오. 찾고 있었던 정보를 알려주십시오. 필요한 내용을 찾을 수 없으면 알려주십시오. 작업을 완료하는 데 어려움이 있다면 해결책 학습을 도와드릴 방법을 알려주십시오.

[!UICONTROL Adobe Experience Cloud]의 협업 설명서 팀과 모든 작가, 내용 생산자의 감사를 전합니다.
