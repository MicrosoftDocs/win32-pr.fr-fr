---
title: Commande MCI_SIGNAL (mmsystem. h)
description: La \_ commande de signal MCI définit une position spécifiée dans l’espace de travail. Les périphériques vidéo numériques reconnaissent cette commande. MCIAVI ne prend en charge qu’un seul signal actif à la fois.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- Commande MCI_SIGNAL Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384476"
---
# <a name="mci_signal-command"></a><span data-ttu-id="435eb-106">\_Commande de signal MCI</span><span class="sxs-lookup"><span data-stu-id="435eb-106">MCI\_SIGNAL command</span></span>

<span data-ttu-id="435eb-107">La \_ commande de signal MCI définit une position spécifiée dans l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="435eb-107">The MCI\_SIGNAL command sets a specified position in the workspace.</span></span> <span data-ttu-id="435eb-108">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="435eb-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="435eb-109">MCIAVI ne prend en charge qu’un seul signal actif à la fois.</span><span class="sxs-lookup"><span data-stu-id="435eb-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="435eb-110">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="435eb-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
);
```



## <a name="parameters"></a><span data-ttu-id="435eb-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="435eb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="435eb-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="435eb-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="435eb-113">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="435eb-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="435eb-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="435eb-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="435eb-115">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="435eb-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="435eb-116">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="435eb-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="435eb-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span><span class="sxs-lookup"><span data-stu-id="435eb-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span></span>
</dt> <dd>

<span data-ttu-id="435eb-118">Pointeur vers une structure de valeur de [**\_ \_ signal \_ DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) .</span><span class="sxs-lookup"><span data-stu-id="435eb-118">Pointer to an [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="435eb-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="435eb-119">Return Value</span></span>

<span data-ttu-id="435eb-120">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="435eb-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="435eb-121">Notes</span><span class="sxs-lookup"><span data-stu-id="435eb-121">Remarks</span></span>

<span data-ttu-id="435eb-122">La fenêtre dont vous spécifiez le descripteur dans le membre **dwCallback** de la structure de [**\_ \_ signal \_ MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) reçoit le \_ message mm MCISIGNAL.</span><span class="sxs-lookup"><span data-stu-id="435eb-122">The window whose handle you specify in the **dwCallback** member of the [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure receives the MM\_MCISIGNAL message.</span></span>

<span data-ttu-id="435eb-123">Les indicateurs suivants s’appliquent aux périphériques vidéo numériques :</span><span class="sxs-lookup"><span data-stu-id="435eb-123">The following flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="435eb-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>\_signal MCI DGV \_ à l' \_ adresse</span><span class="sxs-lookup"><span data-stu-id="435eb-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI\_DGV\_SIGNAL\_AT</span></span>
</dt> <dd>

<span data-ttu-id="435eb-125">Une position de signal est incluse dans le membre **dwPosition** de la structure identifiée par *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="435eb-125">A signal position is included in the **dwPosition** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="435eb-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>\_annulation du \_ signal MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="435eb-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI\_DGV\_SIGNAL\_CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="435eb-127">Supprime la position de signal spécifiée par la valeur associée à MCI \_ DGV \_ signal \_ USERVAL.</span><span class="sxs-lookup"><span data-stu-id="435eb-127">Removes the signal position specified by the value associated with MCI\_DGV\_SIGNAL\_USERVAL.</span></span>

</dd> <dt>

<span data-ttu-id="435eb-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>\_signal DGV \_ MCI \_ chaque</span><span class="sxs-lookup"><span data-stu-id="435eb-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI\_DGV\_SIGNAL\_EVERY</span></span>
</dt> <dd>

<span data-ttu-id="435eb-129">Une valeur signal-period est incluse dans le membre **dwPeriod** de la structure identifiée par *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="435eb-129">A signal-period value is included in the **dwPeriod** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="435eb-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>\_position du \_ signal MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="435eb-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI\_DGV\_SIGNAL\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="435eb-131">L’appareil enverra la valeur de position avec le message Windows au lieu de la valeur spécifiée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="435eb-131">The device will send the position value with the Windows message instead of the user-specified value.</span></span>

</dd> <dt>

<span data-ttu-id="435eb-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI \_ DGV \_ signal \_ USERVAL</span><span class="sxs-lookup"><span data-stu-id="435eb-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI\_DGV\_SIGNAL\_USERVAL</span></span>
</dt> <dd>

<span data-ttu-id="435eb-133">Une valeur de données est incluse dans le membre **dwUserParm** de la structure identifiée par *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="435eb-133">A data value is included in the **dwUserParm** member of the structure identified by *lpSignal*.</span></span> <span data-ttu-id="435eb-134">La valeur de données associée à cette demande est reportée avec le message Windows.</span><span class="sxs-lookup"><span data-stu-id="435eb-134">The data value associated with this request is reported back with the Windows message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="435eb-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="435eb-135">Requirements</span></span>



| <span data-ttu-id="435eb-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="435eb-136">Requirement</span></span> | <span data-ttu-id="435eb-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="435eb-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="435eb-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="435eb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="435eb-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="435eb-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="435eb-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="435eb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="435eb-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="435eb-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="435eb-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="435eb-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="435eb-143"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="435eb-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="435eb-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="435eb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="435eb-145">MCI</span><span class="sxs-lookup"><span data-stu-id="435eb-145">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="435eb-146">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="435eb-146">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

