---
title: Élément ENDMARKER
description: L’élément ENDMARKER spécifie un marqueur auquel le lecteur Windows Media cesse de restituer le flux.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Élément ENDMARKER lecteur Windows Media
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544369"
---
# <a name="endmarker-element"></a><span data-ttu-id="d7e85-104">Élément ENDMARKER</span><span class="sxs-lookup"><span data-stu-id="d7e85-104">ENDMARKER Element</span></span>

<span data-ttu-id="d7e85-105">L’élément **ENDMARKER** spécifie un marqueur auquel le lecteur Windows Media cesse de restituer le flux.</span><span class="sxs-lookup"><span data-stu-id="d7e85-105">The **ENDMARKER** element specifies a marker at which Windows Media Player will stop rendering the stream.</span></span>

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="d7e85-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="d7e85-106">Attributes</span></span>

<span data-ttu-id="d7e85-107">**CERTAIN**</span><span class="sxs-lookup"><span data-stu-id="d7e85-107">**NUMBER**</span></span>

<span data-ttu-id="d7e85-108">Numéro d’un marqueur numérique dans l’index.</span><span class="sxs-lookup"><span data-stu-id="d7e85-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="d7e85-109">La valeur par défaut est la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="d7e85-109">The default value is the end of the content.</span></span>

<span data-ttu-id="d7e85-110">**NAME**</span><span class="sxs-lookup"><span data-stu-id="d7e85-110">**NAME**</span></span>

<span data-ttu-id="d7e85-111">Nom d’un marqueur nommé dans l’index.</span><span class="sxs-lookup"><span data-stu-id="d7e85-111">The name of a named marker in the index.</span></span> <span data-ttu-id="d7e85-112">La valeur par défaut est la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="d7e85-112">The default value is the end of the content.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="d7e85-113">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="d7e85-113">Parent/Child Elements</span></span>



| <span data-ttu-id="d7e85-114">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="d7e85-114">Hierarchy</span></span>       | <span data-ttu-id="d7e85-115">Éléments</span><span class="sxs-lookup"><span data-stu-id="d7e85-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="d7e85-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d7e85-116">Parent elements</span></span> | <span data-ttu-id="d7e85-117">**entry**, **ref**</span><span class="sxs-lookup"><span data-stu-id="d7e85-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="d7e85-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d7e85-118">Child elements</span></span>  | <span data-ttu-id="d7e85-119">Aucune</span><span class="sxs-lookup"><span data-stu-id="d7e85-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="d7e85-120">Notes</span><span class="sxs-lookup"><span data-stu-id="d7e85-120">Remarks</span></span>

<span data-ttu-id="d7e85-121">Cet élément spécifie le marqueur dans lequel le lecteur Windows Media doit arrêter le rendu du flux défini dans l’élément d' **entrée** ou de **référence** parent.</span><span class="sxs-lookup"><span data-stu-id="d7e85-121">This element specifies the marker where Windows Media Player is to stop rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="d7e85-122">Remarque</span><span class="sxs-lookup"><span data-stu-id="d7e85-122">Note</span></span>

<span data-ttu-id="d7e85-123">Utilisez l’élément **ENDMARKER** avec l’attribut **Number** ou **Name** , mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="d7e85-123">Use the **ENDMARKER** element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="d7e85-124">En mode aperçu, le fait d’atteindre un marqueur de fin arrête l’aperçu, même si l’heure spécifiée par l’élément **PREVIEWDURATION** n’est pas écoulée.</span><span class="sxs-lookup"><span data-stu-id="d7e85-124">In preview mode, reaching an end marker stops the preview, even if the time specified by the **PREVIEWDURATION** element has not elapsed.</span></span> <span data-ttu-id="d7e85-125">L’élément **ENDMARKER** est également prioritaire sur l’élément **Duration** .</span><span class="sxs-lookup"><span data-stu-id="d7e85-125">The **ENDMARKER** element also takes precedence over the **DURATION** element.</span></span>

<span data-ttu-id="d7e85-126">Un élément **ENDMARKER** défini dans un élément **ref** est prioritaire sur un **ENDMARKER** défini dans l’élément d' **entrée** parent de l’élément **ref** .</span><span class="sxs-lookup"><span data-stu-id="d7e85-126">An **ENDMARKER** element defined within a **REF** element takes precedence over an **ENDMARKER** defined within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="d7e85-127">Si le marqueur spécifié par un élément **ENDMARKER** se produit plus tôt dans le flux que le marqueur défini par un élément **STARTMARKER** , aucun contenu n’est lu, mais aucune erreur n’est générée.</span><span class="sxs-lookup"><span data-stu-id="d7e85-127">If the marker specified by an **ENDMARKER** element occurs earlier in the stream than the marker defined by a **STARTMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="d7e85-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="d7e85-128">Examples</span></span>


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

```



## <a name="requirements"></a><span data-ttu-id="d7e85-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7e85-129">Requirements</span></span>



| <span data-ttu-id="d7e85-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7e85-130">Requirement</span></span> | <span data-ttu-id="d7e85-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7e85-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="d7e85-132">Version</span><span class="sxs-lookup"><span data-stu-id="d7e85-132">Version</span></span><br/> | <span data-ttu-id="d7e85-133">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="d7e85-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7e85-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7e85-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7e85-135">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d7e85-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d7e85-136">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d7e85-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





