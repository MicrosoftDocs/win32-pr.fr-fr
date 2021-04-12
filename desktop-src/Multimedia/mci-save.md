---
title: Commande MCI_SAVE (mmsystem. h)
description: La \_ commande MCI Save enregistre le fichier actif.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- Commande MCI_SAVE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464626"
---
# <a name="mci_save-command"></a><span data-ttu-id="7f85f-104">\_Commande d’enregistrement MCI</span><span class="sxs-lookup"><span data-stu-id="7f85f-104">MCI\_SAVE command</span></span>

<span data-ttu-id="7f85f-105">La \_ commande MCI Save enregistre le fichier actif.</span><span class="sxs-lookup"><span data-stu-id="7f85f-105">The MCI\_SAVE command saves the current file.</span></span> <span data-ttu-id="7f85f-106">Les appareils qui modifient des fichiers ne doivent pas détruire la copie d’origine jusqu’à ce qu’ils reçoivent le message d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7f85f-106">Devices that modify files should not destroy the original copy until they receive the save message.</span></span> <span data-ttu-id="7f85f-107">Les périphériques vidéo-superposition et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="7f85f-107">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="7f85f-108">Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne les implémentent pas.</span><span class="sxs-lookup"><span data-stu-id="7f85f-108">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="7f85f-109">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="7f85f-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
);
```



## <a name="parameters"></a><span data-ttu-id="7f85f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f85f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f85f-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7f85f-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7f85f-112">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="7f85f-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="7f85f-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7f85f-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7f85f-114">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="7f85f-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="7f85f-115">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7f85f-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f85f-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span><span class="sxs-lookup"><span data-stu-id="7f85f-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span></span>
</dt> <dd>

<span data-ttu-id="7f85f-117">Pointeur vers une structure d' [**\_ \_ enregistrement MCI**](mci-save-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7f85f-117">Pointer to an [**MCI\_SAVE\_PARMS**](mci-save-parms.md) structure.</span></span> <span data-ttu-id="7f85f-118">(Les appareils avec des paramètres supplémentaires peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="7f85f-118">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f85f-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7f85f-119">Return Value</span></span>

<span data-ttu-id="7f85f-120">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="7f85f-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f85f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7f85f-121">Remarks</span></span>

<span data-ttu-id="7f85f-122">Cette commande est prise en charge par les appareils qui renvoient la **valeur true** lorsque vous appelez la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) avec l' \_ indicateur MCI GETDEVCAPS \_ CAN \_ Save.</span><span class="sxs-lookup"><span data-stu-id="7f85f-122">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_SAVE flag.</span></span>

<span data-ttu-id="7f85f-123">L’indicateur supplémentaire suivant s’applique à tous les périphériques prenant en charge [MCI \_ Save](/windows):</span><span class="sxs-lookup"><span data-stu-id="7f85f-123">The following additional flag applies to all devices supporting [MCI\_SAVE](/windows):</span></span>

<dl> <dt>

<span data-ttu-id="7f85f-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>\_fichier d’enregistrement MCI \_</span><span class="sxs-lookup"><span data-stu-id="7f85f-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI\_SAVE\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="7f85f-125">Le membre **lpFileName** de la structure identifiée par *lpSave* contient l’adresse d’une mémoire tampon contenant le nom de fichier de destination.</span><span class="sxs-lookup"><span data-stu-id="7f85f-125">The **lpfilename** member of the structure identified by *lpSave* contains an address of a buffer containing the destination filename.</span></span>

</dd> </dl>

<span data-ttu-id="7f85f-126">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="7f85f-126">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7f85f-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="7f85f-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="7f85f-128">Le membre **RC** de la structure identifiée par *lpSave* contient un rectangle valide.</span><span class="sxs-lookup"><span data-stu-id="7f85f-128">The **rc** member of the structure identified by *lpSave* contains a valid rectangle.</span></span> <span data-ttu-id="7f85f-129">Le rectangle spécifie une région de la mémoire tampon de trame qui sera enregistrée dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f85f-129">The rectangle specifies a region of the frame buffer that will be saved to the specified file.</span></span> <span data-ttu-id="7f85f-130">La première paire de coordonnées spécifie l’angle supérieur gauche du rectangle. la deuxième paire spécifie la largeur et la hauteur.</span><span class="sxs-lookup"><span data-stu-id="7f85f-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="7f85f-131">Les périphériques vidéo numériques doivent utiliser la commande [MCI \_ capture](mci-capture.md) pour capturer le contenu de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="7f85f-131">Digital-video devices must use the [MCI\_CAPTURE](mci-capture.md) command to capture the contents of the frame buffer.</span></span> <span data-ttu-id="7f85f-132">(Les périphériques de superposition vidéo doivent également utiliser MCI \_ CAPTURE.) Cet indicateur est destiné à la compatibilité avec le jeu de commandes de superposition vidéo MCI existant.</span><span class="sxs-lookup"><span data-stu-id="7f85f-132">(Video-overlay devices should also use MCI\_CAPTURE.) This flag is for compatibility with the existing MCI video-overlay command set.</span></span>

</dd> <dt>

<span data-ttu-id="7f85f-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>\_enregistrement d' \_ \_ abandon DGV MCI</span><span class="sxs-lookup"><span data-stu-id="7f85f-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI\_DGV\_SAVE\_ABORT</span></span>
</dt> <dd>

<span data-ttu-id="7f85f-134">Arrête une opération d’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="7f85f-134">Stops a save operation in progress.</span></span> <span data-ttu-id="7f85f-135">Il doit s’agir du seul indicateur présent.</span><span class="sxs-lookup"><span data-stu-id="7f85f-135">This must be the only flag present.</span></span>

</dd> <dt>

<span data-ttu-id="7f85f-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>\_enregistrement DGV \_ MCI \_ KEEPRESERVE</span><span class="sxs-lookup"><span data-stu-id="7f85f-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI\_DGV\_SAVE\_KEEPRESERVE</span></span>
</dt> <dd>

<span data-ttu-id="7f85f-137">L’espace disque restant inutilisé par rapport à la commande de [ \_ réserve MCI](mci-reserve.md) d’origine n’est pas libéré.</span><span class="sxs-lookup"><span data-stu-id="7f85f-137">Unused disk space left over from the original [MCI\_RESERVE](mci-reserve.md) command is not deallocated.</span></span>

</dd> </dl>

<span data-ttu-id="7f85f-138">Pour les périphériques vidéo numériques, le paramètre *lpSave* pointe vers une structure [**MCI \_ DGV \_ Save \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="7f85f-138">For digital-video devices, the *lpSave* parameter points to an [**MCI\_DGV\_SAVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) structure.</span></span>

<span data-ttu-id="7f85f-139">L’indicateur supplémentaire suivant est utilisé avec le type de périphérique de **superposition** :</span><span class="sxs-lookup"><span data-stu-id="7f85f-139">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7f85f-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="7f85f-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="7f85f-141">Le membre **RC** de la structure identifiée par *lpSave* contient un rectangle d’affichage valide indiquant la zone de la mémoire tampon vidéo à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="7f85f-141">The **rc** member of the structure identified by *lpSave* contains a valid display rectangle indicating the area of the video buffer to save.</span></span>

</dd> </dl>

<span data-ttu-id="7f85f-142">Pour les périphériques de superposition vidéo, le paramètre *lpSave* pointe vers une structure [**MCI \_ OVLY \_ Save \_ PARMS**](/previous-versions//dd743447(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7f85f-142">For video-overlay devices, the *lpSave* parameter points to an [**MCI\_OVLY\_SAVE\_PARMS**](/previous-versions//dd743447(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f85f-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f85f-143">Requirements</span></span>



| <span data-ttu-id="7f85f-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f85f-144">Requirement</span></span> | <span data-ttu-id="7f85f-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f85f-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f85f-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f85f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7f85f-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f85f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7f85f-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f85f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7f85f-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f85f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7f85f-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f85f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f85f-151"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f85f-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f85f-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f85f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f85f-153">MCI</span><span class="sxs-lookup"><span data-stu-id="7f85f-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7f85f-154">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="7f85f-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

