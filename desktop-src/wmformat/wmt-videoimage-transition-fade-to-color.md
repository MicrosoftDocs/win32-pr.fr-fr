---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl. h)
description: La transition de fondu à couleur est comprise entre l’image et une image de couleur unie.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542329"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a><span data-ttu-id="a5c5f-104">\_ \_ transition \_ en fondu VIDEOIMAGE WMT \_ vers la \_ couleur</span><span class="sxs-lookup"><span data-stu-id="a5c5f-104">WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR</span></span>

<span data-ttu-id="a5c5f-105">La transition de fondu à couleur est comprise entre l’image et une image de couleur unie.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-105">The fade-to-color transition dissolves from the image to a frame of solid color.</span></span>

## <a name="parameters"></a><span data-ttu-id="a5c5f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5c5f-106">Parameters</span></span>

<span data-ttu-id="a5c5f-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



| <span data-ttu-id="a5c5f-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a5c5f-108">Parameter</span></span>         | <span data-ttu-id="a5c5f-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="a5c5f-109">Structure member</span></span> | <span data-ttu-id="a5c5f-110">Description</span><span class="sxs-lookup"><span data-stu-id="a5c5f-110">Description</span></span>                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c5f-111">Rouge</span><span class="sxs-lookup"><span data-stu-id="a5c5f-111">Red</span></span>               | <span data-ttu-id="a5c5f-112">**fEffectPara0**</span><span class="sxs-lookup"><span data-stu-id="a5c5f-112">**fEffectPara0**</span></span> | <span data-ttu-id="a5c5f-113">Valeur rouge de la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-113">Red value of the background color.</span></span> <span data-ttu-id="a5c5f-114">Défini sur un nombre compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-114">Set to a number between 0 and 255.</span></span>                                                                                                                                                     |
| <span data-ttu-id="a5c5f-115">Vert</span><span class="sxs-lookup"><span data-stu-id="a5c5f-115">Green</span></span>             | <span data-ttu-id="a5c5f-116">**fEffectPara1**</span><span class="sxs-lookup"><span data-stu-id="a5c5f-116">**fEffectPara1**</span></span> | <span data-ttu-id="a5c5f-117">Valeur verte de la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-117">Green value of the background color.</span></span> <span data-ttu-id="a5c5f-118">Défini sur un nombre compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-118">Set to a number between 0 and 255.</span></span>                                                                                                                                                   |
| <span data-ttu-id="a5c5f-119">Bleu</span><span class="sxs-lookup"><span data-stu-id="a5c5f-119">Blue</span></span>              | <span data-ttu-id="a5c5f-120">**fEffectPara2**</span><span class="sxs-lookup"><span data-stu-id="a5c5f-120">**fEffectPara2**</span></span> | <span data-ttu-id="a5c5f-121">Valeur bleue de la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-121">Blue value of the background color.</span></span> <span data-ttu-id="a5c5f-122">Défini sur un nombre compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-122">Set to a number between 0 and 255.</span></span>                                                                                                                                                    |
| <span data-ttu-id="a5c5f-123">Poids de l’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="a5c5f-123">Background weight</span></span> | <span data-ttu-id="a5c5f-124">**fEffectPara3**</span><span class="sxs-lookup"><span data-stu-id="a5c5f-124">**fEffectPara3**</span></span> | <span data-ttu-id="a5c5f-125">Poids de la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-125">Weight of the background color.</span></span> <span data-ttu-id="a5c5f-126">Ce paramètre exprime le pourcentage de la couleur d’arrière-plan dans la combinaison en tant que valeur décimale.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-126">This parameter expresses the percentage of the background color in the mix as a decimal.</span></span> <span data-ttu-id="a5c5f-127">Par exemple, pour mélanger la couleur d’arrière-plan à 30%, en faisant de l’image 70% de la combinaison, définissez sur 0,30.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-127">For example, to blend the background color at 30%, making the image 70% of the mix, set to 0.30.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a5c5f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5c5f-128">Requirements</span></span>



| <span data-ttu-id="a5c5f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5c5f-129">Requirement</span></span> | <span data-ttu-id="a5c5f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5c5f-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c5f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5c5f-131">Header</span></span><br/> | <dl> <span data-ttu-id="a5c5f-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5c5f-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5c5f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5c5f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c5f-134">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="a5c5f-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





