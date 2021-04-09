---
title: Commande MCI_STEP (mmsystem. h)
description: La \_ commande d’étape MCI dénombre les frames d’un ou de plusieurs frames. Les appareils Digital-Video, VCR et CAV-format videodisc reconnaissent cette commande.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- Commande MCI_STEP Windows multimédia
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102845"
---
# <a name="mci_step-command"></a><span data-ttu-id="dda94-105">\_Commande d’étape MCI</span><span class="sxs-lookup"><span data-stu-id="dda94-105">MCI\_STEP command</span></span>

<span data-ttu-id="dda94-106">La \_ commande d’étape MCI dénombre les frames d’un ou de plusieurs frames.</span><span class="sxs-lookup"><span data-stu-id="dda94-106">The MCI\_STEP command steps the player one or more frames.</span></span> <span data-ttu-id="dda94-107">Les appareils Digital-Video, VCR et CAV-format videodisc reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="dda94-107">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="dda94-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="dda94-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
);
```



## <a name="parameters"></a><span data-ttu-id="dda94-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dda94-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda94-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="dda94-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="dda94-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="dda94-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="dda94-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="dda94-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="dda94-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="dda94-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="dda94-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="dda94-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="dda94-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span><span class="sxs-lookup"><span data-stu-id="dda94-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span></span>
</dt> <dd>

<span data-ttu-id="dda94-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="dda94-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="dda94-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="dda94-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dda94-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dda94-118">Return Value</span></span>

<span data-ttu-id="dda94-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="dda94-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dda94-120">Notes</span><span class="sxs-lookup"><span data-stu-id="dda94-120">Remarks</span></span>

<span data-ttu-id="dda94-121">Cette commande prend en charge les appareils qui renvoient la **valeur true** à l' \_ GETDEVCAPS MCI \_ a \_ un indicateur vidéo de la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="dda94-121">This command supports devices that return **TRUE** to the MCI\_GETDEVCAPS\_HAS\_VIDEO flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

<span data-ttu-id="dda94-122">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="dda94-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="dda94-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>\_ \_ frames d’étape DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="dda94-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI\_DGV\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="dda94-124">Le membre **dwFrames** de la structure identifiée par *lpStep* spécifie le nombre d’images à avancer avant d’afficher une autre image.</span><span class="sxs-lookup"><span data-stu-id="dda94-124">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="dda94-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>\_ \_ étape inverse DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="dda94-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI\_DGV\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="dda94-126">Étapes dans l’ordre inverse.</span><span class="sxs-lookup"><span data-stu-id="dda94-126">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="dda94-127">Pour les périphériques vidéo numériques, le paramètre *lpStep* pointe vers une structure [**MCI \_ DGV \_ Step \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) .</span><span class="sxs-lookup"><span data-stu-id="dda94-127">For digital-video devices, the *lpStep* parameter points to an [**MCI\_DGV\_STEP\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) structure.</span></span>

<span data-ttu-id="dda94-128">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="dda94-128">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="dda94-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>\_ \_ images pas à pas de magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="dda94-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI\_VCR\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="dda94-130">Le membre **dwFrames** de la structure identifiée par *lpStep* spécifie le nombre d’images à avancer avant d’afficher une autre image.</span><span class="sxs-lookup"><span data-stu-id="dda94-130">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="dda94-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>\_étape de magnétoscope MCI \_ \_ inversée</span><span class="sxs-lookup"><span data-stu-id="dda94-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI\_VCR\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="dda94-132">Étapes dans l’ordre inverse.</span><span class="sxs-lookup"><span data-stu-id="dda94-132">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="dda94-133">Pour les périphériques VCR, le paramètre *lpStep* pointe vers une structure d' [**\_ \_ étape \_ de magnétoscope MCI**](mci-vcr-step-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="dda94-133">For VCR devices, the *lpStep* parameter points to an [**MCI\_VCR\_STEP\_PARMS**](mci-vcr-step-parms.md) structure.</span></span>

<span data-ttu-id="dda94-134">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **videodisc** :</span><span class="sxs-lookup"><span data-stu-id="dda94-134">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="dda94-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>\_images d' \_ étape MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="dda94-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI\_VD\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="dda94-136">Le membre **dwFrames** de la structure identifiée par *lpStep* spécifie le nombre de frames à exécuter pas à pas.</span><span class="sxs-lookup"><span data-stu-id="dda94-136">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to step.</span></span>

</dd> <dt>

<span data-ttu-id="dda94-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>étape de l’étape MCI MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="dda94-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI\_VD\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="dda94-138">Étapes dans l’ordre inverse.</span><span class="sxs-lookup"><span data-stu-id="dda94-138">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="dda94-139">Pour les appareils videodisc, le paramètre *lpStep* pointe vers une structure d’étape de la [**\_ \_ séquence \_ MCI**](mci-vd-step-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="dda94-139">For videodisc devices, the *lpStep* parameter points to an [**MCI\_VD\_STEP\_PARMS**](mci-vd-step-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="dda94-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dda94-140">Requirements</span></span>



| <span data-ttu-id="dda94-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dda94-141">Requirement</span></span> | <span data-ttu-id="dda94-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="dda94-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dda94-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dda94-143">Minimum supported client</span></span><br/> | <span data-ttu-id="dda94-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dda94-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dda94-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dda94-145">Minimum supported server</span></span><br/> | <span data-ttu-id="dda94-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dda94-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dda94-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="dda94-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="dda94-148"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dda94-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dda94-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dda94-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda94-150">MCI</span><span class="sxs-lookup"><span data-stu-id="dda94-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="dda94-151">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="dda94-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

