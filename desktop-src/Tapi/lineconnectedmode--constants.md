---
description: Les \_ constantes d’indicateur de bit LINECONNECTEDMODE décrivent différents sous-États d’un appel connecté.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: Constantes LINECONNECTEDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542614"
---
# <a name="lineconnectedmode_-constants"></a><span data-ttu-id="93d7a-103">\_Constantes LINECONNECTEDMODE</span><span class="sxs-lookup"><span data-stu-id="93d7a-103">LINECONNECTEDMODE\_ Constants</span></span>

<span data-ttu-id="93d7a-104">Les constantes d’indicateur de bit **LINECONNECTEDMODE \_** décrivent différents sous-États d’un appel connecté.</span><span class="sxs-lookup"><span data-stu-id="93d7a-104">The **LINECONNECTEDMODE\_** bit-flag constants describe different substates of a connected call.</span></span> <span data-ttu-id="93d7a-105">Un mode est disponible en tant qu’État d’appel à l’application après que l’état d’appel passe à Connected, et dans la ligne \_ CALLSTATE message indiquant que l’appel se trouve dans LINECALLSTATE \_ connected.</span><span class="sxs-lookup"><span data-stu-id="93d7a-105">A mode is available as call status to the application after the call state transitions to connected, and within the LINE\_CALLSTATE message indicating the call is in LINECALLSTATE\_CONNECTED.</span></span> <span data-ttu-id="93d7a-106">Ces valeurs sont utilisées lorsque l’appel est sur une adresse partagée (Bridged) avec d’autres stations (pour plus d’informations, consultez [**\_ constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalement des systèmes à clé électronique.</span><span class="sxs-lookup"><span data-stu-id="93d7a-106">These values are used when the call is on an address that is shared (bridged) with other stations (for more information, see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="93d7a-107">Les **\_ constantes LINECONNECTEDMODE** ont les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="93d7a-107">The **LINECONNECTEDMODE\_constants** have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="93d7a-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ actif**</span><span class="sxs-lookup"><span data-stu-id="93d7a-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93d7a-109">Indique que l’appel est connecté à la station active (la station active est un participant à l’appel).</span><span class="sxs-lookup"><span data-stu-id="93d7a-109">Indicates that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="93d7a-110">Si le mode d’état de l’appel est 0 (zéro), l’application doit supposer que la valeur est « active » (ce qui serait la situation sur une adresse sans pont).</span><span class="sxs-lookup"><span data-stu-id="93d7a-110">If the call state mode is 0 (zero), the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="93d7a-111">Le mode peut basculer entre actif et inactif pendant un appel si l’utilisateur rejoint et quitte l’appel via une action manuelle.</span><span class="sxs-lookup"><span data-stu-id="93d7a-111">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span> <span data-ttu-id="93d7a-112">Dans une telle situation, une opération de [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ou de [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) peut ne pas réellement supprimer l’appel ou le mettre en attente, car l’état des autres stations sur l’appel peut être régi (par exemple, la tentative de « conservation » d’un appel lorsque d’autres stations participent n’est pas possible). au lieu de cela, l’appel peut être remplacé par le mode inactif s’il reste connecté sur d’autres stations.</span><span class="sxs-lookup"><span data-stu-id="93d7a-112">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call may be changed to the INACTIVE mode if it remains CONNECTED at other stations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93d7a-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE \_ ACTIVEHELD**</span><span class="sxs-lookup"><span data-stu-id="93d7a-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE\_ACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93d7a-114">Indique que la station est un participant actif dans l’appel, mais que le tiers distant a passé l’appel en attente (l’autre partie considère que l’appel est à l’État onHold).</span><span class="sxs-lookup"><span data-stu-id="93d7a-114">Indicates that the station is an active participant in the call, but that the remote party has placed the call on hold (the other party considers the call to be in the onhold state).</span></span> <span data-ttu-id="93d7a-115">Normalement, ces informations sont disponibles uniquement lorsque les deux points de terminaison de l’appel se trouvent dans le même domaine de basculement.</span><span class="sxs-lookup"><span data-stu-id="93d7a-115">Normally, such information is available only when both endpoints of the call fall within the same switching domain.</span></span> <span data-ttu-id="93d7a-116">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="93d7a-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="93d7a-117">(TAPI versions 2,0 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="93d7a-117">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93d7a-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ confirmé**</span><span class="sxs-lookup"><span data-stu-id="93d7a-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93d7a-119">Indique que le fournisseur de services a reçu une notification affirmative indiquant que l’appel est passé à l’état connecté (par exemple, via la surveillance des réponses ou des mécanismes similaires).</span><span class="sxs-lookup"><span data-stu-id="93d7a-119">Indicates that the service provider received affirmative notification that the call has entered the connected state (for example, through answer supervision or similar mechanisms).</span></span> <span data-ttu-id="93d7a-120">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="93d7a-120">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="93d7a-121">(TAPI versions 2,0 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="93d7a-121">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93d7a-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="93d7a-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93d7a-123">Indique que l’appel est actif sur une ou plusieurs autres stations, mais que la station active n’est pas un participant à l’appel.</span><span class="sxs-lookup"><span data-stu-id="93d7a-123">Indicates that the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="93d7a-124">Si le mode d’état de l’appel est égal à zéro, l’application doit supposer que la valeur est « active » (ce qui serait la situation sur une adresse sans pont).</span><span class="sxs-lookup"><span data-stu-id="93d7a-124">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="93d7a-125">Un appel dans l’état inactif peut être joint à l’aide de [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="93d7a-125">A call in the INACTIVE state can be joined using [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="93d7a-126">De nombreuses opérations qui sont valides dans les appels de l’État CONNECTed peuvent être impossibles dans le mode inactif, par exemple la surveillance des tons et des chiffres, car la station ne participe pas réellement à l’appel ; la surveillance est généralement suspendue (même si elle n’est pas annulée) pendant que l’appel est en mode inactif.</span><span class="sxs-lookup"><span data-stu-id="93d7a-126">Many operations that are valid in calls in the CONNECTED state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93d7a-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE \_ INACTIVEHELD**</span><span class="sxs-lookup"><span data-stu-id="93d7a-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE\_INACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93d7a-128">Indique que la station n’est pas un participant actif dans l’appel et que le tiers distant a passé l’appel en attente.</span><span class="sxs-lookup"><span data-stu-id="93d7a-128">Indicates that the station is not an active participant in the call, and that the remote party has placed the call on hold.</span></span> <span data-ttu-id="93d7a-129">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="93d7a-129">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="93d7a-130">(TAPI versions 2,0 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="93d7a-130">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93d7a-131">Notes</span><span class="sxs-lookup"><span data-stu-id="93d7a-131">Remarks</span></span>

<span data-ttu-id="93d7a-132">Non extensible.</span><span class="sxs-lookup"><span data-stu-id="93d7a-132">Not extensible.</span></span> <span data-ttu-id="93d7a-133">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="93d7a-133">All 32 bits are reserved.</span></span>

<span data-ttu-id="93d7a-134">Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur la ligne et de ne pas utiliser ces \_ valeurs LINECONNECTEDMODE qui ne sont pas prises en charge sur la version négociée.</span><span class="sxs-lookup"><span data-stu-id="93d7a-134">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use those LINECONNECTEDMODE\_ values that are not supported on the negotiated version.</span></span> <span data-ttu-id="93d7a-135">Les applications qui ne sont pas Cognizant de LINECONNECTEDMODE \_ supposent probablement qu’un appel qui se trouve dans LINECALLSTATE \_ connecté est dans LINECONNECTEDMODE \_ actif.</span><span class="sxs-lookup"><span data-stu-id="93d7a-135">Applications that are not cognizant of LINECONNECTEDMODE\_ will most likely assume that a call that is in LINECALLSTATE\_CONNECTED is in LINECONNECTEDMODE\_ACTIVE.</span></span>

<span data-ttu-id="93d7a-136">Les \_ \_ valeurs inactives LINECONNECTEDMODE actives et LINECONNECTEDMODE sont utilisées lorsque l’appel est sur une adresse partagée avec d’autres stations (Bridged, voir [**\_ constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalement des systèmes à clé électronique.</span><span class="sxs-lookup"><span data-stu-id="93d7a-136">The LINECONNECTEDMODE\_ACTIVE and LINECONNECTEDMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="93d7a-137">Si le mode d’état d’appel connecté est « actif », cela signifie que l’appel est connecté à la station active (la station actuelle est un participant à l’appel).</span><span class="sxs-lookup"><span data-stu-id="93d7a-137">If the connected call state mode is "active," it means that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="93d7a-138">Si le mode d’état de l’appel est « inactif », l’appel est actif sur une ou plusieurs autres stations, mais la station actuelle n’est pas un participant à l’appel.</span><span class="sxs-lookup"><span data-stu-id="93d7a-138">If the call state mode is "inactive," the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="93d7a-139">Si le mode d’état de l’appel est égal à zéro, l’application doit supposer que la valeur est « active » (ce qui serait la situation sur une adresse sans pont).</span><span class="sxs-lookup"><span data-stu-id="93d7a-139">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="93d7a-140">Le mode peut basculer entre actif et inactif pendant un appel si l’utilisateur rejoint et quitte l’appel via une action manuelle.</span><span class="sxs-lookup"><span data-stu-id="93d7a-140">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span>

<span data-ttu-id="93d7a-141">Dans une telle situation, une opération de [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ou de [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) peut ne pas réellement supprimer l’appel ou le mettre en attente, car l’état des autres stations sur l’appel peut être régi (par exemple, la tentative de « conservation » d’un appel lorsque d’autres stations participent n’est pas possible); au lieu de cela, l’appel peut simplement être remplacé par le mode inactif s’il reste connecté sur d’autres stations.</span><span class="sxs-lookup"><span data-stu-id="93d7a-141">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating will not be possible); instead, the call can simply be changed to the INACTIVE mode if it remains connected at other stations.</span></span> <span data-ttu-id="93d7a-142">Un appel dans l’état inactif peut être joint à l’aide de [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="93d7a-142">A call in the INACTIVE state can be joined using the [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="93d7a-143">De nombreuses opérations qui sont valides dans les appels de l’État Connected peuvent être impossibles dans le mode inactif, par exemple la surveillance des tons et des chiffres, car la station ne participe pas réellement à l’appel ; la surveillance est généralement suspendue (même si elle n’est pas annulée) pendant que l’appel est en mode inactif.</span><span class="sxs-lookup"><span data-stu-id="93d7a-143">Many operations that are valid in calls in the connected state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="93d7a-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93d7a-144">Requirements</span></span>



| <span data-ttu-id="93d7a-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93d7a-145">Requirement</span></span> | <span data-ttu-id="93d7a-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="93d7a-146">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="93d7a-147">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="93d7a-147">TAPI version</span></span><br/> | <span data-ttu-id="93d7a-148">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="93d7a-148">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="93d7a-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="93d7a-149">Header</span></span><br/>       | <dl> <span data-ttu-id="93d7a-150"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="93d7a-150"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93d7a-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93d7a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d7a-152">**lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="93d7a-152">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[<span data-ttu-id="93d7a-153">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="93d7a-153">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="93d7a-154">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="93d7a-154">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




