---
title: Commande MCI_UNFREEZE (mmsystem. h)
description: La commande MCI dégeler \_ restaure le mouvement vers une zone de la mémoire tampon vidéo figée avec la \_ commande de blocage MCI. Les périphériques numériques vidéo, VCR et vidéo reconnaissent cette commande.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- Commande MCI_UNFREEZE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105913"
---
# <a name="mci_unfreeze-command"></a><span data-ttu-id="186de-105">\_Commande MCI libérer</span><span class="sxs-lookup"><span data-stu-id="186de-105">MCI\_UNFREEZE command</span></span>

<span data-ttu-id="186de-106">La commande MCI dégeler \_ restaure le mouvement vers une zone de la mémoire tampon vidéo figée avec la commande de [ \_ blocage MCI](mci-freeze.md) .</span><span class="sxs-lookup"><span data-stu-id="186de-106">The MCI\_UNFREEZE command restores motion to an area of the video buffer frozen with the [MCI\_FREEZE](mci-freeze.md) command.</span></span> <span data-ttu-id="186de-107">Les périphériques numériques vidéo, VCR et vidéo reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="186de-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="186de-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="186de-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
);
```



## <a name="parameters"></a><span data-ttu-id="186de-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="186de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="186de-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="186de-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="186de-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="186de-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="186de-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="186de-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="186de-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="186de-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="186de-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="186de-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="186de-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span><span class="sxs-lookup"><span data-stu-id="186de-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="186de-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="186de-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="186de-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="186de-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="186de-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="186de-118">Return Value</span></span>

<span data-ttu-id="186de-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="186de-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="186de-120">Notes</span><span class="sxs-lookup"><span data-stu-id="186de-120">Remarks</span></span>

<span data-ttu-id="186de-121">L’indicateur supplémentaire suivant est utilisé avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="186de-121">The following additional flag is used with the **digitalvideo** device type:</span></span>

<span data-ttu-id="186de-122">\_DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="186de-122">MCI\_DGV\_RECT</span></span>

<span data-ttu-id="186de-123">Le membre **RC** de la structure identifiée par *lpUnfreeze* contient un rectangle d’affichage valide.</span><span class="sxs-lookup"><span data-stu-id="186de-123">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="186de-124">Le rectangle spécifie une zone dans la mémoire tampon de trame dont le bit de masque de verrouillage doit être désactivé sur les pixels.</span><span class="sxs-lookup"><span data-stu-id="186de-124">The rectangle specifies a region within the frame buffer whose pixels should have their lock mask bit turned off.</span></span> <span data-ttu-id="186de-125">Les régions rectangulaires sont spécifiées comme décrit pour la commande [ \_ put MCI](mci-put.md) .</span><span class="sxs-lookup"><span data-stu-id="186de-125">Rectangular regions are specified as described for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="186de-126">En cas d’omission, le rectangle a comme valeur par défaut la mémoire tampon de frame entière.</span><span class="sxs-lookup"><span data-stu-id="186de-126">If omitted, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="186de-127">En utilisant une séquence de commandes figer et dégeler avec différents rectangles, des modèles arbitraires de bits de masque de verrouillage peuvent être décrits.</span><span class="sxs-lookup"><span data-stu-id="186de-127">By using a sequence of freeze and unfreeze commands with different rectangles, arbitrary patterns of lock mask bits can be described.</span></span>

<span data-ttu-id="186de-128">Pour les périphériques vidéo numériques, le paramètre *lpUnfreeze* pointe vers une structure **MCI \_ DGV \_ dégeler \_** .</span><span class="sxs-lookup"><span data-stu-id="186de-128">For digital-video devices, the *lpUnfreeze* parameter points to an **MCI\_DGV\_UNFREEZE\_PARMS** structure.</span></span> <span data-ttu-id="186de-129">Pour plus d’informations, consultez les commentaires relatifs à la structure [**MCI \_ DGV \_ rect \_ PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="186de-129">For more information, see the comments for the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="186de-130">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="186de-130">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="186de-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>entrée de l’entrée de \_ magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="186de-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI\_VCR\_UNFREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="186de-132">Libérez l’entrée.</span><span class="sxs-lookup"><span data-stu-id="186de-132">Unfreeze the input.</span></span>

</dd> <dt>

<span data-ttu-id="186de-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>\_sortie du magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="186de-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI\_VCR\_UNFREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="186de-134">Libérez la sortie.</span><span class="sxs-lookup"><span data-stu-id="186de-134">Unfreeze the output.</span></span>

</dd> </dl>

<span data-ttu-id="186de-135">L’indicateur supplémentaire suivant est utilisé avec le type de périphérique de **superposition** :</span><span class="sxs-lookup"><span data-stu-id="186de-135">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="186de-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="186de-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="186de-137">Le membre **RC** de la structure identifiée par *lpUnfreeze* contient un rectangle d’affichage valide.</span><span class="sxs-lookup"><span data-stu-id="186de-137">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="186de-138">Il s’agit d’un paramètre obligatoire.</span><span class="sxs-lookup"><span data-stu-id="186de-138">This is a required parameter.</span></span>

</dd> </dl>

<span data-ttu-id="186de-139">Pour les périphériques de superposition vidéo, le paramètre *lpUnfreeze* pointe vers une structure [**MCI \_ OVLY \_ rect \_ PARMS**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="186de-139">For video-overlay devices, the *lpUnfreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="186de-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="186de-140">Requirements</span></span>



| <span data-ttu-id="186de-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="186de-141">Requirement</span></span> | <span data-ttu-id="186de-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="186de-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186de-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="186de-143">Minimum supported client</span></span><br/> | <span data-ttu-id="186de-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="186de-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="186de-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="186de-145">Minimum supported server</span></span><br/> | <span data-ttu-id="186de-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="186de-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="186de-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="186de-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="186de-148"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="186de-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="186de-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="186de-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186de-150">MCI</span><span class="sxs-lookup"><span data-stu-id="186de-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="186de-151">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="186de-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

