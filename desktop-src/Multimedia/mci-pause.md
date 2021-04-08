---
title: Commande MCI_PAUSE (mmsystem. h)
description: La \_ commande MCI pause interrompt l’action en cours. Les périphériques CD audio, Digital-Video, MIDI Sequencer, VCR, videodisc et Waveform-Audio reconnaissent cette commande.
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- Commande MCI_PAUSE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_PAUSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076397ca9ab770d6f9c23cc5b64853bdd2f07ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739821"
---
# <a name="mci_pause-command"></a><span data-ttu-id="0fc21-105">\_Commande d’interruption MCI</span><span class="sxs-lookup"><span data-stu-id="0fc21-105">MCI\_PAUSE command</span></span>

<span data-ttu-id="0fc21-106">La \_ commande MCI pause interrompt l’action en cours.</span><span class="sxs-lookup"><span data-stu-id="0fc21-106">The MCI\_PAUSE command pauses the current action.</span></span> <span data-ttu-id="0fc21-107">Les périphériques CD audio, Digital-Video, MIDI Sequencer, VCR, videodisc et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="0fc21-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="0fc21-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="0fc21-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PAUSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpPause
);
```



## <a name="parameters"></a><span data-ttu-id="0fc21-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fc21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fc21-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0fc21-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0fc21-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="0fc21-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="0fc21-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="0fc21-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0fc21-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="0fc21-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="0fc21-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0fc21-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fc21-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span><span class="sxs-lookup"><span data-stu-id="0fc21-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span></span>
</dt> <dd>

<span data-ttu-id="0fc21-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="0fc21-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="0fc21-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="0fc21-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fc21-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0fc21-118">Return Value</span></span>

<span data-ttu-id="0fc21-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="0fc21-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fc21-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0fc21-120">Remarks</span></span>

<span data-ttu-id="0fc21-121">La différence entre les commandes d' [ \_ arrêt MCI](mci-stop.md) et de \_ Pause MCI dépend de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0fc21-121">The difference between the [MCI\_STOP](mci-stop.md) and MCI\_PAUSE commands depends on the device.</span></span> <span data-ttu-id="0fc21-122">Si possible, MCI \_ Pause interrompt l’opération de l’appareil, mais laisse l’appareil prêt à reprendre la lecture immédiatement.</span><span class="sxs-lookup"><span data-stu-id="0fc21-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span> <span data-ttu-id="0fc21-123">Avec les pilotes MCICDA, MCISEQ et MCIPIONR, la commande MCI \_ Pause fonctionne de la même façon que la \_ commande MCI stop.</span><span class="sxs-lookup"><span data-stu-id="0fc21-123">With the MCICDA, MCISEQ, and MCIPIONR drivers, the MCI\_PAUSE command works the same as the MCI\_STOP command.</span></span>

<span data-ttu-id="0fc21-124">Pour les périphériques vidéo numériques, le paramètre *lpPause* pointe vers une structure de [**\_ \_ pause \_ MCI DGV**](/previous-versions//dd743395(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0fc21-124">For digital-video devices, the *lpPause* parameter points to an [**MCI\_DGV\_PAUSE\_PARMS**](/previous-versions//dd743395(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fc21-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fc21-125">Requirements</span></span>



| <span data-ttu-id="0fc21-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fc21-126">Requirement</span></span> | <span data-ttu-id="0fc21-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fc21-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc21-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0fc21-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0fc21-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0fc21-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0fc21-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0fc21-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0fc21-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0fc21-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0fc21-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="0fc21-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fc21-133"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fc21-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc21-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fc21-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc21-135">MCI</span><span class="sxs-lookup"><span data-stu-id="0fc21-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0fc21-136">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="0fc21-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

