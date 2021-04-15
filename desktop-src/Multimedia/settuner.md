---
title: commande settuner
description: La commande settuner modifie le tuner actuel ou le paramètre de canal du tuner actuel. Les périphériques VCR reconnaissent cette commande.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- commande settuner multimédia Windows
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467075"
---
# <a name="settuner-command"></a><span data-ttu-id="98812-105">commande settuner</span><span class="sxs-lookup"><span data-stu-id="98812-105">settuner command</span></span>

<span data-ttu-id="98812-106">La commande settuner modifie le tuner actuel ou le paramètre de canal du tuner actuel.</span><span class="sxs-lookup"><span data-stu-id="98812-106">The settuner command changes the current tuner or the channel setting of the current tuner.</span></span> <span data-ttu-id="98812-107">Les périphériques VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="98812-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="98812-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="98812-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="98812-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98812-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98812-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="98812-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="98812-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="98812-111">Identifier of an MCI device.</span></span> <span data-ttu-id="98812-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="98812-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="98812-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span><span class="sxs-lookup"><span data-stu-id="98812-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span></span>
</dt> <dd>

<span data-ttu-id="98812-114">Un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="98812-114">One of the following flags.</span></span>



| <span data-ttu-id="98812-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="98812-115">Value</span></span>                            | <span data-ttu-id="98812-116">Signification</span><span class="sxs-lookup"><span data-stu-id="98812-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98812-117">*canal* de canal</span><span class="sxs-lookup"><span data-stu-id="98812-117">channel *channel*</span></span>                | <span data-ttu-id="98812-118">Définit le tuner sur le *canal*.</span><span class="sxs-lookup"><span data-stu-id="98812-118">Sets the tuner to *channel*.</span></span> <span data-ttu-id="98812-119">Il se peut que vous ne puissiez pas modifier le canal pendant l’enregistrement, en fonction du magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="98812-119">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="98812-120">Un canal supérieur au maximum définit le tuner sur le canal maximal.</span><span class="sxs-lookup"><span data-stu-id="98812-120">A channel larger than the maximum sets the tuner to the maximum channel.</span></span>                                                                                                                    |
| <span data-ttu-id="98812-121">recherche de canal vers le canal vers le dessous</span><span class="sxs-lookup"><span data-stu-id="98812-121">channel seek upchannel seek down</span></span> | <span data-ttu-id="98812-122">Recherche le canal suivant avec un signal valide.</span><span class="sxs-lookup"><span data-stu-id="98812-122">Seeks the next channel with a valid signal.</span></span> <span data-ttu-id="98812-123">« Rechercher » incrémente le numéro de canal dans sa recherche.</span><span class="sxs-lookup"><span data-stu-id="98812-123">"Seek up" increments the channel number in its search.</span></span> <span data-ttu-id="98812-124">« Rechercher » décrémente le numéro de canal dans sa recherche.</span><span class="sxs-lookup"><span data-stu-id="98812-124">"Seek down" decrements the channel number in its search.</span></span> <span data-ttu-id="98812-125">Le tuner est encapsulé dans Channel 1 lorsque le nombre maximal de canaux est dépassé.</span><span class="sxs-lookup"><span data-stu-id="98812-125">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="98812-126">De même, lors de la recherche, le tuner revient au canal maximal.</span><span class="sxs-lookup"><span data-stu-id="98812-126">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span> |
| <span data-ttu-id="98812-127">canal vers le canal vers le PG.</span><span class="sxs-lookup"><span data-stu-id="98812-127">channel upchannel down</span></span>           | <span data-ttu-id="98812-128">Incrémente ou décrémente le canal du tuner.</span><span class="sxs-lookup"><span data-stu-id="98812-128">Increments or decrements the tuner channel.</span></span> <span data-ttu-id="98812-129">Il se peut que vous ne puissiez pas modifier le canal pendant l’enregistrement, en fonction du magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="98812-129">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="98812-130">Le tuner est encapsulé dans Channel 1 lorsque le nombre maximal de canaux est dépassé.</span><span class="sxs-lookup"><span data-stu-id="98812-130">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="98812-131">De même, lors de la recherche, le tuner revient au canal maximal.</span><span class="sxs-lookup"><span data-stu-id="98812-131">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span>                              |
| <span data-ttu-id="98812-132">nombre </span><span class="sxs-lookup"><span data-stu-id="98812-132">number *number*</span></span>                  | <span data-ttu-id="98812-133">Spécifie le tuner à affecter par la commande settuner.</span><span class="sxs-lookup"><span data-stu-id="98812-133">Specifies the tuner to be affected by the settuner command.</span></span> <span data-ttu-id="98812-134">Si le *nombre* n’est pas donné, la valeur par défaut de 1 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="98812-134">If *number* is not given, the default value of 1 is assumed.</span></span>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="98812-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="98812-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="98812-136">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="98812-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="98812-137">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="98812-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98812-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="98812-138">Return Value</span></span>

<span data-ttu-id="98812-139">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="98812-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="98812-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98812-140">Requirements</span></span>



| <span data-ttu-id="98812-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98812-141">Requirement</span></span> | <span data-ttu-id="98812-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="98812-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="98812-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98812-143">Minimum supported client</span></span><br/> | <span data-ttu-id="98812-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98812-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="98812-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98812-145">Minimum supported server</span></span><br/> | <span data-ttu-id="98812-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98812-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="98812-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98812-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98812-148">MCI</span><span class="sxs-lookup"><span data-stu-id="98812-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="98812-149">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="98812-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

