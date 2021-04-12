---
title: arrêter, commande
description: La commande arrêter arrête la lecture ou l’enregistrement. Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- commande arrêter Windows multimédia
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d70aa150c01bd4c0ceab10332b4eca8b15d041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384640"
---
# <a name="stop-command"></a><span data-ttu-id="71863-105">arrêter, commande</span><span class="sxs-lookup"><span data-stu-id="71863-105">stop command</span></span>

<span data-ttu-id="71863-106">La commande arrêter arrête la lecture ou l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="71863-106">The stop command stops playback or recording.</span></span> <span data-ttu-id="71863-107">Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="71863-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="71863-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="71863-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="71863-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71863-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71863-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="71863-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="71863-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="71863-111">Identifier of an MCI device.</span></span> <span data-ttu-id="71863-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="71863-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="71863-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span><span class="sxs-lookup"><span data-stu-id="71863-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span></span>
</dt> <dd>

<span data-ttu-id="71863-114">Pour les périphériques vidéo numériques, il peut s’agir de l’indicateur suivant.</span><span class="sxs-lookup"><span data-stu-id="71863-114">For digital-video devices, it can be the following flag.</span></span>



| <span data-ttu-id="71863-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="71863-115">Value</span></span> | <span data-ttu-id="71863-116">Signification</span><span class="sxs-lookup"><span data-stu-id="71863-116">Meaning</span></span>                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71863-117">inaltérable</span><span class="sxs-lookup"><span data-stu-id="71863-117">hold</span></span>  | <span data-ttu-id="71863-118">Empêche la libération des ressources requises pour redessiner une image toujours à l’écran.</span><span class="sxs-lookup"><span data-stu-id="71863-118">Prevents the release of resources required to redraw a still image on the screen.</span></span> <span data-ttu-id="71863-119">La mémoire tampon de trame reste disponible pour la mise à jour de l’affichage quand, par exemple, la fenêtre est déplacée.</span><span class="sxs-lookup"><span data-stu-id="71863-119">The frame buffer remains available for use in updating the display when, for example, the window is moved.</span></span> |



 

</dd> <dt>

<span data-ttu-id="71863-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="71863-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="71863-121">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="71863-121">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="71863-122">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="71863-122">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="71863-123">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="71863-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71863-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71863-124">Return Value</span></span>

<span data-ttu-id="71863-125">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="71863-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="71863-126">Notes</span><span class="sxs-lookup"><span data-stu-id="71863-126">Remarks</span></span>

<span data-ttu-id="71863-127">Pour les périphériques CD audio, la commande arrêter arrête la lecture et réinitialise la position actuelle de la piste à zéro.</span><span class="sxs-lookup"><span data-stu-id="71863-127">For CD audio devices, the stop command stops playback and resets the current track position to zero.</span></span>

## <a name="examples"></a><span data-ttu-id="71863-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="71863-128">Examples</span></span>

<span data-ttu-id="71863-129">La commande suivante arrête la lecture ou l’enregistrement sur l’appareil « mySound ».</span><span class="sxs-lookup"><span data-stu-id="71863-129">The following command stops playback or recording on the "mysound" device.</span></span>

``` syntax
stop mysound
```

## <a name="requirements"></a><span data-ttu-id="71863-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71863-130">Requirements</span></span>



| <span data-ttu-id="71863-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71863-131">Requirement</span></span> | <span data-ttu-id="71863-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="71863-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="71863-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71863-133">Minimum supported client</span></span><br/> | <span data-ttu-id="71863-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71863-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="71863-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71863-135">Minimum supported server</span></span><br/> | <span data-ttu-id="71863-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71863-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="71863-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71863-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71863-138">MCI</span><span class="sxs-lookup"><span data-stu-id="71863-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="71863-139">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="71863-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

