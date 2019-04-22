---
lastModified: 2018년 06월 28일
title: 설명서에서 링크 사용
seo-title: Adobe Git/Markdown 설명서에서 링크 사용
description: 이 문서에서는 컨텐츠 및 이미지에 대한 링크 만들기에 대한 지침을 제공합니다.
seo-description: 이 문서에서는 Adobe 설명서에 대한 컨텐츠 및 이미지에 대한 링크 만들기에 대한 지침을 제공합니다.
translation-type: tm+mt
source-git-commit: 4d8d741544e5fefe6d186e75ce4157ea127d5b16

---


# 설명서에서 링크 사용

이 문서에서는 설명서 페이지에 하이퍼링크를 사용하는 방법에 대해 설명합니다. 링크는 몇 가지 다양한 규칙을 사용하여 Markdown에 쉽게 추가할 수 있습니다. 링크는 사용자에게 동일한 페이지의 내용을 가리켜 주거나, 인접한 다른 페이지를 가리키거나, 외부 사이트 및 URL을 가리킵니다.

> [!IMPORTANT]
> 모든 링크는 Target 이 지원할 때마다 (대다수가) 항상 보안 링크`https` (vs) `http`여야 합니다.

## URL 링크

링크 텍스트에 포함되는 단어는 연결하는 페이지의 제목이거나 특정하는 설명적 텍스트여야 합니다.

**예:**

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

<!--
## Bob's link test

<table id="table_C27955F6B52A45B28BEEAAF14FFC86D8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> File Type </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .csv </span> </p> </td> 
   <td colname="col2"> <p>A comma-separated values file (such as one created in Excel). This is the file that contains the customer attribute data. See [Link TEST](/help/setup/full-workflow.md) </p> <p> <b>Naming requirements:</b> Ensure that file name extensions do not contain white spaces. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .fin </span> </p> </td> 
   <td colname="col2"> <p>(Required) The <span class="filepath"> .fin </span> file tells the system that you are finished uploading data. The name of the <span class="filepath"> .fin </span> file must match the name of the <span class="filepath"> .csv </span> file. </p> <p>Adobe recommends creating an empty text file with a <span class="filepath"> .fin </span> extension. An empty file saves space and upload time. </p> <p> <p>Note:  Renaming a <span class="filepath"> .fin </span> file is not allowed after it is uploaded. The <span class="filepath"> .fin </span> file must be uploaded separately and cannot be a renamed, previously uploaded file. </p> </p> <p>After you upload the <span class="filepath"> .fin </span> file in the customer attributes FTP, the system retrieves data quickly (within one minute). This differs from other Adobe FTP-based systems, which pick up data less frequently (around once per hour). </p> <p>The <span class="filepath"> .fin </span> file is not required when using the drag-and-drop upload method. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .gz </span> or <span class="filepath"> .zip </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> .gz </span> (gzip) or <span class="filepath"> .zip </span> - for compressed files. A <span class="filepath"> .zip </span> file cannot contain more than one file in the archive. </p> <p> <b>Naming requirements:</b> The name of the <span class="filepath"> .zip </span> or <span class="filepath"> .gz </span> should match the name of the <span class="filepath"> .csv </span>. For example, if your <span class="filepath"> .csv </span> file is <span class="filepath"> crm_small.csv </span>, the <span class="filepath"> .zip </span> file should be <span class="filepath"> crm_small.csv.zip </span>. </p> <p>The .fin file must match the .csv. </p> </td> 
  </tr> 
 </tbody> 
</table>
-->
