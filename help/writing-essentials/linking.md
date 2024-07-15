---
lastModified: 2018-06-28T00:00:00Z
title: 설명서에서 링크 사용
seo-title: Using links in Adobe Git/Markdown documentation
description: 이 문서에서는 콘텐츠 및 이미지에 대한 링크 만들기에 대한 지침을 제공합니다.
seo-description: This article provides guidance on creating links to content and images for Adobe documentation.
exl-id: f9d61aa9-931c-4654-ab21-c6e47936954e
source-git-commit: dad1df81797e6078645449501ed0661cf4bcf3ce
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 100%

---

# 설명서에서 링크 사용

이 문서에서는 설명서 페이지에 하이퍼링크를 사용하는 방법에 대해 설명합니다. 링크는 몇 가지 다양한 규칙을 사용하여 Markdown에 쉽게 추가할 수 있습니다. 링크는 사용자에게 동일한 페이지의 내용을 가리켜 주거나, 인접한 다른 페이지를 가리키거나, 외부 사이트 및 URL을 가리킵니다.

>[!IMPORTANT]
>모든 링크는 Target이 지원할 때마다 (대다수가) 항상 보안 링크(`https` vs `http`)여야 합니다.

## URL 링크

링크 텍스트에 포함되는 단어는 연결하는 페이지의 제목이거나 특정하는 설명적 텍스트여야 합니다.

**예**

- `For more information, see the [overview article](https://github.com/AdobeDocs/target.en/help/overview.md).`

- `For more details, see [Adobe Legal Concerns](https://www.adobe.com/legal).`

## 한 문서에서 다른 문서로의 링크

한 문서에서 동일한 리포지토리 내의 다른 문서에 연결하는 인라인 링크를 만들려면 다음과 같은 링크 구문을 사용하십시오.

- 디렉토리의 문서가 동일한 디렉토리에 있는 다른 문서에 연결됩니다.

  `[link text](article-name.md)`

- 문서가 하위 디렉토리에서 루트 디렉토리에 있는 문서에 연결됩니다.

  `[link text](../article-name.md)`

- 문서가 하위 디렉토리의 하위 디렉토리에서 루트 디렉토리에 있는 문서에 연결됩니다.

  `[link text](../../article-name.md)`

- 루트 디렉토리에 있는 문서가 하위 디렉토리에 있는 문서에 연결됩니다.

  `[link text](./directory/article-name.md)`

- 하위 디렉토리에 있는 문서가 다른 하위 디렉토리에 있는 문서에 연결됩니다.

  `[link text](../directory/article-name.md)`

- 하위 디렉토리의 하위 디렉토리에 있는 문서가 다른 하위 디렉토리에 있는 문서에 연결됩니다.

  `[link text](../../directory/article-name.md)`

## 앵커에 연결된 링크

앵커를 만들 필요는 없습니다. 모든 H2 제목에 대한 앵커는 게시 시 자동으로 생성됩니다. H2(##) 섹션에 연결되는 링크를 만들기만 하면 됩니다.

- 동일한 문서 내의 제목에 연결하려면

  `[link](#the-text-of-the-level2-section-separated-by-hyphens)`

  `[Link to anchors](#links-to-anchors)`

- 동일한 하위 디렉토리의 다른 문서에 있는 앵커에 연결하려면

  `[link text](article-name.md#anchor-name)`

  `[Configure your profile](overview.md#getting-started)`

- 다른 서비스 하위 디렉토리에 있는 앵커에 연결하려면

  `[link text](../directory/article-name.md#anchor-name)`

  `[Configure your profile](../overview.md#configure-your-profile)`

## 이미지에 연결된 링크

이미지와 파일을 해당 파일에 연결되는 Markdown 파일과 동일한 수준의 `assets` 디렉토리에 저장하는 것이 가장 좋습니다.

- 문서가 `assets` 하위 디렉토리에 있는 이미지에 연결됩니다.

  `![alt text](assets/image-name.png)`

- 문서가 `assets/no-localize` 하위 디렉토리에 있는 이미지에 연결됩니다.

  `![alt text](assets/no-localize/image-name.png)`
