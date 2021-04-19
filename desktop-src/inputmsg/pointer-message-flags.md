---
title: Indicateurs de message de pointeur
description: Valeurs utilisées dans différentes macros de pointeur (consultez macros).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510553"
---
# <a name="pointer-message-flags"></a><span data-ttu-id="ace06-103">Indicateurs de message de pointeur</span><span class="sxs-lookup"><span data-stu-id="ace06-103">Pointer Message Flags</span></span>

<span data-ttu-id="ace06-104">Valeurs utilisées dans différentes macros de pointeur (consultez [macros](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="ace06-104">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span>

<dl> <dt>

<span data-ttu-id="ace06-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="ace06-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ace06-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="ace06-107">Indique l’arrivée d’un nouveau pointeur.</span><span class="sxs-lookup"><span data-stu-id="ace06-107">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ace06-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="ace06-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ace06-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="ace06-110">Indique que ce pointeur continue à exister.</span><span class="sxs-lookup"><span data-stu-id="ace06-110">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="ace06-111">Lorsque cet indicateur n’est pas défini, il indique que le pointeur a quitté la plage de détection.</span><span class="sxs-lookup"><span data-stu-id="ace06-111">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="ace06-112">En règle générale, cet indicateur n’est défini que lorsqu’un pointeur de survol quitte la plage de détection (**POINTER_FLAG_UPDATE** est défini) ou lorsqu’un pointeur en contact avec une surface de la fenêtre quitte la plage de détection (**POINTER_FLAG_UP** est définie).</span><span class="sxs-lookup"><span data-stu-id="ace06-112">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ace06-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="ace06-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ace06-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="ace06-115">Indique que ce pointeur est en contact avec la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="ace06-115">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="ace06-116">Lorsque cet indicateur n’est pas défini, il indique un pointeur de pointage.</span><span class="sxs-lookup"><span data-stu-id="ace06-116">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ace06-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="ace06-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-118">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ace06-118">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="ace06-119">Indique une action principale, similaire à un bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="ace06-119">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="ace06-120">Un pointeur tactile a cet indicateur défini lorsqu’il est en contact avec la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="ace06-120">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="ace06-121">Un pointeur de stylet a cet indicateur défini lorsqu’il est en contact avec la surface du digitaliseur sans bouton enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ace06-121">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="ace06-122">Cet indicateur est défini pour le pointeur de la souris lorsque le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ace06-122">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ace06-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="ace06-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-124">0x00000020</span><span class="sxs-lookup"><span data-stu-id="ace06-124">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="ace06-125">Indique une action secondaire, similaire à un bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="ace06-125">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="ace06-126">Un pointeur tactile n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="ace06-126">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="ace06-127">Un pointeur de stylet a cet indicateur défini lorsqu’il est en contact avec la surface du digitaliseur avec le bouton du stylet du stylet enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ace06-127">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="ace06-128">Cet indicateur est défini pour le pointeur de la souris lorsque le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ace06-128">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ace06-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="ace06-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-130">0x00000040</span><span class="sxs-lookup"><span data-stu-id="ace06-130">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="ace06-131">Similaire à un bouton de roulette de la souris.</span><span class="sxs-lookup"><span data-stu-id="ace06-131">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="ace06-132">Un pointeur tactile n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="ace06-132">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="ace06-133">Un pointeur de stylet n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="ace06-133">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="ace06-134">Cet indicateur est défini pour le pointeur de la souris lorsque le bouton roulette de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ace06-134">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ace06-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="ace06-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-136">0x00000080</span><span class="sxs-lookup"><span data-stu-id="ace06-136">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="ace06-137">Analogue à un premier bouton étendu de la souris (le bouton XButton1).</span><span class="sxs-lookup"><span data-stu-id="ace06-137">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="ace06-138">Un pointeur tactile n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="ace06-138">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="ace06-139">Un pointeur de stylet n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="ace06-139">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="ace06-140">Cet indicateur est défini pour le pointeur de la souris lorsque le bouton de la première souris étendue (le bouton XButton1) est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ace06-140">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ace06-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="ace06-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="ace06-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="ace06-143">Similaire à un second bouton de la souris étendue (XButton2).</span><span class="sxs-lookup"><span data-stu-id="ace06-143">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="ace06-144">Un pointeur tactile n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="ace06-144">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="ace06-145">Un pointeur de stylet n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="ace06-145">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="ace06-146">Cet indicateur est défini pour le pointeur de la souris lorsque le bouton de la souris (XBUTTON2) est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ace06-146">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ace06-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="ace06-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-148">0x00002000</span><span class="sxs-lookup"><span data-stu-id="ace06-148">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="ace06-149">Indique que ce pointeur a été désigné comme pointeur principal.</span><span class="sxs-lookup"><span data-stu-id="ace06-149">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="ace06-150">Un pointeur principal est un pointeur unique qui peut effectuer des actions au-delà de celles qui sont disponibles pour les pointeurs non principaux.</span><span class="sxs-lookup"><span data-stu-id="ace06-150">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="ace06-151">Par exemple, lorsqu’un pointeur principal effectue un contact avec une surface de fenêtre, il peut fournir à la fenêtre la possibilité de l’activer en lui envoyant un message de WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="ace06-151">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a WM_POINTERACTIVATE message.</span></span>

<span data-ttu-id="ace06-152">Le pointeur principal est identifié à partir de toutes les interactions de l’utilisateur actuel sur le système (souris, toucher, stylet, etc.).</span><span class="sxs-lookup"><span data-stu-id="ace06-152">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="ace06-153">Par conséquent, le pointeur principal peut ne pas être associé à votre application.</span><span class="sxs-lookup"><span data-stu-id="ace06-153">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="ace06-154">Le premier contact dans une interaction tactile multipoint est défini comme pointeur principal.</span><span class="sxs-lookup"><span data-stu-id="ace06-154">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="ace06-155">Une fois qu’un pointeur principal est identifié, tous les contacts doivent être levés avant qu’un nouveau contact puisse être identifié comme pointeur principal.</span><span class="sxs-lookup"><span data-stu-id="ace06-155">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="ace06-156">Pour les applications qui ne traitent pas l’entrée de pointeur, seuls les événements du pointeur principal sont promus en événements de souris.</span><span class="sxs-lookup"><span data-stu-id="ace06-156">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ace06-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="ace06-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-158">0x00000400</span><span class="sxs-lookup"><span data-stu-id="ace06-158">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="ace06-159">La confiance est une suggestion de l’appareil source indiquant si le pointeur représente une interaction prévue ou accidentelle, qui est particulièrement pertinente pour les pointeurs de PT_TOUCH où une interaction accidentelle (comme avec la paume de la main) peut déclencher l’entrée.</span><span class="sxs-lookup"><span data-stu-id="ace06-159">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="ace06-160">La présence de cet indicateur indique que l’appareil source a une confiance élevée que cette entrée fait partie d’une interaction prévue.</span><span class="sxs-lookup"><span data-stu-id="ace06-160">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ace06-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="ace06-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace06-162">0x00000800</span><span class="sxs-lookup"><span data-stu-id="ace06-162">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="ace06-163">Indique que le pointeur se met anormalement en mode, par exemple lorsque le système reçoit une entrée non valide pour le pointeur ou lorsqu’un appareil avec des pointeurs actifs se met brusquement à part.</span><span class="sxs-lookup"><span data-stu-id="ace06-163">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="ace06-164">Si l’application recevant l’entrée est en mesure de le faire, elle doit traiter l’interaction comme non terminée et inverser les effets du pointeur concerné.</span><span class="sxs-lookup"><span data-stu-id="ace06-164">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ace06-165">Notes</span><span class="sxs-lookup"><span data-stu-id="ace06-165">Remarks</span></span>

<span data-ttu-id="ace06-166">LE bouton XButton1 et XBUTTON2 sont des boutons supplémentaires utilisés sur de nombreux périphériques de souris.</span><span class="sxs-lookup"><span data-stu-id="ace06-166">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="ace06-167">Elles retournent les mêmes données que les boutons de la souris standard.</span><span class="sxs-lookup"><span data-stu-id="ace06-167">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace06-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ace06-168">Requirements</span></span>



| <span data-ttu-id="ace06-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ace06-169">Requirement</span></span> | <span data-ttu-id="ace06-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="ace06-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ace06-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ace06-171">Minimum supported client</span></span><br/> | <span data-ttu-id="ace06-172">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ace06-172">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ace06-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ace06-173">Minimum supported server</span></span><br/> | <span data-ttu-id="ace06-174">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ace06-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ace06-175">En-tête</span><span class="sxs-lookup"><span data-stu-id="ace06-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="ace06-176"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="ace06-176"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ace06-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ace06-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace06-178">Constantes</span><span class="sxs-lookup"><span data-stu-id="ace06-178">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="ace06-179">Macros</span><span class="sxs-lookup"><span data-stu-id="ace06-179">Macros</span></span>](macros.md)
</dt> </dl>

 

 





