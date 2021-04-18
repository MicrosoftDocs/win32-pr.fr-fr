---
title: Élément REPEAT
description: L’élément REPEAT définit le nombre de fois où le lecteur Windows Media répète un ou plusieurs éléments ENTRy ou ENTRYREF.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- RÉPÉTER l’élément du lecteur Windows Media
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540628"
---
# <a name="repeat-element"></a><span data-ttu-id="43257-104">Élément REPEAT</span><span class="sxs-lookup"><span data-stu-id="43257-104">REPEAT Element</span></span>

<span data-ttu-id="43257-105">L’élément **REPEAT** définit le nombre de fois où le lecteur Windows Media répète un ou plusieurs éléments **entry** ou **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="43257-105">The **REPEAT** element defines the number of times Windows Media Player repeats one or more **ENTRY** or **ENTRYREF** elements.</span></span>

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a><span data-ttu-id="43257-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="43257-106">Attributes</span></span>

<span data-ttu-id="43257-107">**COUNT**</span><span class="sxs-lookup"><span data-stu-id="43257-107">**COUNT**</span></span>

<span data-ttu-id="43257-108">Entier représentant le nombre de fois où le lecteur Windows Media répète les éléments d' **entrée** et de **ENTRYREF** dans la portée de cet élément.</span><span class="sxs-lookup"><span data-stu-id="43257-108">Integer representing the number of times Windows Media Player repeats the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="43257-109">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="43257-109">Parent/Child Elements</span></span>



| <span data-ttu-id="43257-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="43257-110">Hierarchy</span></span>       | <span data-ttu-id="43257-111">Éléments</span><span class="sxs-lookup"><span data-stu-id="43257-111">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="43257-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="43257-112">Parent elements</span></span> | <span data-ttu-id="43257-113">**ASX**</span><span class="sxs-lookup"><span data-stu-id="43257-113">**ASX**</span></span>                 |
| <span data-ttu-id="43257-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="43257-114">Child elements</span></span>  | <span data-ttu-id="43257-115">**entrée**, **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="43257-115">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="43257-116">Notes</span><span class="sxs-lookup"><span data-stu-id="43257-116">Remarks</span></span>

<span data-ttu-id="43257-117">Cet élément définit le nombre de fois que le lecteur Windows Media se répète, ou effectue une boucle, sur les clips définis par les éléments **entry** et **ENTRYREF** dans la portée de cet élément.</span><span class="sxs-lookup"><span data-stu-id="43257-117">This element defines the number of times Windows Media Player repeats, or loops through, the clips defined by the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span> <span data-ttu-id="43257-118">Seul le premier élément **REPEAT** d’un métafichier est valide ; les éléments **REPEAT** suivants sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="43257-118">Only the first **REPEAT** element in a metafile is valid; subsequent **REPEAT** elements are ignored.</span></span>

<span data-ttu-id="43257-119">Si aucun attribut **Count** n’est défini, le contenu des éléments d' **entrée** et de **ENTRYREF** associés se répète un nombre infini de fois.</span><span class="sxs-lookup"><span data-stu-id="43257-119">If no **COUNT** attribute is defined, the content in the associated **ENTRY** and **ENTRYREF** elements repeats an infinite number of times.</span></span> <span data-ttu-id="43257-120">La valeur zéro amène le lecteur Windows Media à ignorer l’élément **REPEAT** et à lire le contenu une seule fois.</span><span class="sxs-lookup"><span data-stu-id="43257-120">A value of zero causes Windows Media Player to ignore the **REPEAT** element and play the content once.</span></span>

## <a name="examples"></a><span data-ttu-id="43257-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="43257-121">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="43257-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43257-122">Requirements</span></span>



| <span data-ttu-id="43257-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43257-123">Requirement</span></span> | <span data-ttu-id="43257-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="43257-124">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="43257-125">Version</span><span class="sxs-lookup"><span data-stu-id="43257-125">Version</span></span><br/> | <span data-ttu-id="43257-126">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="43257-126">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43257-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43257-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43257-128">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="43257-128">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="43257-129">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="43257-129">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





