---
title: TITLE, élément (Metafile)
description: L’élément TITLE définit une chaîne de texte spécifiant le titre d’un élément ASX ou d’un élément d’entrée.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- TITRE, élément (métafichier) lecteur Windows Media
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540618"
---
# <a name="title-element-metafile"></a><span data-ttu-id="f320c-104">TITLE, élément (Metafile)</span><span class="sxs-lookup"><span data-stu-id="f320c-104">TITLE Element (metafile)</span></span>

<span data-ttu-id="f320c-105">L’élément **title** définit une chaîne de texte spécifiant le titre d’un élément **ASX** ou d’un élément d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="f320c-105">The **TITLE** element defines a text string specifying the title for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a><span data-ttu-id="f320c-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="f320c-106">Attributes</span></span>

<span data-ttu-id="f320c-107">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="f320c-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="f320c-108">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="f320c-108">Parent/Child Elements</span></span>



| <span data-ttu-id="f320c-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="f320c-109">Hierarchy</span></span>       | <span data-ttu-id="f320c-110">Éléments</span><span class="sxs-lookup"><span data-stu-id="f320c-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="f320c-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f320c-111">Parent elements</span></span> | <span data-ttu-id="f320c-112">**ASX**, **entrée**</span><span class="sxs-lookup"><span data-stu-id="f320c-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="f320c-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f320c-113">Child elements</span></span>  | <span data-ttu-id="f320c-114">Aucune</span><span class="sxs-lookup"><span data-stu-id="f320c-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="f320c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f320c-115">Remarks</span></span>

<span data-ttu-id="f320c-116">Cet élément définit une chaîne de texte qui spécifie le titre d’un élément **ASX** ou d’un élément d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="f320c-116">This element defines a text string that specifies the title of an **ASX** or **ENTRY** element.</span></span> <span data-ttu-id="f320c-117">Le titre s’affiche dans la boîte de dialogue **Propriétés** et panneau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f320c-117">The title is displayed in the display panel and **Properties** dialog box.</span></span>

<span data-ttu-id="f320c-118">Lorsque cet élément apparaît dans un élément **ASX** , le texte est affiché sous la forme **Afficher** les informations.</span><span class="sxs-lookup"><span data-stu-id="f320c-118">When this element appears within an **ASX** element, the text is displayed as **Show** information.</span></span> <span data-ttu-id="f320c-119">Lorsque cet élément apparaît dans un élément **entry** , le texte est affiché sous forme d’informations de **clips** .</span><span class="sxs-lookup"><span data-stu-id="f320c-119">When this element appears within an **ENTRY** element, the text is displayed as **Clip** information.</span></span>

<span data-ttu-id="f320c-120">Si un élément **moreinfo** est également utilisé avec l’élément (parent) associé, il s’agit du texte du titre sur lequel l’utilisateur clique pour accéder à l’URL définie dans l’élément **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="f320c-120">If a **MOREINFO** element is also used with the associated (parent) element, it is the title text that the user clicks to access the URL defined in the **MOREINFO** element.</span></span>

<span data-ttu-id="f320c-121">Chaque **ASX** parent et élément d' **entrée** doit contenir au plus un élément **title** enfant.</span><span class="sxs-lookup"><span data-stu-id="f320c-121">Each parent **ASX** and **ENTRY** element should contain at most one child **TITLE** element.</span></span> <span data-ttu-id="f320c-122">Plusieurs éléments **titre** après le premier seront ignorés et ne seront pas affichés.</span><span class="sxs-lookup"><span data-stu-id="f320c-122">Multiple **TITLE** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="f320c-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="f320c-123">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="f320c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f320c-124">Requirements</span></span>



| <span data-ttu-id="f320c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f320c-125">Requirement</span></span> | <span data-ttu-id="f320c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f320c-126">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="f320c-127">Version</span><span class="sxs-lookup"><span data-stu-id="f320c-127">Version</span></span><br/> | <span data-ttu-id="f320c-128">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="f320c-128">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f320c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f320c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f320c-130">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f320c-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f320c-131">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f320c-131">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





