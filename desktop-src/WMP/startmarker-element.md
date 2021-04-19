---
title: Élément STARTMARKER
description: L’élément STARTMARKER spécifie un marqueur à partir duquel le lecteur Windows Media va commencer le rendu du flux.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Élément STARTMARKER lecteur Windows Media
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535340"
---
# <a name="startmarker-element"></a><span data-ttu-id="fff53-104">Élément STARTMARKER</span><span class="sxs-lookup"><span data-stu-id="fff53-104">STARTMARKER Element</span></span>

<span data-ttu-id="fff53-105">L’élément **STARTMARKER** spécifie un marqueur à partir duquel le lecteur Windows Media va commencer le rendu du flux.</span><span class="sxs-lookup"><span data-stu-id="fff53-105">The **STARTMARKER** element specifies a marker from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="fff53-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="fff53-106">Attributes</span></span>

<span data-ttu-id="fff53-107">**CERTAIN**</span><span class="sxs-lookup"><span data-stu-id="fff53-107">**NUMBER**</span></span>

<span data-ttu-id="fff53-108">Numéro d’un marqueur numérique dans l’index.</span><span class="sxs-lookup"><span data-stu-id="fff53-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="fff53-109">La valeur par défaut est le début du contenu à la demande ou la position actuelle dans un flux en temps réel.</span><span class="sxs-lookup"><span data-stu-id="fff53-109">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

<span data-ttu-id="fff53-110">**NAME**</span><span class="sxs-lookup"><span data-stu-id="fff53-110">**NAME**</span></span>

<span data-ttu-id="fff53-111">Nom d’un marqueur nommé dans l’index.</span><span class="sxs-lookup"><span data-stu-id="fff53-111">The name of a named marker in the index.</span></span> <span data-ttu-id="fff53-112">La valeur par défaut est le début du contenu à la demande ou la position actuelle dans un flux en temps réel.</span><span class="sxs-lookup"><span data-stu-id="fff53-112">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="fff53-113">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="fff53-113">Parent/Child Elements</span></span>



| <span data-ttu-id="fff53-114">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="fff53-114">Hierarchy</span></span>       | <span data-ttu-id="fff53-115">Éléments</span><span class="sxs-lookup"><span data-stu-id="fff53-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="fff53-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fff53-116">Parent elements</span></span> | <span data-ttu-id="fff53-117">**entry**, **ref**</span><span class="sxs-lookup"><span data-stu-id="fff53-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="fff53-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fff53-118">Child elements</span></span>  | <span data-ttu-id="fff53-119">Aucune</span><span class="sxs-lookup"><span data-stu-id="fff53-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="fff53-120">Notes</span><span class="sxs-lookup"><span data-stu-id="fff53-120">Remarks</span></span>

<span data-ttu-id="fff53-121">Cet élément spécifie le marqueur à partir duquel le lecteur Windows Media doit commencer le rendu du flux défini dans l' **entrée** parente ou l’élément **ref** .</span><span class="sxs-lookup"><span data-stu-id="fff53-121">This element specifies the marker from which Windows Media Player is to start rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="fff53-122">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="fff53-122">**Note**</span></span>

<span data-ttu-id="fff53-123">Utilisez cet élément avec l’attribut **Number** ou **Name** , mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="fff53-123">Use this element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="fff53-124">Un élément **STARTMARKER** défini dans un élément **ref** est prioritaire sur un élément **STARTMARKER** défini dans l’élément d' **entrée** parent de l’élément **ref** .</span><span class="sxs-lookup"><span data-stu-id="fff53-124">A **STARTMARKER** element defined within a **REF** element takes precedence over a **STARTMARKER** element defined within the **REF** element's parent **ENTRY** element.</span></span> <span data-ttu-id="fff53-125">Un élément **STARTMARKER** est également prioritaire sur un élément **StartTime** .</span><span class="sxs-lookup"><span data-stu-id="fff53-125">A **STARTMARKER** element also takes precedence over a **STARTTIME** element.</span></span>

<span data-ttu-id="fff53-126">Si le marqueur spécifié par un élément **STARTMARKER** se produit plus tard dans le flux que le marqueur défini par un élément **ENDMARKER** , aucun contenu n’est lu, mais aucune erreur n’est générée.</span><span class="sxs-lookup"><span data-stu-id="fff53-126">If the marker specified by a **STARTMARKER** element occurs later in the stream than the marker defined by an **ENDMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="fff53-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="fff53-127">Examples</span></span>


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
```



## <a name="requirements"></a><span data-ttu-id="fff53-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fff53-128">Requirements</span></span>



| <span data-ttu-id="fff53-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fff53-129">Requirement</span></span> | <span data-ttu-id="fff53-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="fff53-130">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="fff53-131">Version</span><span class="sxs-lookup"><span data-stu-id="fff53-131">Version</span></span><br/> | <span data-ttu-id="fff53-132">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="fff53-132">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fff53-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fff53-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff53-134">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fff53-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="fff53-135">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fff53-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





