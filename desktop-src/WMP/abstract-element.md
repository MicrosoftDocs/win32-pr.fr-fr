---
title: ABSTRACT, élément
description: L’élément ABSTRACT contient du texte qui décrit l’élément ASX, BANNER ou ENTRy associé.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Élément abstrait lecteur Windows Media
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540595"
---
# <a name="abstract-element"></a><span data-ttu-id="7226d-104">ABSTRACT, élément</span><span class="sxs-lookup"><span data-stu-id="7226d-104">ABSTRACT Element</span></span>

<span data-ttu-id="7226d-105">L’élément **abstract** contient du texte qui décrit l’élément **ASX**, **Banner** ou **entry** associé.</span><span class="sxs-lookup"><span data-stu-id="7226d-105">The **ABSTRACT** element contains text that describes the associated **ASX**, **BANNER**, or **ENTRY** element.</span></span>

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a><span data-ttu-id="7226d-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="7226d-106">Attributes</span></span>

<span data-ttu-id="7226d-107">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="7226d-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="7226d-108">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="7226d-108">Parent/Child Elements</span></span>



| <span data-ttu-id="7226d-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="7226d-109">Hierarchy</span></span> | <span data-ttu-id="7226d-110">Éléments</span><span class="sxs-lookup"><span data-stu-id="7226d-110">Elements</span></span>                       |
|-----------|--------------------------------|
| <span data-ttu-id="7226d-111">Parent</span><span class="sxs-lookup"><span data-stu-id="7226d-111">Parent</span></span>    | <span data-ttu-id="7226d-112">**ASX**, **entrée**, **bannière**</span><span class="sxs-lookup"><span data-stu-id="7226d-112">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="7226d-113">Enfant</span><span class="sxs-lookup"><span data-stu-id="7226d-113">Child</span></span>     | <span data-ttu-id="7226d-114">Aucune</span><span class="sxs-lookup"><span data-stu-id="7226d-114">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="7226d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7226d-115">Remarks</span></span>

<span data-ttu-id="7226d-116">Si cet élément apparaît dans un élément **ASX** , le texte s’affiche sous la forme d’une info-bulle lorsque la souris pointe sur le titre de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="7226d-116">If this element appears within an **ASX** element, the text displays as a ToolTip when the mouse hovers over the show title.</span></span>

<span data-ttu-id="7226d-117">Si cet élément apparaît dans un élément d' **entrée** , le texte s’affiche sous la forme d’une info-bulle lorsque la souris pointe sur le titre du clip.</span><span class="sxs-lookup"><span data-stu-id="7226d-117">If this element appears within an **ENTRY** element, the text displays as a ToolTip when the mouse hovers over the clip title.</span></span>

<span data-ttu-id="7226d-118">Si cet élément apparaît dans un élément de **bannière** , le texte s’affiche sous la forme d’une info-bulle pour le graphique de bannière.</span><span class="sxs-lookup"><span data-stu-id="7226d-118">If this element appears within a **BANNER** element, the text displays as a ToolTip for the banner graphic.</span></span>

<span data-ttu-id="7226d-119">Utilisez un seul élément **abstrait** par portée.</span><span class="sxs-lookup"><span data-stu-id="7226d-119">Use only one **ABSTRACT** element per scope.</span></span> <span data-ttu-id="7226d-120">Seul le premier élément **abstrait** au sein de la portée d’un autre élément est utilisé lors du traitement d’un fichier de métafichier.</span><span class="sxs-lookup"><span data-stu-id="7226d-120">Only the first **ABSTRACT** element within the scope of another element is used when a metafile file is processed.</span></span> <span data-ttu-id="7226d-121">Tous les éléments **abstraits** suivants dans cette portée sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="7226d-121">Any subsequent **ABSTRACT** elements in that scope are ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="7226d-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="7226d-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="7226d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7226d-123">Requirements</span></span>



| <span data-ttu-id="7226d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7226d-124">Requirement</span></span> | <span data-ttu-id="7226d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7226d-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="7226d-126">Version</span><span class="sxs-lookup"><span data-stu-id="7226d-126">Version</span></span><br/> | <span data-ttu-id="7226d-127">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="7226d-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7226d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7226d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7226d-129">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7226d-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="7226d-130">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7226d-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





