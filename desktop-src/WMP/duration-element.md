---
title: Élément DURATION
description: L’élément DURATION définit la durée pendant laquelle le lecteur Windows Media affiche l’entrée de playlist associée.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Élément DURATION lecteur Windows Media
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526619"
---
# <a name="duration-element"></a><span data-ttu-id="38064-104">Élément DURATION</span><span class="sxs-lookup"><span data-stu-id="38064-104">DURATION Element</span></span>

<span data-ttu-id="38064-105">L’élément **Duration** définit la durée pendant laquelle le lecteur Windows Media affiche l’entrée de playlist associée.</span><span class="sxs-lookup"><span data-stu-id="38064-105">The **DURATION** element defines the length of time Windows Media Player will render the associated playlist entry.</span></span>

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="38064-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="38064-106">Attributes</span></span>

<span data-ttu-id="38064-107">**Valeur** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="38064-107">**VALUE** (required)</span></span>

<span data-ttu-id="38064-108">Durée, en heures, minutes, secondes et centièmes de seconde, qu’une entrée est affichée par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="38064-108">The length of time, in hours, minutes, seconds, and hundredths of a second, that an entry is rendered by Windows Media Player.</span></span> <span data-ttu-id="38064-109">La valeur par défaut correspond à la longueur totale de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="38064-109">The default value is the entire length of the entry.</span></span> <span data-ttu-id="38064-110">Si l’entrée est un fichier graphique, vous devez spécifier une valeur de durée.</span><span class="sxs-lookup"><span data-stu-id="38064-110">If the entry is a graphic file, a duration value must be specified.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="38064-111">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="38064-111">Parent/Child Elements</span></span>



| <span data-ttu-id="38064-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="38064-112">Hierarchy</span></span>       | <span data-ttu-id="38064-113">Éléments</span><span class="sxs-lookup"><span data-stu-id="38064-113">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="38064-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="38064-114">Parent elements</span></span> | <span data-ttu-id="38064-115">**entry**, **ref**</span><span class="sxs-lookup"><span data-stu-id="38064-115">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="38064-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="38064-116">Child elements</span></span>  | <span data-ttu-id="38064-117">Aucune</span><span class="sxs-lookup"><span data-stu-id="38064-117">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="38064-118">Notes</span><span class="sxs-lookup"><span data-stu-id="38064-118">Remarks</span></span>

<span data-ttu-id="38064-119">Cet élément définit la durée pendant laquelle un flux doit être rendu.</span><span class="sxs-lookup"><span data-stu-id="38064-119">This element defines the length of time a stream is to be rendered.</span></span> <span data-ttu-id="38064-120">Si l’attribut de **valeur** dépasse la longueur du flux de contenu, le flux se termine à son point de terminaison normal.</span><span class="sxs-lookup"><span data-stu-id="38064-120">If the **VALUE** attribute exceeds the length of the content stream, the stream terminates at its normal end-point.</span></span>

<span data-ttu-id="38064-121">Cet élément peut apparaître dans un élément **ref** ou dans un élément **entry** .</span><span class="sxs-lookup"><span data-stu-id="38064-121">This element can appear either within a **REF** element or within an **ENTRY** element.</span></span> <span data-ttu-id="38064-122">Toutefois, un élément **Duration** défini dans un élément **ref** remplace celui qui apparaît dans l’élément d' **entrée** parent de l’élément **ref** .</span><span class="sxs-lookup"><span data-stu-id="38064-122">However, a **DURATION** element defined within a **REF** element overrides one that appears within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="38064-123">L’élément **Duration** remplace un élément **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="38064-123">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="38064-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="38064-124">Examples</span></span>


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a><span data-ttu-id="38064-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38064-125">Requirements</span></span>



| <span data-ttu-id="38064-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38064-126">Requirement</span></span> | <span data-ttu-id="38064-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="38064-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="38064-128">Version</span><span class="sxs-lookup"><span data-stu-id="38064-128">Version</span></span><br/> | <span data-ttu-id="38064-129">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="38064-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38064-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38064-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38064-131">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="38064-131">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="38064-132">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="38064-132">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





