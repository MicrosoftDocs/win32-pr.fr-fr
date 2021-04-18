---
description: Cette propriété interroge le décodeur à la fréquence d’images entières maximale que le décodeur prend en charge. Le type de données de cette propriété est une \_ structure am QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526777"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="01768-104">\_ \_ Propriété QUERYFULLFRAMERATE rate AM</span><span class="sxs-lookup"><span data-stu-id="01768-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="01768-105">Cette propriété interroge le décodeur à la fréquence d’images entières maximale que le décodeur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="01768-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="01768-106">Le type de données de cette propriété est une structure **am \_ QueryRate** .</span><span class="sxs-lookup"><span data-stu-id="01768-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="01768-107">Cette propriété est définie pour la version 1,1 de ce jeu de propriétés ; consultez [**am \_ rate \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="01768-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="01768-108">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="01768-108">Property Set GUID</span></span> | <span data-ttu-id="01768-109">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="01768-109">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="01768-110">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="01768-110">Property ID</span></span>       | <span data-ttu-id="01768-111">\_ \_ Propriété QUERYFULLFRAMERATE rate AM</span><span class="sxs-lookup"><span data-stu-id="01768-111">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="01768-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="01768-112">Data Type</span></span>         | [<span data-ttu-id="01768-113">**AM \_ QueryRate**</span><span class="sxs-lookup"><span data-stu-id="01768-113">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="01768-114">Notes</span><span class="sxs-lookup"><span data-stu-id="01768-114">Remarks</span></span>

<span data-ttu-id="01768-115">Si la vitesse de lecture dépasse la vitesse maximale du décodeur, le filtre source envoie des groupes d’échantillons continus séparés par des discontinuités.</span><span class="sxs-lookup"><span data-stu-id="01768-115">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="01768-116">Les horodatages sautent dans les discontinuités.</span><span class="sxs-lookup"><span data-stu-id="01768-116">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="01768-117">Le filtre source peut effectuer cette opération même si la vitesse de lecture est comprise dans la vitesse maximale du décodeur, car il peut y avoir d’autres facteurs, tels que les e/s disque, qui limitent la vitesse de lecture complète.</span><span class="sxs-lookup"><span data-stu-id="01768-117">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="01768-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01768-118">Requirements</span></span>



| <span data-ttu-id="01768-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01768-119">Requirement</span></span> | <span data-ttu-id="01768-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="01768-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01768-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="01768-121">Header</span></span><br/> | <dl> <span data-ttu-id="01768-122"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="01768-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01768-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01768-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01768-124">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="01768-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




