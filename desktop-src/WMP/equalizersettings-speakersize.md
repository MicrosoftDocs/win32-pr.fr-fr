---
title: EQUALIZERSETTINGS. Speaker
description: L’attribut Speaker spécifie ou récupère le numéro d’index de la taille actuelle de l’intervenant.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS. Speakers Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532839"
---
# <a name="equalizersettingsspeakersize"></a><span data-ttu-id="2572d-104">EQUALIZERSETTINGS. Speaker</span><span class="sxs-lookup"><span data-stu-id="2572d-104">EQUALIZERSETTINGS.speakerSize</span></span>

<span data-ttu-id="2572d-105">L’attribut **Speaker** spécifie ou récupère le numéro d’index de la taille actuelle de l’intervenant.</span><span class="sxs-lookup"><span data-stu-id="2572d-105">The **speakerSize** attribute specifies or retrieves the index number of the current speaker size.</span></span>

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a><span data-ttu-id="2572d-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="2572d-106">Possible Values</span></span>

<span data-ttu-id="2572d-107">Cet attribut est un **nombre** en lecture/écriture (long) contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2572d-107">This attribute is a read/write **Number** (long) containing one of the following values.</span></span>



| <span data-ttu-id="2572d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="2572d-108">Value</span></span> | <span data-ttu-id="2572d-109">Description</span><span class="sxs-lookup"><span data-stu-id="2572d-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="2572d-110">0</span><span class="sxs-lookup"><span data-stu-id="2572d-110">0</span></span>     | <span data-ttu-id="2572d-111">Les haut-parleurs actuels sont des casques.</span><span class="sxs-lookup"><span data-stu-id="2572d-111">The current speakers are headphones.</span></span>     |
| <span data-ttu-id="2572d-112">1</span><span class="sxs-lookup"><span data-stu-id="2572d-112">1</span></span>     | <span data-ttu-id="2572d-113">Les haut-parleurs actuels sont de taille normale.</span><span class="sxs-lookup"><span data-stu-id="2572d-113">The current speakers are of normal size.</span></span> |
| <span data-ttu-id="2572d-114">2</span><span class="sxs-lookup"><span data-stu-id="2572d-114">2</span></span>     | <span data-ttu-id="2572d-115">Les haut-parleurs actuels sont volumineux.</span><span class="sxs-lookup"><span data-stu-id="2572d-115">The current speakers are large.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="2572d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2572d-116">Remarks</span></span>

<span data-ttu-id="2572d-117">Le nom convivial de la taille de l’orateur peut être récupéré à l’aide de l’attribut **currentSpeakerName** .</span><span class="sxs-lookup"><span data-stu-id="2572d-117">The friendly name of the speaker size can be retrieved using the **currentSpeakerName** attribute.</span></span>

<span data-ttu-id="2572d-118">Cet attribut est ignoré si **enhancedAudio** est défini sur false.</span><span class="sxs-lookup"><span data-stu-id="2572d-118">This attribute is ignored if **enhancedAudio** is set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="2572d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2572d-119">Requirements</span></span>



| <span data-ttu-id="2572d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2572d-120">Requirement</span></span> | <span data-ttu-id="2572d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2572d-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="2572d-122">Version</span><span class="sxs-lookup"><span data-stu-id="2572d-122">Version</span></span><br/> | <span data-ttu-id="2572d-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2572d-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2572d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2572d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2572d-125">**Élément EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="2572d-125">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="2572d-126">**EQUALIZERSETTINGS.currentSpeakerName**</span><span class="sxs-lookup"><span data-stu-id="2572d-126">**EQUALIZERSETTINGS.currentSpeakerName**</span></span>](equalizersettings-currentspeakername.md)
</dt> <dt>

[<span data-ttu-id="2572d-127">**EQUALIZERSETTINGS.enhancedAudio**</span><span class="sxs-lookup"><span data-stu-id="2572d-127">**EQUALIZERSETTINGS.enhancedAudio**</span></span>](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





