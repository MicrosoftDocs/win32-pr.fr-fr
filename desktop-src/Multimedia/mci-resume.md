---
title: Commande MCI_RESUME (mmsystem. h)
description: La \_ commande de reprise MCI provoque la reprise de l’opération suspendue par un appareil mis en pause.
ms.assetid: 2df712c1-5005-4e89-a439-a651076bbb73
keywords:
- Commande MCI_RESUME Windows multimédia
topic_type:
- apiref
api_name:
- MCI_RESUME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd83b6d753cd223235b8b11f2d4b0be4c828ec28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941786"
---
# <a name="mci_resume-command"></a><span data-ttu-id="1e615-104">\_Commande de reprise MCI</span><span class="sxs-lookup"><span data-stu-id="1e615-104">MCI\_RESUME command</span></span>

<span data-ttu-id="1e615-105">La \_ commande de reprise MCI provoque la reprise de l’opération suspendue par un appareil mis en pause.</span><span class="sxs-lookup"><span data-stu-id="1e615-105">The MCI\_RESUME command causes a paused device to resume the paused operation.</span></span> <span data-ttu-id="1e615-106">Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="1e615-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="1e615-107">Bien que les périphériques CD audio, MIDI Sequencer et videodisc reconnaissent également cette commande, les pilotes de périphérique MCICDA, MCISEQ et MCIPIONR ne le prennent pas en charge.</span><span class="sxs-lookup"><span data-stu-id="1e615-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="1e615-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="1e615-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESUME, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpResume
);
```



## <a name="parameters"></a><span data-ttu-id="1e615-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e615-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e615-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1e615-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1e615-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="1e615-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="1e615-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1e615-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1e615-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="1e615-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="1e615-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1e615-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e615-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span><span class="sxs-lookup"><span data-stu-id="1e615-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span></span>
</dt> <dd>

<span data-ttu-id="1e615-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1e615-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="1e615-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="1e615-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e615-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1e615-118">Return Value</span></span>

<span data-ttu-id="1e615-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="1e615-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e615-120">Notes</span><span class="sxs-lookup"><span data-stu-id="1e615-120">Remarks</span></span>

<span data-ttu-id="1e615-121">Cette commande reprend la lecture et l’enregistrement sans modifier le jeu de positions de suivi actuel avec [l' \_ enregistrement](mci-record.md) [MCI \_ Play](mci-play.md) ou MCI.</span><span class="sxs-lookup"><span data-stu-id="1e615-121">This command resumes playing and recording without changing the current track position set with [MCI\_PLAY](mci-play.md) or [MCI\_RECORD](mci-record.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e615-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e615-122">Requirements</span></span>



| <span data-ttu-id="1e615-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e615-123">Requirement</span></span> | <span data-ttu-id="1e615-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e615-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e615-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e615-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1e615-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e615-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1e615-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e615-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1e615-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e615-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1e615-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e615-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e615-130"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e615-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e615-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e615-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e615-132">MCI</span><span class="sxs-lookup"><span data-stu-id="1e615-132">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1e615-133">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="1e615-133">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

