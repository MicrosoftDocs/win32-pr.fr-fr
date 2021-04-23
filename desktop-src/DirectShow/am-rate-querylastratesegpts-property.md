---
description: Cette propriété interroge le décodeur pour l’heure de début du changement de taux mis en file d’attente le plus récemment, quelle que soit sa position dans la file d’attente rate-change.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c6e3e00985ba6e714bf48d349fd5af5c9593b9
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910267"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="a73af-103">\_ \_ Propriété QUERYLASTRATESEGPTS rate AM</span><span class="sxs-lookup"><span data-stu-id="a73af-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="a73af-104">Cette propriété interroge le décodeur pour l’heure de début du changement de taux mis en file d’attente le plus récemment, quelle que soit sa position dans la file d’attente rate-change.</span><span class="sxs-lookup"><span data-stu-id="a73af-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="a73af-105">Cette propriété est définie pour la version 1,1 de ce jeu de propriétés ; consultez [**am \_ rate \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="a73af-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="a73af-106">Étiquette</span><span class="sxs-lookup"><span data-stu-id="a73af-106">Label</span></span> | <span data-ttu-id="a73af-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="a73af-107">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="a73af-108">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="a73af-108">Property Set GUID</span></span> | <span data-ttu-id="a73af-109">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="a73af-109">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="a73af-110">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="a73af-110">Property ID</span></span>       | <span data-ttu-id="a73af-111">\_Taux am \_ QueryLastRateSegPTS</span><span class="sxs-lookup"><span data-stu-id="a73af-111">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="a73af-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="a73af-112">Data Type</span></span>         | <span data-ttu-id="a73af-113">**temps de référence \_**</span><span class="sxs-lookup"><span data-stu-id="a73af-113">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="a73af-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a73af-114">Remarks</span></span>

<span data-ttu-id="a73af-115">Le filtre source peut utiliser cette propriété pour synchroniser les changements de taux sur plusieurs flux audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="a73af-115">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73af-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a73af-116">Requirements</span></span>



| <span data-ttu-id="a73af-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a73af-117">Requirement</span></span> | <span data-ttu-id="a73af-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a73af-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a73af-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="a73af-119">Header</span></span><br/> | <dl> <span data-ttu-id="a73af-120"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="a73af-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a73af-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a73af-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73af-122">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="a73af-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




