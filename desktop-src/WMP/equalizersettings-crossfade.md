---
title: EQUALIZERSETTINGS. fondu enchaîné
description: L’attribut fondu enchaîné spécifie ou récupère une valeur indiquant si le fondu croisé est activé.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS. fondu enchaîné lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537681"
---
# <a name="equalizersettingscrossfade"></a><span data-ttu-id="55322-104">EQUALIZERSETTINGS. fondu enchaîné</span><span class="sxs-lookup"><span data-stu-id="55322-104">EQUALIZERSETTINGS.crossFade</span></span>

<span data-ttu-id="55322-105">L’attribut **fondu enchaîné** spécifie ou récupère une valeur indiquant si le fondu croisé est activé.</span><span class="sxs-lookup"><span data-stu-id="55322-105">The **crossFade** attribute specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a><span data-ttu-id="55322-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="55322-106">Possible Values</span></span>

<span data-ttu-id="55322-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="55322-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="55322-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="55322-108">Value</span></span> | <span data-ttu-id="55322-109">Description</span><span class="sxs-lookup"><span data-stu-id="55322-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="55322-110">true</span><span class="sxs-lookup"><span data-stu-id="55322-110">true</span></span>  | <span data-ttu-id="55322-111">Le fondu croisé est activé.</span><span class="sxs-lookup"><span data-stu-id="55322-111">Cross-fade is enabled.</span></span>           |
| <span data-ttu-id="55322-112">false</span><span class="sxs-lookup"><span data-stu-id="55322-112">false</span></span> | <span data-ttu-id="55322-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="55322-113">Default.</span></span> <span data-ttu-id="55322-114">Le fondu croisé est désactivé.</span><span class="sxs-lookup"><span data-stu-id="55322-114">Cross-fade is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="55322-115">Notes</span><span class="sxs-lookup"><span data-stu-id="55322-115">Remarks</span></span>

<span data-ttu-id="55322-116">La fondu enchaîné est une fonctionnalité de traitement audio qui diminue progressivement le volume d’un élément multimédia près de la fin de sa lecture tout en démarrant simultanément la lecture de l’élément multimédia suivant au niveau du volume minimum et en l’accroissant progressivement au volume normal.</span><span class="sxs-lookup"><span data-stu-id="55322-116">Cross-fade is an audio processing feature that gradually decreases the volume of one media item near the end of its playback while simultaneously starting playback of the next media item at minimum volume and gradually increasing it to normal volume.</span></span> <span data-ttu-id="55322-117">Le chevauchement entre le début du deuxième élément multimédia et la fin du premier élément multimédia est spécifié par l’attribut **crossFadeWindow** .</span><span class="sxs-lookup"><span data-stu-id="55322-117">The overlap between the start of the second media item and the end of the first media item is specified by the **crossFadeWindow** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="55322-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55322-118">Requirements</span></span>



| <span data-ttu-id="55322-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55322-119">Requirement</span></span> | <span data-ttu-id="55322-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="55322-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="55322-121">Version</span><span class="sxs-lookup"><span data-stu-id="55322-121">Version</span></span><br/> | <span data-ttu-id="55322-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="55322-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55322-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55322-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55322-124">**Élément EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="55322-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="55322-125">**EQUALIZERSETTINGS.crossFadeWindow**</span><span class="sxs-lookup"><span data-stu-id="55322-125">**EQUALIZERSETTINGS.crossFadeWindow**</span></span>](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





