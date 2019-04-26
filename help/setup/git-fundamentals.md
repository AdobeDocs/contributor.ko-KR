---
title: Git 및 GitHub 설명서 핵심 사항
seo-title: Git 및 GitHub 설명서 핵심 사항
description: 이 문서에서는 Git, GitHub 리포지토리 및 내용이 구성되는 방식에 대한 개요와 Adobe 설명서에 사용되는 명명 규칙을 설명합니다.
seo-description: 이 문서에서는 Git, GitHub 리포지토리 및 내용이 구성되는 방식에 대한 개요와 Adobe 설명서에 사용되는 명명 규칙을 설명합니다.
translation-type: ht
source-git-commit: 4d8d741544e5fefe6d186e75ce4157ea127d5b16

---

# Git 및 GitHub 설명서 핵심 사항

## 개요

텍스트만 포함된 부분 변경 사항을 문서에 적용해야 하는 경우에는 이 문서의 세부 사항을 이해하지 않아도 됩니다. 이 문서에서는 새 문서 작성, 이미지 추가 또는 지속적인 Adobe 설명서 편집과 같은 주요 편집 작업을 수행하는 워크플로우에 대해 설명합니다.

Adobe 설명서 내용에 대한 기여자는 여러 가지 도구와 프로세스를 사용할 수 있습니다. 동일한 프로젝트에서 다른 기여자와 동시에 작업할 수 있으며, 정확히 동일한 내용에 대해 동시에 작업하게 될 수도 있습니다. 이러한 작업은 모두 Git 및 GitHub 소프트웨어를 통해 가능합니다.

Git은 협업이 가능한 오픈소스 버전 제어 시스템입니다. 여러 기여자가 *리포지토리*에 있는 파일에서 작업할 수 있습니다.

GitHub는 Git 저장소에 사용되는 웹 기반 호스팅 서비스로 docs.adobe.com[https://docs.adobe.com]() 콘텐츠를 저장하는 데 사용됩니다. 모든 프로젝트에 대해 GitHub는 주 리포지토리를 호스팅하며, 여기에서 기여자는 자신의 작업에 대한 복사본을 만들 수 있습니다.

## Git

Git에는 배포된 해당 모델을 지원하는 고유한 기여 워크플로우 및 용어가 있습니다. 예를 들어 일반적으로 체크아웃/체크인 작업과 연결된 파일 잠금이 없습니다. Git을 사용하면 파일을 바이트 단위로 비교하여 더욱 자세한 수준에서 변경 사항을 확인할 수 있습니다.

또한 Git은 계층화된 구조를 사용하여 프로젝트에 대한 내용을 저장하고 관리합니다.

- *저장소* - *Repo*라고도 하며 가장 높은 스토리지 단위입니다. 저장소는 하나 이상의 분기를 포함합니다.
- *분기* - 모든 저장소는 기본 분기(일반적으로 마스터라고 함)와, 마스터 분기에 다시 병합되도록 지정된 하나 이상의 분기를 포함합니다. 마스터 분기는 현재 버전으로서의 역할과 내용이 게시되는 소스의 역할을 합니다. 리포지토리의 다른 모든 분기가 생성되어 나오는 상위 분기입니다.

기여자는 Git과 상호 작용하여 로컬 수준과 GitHub 수준 모두에서 리포지토리를 업데이트하고 조작합니다.

- 로컬로 GitHub Desktop과 같은 도구를 통해
- [www.github.com](https://www.github.com)을 통해 기본 저장소로 돌아가는 기여도의 조정을 관리하기 위해 Git를 통합.

## GitHub

모든 워크플로우는 임의의 Adobe 설명서 프로젝트의 주 리포지토리가 저장되는 GitHub 수준에서 시작하고 끝납니다. 기여자가 직접 사용하기 위해 만드는 복사본은 여러 컴퓨터에 분산됩니다. 이러한 복사본은 결과적으로 적절하게 조정되어 프로젝트의 주 GitHub 리포지토리에 적용됩니다.

### 디렉토리 조직

프로젝트의 기본/마스터 분기는 프로젝트 내용의 현재 버전으로 사용됩니다. 마스터 분기 및 이 분기에서 생성된 분기의 내용은 문서 항목들의 구성에 맞추어 조정됩니다. 하위 디렉토리는 내용과 이미지 자산을 조직하는 데 사용됩니다.

주 `help` 디렉토리는 일반적으로 리포지토리의 루트와 떨어져 있습니다. 문서 디렉토리에는 하위 디렉토리들이 있습니다. 하위 디렉토리에 있는 문서는 *.md* 확장명을 사용하는 Markdown 파일로 서식이 지정됩니다.

이 디렉토리의 루트 내에서 전체 서비스 또는 제품과 관련된 일반적인 문서를 찾을 수 있습니다. 또한 일반적으로 기능/서비스 또는 일반적인 시나리오와 일치하는 또 다른 일련의 하위 디렉토리를 찾을 수 있습니다.

### 자산 디렉토리

사용자 안내서 디렉토리에는 디렉토리 내에서 참조되는 이미지 파일에 대한 `/assets` 하위 디렉토리가 있습니다.

<!---
### Markdown file template

For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`. You can use this template file as a "starter file" if you need to create a new article for submission to the repository. The file contains:

- A **metadata header** at the top of the file, delineated by two, 3-hyphen lines. It contains the various tags used for tracking information related to the article. It also includes SEO optimizations and reporting processes that Adobe uses to evaluate the performance of the content. So the metadata is important!
- Various **examples of using Markdown** to format the elements of an article.
- General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.
- Examples of **embedding video** by using an iframe.
- General **instructions on the use of docs.adobe.com extensions**, which you can use for special controls such as buttons and selectors.
-->

## 끌어오기 요청

*끌어오기 요청*을 사용하면 기여자가 기본 분기에 적용할 일련의 변경 사항을 편리하게 제안할 수 있습니다. 변경 사항(*커밋*이라고도 함)은 기여자의 분기에 저장되므로 GitHub는 먼저 이러한 변경 사항을 기본 분기에 *병합*하는 것의 영향을 모델링할 수 있습니다. 끌어오기 요청은 기여자에게 빌드/유효성 검사 프로세스, 끌어오기 요청 검토자의 피드백을 제공하고, 변경 사항이 기본 분기에 병합되기 전에 잠재적인 문제나 질문을 해결하는 메커니즘으로도 사용됩니다.

제안하려는 변경 사항의 크기에 따라 끌어오기 요청으로 기여하는 방법은 두 가지가 있습니다. 이 내용은 나중에 이 안내서의 [GitHub 워크플로우](local-repo.md) 섹션에서 자세히 다룹니다.
