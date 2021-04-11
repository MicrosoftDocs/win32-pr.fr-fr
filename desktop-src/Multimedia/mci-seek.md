---
title: Commande MCI_SEEK (mmsystem. h)
description: La \_ commande MCI Seek change la position actuelle dans le contenu aussi rapidement que possible.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- Commande MCI_SEEK Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032549"
---
# <a name="mci_seek-command"></a><span data-ttu-id="ac638-104">\_Commande MCI Seek</span><span class="sxs-lookup"><span data-stu-id="ac638-104">MCI\_SEEK command</span></span>

<span data-ttu-id="ac638-105">La \_ commande MCI Seek change la position actuelle dans le contenu aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="ac638-105">The MCI\_SEEK command changes the current position in the content as quickly as possible.</span></span> <span data-ttu-id="ac638-106">La sortie vidéo et audio est désactivée au cours de la recherche.</span><span class="sxs-lookup"><span data-stu-id="ac638-106">Video and audio output are disabled during the seek.</span></span> <span data-ttu-id="ac638-107">Une fois la recherche terminée, l’appareil est arrêté.</span><span class="sxs-lookup"><span data-stu-id="ac638-107">After the seek is complete, the device is stopped.</span></span> <span data-ttu-id="ac638-108">Les périphériques CD audio, Digital-Video, MIDI Sequencer, VCR, videodisc et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="ac638-108">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="ac638-109">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="ac638-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
);
```



## <a name="parameters"></a><span data-ttu-id="ac638-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac638-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac638-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ac638-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ac638-112">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="ac638-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ac638-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ac638-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ac638-114">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="ac638-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="ac638-115">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ac638-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac638-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span><span class="sxs-lookup"><span data-stu-id="ac638-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span></span>
</dt> <dd>

<span data-ttu-id="ac638-117">Pointeur vers une structure de [**\_ \_ recherche MCI**](mci-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ac638-117">Pointer to an [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="ac638-118">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="ac638-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac638-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ac638-119">Return Value</span></span>

<span data-ttu-id="ac638-120">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="ac638-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac638-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ac638-121">Remarks</span></span>

<span data-ttu-id="ac638-122">Si la taille de l’échantillon de données d’un appareil est supérieure à 1 octet (comme avec les données stéréo audio Wave), cette commande passe au début de l’échantillon le plus proche lorsqu’une position spécifiée ne coïncide pas avec le début d’un échantillon.</span><span class="sxs-lookup"><span data-stu-id="ac638-122">If a data sample size for a device is larger than 1 byte (such as with waveform-audio stereo data), this command moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

<span data-ttu-id="ac638-123">Les indicateurs supplémentaires suivants s’appliquent à tous les appareils prenant en charge MCI \_ Seek :</span><span class="sxs-lookup"><span data-stu-id="ac638-123">The following additional flags apply to all devices supporting MCI\_SEEK:</span></span>

<dl> <dt>

<span data-ttu-id="ac638-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>\_recherche MCI \_ à la \_ fin</span><span class="sxs-lookup"><span data-stu-id="ac638-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI\_SEEK\_TO\_END</span></span>
</dt> <dd>

<span data-ttu-id="ac638-125">Recherchez la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="ac638-125">Seek to the end of the content.</span></span>

</dd> <dt>

<span data-ttu-id="ac638-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI \_ Seek \_ to \_ Start</span><span class="sxs-lookup"><span data-stu-id="ac638-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI\_SEEK\_TO\_START</span></span>
</dt> <dd>

<span data-ttu-id="ac638-127">Recherche jusqu’au début du contenu.</span><span class="sxs-lookup"><span data-stu-id="ac638-127">Seek to the beginning of the content.</span></span>

</dd> <dt>

<span data-ttu-id="ac638-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers</span><span class="sxs-lookup"><span data-stu-id="ac638-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="ac638-129">Une position est incluse dans le membre **dwTo** de la structure identifiée par *lpSeek*.</span><span class="sxs-lookup"><span data-stu-id="ac638-129">A position is included in the **dwTo** member of the structure identified by *lpSeek*.</span></span> <span data-ttu-id="ac638-130">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="ac638-130">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="ac638-131">N’utilisez pas cet indicateur avec MCI \_ Seek \_ to \_ end ou MCI \_ Seek \_ to \_ Start.</span><span class="sxs-lookup"><span data-stu-id="ac638-131">Do not use this flag with MCI\_SEEK\_TO\_END or MCI\_SEEK\_TO\_START.</span></span>

</dd> </dl>

<span data-ttu-id="ac638-132">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="ac638-132">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ac638-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>\_magnétoscope \_ de recherche MCI \_ à</span><span class="sxs-lookup"><span data-stu-id="ac638-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI\_VCR\_SEEK\_AT</span></span>
</dt> <dd>

<span data-ttu-id="ac638-134">Le membre **dwAt** de la structure identifiée par *lpSeek* contient une heure de début de la commande entière.</span><span class="sxs-lookup"><span data-stu-id="ac638-134">The **dwAt** member of the structure identified by *lpSeek* contains a time when the entire command begins.</span></span>

</dd> <dt>

<span data-ttu-id="ac638-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>\_marque de \_ recherche MCI magnétoscope \_</span><span class="sxs-lookup"><span data-stu-id="ac638-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI\_VCR\_SEEK\_MARK</span></span>
</dt> <dd>

<span data-ttu-id="ac638-136">Le membre **dwMark** de la structure identifiée par *lpSeek* contient la marque numérotée à rechercher.</span><span class="sxs-lookup"><span data-stu-id="ac638-136">The **dwMark** member of the structure identified by *lpSeek* contains the numbered mark to search for.</span></span>

</dd> <dt>

<span data-ttu-id="ac638-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>l' \_ inverse de la recherche MCI magnétoscope \_ \_</span><span class="sxs-lookup"><span data-stu-id="ac638-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI\_VCR\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="ac638-138">La direction de la recherche est inversée ; utilisé uniquement avec l' \_ indicateur de marque de recherche de magnétoscope MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ac638-138">Seek direction is reverse; this is used only with the MCI\_VCR\_SEEK\_MARK flag.</span></span>

</dd> </dl>

<span data-ttu-id="ac638-139">Pour les périphériques VCR, le paramètre *lpSeek* pointe vers une structure de [**\_ \_ recherche \_ de magnétoscope MCI**](mci-vcr-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ac638-139">For VCR devices, the *lpSeek* parameter points to an [**MCI\_VCR\_SEEK\_PARMS**](mci-vcr-seek-parms.md) structure.</span></span>

<span data-ttu-id="ac638-140">L’indicateur supplémentaire suivant est utilisé avec le type d’appareil **videodisc** :</span><span class="sxs-lookup"><span data-stu-id="ac638-140">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ac638-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI \_ de \_ recherche \_ MCI</span><span class="sxs-lookup"><span data-stu-id="ac638-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI\_VD\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="ac638-142">La direction de la recherche est inversée.</span><span class="sxs-lookup"><span data-stu-id="ac638-142">Seek direction is reverse.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac638-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac638-143">Requirements</span></span>



| <span data-ttu-id="ac638-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac638-144">Requirement</span></span> | <span data-ttu-id="ac638-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac638-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac638-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac638-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ac638-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac638-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ac638-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac638-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ac638-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac638-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ac638-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac638-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac638-151"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac638-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac638-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac638-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac638-153">MCI</span><span class="sxs-lookup"><span data-stu-id="ac638-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ac638-154">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="ac638-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

