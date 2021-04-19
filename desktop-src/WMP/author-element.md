---
title: Élément AUTHOR
description: L’élément AUTHOR contient le nom de l’auteur d’un métafichier Windows Media ou d’un clip multimédia.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Élément auteur Windows Media Player
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544420"
---
# <a name="author-element"></a><span data-ttu-id="3b257-104">Élément AUTHOR</span><span class="sxs-lookup"><span data-stu-id="3b257-104">AUTHOR Element</span></span>

<span data-ttu-id="3b257-105">L’élément **Author** contient le nom de l’auteur d’un métafichier Windows Media ou d’un clip multimédia.</span><span class="sxs-lookup"><span data-stu-id="3b257-105">The **AUTHOR** element contains the name of the author of a Windows Media metafile or media clip.</span></span>

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a><span data-ttu-id="3b257-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="3b257-106">Attributes</span></span>

<span data-ttu-id="3b257-107">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="3b257-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="3b257-108">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="3b257-108">Parent/Child Elements</span></span>



| <span data-ttu-id="3b257-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="3b257-109">Hierarchy</span></span>       | <span data-ttu-id="3b257-110">Élément</span><span class="sxs-lookup"><span data-stu-id="3b257-110">Element</span></span>            |
|-----------------|--------------------|
| <span data-ttu-id="3b257-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3b257-111">Parent elements</span></span> | <span data-ttu-id="3b257-112">**ASX**, **entrée**</span><span class="sxs-lookup"><span data-stu-id="3b257-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="3b257-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3b257-113">Child elements</span></span>  | <span data-ttu-id="3b257-114">Aucune</span><span class="sxs-lookup"><span data-stu-id="3b257-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="3b257-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3b257-115">Remarks</span></span>

<span data-ttu-id="3b257-116">Cet élément contient une chaîne de texte représentant le nom de l’auteur d’un métafichier Windows Media ou d’un clip multimédia.</span><span class="sxs-lookup"><span data-stu-id="3b257-116">This element contains a text string representing the name of the author of a Windows Media metafile or media clip.</span></span> <span data-ttu-id="3b257-117">Vous pouvez utiliser l’élément **Author** au sein de l’élément **ASX** et dans les éléments d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="3b257-117">You can use the **AUTHOR** element within the **ASX** element and within **ENTRY** elements.</span></span>

<span data-ttu-id="3b257-118">Si cet élément apparaît dans l’élément **ASX** , le texte est affiché sous la forme **Afficher** les informations.</span><span class="sxs-lookup"><span data-stu-id="3b257-118">If this element appears in the **ASX** element, the text is displayed as **Show** information.</span></span>

<span data-ttu-id="3b257-119">Si cet élément apparaît dans un élément d' **entrée** , le texte est affiché en tant qu’auteur de clip.</span><span class="sxs-lookup"><span data-stu-id="3b257-119">If this element appears in an **ENTRY** element, the text is displayed as the clip author.</span></span>

<span data-ttu-id="3b257-120">Chaque **ASX** parent et élément d' **entrée** doit contenir au plus un élément **Author** enfant.</span><span class="sxs-lookup"><span data-stu-id="3b257-120">Each parent **ASX** and **ENTRY** element should contain at most one child **AUTHOR** element.</span></span> <span data-ttu-id="3b257-121">Plusieurs éléments d' **auteur** après le premier seront ignorés et ne seront pas affichés.</span><span class="sxs-lookup"><span data-stu-id="3b257-121">Multiple **AUTHOR** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="3b257-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="3b257-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="3b257-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b257-123">Requirements</span></span>



| <span data-ttu-id="3b257-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b257-124">Requirement</span></span> | <span data-ttu-id="3b257-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b257-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="3b257-126">Version</span><span class="sxs-lookup"><span data-stu-id="3b257-126">Version</span></span><br/> | <span data-ttu-id="3b257-127">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="3b257-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b257-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b257-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b257-129">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3b257-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="3b257-130">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3b257-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





