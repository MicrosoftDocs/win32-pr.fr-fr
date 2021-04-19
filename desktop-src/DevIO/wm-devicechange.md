---
description: Avertit une application d’une modification apportée à la configuration matérielle d’un appareil ou de l’ordinateur.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Message WM_DEVICECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: 8c1942ac6731488abbeae46a7dbe3da166fee2d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "107581501"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="cac2a-103">\_Message WM DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="cac2a-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="cac2a-104">Avertit une application d’une modification apportée à la configuration matérielle d’un appareil ou de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cac2a-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="cac2a-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cac2a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a><span data-ttu-id="cac2a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cac2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac2a-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="cac2a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="cac2a-108">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cac2a-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="cac2a-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="cac2a-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="cac2a-110">Identificateur **WM \_ DEVICECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="cac2a-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="cac2a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cac2a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cac2a-112">Événement qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="cac2a-112">The event that has occurred.</span></span> <span data-ttu-id="cac2a-113">Ce paramètre peut avoir l’une des valeurs suivantes du fichier d’en-tête DBT. h.</span><span class="sxs-lookup"><span data-stu-id="cac2a-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>

| <span data-ttu-id="cac2a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cac2a-114">Value</span></span> | <span data-ttu-id="cac2a-115">Signification</span><span class="sxs-lookup"><span data-stu-id="cac2a-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="cac2a-116">**[DBT \_ DEVNODES \_ modifié](dbt-devnodes-changed.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-116">**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</span></span></br><span data-ttu-id="cac2a-117">0x0007</span><span class="sxs-lookup"><span data-stu-id="cac2a-117">0x0007</span></span> | <span data-ttu-id="cac2a-118">Un appareil a été ajouté ou supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="cac2a-118">A device has been added to or removed from the system.</span></span> |
| <span data-ttu-id="cac2a-119">**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-119">**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span></span></br><span data-ttu-id="cac2a-120">0x0017</span><span class="sxs-lookup"><span data-stu-id="cac2a-120">0x0017</span></span> | <span data-ttu-id="cac2a-121">Une autorisation est requise pour modifier la configuration actuelle (ancrer ou détacher).</span><span class="sxs-lookup"><span data-stu-id="cac2a-121">Permission is requested to change the current configuration (dock or undock).</span></span> |
| <span data-ttu-id="cac2a-122">**[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-122">**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</span></span></br><span data-ttu-id="cac2a-123">0x0018</span><span class="sxs-lookup"><span data-stu-id="cac2a-123">0x0018</span></span> | <span data-ttu-id="cac2a-124">La configuration actuelle a changé, en raison d’une station d’accueil ou d’une déconnexion.</span><span class="sxs-lookup"><span data-stu-id="cac2a-124">The current configuration has changed, due to a dock or undock.</span></span> |
| <span data-ttu-id="cac2a-125">**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-125">**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span></span></br><span data-ttu-id="cac2a-126">0x0019</span><span class="sxs-lookup"><span data-stu-id="cac2a-126">0x0019</span></span> | <span data-ttu-id="cac2a-127">Une demande de modification de la configuration actuelle (ancrer ou détacher) a été annulée.</span><span class="sxs-lookup"><span data-stu-id="cac2a-127">A request to change the current configuration (dock or undock) has been canceled.</span></span> |
| <span data-ttu-id="cac2a-128">**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-128">**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</span></span></br><span data-ttu-id="cac2a-129">0x8000</span><span class="sxs-lookup"><span data-stu-id="cac2a-129">0x8000</span></span> | <span data-ttu-id="cac2a-130">Un appareil ou un élément multimédia a été inséré et est maintenant disponible.</span><span class="sxs-lookup"><span data-stu-id="cac2a-130">A device or piece of media has been inserted and is now available.</span></span> |
| <span data-ttu-id="cac2a-131">**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-131">**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span></span></br><span data-ttu-id="cac2a-132">0x8001</span><span class="sxs-lookup"><span data-stu-id="cac2a-132">0x8001</span></span> | <span data-ttu-id="cac2a-133">Une autorisation est requise pour supprimer un périphérique ou un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="cac2a-133">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="cac2a-134">Toute application peut refuser cette demande et annuler la suppression.</span><span class="sxs-lookup"><span data-stu-id="cac2a-134">Any application can deny this request and cancel the removal.</span></span> |
| <span data-ttu-id="cac2a-135">**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-135">**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span></span></br><span data-ttu-id="cac2a-136">0x8002</span><span class="sxs-lookup"><span data-stu-id="cac2a-136">0x8002</span></span> | <span data-ttu-id="cac2a-137">Une demande de suppression d’un appareil ou d’un élément multimédia a été annulée.</span><span class="sxs-lookup"><span data-stu-id="cac2a-137">A request to remove a device or piece of media has been canceled.</span></span> |
| <span data-ttu-id="cac2a-138">**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-138">**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span></span></br><span data-ttu-id="cac2a-139">0x8003</span><span class="sxs-lookup"><span data-stu-id="cac2a-139">0x8003</span></span> | <span data-ttu-id="cac2a-140">Un appareil ou un élément multimédia est sur le lieu d’être supprimé.</span><span class="sxs-lookup"><span data-stu-id="cac2a-140">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="cac2a-141">Ne peut pas être refusé.</span><span class="sxs-lookup"><span data-stu-id="cac2a-141">Cannot be denied.</span></span> |
| <span data-ttu-id="cac2a-142">**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-142">**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span></span></br><span data-ttu-id="cac2a-143">0x8004</span><span class="sxs-lookup"><span data-stu-id="cac2a-143">0x8004</span></span> | <span data-ttu-id="cac2a-144">Un appareil ou un élément multimédia a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="cac2a-144">A device or piece of media has been removed.</span></span> |
| <span data-ttu-id="cac2a-145">**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-145">**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span></span></br><span data-ttu-id="cac2a-146">0x8005</span><span class="sxs-lookup"><span data-stu-id="cac2a-146">0x8005</span></span> | <span data-ttu-id="cac2a-147">Un événement spécifique à l’appareil s’est produit.</span><span class="sxs-lookup"><span data-stu-id="cac2a-147">A device-specific event has occurred.</span></span> |
| <span data-ttu-id="cac2a-148">**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-148">**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</span></span></br><span data-ttu-id="cac2a-149">0x8006</span><span class="sxs-lookup"><span data-stu-id="cac2a-149">0x8006</span></span> | <span data-ttu-id="cac2a-150">Un événement personnalisé s’est produit.</span><span class="sxs-lookup"><span data-stu-id="cac2a-150">A custom event has occurred.</span></span> |
| <span data-ttu-id="cac2a-151">**[DBT \_ USERDEFINED](dbt-userdefined.md)**</span><span class="sxs-lookup"><span data-stu-id="cac2a-151">**[DBT\_USERDEFINED](dbt-userdefined.md)**</span></span></br><span data-ttu-id="cac2a-152">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="cac2a-152">0xFFFF</span></span> | <span data-ttu-id="cac2a-153">La signification de ce message est définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cac2a-153">The meaning of this message is user-defined.</span></span> |

</dd> <dt>

<span data-ttu-id="cac2a-154">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cac2a-154">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cac2a-155">Pointeur vers une structure qui contient des données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="cac2a-155">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="cac2a-156">Son format dépend de la valeur du paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="cac2a-156">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="cac2a-157">Pour plus d’informations, reportez-vous à la documentation de chaque événement.</span><span class="sxs-lookup"><span data-stu-id="cac2a-157">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac2a-158">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cac2a-158">Return value</span></span>

<span data-ttu-id="cac2a-159">Retourne la **valeur true** pour accorder la demande.</span><span class="sxs-lookup"><span data-stu-id="cac2a-159">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="cac2a-160">Retourne **la \_ requête \_ de diffusion Deny** pour refuser la demande.</span><span class="sxs-lookup"><span data-stu-id="cac2a-160">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="cac2a-161">Remarques</span><span class="sxs-lookup"><span data-stu-id="cac2a-161">Remarks</span></span>

<span data-ttu-id="cac2a-162">Pour les appareils qui offrent des fonctionnalités contrôlables par logiciel, telles que l’éjection et le verrouillage, le système envoie généralement un message [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) pour permettre aux applications et pilotes de périphérique de mettre fin à leur utilisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cac2a-162">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="cac2a-163">Si le système supprime de force un appareil, il ne peut pas envoyer un message [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) .</span><span class="sxs-lookup"><span data-stu-id="cac2a-163">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac2a-164">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cac2a-164">Requirements</span></span>

| <span data-ttu-id="cac2a-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cac2a-165">Requirement</span></span> | <span data-ttu-id="cac2a-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="cac2a-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac2a-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cac2a-167">Minimum supported client</span></span> | <span data-ttu-id="cac2a-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cac2a-168">Windows XP</span></span> |
| <span data-ttu-id="cac2a-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cac2a-169">Minimum supported server</span></span> | <span data-ttu-id="cac2a-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cac2a-170">Windows Server 2003</span></span>|
| <span data-ttu-id="cac2a-171">Header</span><span class="sxs-lookup"><span data-stu-id="cac2a-171">Header</span></span> | <dl> <span data-ttu-id="cac2a-172"><dt>Winuser. h (inclure Windows. h ou DBT. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cac2a-172"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="cac2a-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cac2a-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac2a-174">DBT \_ CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="cac2a-174">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="cac2a-175">DBT \_ CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="cac2a-175">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="cac2a-176">DBT \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="cac2a-176">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="cac2a-177">DBT \_ DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="cac2a-177">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="cac2a-178">DBT \_ DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="cac2a-178">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="cac2a-179">DBT \_ DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="cac2a-179">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="cac2a-180">DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="cac2a-180">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="cac2a-181">DBT \_ DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="cac2a-181">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="cac2a-182">DBT \_ DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="cac2a-182">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="cac2a-183">DBT \_ DEVNODES \_ modifié</span><span class="sxs-lookup"><span data-stu-id="cac2a-183">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="cac2a-184">DBT \_ QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="cac2a-184">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="cac2a-185">DBT \_ USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="cac2a-185">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>
