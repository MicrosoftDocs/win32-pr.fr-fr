---
description: Les constantes d’indicateur de bit PHONEBUTTONSTATE décrivent les positions des boutons.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: Constantes PHONEBUTTONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539265"
---
# <a name="phonebuttonstate_-constants"></a><span data-ttu-id="347ee-103">Constantes PHONEBUTTONSTATE_</span><span class="sxs-lookup"><span data-stu-id="347ee-103">PHONEBUTTONSTATE_ Constants</span></span>

<span data-ttu-id="347ee-104">Les constantes d’indicateur de bit **PHONEBUTTONSTATE_** décrivent les positions du bouton.</span><span class="sxs-lookup"><span data-stu-id="347ee-104">The **PHONEBUTTONSTATE_** bit-flag constants describe the button's positions.</span></span>

<dl> <dt>

<span data-ttu-id="347ee-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span><span class="sxs-lookup"><span data-stu-id="347ee-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="347ee-106">Le bouton est à l’état « enfoncé » (enfoncé).</span><span class="sxs-lookup"><span data-stu-id="347ee-106">The button is in the "down" state (pressed down).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="347ee-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="347ee-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="347ee-108">Indique que l’État haut ou de l’état enfoncé du bouton n’est pas connu du fournisseur de services et qu’il ne sera pas connu à un moment ultérieur.</span><span class="sxs-lookup"><span data-stu-id="347ee-108">Indicates that the up or down state of the button is not known to the service provider, and will not become known at a future time.</span></span> <span data-ttu-id="347ee-109">(TAPI versions 1,4 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="347ee-109">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="347ee-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="347ee-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="347ee-111">Indique que l’État en haut ou en aval du bouton n’est pas connu pour l’instant, mais peut devenir connu à un moment ultérieur.</span><span class="sxs-lookup"><span data-stu-id="347ee-111">Indicates that the up or down state of the button is not known at this time, but may become known at a future time.</span></span> <span data-ttu-id="347ee-112">(TAPI versions 1,4 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="347ee-112">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="347ee-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span><span class="sxs-lookup"><span data-stu-id="347ee-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="347ee-114">Le bouton est à l’État « haut ».</span><span class="sxs-lookup"><span data-stu-id="347ee-114">The button is in the "up" state.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="347ee-115">Notes</span><span class="sxs-lookup"><span data-stu-id="347ee-115">Remarks</span></span>

<span data-ttu-id="347ee-116">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="347ee-116">No extensibility.</span></span> <span data-ttu-id="347ee-117">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="347ee-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="347ee-118">Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur le téléphone et de ne pas utiliser ces PHONEBUTTONSTATE_ valeurs que la version négociée ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="347ee-118">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the phone, and to not use those PHONEBUTTONSTATE_ values that the negotiated version does not support.</span></span>

## <a name="requirements"></a><span data-ttu-id="347ee-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="347ee-119">Requirements</span></span>



| <span data-ttu-id="347ee-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="347ee-120">Requirement</span></span> | <span data-ttu-id="347ee-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="347ee-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="347ee-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="347ee-122">TAPI version</span></span><br/> | <span data-ttu-id="347ee-123">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="347ee-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="347ee-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="347ee-124">Header</span></span><br/>       | <dl> <span data-ttu-id="347ee-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="347ee-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




