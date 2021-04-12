---
description: Avertit une application d’une modification apportée à la configuration matérielle d’un appareil ou de l’ordinateur.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Message WM_DEVICECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393028"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="00c2b-103">\_Message WM DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="00c2b-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="00c2b-104">Avertit une application d’une modification apportée à la configuration matérielle d’un appareil ou de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="00c2b-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="00c2b-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="00c2b-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="00c2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00c2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00c2b-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="00c2b-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="00c2b-108">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="00c2b-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="00c2b-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="00c2b-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="00c2b-110">Identificateur **WM \_ DEVICECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="00c2b-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="00c2b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00c2b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00c2b-112">Événement qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="00c2b-112">The event that has occurred.</span></span> <span data-ttu-id="00c2b-113">Ce paramètre peut avoir l’une des valeurs suivantes du fichier d’en-tête DBT. h.</span><span class="sxs-lookup"><span data-stu-id="00c2b-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>



| <span data-ttu-id="00c2b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="00c2b-114">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="00c2b-115">Signification</span><span class="sxs-lookup"><span data-stu-id="00c2b-115">Meaning</span></span>                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <span data-ttu-id="00c2b-116"><dt>**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-116"><dt>**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span></span> </dl>             | <span data-ttu-id="00c2b-117">Une demande de modification de la configuration actuelle (ancrer ou détacher) a été annulée.</span><span class="sxs-lookup"><span data-stu-id="00c2b-117">A request to change the current configuration (dock or undock) has been canceled.</span></span><br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <span data-ttu-id="00c2b-118"><dt>**[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-118"><dt>**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span></span> </dl>                                         | <span data-ttu-id="00c2b-119">La configuration actuelle a changé, en raison d’une station d’accueil ou d’une déconnexion.</span><span class="sxs-lookup"><span data-stu-id="00c2b-119">The current configuration has changed, due to a dock or undock.</span></span><br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <span data-ttu-id="00c2b-120"><dt>**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-120"><dt>**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span></span> </dl>                                                 | <span data-ttu-id="00c2b-121">Un événement personnalisé s’est produit.</span><span class="sxs-lookup"><span data-stu-id="00c2b-121">A custom event has occurred.</span></span><br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <span data-ttu-id="00c2b-122"><dt>**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-122"><dt>**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span></span> </dl>                                         | <span data-ttu-id="00c2b-123">Un appareil ou un élément multimédia a été inséré et est maintenant disponible.</span><span class="sxs-lookup"><span data-stu-id="00c2b-123">A device or piece of media has been inserted and is now available.</span></span><br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <span data-ttu-id="00c2b-124"><dt>**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-124"><dt>**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span></span> </dl>                         | <span data-ttu-id="00c2b-125">Une autorisation est requise pour supprimer un périphérique ou un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="00c2b-125">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="00c2b-126">Toute application peut refuser cette demande et annuler la suppression.</span><span class="sxs-lookup"><span data-stu-id="00c2b-126">Any application can deny this request and cancel the removal.</span></span><br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <span data-ttu-id="00c2b-127"><dt>**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-127"><dt>**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span></span> </dl> | <span data-ttu-id="00c2b-128">Une demande de suppression d’un appareil ou d’un élément multimédia a été annulée.</span><span class="sxs-lookup"><span data-stu-id="00c2b-128">A request to remove a device or piece of media has been canceled.</span></span><br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <span data-ttu-id="00c2b-129"><dt>**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-129"><dt>**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span></span> </dl>             | <span data-ttu-id="00c2b-130">Un appareil ou un élément multimédia a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="00c2b-130">A device or piece of media has been removed.</span></span><br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <span data-ttu-id="00c2b-131"><dt>**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-131"><dt>**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span></span> </dl>                 | <span data-ttu-id="00c2b-132">Un appareil ou un élément multimédia est sur le lieu d’être supprimé.</span><span class="sxs-lookup"><span data-stu-id="00c2b-132">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="00c2b-133">Ne peut pas être refusé.</span><span class="sxs-lookup"><span data-stu-id="00c2b-133">Cannot be denied.</span></span><br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <span data-ttu-id="00c2b-134"><dt>**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-134"><dt>**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span></span> </dl>                     | <span data-ttu-id="00c2b-135">Un événement spécifique à l’appareil s’est produit.</span><span class="sxs-lookup"><span data-stu-id="00c2b-135">A device-specific event has occurred.</span></span><br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <span data-ttu-id="00c2b-136"><dt>**[DBT \_ DEVNODES \_ modifié](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-136"><dt>**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span></span> </dl>                            | <span data-ttu-id="00c2b-137">Un appareil a été ajouté ou supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="00c2b-137">A device has been added to or removed from the system.</span></span><br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <span data-ttu-id="00c2b-138"><dt>**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-138"><dt>**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span></span> </dl>                         | <span data-ttu-id="00c2b-139">Une autorisation est requise pour modifier la configuration actuelle (ancrer ou détacher).</span><span class="sxs-lookup"><span data-stu-id="00c2b-139">Permission is requested to change the current configuration (dock or undock).</span></span><br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <span data-ttu-id="00c2b-140"><dt>**[DBT \_ USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-140"><dt>**[DBT\_USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span></span> </dl>                                                 | <span data-ttu-id="00c2b-141">La signification de ce message est définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="00c2b-141">The meaning of this message is user-defined.</span></span><br/>                                                                                |



 

</dd> <dt>

<span data-ttu-id="00c2b-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00c2b-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00c2b-143">Pointeur vers une structure qui contient des données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="00c2b-143">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="00c2b-144">Son format dépend de la valeur du paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="00c2b-144">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="00c2b-145">Pour plus d’informations, reportez-vous à la documentation de chaque événement.</span><span class="sxs-lookup"><span data-stu-id="00c2b-145">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00c2b-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00c2b-146">Return value</span></span>

<span data-ttu-id="00c2b-147">Retourne la **valeur true** pour accorder la demande.</span><span class="sxs-lookup"><span data-stu-id="00c2b-147">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="00c2b-148">Retourne **la \_ requête \_ de diffusion Deny** pour refuser la demande.</span><span class="sxs-lookup"><span data-stu-id="00c2b-148">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="00c2b-149">Notes</span><span class="sxs-lookup"><span data-stu-id="00c2b-149">Remarks</span></span>

<span data-ttu-id="00c2b-150">Pour les appareils qui offrent des fonctionnalités contrôlables par logiciel, telles que l’éjection et le verrouillage, le système envoie généralement un message [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) pour permettre aux applications et pilotes de périphérique de mettre fin à leur utilisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00c2b-150">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="00c2b-151">Si le système supprime de force un appareil, il ne peut pas envoyer un message [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) .</span><span class="sxs-lookup"><span data-stu-id="00c2b-151">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="00c2b-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00c2b-152">Requirements</span></span>



| <span data-ttu-id="00c2b-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00c2b-153">Requirement</span></span> | <span data-ttu-id="00c2b-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="00c2b-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c2b-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00c2b-155">Minimum supported client</span></span><br/> | <span data-ttu-id="00c2b-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="00c2b-156">Windows XP</span></span><br/>                                                                                             |
| <span data-ttu-id="00c2b-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00c2b-157">Minimum supported server</span></span><br/> | <span data-ttu-id="00c2b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00c2b-158">Windows Server 2003</span></span><br/>                                                                                    |
| <span data-ttu-id="00c2b-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="00c2b-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="00c2b-160"><dt>Winuser. h (inclure Windows. h ou DBT. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00c2b-160"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00c2b-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00c2b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c2b-162">DBT \_ CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="00c2b-162">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="00c2b-163">DBT \_ CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="00c2b-163">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="00c2b-164">DBT \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="00c2b-164">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="00c2b-165">DBT \_ DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="00c2b-165">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="00c2b-166">DBT \_ DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="00c2b-166">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="00c2b-167">DBT \_ DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="00c2b-167">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="00c2b-168">DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="00c2b-168">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="00c2b-169">DBT \_ DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="00c2b-169">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="00c2b-170">DBT \_ DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="00c2b-170">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="00c2b-171">DBT \_ DEVNODES \_ modifié</span><span class="sxs-lookup"><span data-stu-id="00c2b-171">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="00c2b-172">DBT \_ QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="00c2b-172">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="00c2b-173">DBT \_ USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="00c2b-173">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>

 

