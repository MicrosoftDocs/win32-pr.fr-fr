---
description: Cette propriété interroge le décodeur à la fréquence d’images entières maximale que le décodeur prend en charge. Le type de données de cette propriété est une \_ structure am QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70bc096e5b68737ca877a037571223d673284dab
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910277"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="f9289-104">\_ \_ Propriété QUERYFULLFRAMERATE rate AM</span><span class="sxs-lookup"><span data-stu-id="f9289-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="f9289-105">Cette propriété interroge le décodeur à la fréquence d’images entières maximale que le décodeur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="f9289-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="f9289-106">Le type de données de cette propriété est une structure **am \_ QueryRate** .</span><span class="sxs-lookup"><span data-stu-id="f9289-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="f9289-107">Cette propriété est définie pour la version 1,1 de ce jeu de propriétés ; consultez [**am \_ rate \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="f9289-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="f9289-108">Étiquette</span><span class="sxs-lookup"><span data-stu-id="f9289-108">Label</span></span> | <span data-ttu-id="f9289-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9289-109">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="f9289-110">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="f9289-110">Property Set GUID</span></span> | <span data-ttu-id="f9289-111">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="f9289-111">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="f9289-112">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="f9289-112">Property ID</span></span>       | <span data-ttu-id="f9289-113">\_ \_ Propriété QUERYFULLFRAMERATE rate AM</span><span class="sxs-lookup"><span data-stu-id="f9289-113">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="f9289-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="f9289-114">Data Type</span></span>         | [<span data-ttu-id="f9289-115">**AM \_ QueryRate**</span><span class="sxs-lookup"><span data-stu-id="f9289-115">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="f9289-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9289-116">Remarks</span></span>

<span data-ttu-id="f9289-117">Si la vitesse de lecture dépasse la vitesse maximale du décodeur, le filtre source envoie des groupes d’échantillons continus séparés par des discontinuités.</span><span class="sxs-lookup"><span data-stu-id="f9289-117">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="f9289-118">Les horodatages sautent dans les discontinuités.</span><span class="sxs-lookup"><span data-stu-id="f9289-118">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="f9289-119">Le filtre source peut effectuer cette opération même si la vitesse de lecture est comprise dans la vitesse maximale du décodeur, car il peut y avoir d’autres facteurs, tels que les e/s disque, qui limitent la vitesse de lecture complète.</span><span class="sxs-lookup"><span data-stu-id="f9289-119">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9289-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9289-120">Requirements</span></span>



| <span data-ttu-id="f9289-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9289-121">Requirement</span></span> | <span data-ttu-id="f9289-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9289-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9289-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9289-123">Header</span></span><br/> | <dl> <span data-ttu-id="f9289-124"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9289-124"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9289-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9289-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9289-126">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="f9289-126">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




