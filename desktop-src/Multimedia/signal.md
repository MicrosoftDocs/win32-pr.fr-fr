---
title: signal, commande
description: La commande signal identifie une position spécifiée dans l’espace de travail en envoyant à l’application un \_ message MCISIGNAL mm. Les périphériques vidéo numériques reconnaissent cette commande. MCIAVI ne prend en charge qu’un seul signal actif à la fois.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- commande de signal Windows Multimedia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510973"
---
# <a name="signal-command"></a><span data-ttu-id="1eaae-106">signal, commande</span><span class="sxs-lookup"><span data-stu-id="1eaae-106">signal command</span></span>

<span data-ttu-id="1eaae-107">La commande signal identifie une position spécifiée dans l’espace de travail en envoyant à l’application un message [ \_ MCISIGNAL mm](mm-mcisignal.md) .</span><span class="sxs-lookup"><span data-stu-id="1eaae-107">The signal command identifies a specified position in the workspace by sending the application an [MM\_MCISIGNAL](mm-mcisignal.md) message.</span></span> <span data-ttu-id="1eaae-108">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="1eaae-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="1eaae-109">MCIAVI ne prend en charge qu’un seul signal actif à la fois.</span><span class="sxs-lookup"><span data-stu-id="1eaae-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="1eaae-110">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="1eaae-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="1eaae-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1eaae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eaae-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1eaae-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1eaae-113">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="1eaae-113">Identifier of an MCI device.</span></span> <span data-ttu-id="1eaae-114">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="1eaae-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="1eaae-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span><span class="sxs-lookup"><span data-stu-id="1eaae-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1eaae-116">Un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="1eaae-116">One of the following flags.</span></span>



