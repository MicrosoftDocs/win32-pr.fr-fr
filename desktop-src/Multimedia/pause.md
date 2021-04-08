---
title: pause, commande
description: La commande pause interrompt la diffusion ou l’enregistrement.
ms.assetid: 8fa1a40d-fdb1-4c9f-a8db-9dd6a0d83b87
keywords:
- commande suspendre Windows Multimedia
topic_type:
- apiref
api_name:
- pause
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25957defa4db514ce84f2e013dcc3751e21779b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844394"
---
# <a name="pause-command"></a><span data-ttu-id="685aa-104">pause, commande</span><span class="sxs-lookup"><span data-stu-id="685aa-104">pause command</span></span>

<span data-ttu-id="685aa-105">La commande pause interrompt la diffusion ou l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="685aa-105">The pause command pauses playing or recording.</span></span> <span data-ttu-id="685aa-106">La plupart des pilotes conservent la position actuelle et finissent par reprendre la lecture ou l’enregistrement à cette position.</span><span class="sxs-lookup"><span data-stu-id="685aa-106">Most drivers retain the current position and eventually resume playback or recording at this position.</span></span> <span data-ttu-id="685aa-107">Les périphériques CD audio, Digital-Video, MIDI Sequencer, VCR, videodisc et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="685aa-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="685aa-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="685aa-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("pause %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="685aa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="685aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685aa-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="685aa-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="685aa-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="685aa-111">Identifier of an MCI device.</span></span> <span data-ttu-id="685aa-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="685aa-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="685aa-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="685aa-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="685aa-114">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="685aa-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="685aa-115">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="685aa-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="685aa-116">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="685aa-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="685aa-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="685aa-117">Return Value</span></span>

<span data-ttu-id="685aa-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="685aa-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="685aa-119">Notes</span><span class="sxs-lookup"><span data-stu-id="685aa-119">Remarks</span></span>

<span data-ttu-id="685aa-120">Avec les pilotes MCICDA, MCISEQ et MCIPIONR, la commande pause fonctionne de la même façon que la commande [Stop](stop.md) .</span><span class="sxs-lookup"><span data-stu-id="685aa-120">With the MCICDA, MCISEQ, and MCIPIONR drivers, the pause command works the same as the [stop](stop.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="685aa-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="685aa-121">Examples</span></span>

<span data-ttu-id="685aa-122">La commande suivante suspend l’appareil « mySound ».</span><span class="sxs-lookup"><span data-stu-id="685aa-122">The following command pauses the "mysound" device.</span></span>

``` syntax
pause mysound
```

## <a name="requirements"></a><span data-ttu-id="685aa-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="685aa-123">Requirements</span></span>



| <span data-ttu-id="685aa-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="685aa-124">Requirement</span></span> | <span data-ttu-id="685aa-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="685aa-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="685aa-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="685aa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="685aa-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="685aa-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="685aa-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="685aa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="685aa-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="685aa-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="685aa-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="685aa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685aa-131">MCI</span><span class="sxs-lookup"><span data-stu-id="685aa-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="685aa-132">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="685aa-132">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="685aa-133">stop</span><span class="sxs-lookup"><span data-stu-id="685aa-133">stop</span></span>](stop.md)
</dt> </dl>

 

