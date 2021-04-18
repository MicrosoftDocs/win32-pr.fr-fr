---
description: Les \_ constantes d’indicateur de bit LINEANSWERMODE décrivent comment un appel actif existant sur un appareil de ligne est affecté en répondant à un autre appel d’offre sur la même ligne.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: Constantes LINEANSWERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526667"
---
# <a name="lineanswermode_-constants"></a><span data-ttu-id="14c47-103">\_Constantes LINEANSWERMODE</span><span class="sxs-lookup"><span data-stu-id="14c47-103">LINEANSWERMODE\_ Constants</span></span>

<span data-ttu-id="14c47-104">Les constantes d’indicateur de bit **LINEANSWERMODE \_** décrivent comment un appel actif existant sur un appareil de ligne est affecté en répondant à un autre appel d' *offre* sur la même ligne.</span><span class="sxs-lookup"><span data-stu-id="14c47-104">The **LINEANSWERMODE\_** bit-flag constants describe how an existing active call on a line device is affected by answering another *offering* call on the same line.</span></span>

<dl> <dt>

<span data-ttu-id="14c47-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE \_ Drop**</span><span class="sxs-lookup"><span data-stu-id="14c47-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="14c47-106">L’appel actuellement actif est automatiquement supprimé.</span><span class="sxs-lookup"><span data-stu-id="14c47-106">The currently active call will automatically be dropped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14c47-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_ conserver**</span><span class="sxs-lookup"><span data-stu-id="14c47-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE\_HOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="14c47-108">L’appel actuellement actif sera automatiquement mis en attente.</span><span class="sxs-lookup"><span data-stu-id="14c47-108">The currently active call will automatically be placed on hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14c47-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="14c47-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="14c47-110">La réponse à un autre appel sur la même ligne n’a aucun effet sur l’appel actif existant sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="14c47-110">Answering another call on the same line has no effect on the existing active call on the line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14c47-111">Notes</span><span class="sxs-lookup"><span data-stu-id="14c47-111">Remarks</span></span>

<span data-ttu-id="14c47-112">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="14c47-112">No extensibility.</span></span> <span data-ttu-id="14c47-113">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="14c47-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="14c47-114">Si un appel arrive (est offert) au moment où un autre appel est déjà actif, le nouvel appel est connecté à en appelant [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="14c47-114">If a call comes in (is offered) at the time another call is already active, the new call is connected to by invoking [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="14c47-115">L’effet de cette action sur l’appel actif existant dépend des fonctionnalités de l’appareil de la ligne.</span><span class="sxs-lookup"><span data-stu-id="14c47-115">The effect this has on the existing active call depends on the line's device capabilities.</span></span> <span data-ttu-id="14c47-116">Le premier appel peut ne pas être affecté, il peut être automatiquement supprimé ou placé automatiquement en attente.</span><span class="sxs-lookup"><span data-stu-id="14c47-116">The first call may be unaffected, it may automatically be dropped, or it may automatically be placed on hold.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c47-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14c47-117">Requirements</span></span>



| <span data-ttu-id="14c47-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14c47-118">Requirement</span></span> | <span data-ttu-id="14c47-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="14c47-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="14c47-120">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="14c47-120">TAPI version</span></span><br/> | <span data-ttu-id="14c47-121">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="14c47-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="14c47-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="14c47-122">Header</span></span><br/>       | <dl> <span data-ttu-id="14c47-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="14c47-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




