---
title: Indicateurs de pointeur
description: Valeurs qui peuvent apparaître dans le champ pointerFlags de la structure POINTER_INFO.
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742332"
---
# <a name="pointer-flags"></a><span data-ttu-id="1d210-103">Indicateurs de pointeur</span><span class="sxs-lookup"><span data-stu-id="1d210-103">Pointer Flags</span></span>

<span data-ttu-id="1d210-104">Valeurs qui peuvent apparaître dans le champ **pointerFlags** de la structure [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="1d210-104">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="1d210-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="1d210-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d210-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-107">Default</span><span class="sxs-lookup"><span data-stu-id="1d210-107">Default</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="1d210-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1d210-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="1d210-110">Indique l’arrivée d’un nouveau pointeur.</span><span class="sxs-lookup"><span data-stu-id="1d210-110">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="1d210-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-112">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1d210-112">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="1d210-113">Indique que ce pointeur continue à exister.</span><span class="sxs-lookup"><span data-stu-id="1d210-113">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="1d210-114">Lorsque cet indicateur n’est pas défini, il indique que le pointeur a quitté la plage de détection.</span><span class="sxs-lookup"><span data-stu-id="1d210-114">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="1d210-115">En règle générale, cet indicateur n’est défini que lorsqu’un pointeur de survol quitte la plage de détection (**POINTER_FLAG_UPDATE** est défini) ou lorsqu’un pointeur en contact avec une surface de la fenêtre quitte la plage de détection (**POINTER_FLAG_UP** est définie).</span><span class="sxs-lookup"><span data-stu-id="1d210-115">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="1d210-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-117">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1d210-117">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="1d210-118">Indique que ce pointeur est en contact avec la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="1d210-118">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="1d210-119">Lorsque cet indicateur n’est pas défini, il indique un pointeur de pointage.</span><span class="sxs-lookup"><span data-stu-id="1d210-119">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="1d210-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-121">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d210-121">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="1d210-122">Indique une action principale, similaire à un bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="1d210-122">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="1d210-123">Un pointeur tactile a cet indicateur défini lorsqu’il est en contact avec la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="1d210-123">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="1d210-124">Un pointeur de stylet a cet indicateur défini lorsqu’il est en contact avec la surface du digitaliseur sans bouton enfoncé.</span><span class="sxs-lookup"><span data-stu-id="1d210-124">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="1d210-125">Cet indicateur est défini pour le pointeur de la souris lorsque le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="1d210-125">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="1d210-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-127">0x00000020</span><span class="sxs-lookup"><span data-stu-id="1d210-127">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="1d210-128">Indique une action secondaire, similaire à un bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="1d210-128">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="1d210-129">Un pointeur tactile n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="1d210-129">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="1d210-130">Un pointeur de stylet a cet indicateur défini lorsqu’il est en contact avec la surface du digitaliseur avec le bouton du stylet du stylet enfoncé.</span><span class="sxs-lookup"><span data-stu-id="1d210-130">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="1d210-131">Cet indicateur est défini pour le pointeur de la souris lorsque le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="1d210-131">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="1d210-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-133">0x00000040</span><span class="sxs-lookup"><span data-stu-id="1d210-133">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="1d210-134">Similaire à un bouton de roulette de la souris.</span><span class="sxs-lookup"><span data-stu-id="1d210-134">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="1d210-135">Un pointeur tactile n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="1d210-135">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="1d210-136">Un pointeur de stylet n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="1d210-136">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="1d210-137">Cet indicateur est défini pour le pointeur de la souris lorsque le bouton roulette de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="1d210-137">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="1d210-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="1d210-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="1d210-140">Analogue à un premier bouton étendu de la souris (le bouton XButton1).</span><span class="sxs-lookup"><span data-stu-id="1d210-140">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="1d210-141">Un pointeur tactile n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="1d210-141">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="1d210-142">Un pointeur de stylet n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="1d210-142">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="1d210-143">Cet indicateur est défini pour le pointeur de la souris lorsque le bouton de la première souris étendue (le bouton XButton1) est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="1d210-143">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="1d210-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-145">0x00000100</span><span class="sxs-lookup"><span data-stu-id="1d210-145">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="1d210-146">Similaire à un second bouton de la souris étendue (XButton2).</span><span class="sxs-lookup"><span data-stu-id="1d210-146">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="1d210-147">Un pointeur tactile n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="1d210-147">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="1d210-148">Un pointeur de stylet n’utilise pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="1d210-148">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="1d210-149">Cet indicateur est défini pour le pointeur de la souris lorsque le bouton de la souris (XBUTTON2) est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="1d210-149">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="1d210-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="1d210-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-152">Indique que ce pointeur a été désigné comme pointeur principal.</span><span class="sxs-lookup"><span data-stu-id="1d210-152">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="1d210-153">Un pointeur principal est un pointeur unique qui peut effectuer des actions au-delà de celles qui sont disponibles pour les pointeurs non principaux.</span><span class="sxs-lookup"><span data-stu-id="1d210-153">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="1d210-154">Par exemple, lorsqu’un pointeur principal effectue un contact avec une surface de fenêtre, il peut fournir à la fenêtre la possibilité de l’activer en lui envoyant un message de [**WM_POINTERACTIVATE**](wm-pointeractivate.md) .</span><span class="sxs-lookup"><span data-stu-id="1d210-154">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a [**WM_POINTERACTIVATE**](wm-pointeractivate.md) message.</span></span>

<span data-ttu-id="1d210-155">Le pointeur principal est identifié à partir de toutes les interactions de l’utilisateur actuel sur le système (souris, toucher, stylet, etc.).</span><span class="sxs-lookup"><span data-stu-id="1d210-155">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="1d210-156">Par conséquent, le pointeur principal peut ne pas être associé à votre application.</span><span class="sxs-lookup"><span data-stu-id="1d210-156">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="1d210-157">Le premier contact dans une interaction tactile multipoint est défini comme pointeur principal.</span><span class="sxs-lookup"><span data-stu-id="1d210-157">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="1d210-158">Une fois qu’un pointeur principal est identifié, tous les contacts doivent être levés avant qu’un nouveau contact puisse être identifié comme pointeur principal.</span><span class="sxs-lookup"><span data-stu-id="1d210-158">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="1d210-159">Pour les applications qui ne traitent pas l’entrée de pointeur, seuls les événements du pointeur principal sont promus en événements de souris.</span><span class="sxs-lookup"><span data-stu-id="1d210-159">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="1d210-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-161">0x000004000</span><span class="sxs-lookup"><span data-stu-id="1d210-161">0x000004000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-162">La confiance est une suggestion de l’appareil source indiquant si le pointeur représente une interaction prévue ou accidentelle, qui est particulièrement pertinente pour les pointeurs de PT_TOUCH où une interaction accidentelle (comme avec la paume de la main) peut déclencher l’entrée.</span><span class="sxs-lookup"><span data-stu-id="1d210-162">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="1d210-163">La présence de cet indicateur indique que l’appareil source a une confiance élevée que cette entrée fait partie d’une interaction prévue.</span><span class="sxs-lookup"><span data-stu-id="1d210-163">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="1d210-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-165">0x000008000</span><span class="sxs-lookup"><span data-stu-id="1d210-165">0x000008000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-166">Indique que le pointeur se met anormalement en mode, par exemple lorsque le système reçoit une entrée non valide pour le pointeur ou lorsqu’un appareil avec des pointeurs actifs se met brusquement à part.</span><span class="sxs-lookup"><span data-stu-id="1d210-166">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="1d210-167">Si l’application recevant l’entrée est en mesure de le faire, elle doit traiter l’interaction comme non terminée et inverser les effets du pointeur concerné.</span><span class="sxs-lookup"><span data-stu-id="1d210-167">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span><span class="sxs-lookup"><span data-stu-id="1d210-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-169">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1d210-169">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-170">Indique que ce pointeur est passé à l’état inactif ; autrement dit, il a effectué un contact avec la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="1d210-170">Indicates that this pointer transitioned to a down state; that is, it made contact with the digitizer surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span><span class="sxs-lookup"><span data-stu-id="1d210-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-172">0x00020000</span><span class="sxs-lookup"><span data-stu-id="1d210-172">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-173">Indique qu’il s’agit d’une mise à jour simple qui n’inclut pas les modifications de l’état du pointeur.</span><span class="sxs-lookup"><span data-stu-id="1d210-173">Indicates that this is a simple update that does not include pointer state changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span><span class="sxs-lookup"><span data-stu-id="1d210-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-175">0x00040000</span><span class="sxs-lookup"><span data-stu-id="1d210-175">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-176">Indique que ce pointeur est passé à l’État haut ; autrement dit, les contacts avec la surface du digitaliseur sont terminés.</span><span class="sxs-lookup"><span data-stu-id="1d210-176">Indicates that this pointer transitioned to an up state; that is, contact with the digitizer surface ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span><span class="sxs-lookup"><span data-stu-id="1d210-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-178">0x00080000</span><span class="sxs-lookup"><span data-stu-id="1d210-178">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-179">Indique l’entrée associée à une roulette de pointeur.</span><span class="sxs-lookup"><span data-stu-id="1d210-179">Indicates input associated with a pointer wheel.</span></span> <span data-ttu-id="1d210-180">Pour les pointeurs de souris, cela équivaut à l’action de la molette de défilement de la souris ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="1d210-180">For mouse pointers, this is equivalent to the action of the mouse scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span><span class="sxs-lookup"><span data-stu-id="1d210-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="1d210-182">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-183">Indique l’entrée associée à un pointeur h-Wheel.</span><span class="sxs-lookup"><span data-stu-id="1d210-183">Indicates input associated with a pointer h-wheel.</span></span> <span data-ttu-id="1d210-184">Pour les pointeurs de souris, cela équivaut à l’action de la roulette de défilement horizontale de la souris ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="1d210-184">For mouse pointers, this is equivalent to the action of the mouse horizontal scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span><span class="sxs-lookup"><span data-stu-id="1d210-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-186">0x00200000</span><span class="sxs-lookup"><span data-stu-id="1d210-186">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-187">Indique que ce pointeur a été capturé par (associé à) un autre élément et que l’élément d’origine a perdu la capture (voir [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span><span class="sxs-lookup"><span data-stu-id="1d210-187">Indicates that this pointer was captured by (associated with) another element and the original element has lost capture (see [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d210-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="1d210-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d210-189">0x00400000</span><span class="sxs-lookup"><span data-stu-id="1d210-189">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="1d210-190">Indique que ce pointeur a une transformation associée.</span><span class="sxs-lookup"><span data-stu-id="1d210-190">Indicates that this pointer has an associated transform.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d210-191">Notes</span><span class="sxs-lookup"><span data-stu-id="1d210-191">Remarks</span></span>

<span data-ttu-id="1d210-192">LE bouton XButton1 et XBUTTON2 sont des boutons supplémentaires utilisés sur de nombreux périphériques de souris.</span><span class="sxs-lookup"><span data-stu-id="1d210-192">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="1d210-193">Elles retournent les mêmes données que les boutons de la souris standard.</span><span class="sxs-lookup"><span data-stu-id="1d210-193">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d210-194">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d210-194">Requirements</span></span>



| <span data-ttu-id="1d210-195">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d210-195">Requirement</span></span> | <span data-ttu-id="1d210-196">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d210-196">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1d210-197">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d210-197">Minimum supported client</span></span><br/> | <span data-ttu-id="1d210-198">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d210-198">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1d210-199">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d210-199">Minimum supported server</span></span><br/> | <span data-ttu-id="1d210-200">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d210-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1d210-201">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d210-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d210-202"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d210-202"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d210-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d210-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d210-204">Constantes</span><span class="sxs-lookup"><span data-stu-id="1d210-204">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="1d210-205">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="1d210-205">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="1d210-206">**POINTER_BUTTON_CHANGE_TYPE**</span><span class="sxs-lookup"><span data-stu-id="1d210-206">**POINTER_BUTTON_CHANGE_TYPE**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

