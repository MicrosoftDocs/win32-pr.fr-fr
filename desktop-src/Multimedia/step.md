---
title: commande Step
description: La commande Step exécute un ou plusieurs frames vers l’avant ou vers l’arrière. L’action par défaut consiste à avancer d’une image. Les appareils Digital-Video, VCR et CAV-format videodisc reconnaissent cette commande.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- commande Step Windows multimédia
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465219"
---
# <a name="step-command"></a><span data-ttu-id="f800b-106">commande Step</span><span class="sxs-lookup"><span data-stu-id="f800b-106">step command</span></span>

<span data-ttu-id="f800b-107">La commande Step exécute un ou plusieurs frames vers l’avant ou vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="f800b-107">The step command steps the play one or more frames forward or reverse.</span></span> <span data-ttu-id="f800b-108">L’action par défaut consiste à avancer d’une image.</span><span class="sxs-lookup"><span data-stu-id="f800b-108">The default action is to step forward one frame.</span></span> <span data-ttu-id="f800b-109">Les appareils Digital-Video, VCR et CAV-format videodisc reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="f800b-109">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="f800b-110">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="f800b-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f800b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f800b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f800b-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f800b-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f800b-113">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="f800b-113">Identifier of an MCI device.</span></span> <span data-ttu-id="f800b-114">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="f800b-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f800b-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span><span class="sxs-lookup"><span data-stu-id="f800b-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f800b-116">L’un des indicateurs suivants, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="f800b-116">One or both of the following flags.</span></span>



| <span data-ttu-id="f800b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f800b-117">Value</span></span>       | <span data-ttu-id="f800b-118">Signification</span><span class="sxs-lookup"><span data-stu-id="f800b-118">Meaning</span></span>                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f800b-119">par *frames*</span><span class="sxs-lookup"><span data-stu-id="f800b-119">by *frames*</span></span> | <span data-ttu-id="f800b-120">Indique le nombre de frames à exécuter pas à pas.</span><span class="sxs-lookup"><span data-stu-id="f800b-120">Indicates the number of frames to step.</span></span> <span data-ttu-id="f800b-121">Si vous spécifiez une valeur de *trame* négative, vous ne pouvez pas spécifier l’indicateur « inverseur ».</span><span class="sxs-lookup"><span data-stu-id="f800b-121">If you specify a negative *frames* value, you cannot specify the "reverse" flag.</span></span> |
| <span data-ttu-id="f800b-122">reverse</span><span class="sxs-lookup"><span data-stu-id="f800b-122">reverse</span></span>     | <span data-ttu-id="f800b-123">Effectuez un pas à pas détaillé des frames.</span><span class="sxs-lookup"><span data-stu-id="f800b-123">Step the frames in reverse.</span></span>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="f800b-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f800b-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f800b-125">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="f800b-125">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="f800b-126">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="f800b-126">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="f800b-127">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f800b-127">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f800b-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f800b-128">Return Value</span></span>

<span data-ttu-id="f800b-129">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="f800b-129">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f800b-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f800b-130">Requirements</span></span>



| <span data-ttu-id="f800b-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f800b-131">Requirement</span></span> | <span data-ttu-id="f800b-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f800b-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f800b-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f800b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f800b-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f800b-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f800b-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f800b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f800b-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f800b-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f800b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f800b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f800b-138">MCI</span><span class="sxs-lookup"><span data-stu-id="f800b-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f800b-139">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="f800b-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

