---
title: 설명서 작성에 Markdown을 사용하는 방법
description: Markdown 작성의 기본 사항에 대해 알아보십시오. 문서 작성에 사용되는 Markdown 언어에 대한 참조 정보를 확인하십시오.
exl-id: 3e5726e2-139e-4e44-ae5b-8a3ae4782faf
source-git-commit: 065e43d5251f80050deef02e9c18b3fb4e9c1204
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 97%

---

# 기술 설명서 작성에 Markdown을 사용하는 방법

Adobe 기술 설명서 문서는 읽기 쉽고 배우기 쉬운 [Markdown](https://daringfireball.net/projects/markdown/)이라는 간단한 마크업 언어로 작성됩니다.

Adobe Docs 내용은 GitHub에 저장되므로 일반적인 형식 요구 사항에 대한 추가 기능을 제공하는 [GFM(GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/)이라는 Markdown의 버전을 사용할 수 있습니다. 또한 Adobe에서는 참고 사항, 팁 및 임베드된 비디오와 같은 특정 도움말 관련 기능을 지원하기 위해 몇 가지 방법으로 Markdown을 확장했습니다.

## Markdown 기본 사항

다음 섹션에서는 Markdown 작성의 기본 사항에 대해 설명합니다.

### 제목

제목을 만들려면 다음과 같이 줄의 시작 부분에 해시 표시(#)를 사용하십시오.

```
# This is level 1 (article title)
## This is level 2
### This is level 3
#### This is level 4
##### This is level 5
```

### 기본 텍스트

단락에는 Markdown으로 된 특별한 구문이 필요하지 않습니다.

텍스트 서식을 **굵게**&#x200B;로 지정하려면 두 개의 별표로 묶습니다. 텍스트 서식을 *기울임꼴*&#x200B;로 지정하려면 한 개의 별표로 묶습니다.

```markdown
   This text is **bold**.
   This text is *italic*.
   This text is both ***bold and italic***.
```

Markdown 서식 문자를 무시하려면 문자 앞에 \를 사용합니다.

```markdown
This is not \*italicized\* type.
```

### 번호 매기기 목록 및 글머리 기호 목록

번호 매기기 목록을 만들려면 줄을 `1.` 또는 `1)`로 시작하되 동일한 목록 내에서 두 형식을 함께 사용하지 마십시오. 번호를 지정할 필요는 없습니다. GitHub에서 자동으로 수행합니다.

```markdown
1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.
```

표시 -

1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.

글머리 기호 목록을 만들려면 줄을 \* 또는 - 또는 +로 시작하되, 동일한 목록 내에서 형식들을 혼합하지 마십시오. (동일한 문서 내에서 \* 및 \+와 같은 글머리 기호 형식을 혼합하지 마십시오.)

```markdown
* First item in an unordered list.
* Another item.
* Here we go again.
```

표시 -

* First item in an unordered list.
* Another item.
* Here we go again.

목록 내에 목록을 임베드하고 목록 항목 사이에 내용을 추가할 수도 있습니다.

```markdown
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)

1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |  

1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.
```

표시 -

1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)

1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |

1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.

### 표

표는 주요 Markdown 사양의 일부가 아니지만 Adobe에서는 어느 정도 지원합니다. Markdown은 셀에서 여러 줄 목록을 지원하지 않습니다. 표에서는 여러 줄을 사용하지 않는 것이 좋습니다. 파이프(|) 문자로 열과 행을 그려 표를 만들 수 있습니다. 하이픈은 각 열의 헤더를 만드는 반면 파이프는 각 열을 분리합니다. 표가 올바로 렌더링되도록 표 앞에 빈 줄을 포함하십시오.

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

표시 -

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

간단한 표는 Markdown으로 적절히 작동합니다. 그러나 셀 내에 여러 단락이나 목록을 포함하는 표는 함께 사용하기 어렵습니다. 이러한 내용의 경우 제목 및 텍스트와 같이 서로 다른 형식을 사용하는 것이 좋습니다.

표 만들기에 대한 자세한 내용은 다음을 참조하십시오.

* GitHub의 [표 구성 정보](https://help.github.com/articles/organizing-information-with-tables/)
* [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) 웹 앱
* [HTML 표를 Markdown으로 변환](https://jmalarcon.github.io/markdowntables/)

### 링크

인라인 링크의 Markdown 구문은 하이퍼링크되는 텍스트인 `[link text]` 부분과, 그다음에 나오며 연결되는 URL 또는 파일 이름인 `(file-name.md)` 부분으로 구성됩니다.

`[link text](file-name.md)`

```markdown
[Adobe](https://www.adobe.com)
```

표시 -

[Adobe](https://www.adobe.com/kr/)

저장소 내의 문서에 연결되는 링크(상호 참조)에 대해서는 상대 링크를 사용하십시오. ./(현재 디렉터리), ../(한 디렉터리 뒤로) 및 ../../(두 디렉터리 뒤로)와 같은 모든 상대 링크 피연산자를 사용할 수 있습니다.

```markdown
See [Overview example article](../../overview.md)
```

링크에 대한 자세한 내용은 링크 구문에 대한 이 안내서의 [링크](linking.md) 문서를 참조하십시오.

### 이미지

```markdown
![Adobe Logo](assets/no-localize/adobe_standard_logo.png "Hover text")
```

표시 -

![Adobe 로고](assets/no-localize/adobe_standard_logo.png "마우스로 가리키면 표시되는 텍스트")

### 코드 블록

Markdown에서는 코드 블록을 문장에서 인라인으로 배치하거나 문장 사이에 별도의 “펜싱된” 블록으로 배치할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [코드 블록에 대한 Markdown의 네이티브 지원](https://daringfireball.net/projects/markdown/syntax#precode)

백틱(`` ` ``)을 사용하여 단락 내에 인라인 코드 스타일을 만듭니다. 특정 여러 줄 코드 블록을 생성하려면 코드 블록(Markdown에서는 “펜스 코드 블록”이라고 하며 AEM에서는 “코드 블록” 구성 요소라고 함) 전후에 세 개의 백틱(` ``` `)을 추가합니다. 펜싱된 코드 블록의 경우에는 Markdown이 코드 구문을 올바르게 강조 표시하도록 첫 번째 역따옴표 세트의 뒤에 코드 언어를 추가하십시오. 예: ` ```javascript`

예:

```markdown
This is `inline code` within a paragraph of text.
```

표시 -

This is `inline code` within a paragraph of text.

다음은 펜싱된 코드 블록입니다.

```javascript
function test() {
 console.log("notice the blank line before this function?");
```

## 맞춤형 Markdown 확장 기능

Adobe 문서는 단락, 링크, 목록, 제목 등 대부분의 문서 서식에 표준 Markdown을 사용합니다. 더 많은 서식의 경우 문서는 다음과 같은 확장된 Markdown 기능을 사용할 수 있습니다.

* 참고 블록
* 임베드된 비디오
* 번역 태그
* 다른 제목 ID를 제목에 할당하고 이미지 크기를 지정하는 것과 같은 구성 요소 속성

참고 사항과 같은 확장된 구성 요소를 함께 연결하려면 각 줄의 맨 앞에 Markdown 블록 따옴표(>)를 사용하십시오.

제목 및 코드 블록과 같은 일부 일반적인 Markdown 요소에는 확장된 속성이 포함됩니다. 기본 속성을 변경해야 하는 경우 구성 요소 뒤에 프랑스식 중괄호 /{ /}로 매개변수를 추가하십시오. 확장된 속성은 문맥 내에 설명되어 있습니다.

### 참고 블록

특정 내용에 주의를 집중하도록 하려면 이 형식의 참고 블록 중에 선택할 수 있습니다.

* `[!NOTE]`
* `[!TIP]`
* `[!IMPORTANT]`
* `[!CAUTION]`
* `[!WARNING]`
* `[!ADMINISTRATION]`
* `[!AVAILABILITY]`
* `[!PREREQUISITES]`

일반적으로 참고 블록은 문맥을 끊을 수 있으므로 제한적으로 사용해야 합니다. 참고 블록에 코드 블록, 이미지, 목록, 링크를 사용할 수도 있지만 참고 블록은 간단하고 단순하게 유지하도록 하십시오.

```markdown
>[!NOTE]
>
>This is a standard NOTE block.
```

표시 -

>[!NOTE]
>
>This is a standard NOTE block.

```markdown
>[!TIP]
>
>This is a standard tip.
```

표시 -

>[!TIP]
>
>This is a standard tip.

### 비디오

임베드된 비디오는 기본적으로 Markdown으로 렌더링되지는 않지만 이 Markdown 확장 기능을 사용할 수 있습니다.

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

표시:

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

### 다음과 같음

AEM의 “다음과 같음”(More Like This) 구성 요소는 문서의 끝에 나타납니다. 이 구성 요소는 관련 링크를 표시합니다. 문서가 렌더링되면 미니 목차에 추가되지 않고 수준 2 제목(##)과 동일한 서식을 지정할 수 있습니다.

```markdown
>[!MORELIKETHIS]
>
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html)
```

표시:

>[!MORELIKETHIS]
>
>* [Article 1](https://helpx.adobe.com/kr/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/kr/support/audience-manager.html)


### UICONTROL 및 DNL

모든 Markdown 도움말 콘텐츠는 초기에 기계 번역을 사용하여 현지화됩니다. 도움말이 현지화되지 않은 경우 기계 번역을 유지합니다. 그러나 도움말 콘텐츠가 과거에 현지화된 경우 기계 번역된 콘텐츠는 사람 번역 과정의 플레이스 홀더로서 기능합니다.

**``**

기계 번역 중에 ``로 태그가 지정된 항목은 적절한 번역을 위해 현지화 데이터베이스에 대해 확인됩니다. UI가 현지화되지 않은 경우 이 태그를 사용하면 시스템에서 특정 언어에 대한 UI 참조를 영어로 남길 수 있습니다.(예: 이탈리아어로 된 Analytics 참조).

**예:**

1. **[!UICONTROL Run Process]** 화면으로 이동합니다.
1. **[!UICONTROL File > Print > Print All]**&#x200B;를 선택하여 서버의 모든 파일을 인쇄합니다.
1. [!UICONTROL Processing Rules] 대화 상자가 표시됩니다.

**소스 -**

```markdown
1. Go to the **[!UICONTROL Run Process]** screen.
1. Choose **[!UICONTROL File > Print > Print All]** to print all the files on your server.
1. The [!UICONTROL Processing Rules] dialog box appears.
```

**참고:** 세 가지 태그 지정 옵션 중 고품질을 제공하는 데 가장 중요하며 필수입니다.

**`[!DNL]`**

일반적으로 기계 번역 엔진에 영어로 무엇을 유지해야 하는지를 알리기 위해 “번역하지 않음” 목록을 사용합니다. 가장 일반적인 항목은 “Adobe Analytics”, “Adobe Campaign”, “Adobe Target”과 같은 긴 솔루션 이름입니다. 그러나 해당 용어가 특정하거나 일반적인 방법으로 사용될 수 있으므로 엔진에 영어를 사용하도록 강제해야 하는 경우가 있을 수 있습니다. 이 가장 명백한 사례는 “Analytics”, “Campaign”, “Target” 등과 같은 솔루션의 짧은 이름입니다. 이러한 이름은 일반적인 용어가 아니라 솔루션 이름이라는 것을 기계가 이해하기 어려울 것입니다. 태그는 항상 영어로 유지되는 서드파티 이름/기능이나 영어로 유지되어야 하는 문구 또는 문장과 같은 짧은 텍스트 섹션에도 사용될 수 있습니다.

**예:**

* [!DNL Target]을 사용하여 최적의 것을 찾기 위한 A/B 테스트를 만들 수 있습니다.
* Adobe Analytics는 사이트에서 분석을 수집하는 강력한 솔루션입니다. [!DNL Analytics]는 또한 해당 데이터를 쉽게 요약할 수 있도록 보고하는 데 도움이 될 수 있습니다.

**소스 -**

```markdown
* With [!DNL Target], you can create A/B tests to find the optimal 
* Adobe Analytics is a powerful solution to collect analytics on your site. [!DNL Analytics] can also help you with reporting to easily digest that data.
```

## 과제 및 문제 해결

### 대체 텍스트

밑줄이 포함된 대체 텍스트는 올바로 렌더링되지 않습니다. 예를 들어 아래 텍스트를 사용하는 대신

```markdown
![Settings_Step_2](/assets/settings_step_2.png)
```

파일 이름에서 밑줄(_) 대신 하이픈(-)을 사용하는 것이 좋습니다.

```markdown
![Settings-Step-2](/assets/settings-step-2.png)
```

### 아포스트로피 및 큰따옴표

텍스트를 Markdown 편집기에 복사하는 경우 텍스트에 “스마트”(둥근) 아포스트로피나 큰따옴표가 있을 수 있습니다. 이러한 기호는 인코딩하거나 기본 아포스트로피나 큰따옴표로 변경해야 합니다. 그렇지 않을 경우 파일이 게시되면 Itâ€™s와 같이 이상한 문자가 표시됩니다.

이러한 “스마트” 버전의 문장 부호는 다음과 같이 인코딩합니다.

* 왼쪽(열린) 큰따옴표 - `&#8220;`
* 오른쪽(닫힌) 큰따옴표 - `&#8221;`
* 오른쪽(닫힌) 작은따옴표 또는 아포스트로피 - `&#8217;`
* 왼쪽(열린) 작은따옴표(거의 사용 안 함) - `&#8216;`

### 꺾쇠 괄호

파일에서 텍스트(코드가 아님)에 꺾쇠 괄호를 사용하는 경우(예를 들어 자리 표시자를 표시하기 위해)에는 꺾쇠 괄호를 수동으로 인코딩해야 합니다. 그렇지 않으면 Markdown에서는 해당 기호를 HTML 태그로 인식합니다.

예를 들어 `<script name>`을 다음과 같이 인코딩하십시오. `&lt;script name&gt;`

### 제목의 앰퍼샌드

앰퍼샌드(&amp;)는 제목에서 허용되지 않습니다. 대신 “and”(및)를 사용하거나 `&amp;` 인코딩을 사용하십시오.

## 참조 -

### Markdown 리소스

* [Markdown 소개](https://daringfireball.net/projects/markdown/syntax)
* [GitHub의 Markdown 기본 사항](https://help.github.com/articles/markdown-basics/)
