---
title: Message MM_MCINOTIFY (mmsystem. h)
description: Le \_ message mm MCINOTIFY avertit une application qu’un périphérique MCI a terminé une opération. Les appareils MCI envoient ce message uniquement lorsque l' \_ indicateur de notification MCI est utilisé.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- Message MM_MCINOTIFY Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104710"
---
# <a name="mm_mcinotify-message"></a><span data-ttu-id="3e397-105">MM \_ message MCINOTIFY</span><span class="sxs-lookup"><span data-stu-id="3e397-105">MM\_MCINOTIFY message</span></span>

<span data-ttu-id="3e397-106">Le message **mm \_ MCINOTIFY** avertit une application qu’un périphérique MCI a terminé une opération.</span><span class="sxs-lookup"><span data-stu-id="3e397-106">The **MM\_MCINOTIFY** message notifies an application that an MCI device has completed an operation.</span></span> <span data-ttu-id="3e397-107">Les appareils MCI envoient ce message uniquement lorsque l' \_ indicateur de notification MCI est utilisé.</span><span class="sxs-lookup"><span data-stu-id="3e397-107">MCI devices send this message only when the MCI\_NOTIFY flag is used.</span></span>


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a><span data-ttu-id="3e397-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e397-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e397-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="3e397-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3e397-110">Raison de la notification.</span><span class="sxs-lookup"><span data-stu-id="3e397-110">Reason for the notification.</span></span> <span data-ttu-id="3e397-111">Les valeurs suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="3e397-111">The following values are defined:</span></span>



| <span data-ttu-id="3e397-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e397-112">Requirement</span></span> | <span data-ttu-id="3e397-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e397-113">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e397-114">\_notification MCI \_ abandonnée</span><span class="sxs-lookup"><span data-stu-id="3e397-114">MCI\_NOTIFY\_ABORTED</span></span>    | <span data-ttu-id="3e397-115">L’appareil a reçu une commande qui empêchait la satisfaction des conditions actuelles de lancement de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="3e397-115">The device received a command that prevented the current conditions for initiating the callback function from being met.</span></span> <span data-ttu-id="3e397-116">Si une nouvelle commande interrompt la commande active et qu’elle demande également une notification, l’appareil envoie ce message uniquement et n’émet pas de notification MCI \_ \_ remplacée</span><span class="sxs-lookup"><span data-stu-id="3e397-116">If a new command interrupts the current command and it also requests notification, the device sends this message only and not MCI\_NOTIFY\_SUPERSEDED</span></span> |
| <span data-ttu-id="3e397-117">échec de la \_ notification MCI \_</span><span class="sxs-lookup"><span data-stu-id="3e397-117">MCI\_NOTIFY\_FAILURE</span></span>    | <span data-ttu-id="3e397-118">Une erreur d’appareil s’est produite lors de l’exécution de la commande par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3e397-118">A device error occurred while the device was executing the command.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="3e397-119">\_notification MCI \_ réussie</span><span class="sxs-lookup"><span data-stu-id="3e397-119">MCI\_NOTIFY\_SUCCESSFUL</span></span> | <span data-ttu-id="3e397-120">Les conditions qui initialisent la fonction de rappel ont été remplies.</span><span class="sxs-lookup"><span data-stu-id="3e397-120">The conditions initiating the callback function have been met.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="3e397-121">\_notification MCI \_ remplacée</span><span class="sxs-lookup"><span data-stu-id="3e397-121">MCI\_NOTIFY\_SUPERSEDED</span></span> | <span data-ttu-id="3e397-122">L’appareil a reçu une autre commande avec l’indicateur « Notify » défini et les conditions actuelles pour l’initialisation de la fonction de rappel ont été remplacées.</span><span class="sxs-lookup"><span data-stu-id="3e397-122">The device received another command with the "notify" flag set and the current conditions for initiating the callback function have been superseded.</span></span>                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="3e397-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span><span class="sxs-lookup"><span data-stu-id="3e397-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span></span>
</dt> <dd>

<span data-ttu-id="3e397-124">Identificateur de l’appareil initialisant la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="3e397-124">Identifier of the device initiating the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e397-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3e397-125">Return Value</span></span>

<span data-ttu-id="3e397-126">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="3e397-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e397-127">Notes</span><span class="sxs-lookup"><span data-stu-id="3e397-127">Remarks</span></span>

<span data-ttu-id="3e397-128">Pour plus d’informations sur l' \_ indicateur de notification MCI, consultez [l’indicateur Notify](the-notify-flag.md).</span><span class="sxs-lookup"><span data-stu-id="3e397-128">For more information about the MCI\_NOTIFY flag, see [The Notify Flag](the-notify-flag.md).</span></span>

