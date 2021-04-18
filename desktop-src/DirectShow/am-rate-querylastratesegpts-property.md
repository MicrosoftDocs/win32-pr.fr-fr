---
description: Cette propriété interroge le décodeur pour l’heure de début du changement de taux mis en file d’attente le plus récemment, quelle que soit sa position dans la file d’attente rate-change.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 024ac26d8307dc9b8ff8e16603dfcc61b0704390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528904"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="0ddfe-103">\_ \_ Propriété QUERYLASTRATESEGPTS rate AM</span><span class="sxs-lookup"><span data-stu-id="0ddfe-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="0ddfe-104">Cette propriété interroge le décodeur pour l’heure de début du changement de taux mis en file d’attente le plus récemment, quelle que soit sa position dans la file d’attente rate-change.</span><span class="sxs-lookup"><span data-stu-id="0ddfe-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="0ddfe-105">Cette propriété est définie pour la version 1,1 de ce jeu de propriétés ; consultez [**am \_ rate \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="0ddfe-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="0ddfe-106">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="0ddfe-106">Property Set GUID</span></span> | <span data-ttu-id="0ddfe-107">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="0ddfe-107">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="0ddfe-108">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="0ddfe-108">Property ID</span></span>       | <span data-ttu-id="0ddfe-109">\_Taux am \_ QueryLastRateSegPTS</span><span class="sxs-lookup"><span data-stu-id="0ddfe-109">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="0ddfe-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="0ddfe-110">Data Type</span></span>         | <span data-ttu-id="0ddfe-111">**temps de référence \_**</span><span class="sxs-lookup"><span data-stu-id="0ddfe-111">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="0ddfe-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0ddfe-112">Remarks</span></span>

<span data-ttu-id="0ddfe-113">Le filtre source peut utiliser cette propriété pour synchroniser les changements de taux sur plusieurs flux audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ddfe-113">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ddfe-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ddfe-114">Requirements</span></span>



| <span data-ttu-id="0ddfe-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ddfe-115">Requirement</span></span> | <span data-ttu-id="0ddfe-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ddfe-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddfe-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ddfe-117">Header</span></span><br/> | <dl> <span data-ttu-id="0ddfe-118"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ddfe-118"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ddfe-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ddfe-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ddfe-120">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="0ddfe-120">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




