---
title: Élément PREVIEWDURATION
description: L’élément PREVIEWDURATION définit la durée pendant laquelle un clip est lu en mode aperçu.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Élément PREVIEWDURATION lecteur Windows Media
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525181"
---
# <a name="previewduration-element"></a><span data-ttu-id="c06e9-104">Élément PREVIEWDURATION</span><span class="sxs-lookup"><span data-stu-id="c06e9-104">PREVIEWDURATION Element</span></span>

<span data-ttu-id="c06e9-105">L’élément **PREVIEWDURATION** définit la durée pendant laquelle un clip est lu en mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="c06e9-105">The **PREVIEWDURATION** element defines the length of time a clip plays in preview mode.</span></span>

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="c06e9-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="c06e9-106">Attributes</span></span>

<span data-ttu-id="c06e9-107">**Valeur** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="c06e9-107">**VALUE** (required)</span></span>

<span data-ttu-id="c06e9-108">Durée (en heures, minutes, secondes et centièmes de seconde) pendant laquelle le clip est lu en mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="c06e9-108">Length of time (in hours, minutes, seconds, and hundredths of a second) that the clip plays in preview mode.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="c06e9-109">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="c06e9-109">Parent/Child Elements</span></span>



| <span data-ttu-id="c06e9-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="c06e9-110">Hierarchy</span></span>       | <span data-ttu-id="c06e9-111">Éléments</span><span class="sxs-lookup"><span data-stu-id="c06e9-111">Elements</span></span>                    |
|-----------------|-----------------------------|
| <span data-ttu-id="c06e9-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c06e9-112">Parent elements</span></span> | <span data-ttu-id="c06e9-113">**ASX**, **entrée**, **référence**</span><span class="sxs-lookup"><span data-stu-id="c06e9-113">**ASX**, **ENTRY**, **REF**</span></span> |
| <span data-ttu-id="c06e9-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c06e9-114">Child elements</span></span>  | <span data-ttu-id="c06e9-115">Aucune</span><span class="sxs-lookup"><span data-stu-id="c06e9-115">None</span></span>                        |



 

## <a name="remarks"></a><span data-ttu-id="c06e9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c06e9-116">Remarks</span></span>

<span data-ttu-id="c06e9-117">Cet élément définit la durée pendant laquelle un clip est lu en mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="c06e9-117">This element defines the length of time that a clip plays in preview mode.</span></span> <span data-ttu-id="c06e9-118">Si cet élément apparaît dans un élément **entry** ou **ref** , il s’applique à l’élément défini par cet élément.</span><span class="sxs-lookup"><span data-stu-id="c06e9-118">If this element appears within an **ENTRY** element or a **REF** element, it applies to the clip defined by that element.</span></span> <span data-ttu-id="c06e9-119">S’il apparaît dans l’étendue d’un élément **ASX** , il s’applique à chaque clip dans le métafichier.</span><span class="sxs-lookup"><span data-stu-id="c06e9-119">If it appears within the scope of an **ASX** element, it applies to every clip in the metafile.</span></span> <span data-ttu-id="c06e9-120">Un élément **PREVIEWDURATION** dans un élément **ref** est prioritaire sur un élément dans un **élément** Entry et est prioritaire sur un élément **PREVIEWDURATION** dans un élément **ASX** .</span><span class="sxs-lookup"><span data-stu-id="c06e9-120">A **PREVIEWDURATION** element in a **REF** element takes precedence over one in an ENTRY **element**, and either takes precedence over a **PREVIEWDURATION** element in an **ASX** element.</span></span> <span data-ttu-id="c06e9-121">Si aucun élément **PREVIEWDURATION** n’est défini pour un clip, la durée d’aperçu par défaut est de 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="c06e9-121">If no **PREVIEWDURATION** element is defined for a clip, the default preview time is 10 seconds.</span></span>

<span data-ttu-id="c06e9-122">S’il existe un élément **StartTime** ou **STARTMARKER** pour le clip, le lecteur Windows Media effectue le rendu du clip en commençant par le point défini par l’un de ces éléments. Sinon, elle effectue un rendu à partir du début du clip.</span><span class="sxs-lookup"><span data-stu-id="c06e9-122">If there is a **STARTTIME** or **STARTMARKER** element for the clip, Windows Media Player renders the clip starting at the point defined by one of these elements; otherwise it renders from the beginning of the clip.</span></span> <span data-ttu-id="c06e9-123">Le clip s’arrête normalement s’il est plus petit que l’heure définie par l’élément **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="c06e9-123">The clip stops normally if it is shorter than the time defined by the **PREVIEWDURATION** element.</span></span>

<span data-ttu-id="c06e9-124">L’élément **Duration** remplace un élément **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="c06e9-124">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="c06e9-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="c06e9-125">Examples</span></span>


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="c06e9-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c06e9-126">Requirements</span></span>



| <span data-ttu-id="c06e9-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c06e9-127">Requirement</span></span> | <span data-ttu-id="c06e9-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c06e9-128">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="c06e9-129">Version</span><span class="sxs-lookup"><span data-stu-id="c06e9-129">Version</span></span><br/> | <span data-ttu-id="c06e9-130">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="c06e9-130">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c06e9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c06e9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c06e9-132">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c06e9-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="c06e9-133">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c06e9-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





