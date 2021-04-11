---
title: Commande MCI_FREEZE (mmsystem. h)
description: La \_ commande MCI Freeze fige le mouvement à l’écran. Les appareils vidéo numérique, vidéo-superposition et VCR reconnaissent cette commande.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- Commande MCI_FREEZE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032554"
---
# <a name="mci_freeze-command"></a><span data-ttu-id="59bfc-105">\_Commande de blocage MCI</span><span class="sxs-lookup"><span data-stu-id="59bfc-105">MCI\_FREEZE command</span></span>

<span data-ttu-id="59bfc-106">La \_ commande MCI Freeze fige le mouvement à l’écran.</span><span class="sxs-lookup"><span data-stu-id="59bfc-106">The MCI\_FREEZE command freezes motion on the display.</span></span> <span data-ttu-id="59bfc-107">Les appareils vidéo numérique, vidéo-superposition et VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="59bfc-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="59bfc-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="59bfc-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
);
```



## <a name="parameters"></a><span data-ttu-id="59bfc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59bfc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59bfc-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="59bfc-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="59bfc-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="59bfc-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="59bfc-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="59bfc-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="59bfc-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="59bfc-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="59bfc-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="59bfc-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="59bfc-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span><span class="sxs-lookup"><span data-stu-id="59bfc-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span></span>
</dt> <dd>

<span data-ttu-id="59bfc-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="59bfc-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="59bfc-117">(Les appareils avec des paramètres supplémentaires peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="59bfc-117">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59bfc-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="59bfc-118">Return Value</span></span>

<span data-ttu-id="59bfc-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="59bfc-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="59bfc-120">Notes</span><span class="sxs-lookup"><span data-stu-id="59bfc-120">Remarks</span></span>

<span data-ttu-id="59bfc-121">Les indicateurs supplémentaires suivants sont utilisés par le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="59bfc-121">The following additional flags are used by the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="59bfc-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>\_ \_ blocage de DGV MCI \_ à</span><span class="sxs-lookup"><span data-stu-id="59bfc-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI\_DGV\_FREEZE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="59bfc-123">Le membre **RC** de la structure identifiée par *lpFreeze* contient un rectangle valide.</span><span class="sxs-lookup"><span data-stu-id="59bfc-123">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="59bfc-124">Le rectangle spécifie une zone dans la mémoire tampon de trame dont le bit de masque de verrouillage est activé pour chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="59bfc-124">The rectangle specifies a region within the frame buffer that will have the lock mask bit for each pixel turned on.</span></span> <span data-ttu-id="59bfc-125">Les pixels spécifiés ne sont pas mis à jour tant que le bit de masque de verrouillage n’est pas désactivé.</span><span class="sxs-lookup"><span data-stu-id="59bfc-125">The specified pixels will not be updated until their lock mask bit is turned off.</span></span> <span data-ttu-id="59bfc-126">Si cet indicateur n’est pas spécifié, le rectangle prend par défaut la totalité de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="59bfc-126">If this flag is not specified, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="59bfc-127">Cet indicateur est pris en charge uniquement si la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) retourne la **valeur true** pour l' \_ indicateur de verrouillage MCI DGV \_ GETDEVCAPS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="59bfc-127">This flag is supported only if the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command returns **TRUE** for the MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK flag.</span></span>

</dd> <dt>

<span data-ttu-id="59bfc-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI \_ DGV \_ bloqué \_ en dehors</span><span class="sxs-lookup"><span data-stu-id="59bfc-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI\_DGV\_FREEZE\_OUTSIDE</span></span>
</dt> <dd>

<span data-ttu-id="59bfc-129">La zone en dehors de la région spécifiée pour \_ l' \_ indicateur MCI DGV Freeze \_ est figée.</span><span class="sxs-lookup"><span data-stu-id="59bfc-129">The area outside the region specified for the MCI\_DGV\_FREEZE\_AT flag is frozen.</span></span>

</dd> </dl>

<span data-ttu-id="59bfc-130">Pour les périphériques vidéo numériques, le paramètre *lpFreeze* pointe vers une structure [**MCI \_ DGV \_ Freeze \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="59bfc-130">For digital-video devices, the *lpFreeze* parameter points to an [**MCI\_DGV\_FREEZE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="59bfc-131">Les indicateurs supplémentaires suivants sont utilisés par le type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="59bfc-131">The following additional flags are used by the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="59bfc-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>\_champ de \_ blocage du magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="59bfc-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI\_VCR\_FREEZE\_FIELD</span></span>
</dt> <dd>

<span data-ttu-id="59bfc-133">Figer un seul membre du frame actuel.</span><span class="sxs-lookup"><span data-stu-id="59bfc-133">Freeze only one member of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="59bfc-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>\_Frame de \_ blocage MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="59bfc-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI\_VCR\_FREEZE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="59bfc-135">Figer les deux champs du frame actuel.</span><span class="sxs-lookup"><span data-stu-id="59bfc-135">Freeze both fields of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="59bfc-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>\_ \_ entrée figer le magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="59bfc-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI\_VCR\_FREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="59bfc-137">Fige le frame actuel sur l’écran (utilisé pour l’enregistrement).</span><span class="sxs-lookup"><span data-stu-id="59bfc-137">Freeze the current frame on the screen (used for recording).</span></span>

</dd> <dt>

<span data-ttu-id="59bfc-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>\_sortie de \_ blocage de magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="59bfc-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI\_VCR\_FREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="59bfc-139">Figer le frame actuel à partir du magnétoscope (utilisé avec la capture de frame).</span><span class="sxs-lookup"><span data-stu-id="59bfc-139">Freeze the current frame from the VCR (used with frame capture).</span></span>

</dd> </dl>

<span data-ttu-id="59bfc-140">Pour les périphériques VCR, le paramètre *lpFreeze* pointe vers une structure de paramètres [**\_ génériques \_ MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="59bfc-140">For VCR devices, the *lpFreeze* parameter points to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

<span data-ttu-id="59bfc-141">L’indicateur supplémentaire suivant est utilisé par le type de périphérique de **superposition** :</span><span class="sxs-lookup"><span data-stu-id="59bfc-141">The following additional flag is used by the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="59bfc-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="59bfc-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="59bfc-143">Le membre **RC** de la structure identifiée par *lpFreeze* contient un rectangle valide.</span><span class="sxs-lookup"><span data-stu-id="59bfc-143">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="59bfc-144">Si cet indicateur n’est pas spécifié, le pilote de périphérique gèle l’ensemble du frame.</span><span class="sxs-lookup"><span data-stu-id="59bfc-144">If this flag is not specified, the device driver will freeze the entire frame.</span></span>

</dd> </dl>

<span data-ttu-id="59bfc-145">Pour les périphériques de superposition vidéo, le paramètre *lpFreeze* pointe vers une structure [**MCI \_ OVLY \_ rect \_ PARMS**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="59bfc-145">For video-overlay devices, the *lpFreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="59bfc-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59bfc-146">Requirements</span></span>



| <span data-ttu-id="59bfc-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59bfc-147">Requirement</span></span> | <span data-ttu-id="59bfc-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="59bfc-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59bfc-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59bfc-149">Minimum supported client</span></span><br/> | <span data-ttu-id="59bfc-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59bfc-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="59bfc-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59bfc-151">Minimum supported server</span></span><br/> | <span data-ttu-id="59bfc-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59bfc-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="59bfc-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="59bfc-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="59bfc-154"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59bfc-154"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59bfc-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59bfc-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59bfc-156">MCI</span><span class="sxs-lookup"><span data-stu-id="59bfc-156">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="59bfc-157">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="59bfc-157">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

