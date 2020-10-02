---
lastModified: 2018-06-28T00:00:00Z
title: 설명서 작성에 Markdown을 사용하는 방법
seo-title: Adobe 설명서 작성에 Markdown을 사용하는 방법
description: 이 문서에서는 문서 작성에 사용되는 Markdown 언어에 대한 기본 사항과 참조 정보를 제공합니다.
seo-description: 이 문서에서는 Adobe 설명서용 문서 작성에 사용되는 Markdown 언어에 대한 기본 사항과 참조 정보를 제공합니다.
translation-type: tm+mt
source-git-commit: 4ebbbde3337183a19fd3a59ae091b621a092e6f8
workflow-type: tm+mt
source-wordcount: '1322'
ht-degree: 100%

---


# 기술 설명서 작성에 Markdown을 사용하는 방법

Adobe 기술 설명서 문서는 읽기 쉽고 배우기 쉬운 [Markdown](https://daringfireball.net/projects/markdown/)이라는 간단한 마크업 언어로 작성됩니다.

Adobe Docs 내용은 GitHub에 저장되므로 일반적인 형식 요구 사항에 대한 추가 기능을 제공하는 [GFM(GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/)이라는 Markdown의 버전을 사용할 수 있습니다. 또한 Adobe에서는 참고 사항, 팁 및 포함된 비디오와 같은 특정 도움말 관련 기능을 지원하기 위해 몇 가지 방법으로 Markdown을 확장했습니다.

## Markdown 기본 사항

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

<!--
To format superscript (H<sub>2</sub>O) and subscript (e=mc<sup>2</sup>) text:

```markdown
This is subscript H<sub>2</sub>O and superscript e=mc<sup>2</sup>.
```
-->

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

<!-- markdownlint-disable MD037 -->
글머리 기호 목록을 만들려면, 줄을 \* 또는 - 또는 +로 시작하되, 동일한 목록 내에서 형식들을 혼합하지 마십시오. (동일한 문서 내에서 \* 및 \+와 같은 글머리 기호 형식을 혼합하지 마십시오.)
<!-- markdownlint-disable MD037 -->

```markdown
* First item in an unordered list.
* Another item.
* Here we go again.
```

표시 -

* First item in an unordered list.
* Another item.
* Here we go again.

목록 내에 목록을 포함하고 목록 항목 사이에 내용을 추가할 수도 있습니다.

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
* [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) 웹앱
* [HTML 표를 Markdown으로 변환](https://jmalarcon.github.io/markdowntables/)

### 링크

인라인 링크의 Markdown 구문은 하이퍼링크되는 텍스트인 `[link text]` 부분과, 그다음에 나오며 연결되는 URL 또는 파일 이름인 `(file-name.md)` 부분으로 구성됩니다.

`[link text](file-name.md)`

```markdown
[Adobe](https://www.adobe.com)
```

표시 -

[Adobe](https://www.adobe.com/kr/)

리포지토리 내의 문서에 연결되는 링크(상호 참조)에 대해서는 상대 링크를 사용하십시오. ./(현재 디렉토리), ../(한 디렉토리 뒤로) 및 ../../(두 디렉토리 뒤로)와 같은 모든 상대 링크 피연산자를 사용할 수 있습니다.

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

Markdown에서는 코드 블록을 문장에서 인라인으로 배치하거나 문장 사이에 별도의 &quot;펜싱된&quot; 블록으로 배치할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [코드 블록에 대한 Markdown의 네이티브 지원](https://daringfireball.net/projects/markdown/syntax#precode)

단락 내에서 인라인 코드 스타일을 만들려면 역따옴표( \` )를 사용하십시오. 특정한 여러 줄 코드 블록을 만들려면 코드 블록(Markdown에서 &quot;펜싱된 코드 블록&quot;이라고 하고, AEM에서는 단순히 &quot;코드 블록&quot; 구성 요소라고 함)의 앞과 뒤에 세 개의 역따옴표(\`\`\`)를 추가하십시오. 펜싱된 코드 블록의 경우에는 Markdown이 코드 구문을 올바르게 강조 표시하도록 첫 번째 역따옴표 세트의 뒤에 코드 언어를 추가하십시오. 예, \`\`\`javascript

예

```markdown
This is `inline code` within a paragraph of text.
```

표시 -

This is `inline code` within a paragraph of text.

다음은 펜싱된 코드 블록입니다.

```markdown
\```javascript
function test() {
 console.log("notice the blank line before this function?");
\```
```

표시 -

```javascript
function test() {
 console.log("notice the blank line before this function?");
```

### 정의 목록

정의 목록은 AEM의 정의 목록 구성 요소를 지원하는 Markdown 확장입니다. 정의 목록은 용어와 해당 정의로 구성됩니다.

<!--

```markdown
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

Displayed:

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
--->

#### 설명 및 주석

주석(설명)은 공개 도움말 문서에는 표시되지 않습니다. 그러나 사용자가 보고 편집할 수 있는 공개 Markdown 파일에서는 주석이 표시됩니다.

## 사용자 지정 Markdown 확장

Adobe 문서는 단락, 링크, 목록, 제목 등 대부분의 문서 서식에 표준 Markdown을 사용합니다. 더 많은 서식의 경우 문서는 다음과 같은 확장된 Markdown 기능을 사용할 수 있습니다.

* 참고 블록
* 포함된 비디오
* 현지화하지 않음
* 다른 제목 ID를 제목에 지정하는 것과 같은 구성 요소 속성

참고 사항과 같은 확장된 구성 요소를 함께 연결하려면 각 줄의 맨 앞에 Markdown 블록 따옴표(>)를 사용하십시오. 구성 요소 내에 하위 구성 요소를 사용해야 하는 경우에는 해당 하위 구성 요소 섹션용으로 추가 블록 따옴표(> >)를 추가합니다. 예를 들어, DONOTLOCALIZE 섹션 내의 NOTE는 >    >로 시작해야 합니다.

제목 및 코드 블록과 같은 일부 일반적인 Markdown 요소에는 확장된 속성이 포함됩니다. 기본 속성을 변경해야 하는 경우 구성 요소 뒤에 프랑스식 중괄호 /{ /}로 매개 변수를 추가하십시오. 확장된 속성은 문맥 내에 설명되어 있습니다.

### 참고 블록

특정 내용에 주의를 집중하도록 하려면 4가지 형식의 참고 블록 중에 선택할 수 있습니다.

* `[!NOTE]`
* `[!CAUTION]`
* `[!TIP]`
* `[!IMPORTANT]`

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

포함된 비디오는 기본적으로 Markdown으로 렌더링되지는 않지만 이 Markdown 확장을 사용할 수 있습니다.

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

표시:

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

### 다음과 같음

AEM의 &quot;다음과 같음&quot;(More Like This) 구성 요소는 문서의 끝에 나타납니다. 이 구성 요소는 관련 링크를 표시합니다. 문서가 렌더링되면 미니 목차에 추가되지 않고 수준 2 제목(##)과 동일한 서식을 지정할 수 있습니다.

```markdown
>[!MORELIKETHIS]
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html)
```

표시:

>[!MORELIKETHIS]
>* [Article 1](https://helpx.adobe.com/kr/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/kr/support/audience-manager.html)


### DNL - 현지화하지 않음 - 및 UICONTROL

경우에 따라 문서 내의 특정 내용 섹션에 [영어로만] 플래그를 지정해야 합니다.
단어, 구문 및 기타 요소는 번역 시스템에 선언해야 합니다. 그리고 제어된 어휘를 관리하는 기능을 만듭니다.

현지화하지 말아야 하는 단어 또는 구문의 경우 `[!DNL]` 확장을 사용하여 단어 또는 섹션을 둘러싸십시오.

솔루션의 사용자 인터페이스와 메뉴에 있는 요소의 경우 Adobe에서는 `` 확장을 사용합니다.

**예**

[!DNL Adobe Target]에서는 [!DNL Target]-enabled 페이지에서 직접 테스트를 생성할 수 있습니다.

**소스 -**

```markdown
In [!DNL Adobe Target] you can create your tests directly on a [!DNL Target]-enabled page.
```

**예**

[!UICONTROL Visual Experience Composer]에서 [!DNL Target]을(를) 사용하여 페이지에서 직접 테스트를 만듭니다.

**소스 -**

```markdown
Use the [!UICONTROL Visual Experience Composer] in [!DNL Target] to create your test directly on a page.
```

## 과제 및 문제 해결

### 대체 텍스트

밑줄이 포함된 대체 텍스트는 올바로 렌더링되지 않습니다. 예를 들어 아래 텍스트를 사용하는 대신

```markdown
![Settings_Step_2](/assets/settings_step_2.png)
```

다음과 같은 텍스트를 사용하는 것이 좋습니다(파일 이름에서 밑줄(_) 대신 하이픈(-) 사용).

```markdown
![Settings-Step-2](/assets/settings-step-2.png)
```

### 아포스트로피 및 큰따옴표

텍스트를 Markdown 편집기에 복사하는 경우 텍스트에 &quot;스마트&quot;(둥근) 아포스트로피나 큰따옴표가 있을 수 있습니다. 이러한 기호는 인코딩하거나 기본 아포스트로피나 큰따옴표로 변경해야 합니다. 그렇지 않을 경우 파일이 게시되면 Itâ€™s와 같이 이상한 문자가 표시됩니다.

이러한 &quot;스마트&quot; 버전의 문장 부호는 다음과 같이 인코딩합니다.

* 왼쪽(열린) 큰따옴표 - `&#8220;`
* 오른쪽(닫힌) 큰따옴표 - `&#8221;`
* 오른쪽(닫힌) 작은따옴표 또는 아포스트로피 - `&#8217;`
* 왼쪽(열린) 작은따옴표(거의 사용 안 함) - `&#8216;`

### 꺾쇠 괄호

파일에서 텍스트(코드가 아님)에 꺾쇠 괄호를 사용하는 경우(예를 들어, 자리 표시자를 표시하기 위해)에는 꺾쇠 괄호를 수동으로 인코딩해야 합니다. 그렇지 않으면 Markdown에서는 해당 기호를 HTML 태그로 인식합니다.

예를 들어 `<script name>`을 다음과 같이 인코딩하십시오. `&lt;script name&gt;`

### 제목의 앰퍼샌드

앰퍼샌드(&amp;)는 제목에서 허용되지 않습니다. 대신 &quot;and&quot;(및)를 사용하거나 `&amp;` 인코딩을 사용하십시오.

## 참조 -

### Markdown 리소스

* [Markdown 소개](https://daringfireball.net/projects/markdown/syntax)
* [GitHub의 Markdown 기본 사항](https://help.github.com/articles/markdown-basics/)
