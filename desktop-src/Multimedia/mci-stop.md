---
title: Commande MCI_STOP (mmsystem. h)
description: La \_ commande d’arrêt MCI arrête toutes les séquences de lecture et d’enregistrement, décharge toutes les mémoires tampons de lecture et arrête l’affichage des images vidéo. Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- Commande MCI_STOP Windows multimédia
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea5f2acbe39b0be64ebc640ae31ceede7591c7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384768"
---
# <a name="mci_stop-command"></a><span data-ttu-id="b581d-105">\_Commande d’arrêt MCI</span><span class="sxs-lookup"><span data-stu-id="b581d-105">MCI\_STOP command</span></span>

<span data-ttu-id="b581d-106">La \_ commande d’arrêt MCI arrête toutes les séquences de lecture et d’enregistrement, décharge toutes les mémoires tampons de lecture et arrête l’affichage des images vidéo.</span><span class="sxs-lookup"><span data-stu-id="b581d-106">The MCI\_STOP command stops all play and record sequences, unloads all play buffers, and ceases display of video images.</span></span> <span data-ttu-id="b581d-107">Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="b581d-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="b581d-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="b581d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
);
```



## <a name="parameters"></a><span data-ttu-id="b581d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b581d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b581d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b581d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b581d-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="b581d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b581d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b581d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b581d-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="b581d-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="b581d-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b581d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b581d-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span><span class="sxs-lookup"><span data-stu-id="b581d-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span></span>
</dt> <dd>

<span data-ttu-id="b581d-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="b581d-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="b581d-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="b581d-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b581d-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b581d-118">Return Value</span></span>

<span data-ttu-id="b581d-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="b581d-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b581d-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b581d-120">Remarks</span></span>

<span data-ttu-id="b581d-121">La différence entre les \_ commandes d’arrêt MCI et de [ \_ Pause MCI](mci-pause.md) dépend de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b581d-121">The difference between the MCI\_STOP and [MCI\_PAUSE](mci-pause.md) commands depends on the device.</span></span> <span data-ttu-id="b581d-122">Si possible, MCI \_ Pause interrompt l’opération de l’appareil, mais laisse l’appareil prêt à reprendre la lecture immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b581d-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span>

<span data-ttu-id="b581d-123">Pour le périphérique CD audio, MCI \_ Stop réinitialise la position actuelle de la piste à zéro ; en revanche, la [ \_ Pause MCI](mci-pause.md) maintient la position actuelle de la piste, anticipant ainsi que l’appareil reprend sa lecture.</span><span class="sxs-lookup"><span data-stu-id="b581d-123">For the CD audio device, MCI\_STOP resets the current track position to zero; in contrast, [MCI\_PAUSE](mci-pause.md) maintains the current track position, anticipating that the device will resume playing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b581d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b581d-124">Requirements</span></span>



| <span data-ttu-id="b581d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b581d-125">Requirement</span></span> | <span data-ttu-id="b581d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b581d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b581d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b581d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b581d-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b581d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b581d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b581d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b581d-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b581d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b581d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="b581d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b581d-132"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b581d-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b581d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b581d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b581d-134">MCI</span><span class="sxs-lookup"><span data-stu-id="b581d-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b581d-135">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="b581d-135">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