| <span data-ttu-id="1eaae-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eaae-117">Value</span></span>            | <span data-ttu-id="1eaae-118">Signification</span><span class="sxs-lookup"><span data-stu-id="1eaae-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eaae-119">à la position</span><span class="sxs-lookup"><span data-stu-id="1eaae-119">at position</span></span>      | <span data-ttu-id="1eaae-120">Spécifie le frame pour appeler un signal.</span><span class="sxs-lookup"><span data-stu-id="1eaae-120">Specifies the frame to invoke a signal.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1eaae-121">annuler</span><span class="sxs-lookup"><span data-stu-id="1eaae-121">cancel</span></span>           | <span data-ttu-id="1eaae-122">Supprime les signaux de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="1eaae-122">Removes signals from the workspace.</span></span> <span data-ttu-id="1eaae-123">Un signal individuel est spécifié à l’aide de l’indicateur « uservalue ».</span><span class="sxs-lookup"><span data-stu-id="1eaae-123">An individual signal is specified by using the "uservalue" flag.</span></span> <span data-ttu-id="1eaae-124">Si l’indicateur « uservalue » n’est pas spécifié à l’aide de « Cancel », l’appareil annule tous les signaux.</span><span class="sxs-lookup"><span data-stu-id="1eaae-124">If the "uservalue" flag is not specified by using "cancel", the device cancels all signals.</span></span> <span data-ttu-id="1eaae-125">L’indicateur « Cancel » est incompatible avec les indicateurs « at », « Every » et « Return position ».</span><span class="sxs-lookup"><span data-stu-id="1eaae-125">The "cancel" flag is incompatible with the "at", "every", and "return position" flags.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1eaae-126">tous les *intervalles*</span><span class="sxs-lookup"><span data-stu-id="1eaae-126">every *interval*</span></span> | <span data-ttu-id="1eaae-127">Spécifie la période des signaux.</span><span class="sxs-lookup"><span data-stu-id="1eaae-127">Specifies the period of the signals.</span></span> <span data-ttu-id="1eaae-128">La valeur d' *intervalle* est spécifiée dans le format d’heure actuel. S’il est utilisé avec la *position*« at », les signaux sont placés dans l’espace de travail avec une marque de signal placée à la *position*.</span><span class="sxs-lookup"><span data-stu-id="1eaae-128">The *interval* value is specified in the current time format.If used with "at" *position*, signals are placed throughout the workspace with one signal mark placed at *position*.</span></span><br/> <span data-ttu-id="1eaae-129">Sans l’indicateur « at », les signaux sont placés dans l’espace de travail avec un signal à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="1eaae-129">Without the "at" flag, signals are placed throughout the workspace with one signal at the current position.</span></span><br/> <span data-ttu-id="1eaae-130">Si cet indicateur est omis, seule la position indiquée par l’indicateur « at » est marquée.</span><span class="sxs-lookup"><span data-stu-id="1eaae-130">If this flag is omitted, only the position indicated by the "at" flag is marked.</span></span><br/> <span data-ttu-id="1eaae-131">Si la valeur d' *intervalle* est inférieure à la fréquence minimale prise en charge par un appareil, elle utilise sa valeur minimale.</span><span class="sxs-lookup"><span data-stu-id="1eaae-131">If the *interval* value is less than the minimum frequency supported by a device, it will use its minimum value.</span></span><br/> |
| <span data-ttu-id="1eaae-132">position de retour</span><span class="sxs-lookup"><span data-stu-id="1eaae-132">return position</span></span>  | <span data-ttu-id="1eaae-133">Indique que l’appareil doit envoyer la valeur de position au lieu de l’identificateur « uservalue » dans le message de signalisation.</span><span class="sxs-lookup"><span data-stu-id="1eaae-133">Indicates the device should send the position value instead of the "uservalue" identifier in the signaling message.</span></span> <span data-ttu-id="1eaae-134">L’identificateur « uservalue » peut toujours être utilisé pour annuler ou redéfinir les marques signalées.</span><span class="sxs-lookup"><span data-stu-id="1eaae-134">The "uservalue" identifier can still be used to cancel or to redefine the signal marks.</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="1eaae-135">*ID* uservalue</span><span class="sxs-lookup"><span data-stu-id="1eaae-135">uservalue *id*</span></span>   | <span data-ttu-id="1eaae-136">Spécifie un identificateur qui est renvoyé avec le message de signalisation.</span><span class="sxs-lookup"><span data-stu-id="1eaae-136">Specifies an identifier that is reported back with the signaling message.</span></span> <span data-ttu-id="1eaae-137">Cet identificateur agit comme un identificateur qui peut être utilisé avec d’autres commandes de **signal** pour faire référence à ce paramètre de **signal** .</span><span class="sxs-lookup"><span data-stu-id="1eaae-137">This identifier acts as an identifier that can be used with other **signal** commands to reference this **signal** setting.</span></span> <span data-ttu-id="1eaae-138">En cas d’omission, la valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="1eaae-138">If omitted, the default value is zero.</span></span>                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="1eaae-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="1eaae-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1eaae-140">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="1eaae-140">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="1eaae-141">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1eaae-141">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eaae-142">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1eaae-142">Return Value</span></span>

<span data-ttu-id="1eaae-143">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="1eaae-143">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eaae-144">Notes</span><span class="sxs-lookup"><span data-stu-id="1eaae-144">Remarks</span></span>

<span data-ttu-id="1eaae-145">Le handle de fenêtre utilisé pour la notification des messages de saisie semi-automatique de commande est également utilisé pour la signalisation.</span><span class="sxs-lookup"><span data-stu-id="1eaae-145">The window handle used for notification of command completion messages is also used for signaling.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eaae-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1eaae-146">Requirements</span></span>



| <span data-ttu-id="1eaae-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eaae-147">Requirement</span></span> | <span data-ttu-id="1eaae-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eaae-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1eaae-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eaae-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1eaae-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1eaae-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1eaae-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eaae-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1eaae-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1eaae-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1eaae-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eaae-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eaae-154">MCI</span><span class="sxs-lookup"><span data-stu-id="1eaae-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1eaae-155">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="1eaae-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="1eaae-156">\_MCISIGNAL mm</span><span class="sxs-lookup"><span data-stu-id="1eaae-156">MM\_MCISIGNAL</span></span>](mm-mcisignal.md)
</dt> </dl>

 