<span data-ttu-id="3e397-129">Un appareil retourne l' \_ indicateur MCI Notify \_ réussis avec **mm \_ MCINOTIFY** quand l’action pour une commande se termine.</span><span class="sxs-lookup"><span data-stu-id="3e397-129">A device returns the MCI\_NOTIFY\_SUCCESSFUL flag with **MM\_MCINOTIFY** when the action for a command finishes.</span></span> <span data-ttu-id="3e397-130">Par exemple, un périphérique CD audio utilise cet indicateur pour la notification de la commande [**Play**](play.md) ( [**\_ lecture MCI**](mci-play.md)) à la fin de la lecture de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3e397-130">For example, a CD audio device uses this flag for notification for the [**play**](play.md) ( [**MCI\_PLAY**](mci-play.md)) command when the device finishes playing.</span></span> <span data-ttu-id="3e397-131">La commande de **lecture** est réussie uniquement lorsqu’elle atteint la position de fin spécifiée ou atteint la fin du média.</span><span class="sxs-lookup"><span data-stu-id="3e397-131">The **play** command is successful only when it reaches the specified end position or reaches the end of the media.</span></span> <span data-ttu-id="3e397-132">De même, les commandes [**Seek**](seek.md) ( [**MCI \_ Seek**](mci-seek.md)) et [**Record**](record.md) ( [**\_ enregistrement MCI**](mci-record.md)) ne retournent pas la \_ notification MCI \_ correctement tant qu’elles n’atteignent pas la position de fin spécifiée ou n’atteignent la fin du support.</span><span class="sxs-lookup"><span data-stu-id="3e397-132">Similarly, the [**seek**](seek.md) ( [**MCI\_SEEK**](mci-seek.md)) and [**record**](record.md) ( [**MCI\_RECORD**](mci-record.md)) commands do not return MCI\_NOTIFY\_SUCCESSFUL until they reach the specified end position or reach the end of the media.</span></span>

<span data-ttu-id="3e397-133">Un appareil retourne l' \_ \_ indicateur de notification abandonnée MCI avec **mm \_ MCINOTIFY** uniquement lorsqu’il reçoit une commande qui l’empêche de respecter les conditions de notification.</span><span class="sxs-lookup"><span data-stu-id="3e397-133">A device returns the MCI\_NOTIFY\_ABORTED flag with **MM\_MCINOTIFY** only when it receives a command that prevents it from meeting the notification conditions.</span></span> <span data-ttu-id="3e397-134">Par exemple, la commande de [**lecture**](play.md) n’interrompt pas la notification pour une commande de **lecture** précédente, à condition que la nouvelle commande ne change pas le sens de lecture ou ne change pas la position de fin.</span><span class="sxs-lookup"><span data-stu-id="3e397-134">For example, the [**play**](play.md) command would not abort notification for a previous **play** command provided that the new command does not change the play direction or change the ending position.</span></span> <span data-ttu-id="3e397-135">Les commandes [**Seek**](seek.md) et [**Record**](record.md) se comportent de la même façon.</span><span class="sxs-lookup"><span data-stu-id="3e397-135">The [**seek**](seek.md) and [**record**](record.md) commands behave similarly.</span></span> <span data-ttu-id="3e397-136">En outre, MCI n’envoie \_ pas \_ de notification MCI abandonnée lorsque la lecture ou l’enregistrement est suspendu avec la commande [**Pause**](pause.md) ( [**\_ Pause MCI**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="3e397-136">MCI also does not send MCI\_NOTIFY\_ABORTED when playback or recording is paused with the [**pause**](pause.md) ( [**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="3e397-137">L’envoi de la commande [**Resume**](resume.md) ( [**\_ reprise MCI**](mci-resume.md)) leur permet de continuer à respecter les conditions de rappel.</span><span class="sxs-lookup"><span data-stu-id="3e397-137">Sending the [**resume**](resume.md) ( [**MCI\_RESUME**](mci-resume.md)) command allows them to continue to meet the callback conditions.</span></span>

<span data-ttu-id="3e397-138">Lorsque votre application demande une notification pour une commande, vérifiez le retour d’erreur des fonctions [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ou [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3e397-138">When your application requests notification for a command, check the error return of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) functions.</span></span> <span data-ttu-id="3e397-139">Si ces fonctions rencontrent une erreur et retournent une valeur différente de zéro, MCI ne définit pas la notification pour la commande.</span><span class="sxs-lookup"><span data-stu-id="3e397-139">If these functions encounter an error and return a nonzero value, MCI will not set notification for the command.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e397-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e397-140">Requirements</span></span>



| <span data-ttu-id="3e397-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e397-141">Requirement</span></span> | <span data-ttu-id="3e397-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e397-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e397-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e397-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3e397-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e397-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3e397-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e397-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3e397-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e397-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3e397-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e397-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e397-148"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e397-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e397-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e397-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e397-150">MCI</span><span class="sxs-lookup"><span data-stu-id="3e397-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3e397-151">Messages MCI</span><span class="sxs-lookup"><span data-stu-id="3e397-151">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="3e397-152">**suspen**</span><span class="sxs-lookup"><span data-stu-id="3e397-152">**pause**</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="3e397-153">**répétition**</span><span class="sxs-lookup"><span data-stu-id="3e397-153">**play**</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="3e397-154">**enregistrement**</span><span class="sxs-lookup"><span data-stu-id="3e397-154">**record**</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="3e397-155">**sort**</span><span class="sxs-lookup"><span data-stu-id="3e397-155">**resume**</span></span>](resume.md)
</dt> <dt>

[<span data-ttu-id="3e397-156">**Demandez**</span><span class="sxs-lookup"><span data-stu-id="3e397-156">**seek**</span></span>](seek.md)
</dt> </dl>

 

