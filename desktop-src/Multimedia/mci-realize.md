---
title: Commande MCI_REALIZE (mmsystem. h)
description: La \_ commande MCI réalise fait en sorte qu’un appareil graphique réalise sa palette dans un contexte de périphérique (DC). Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- Commande MCI_REALIZE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509519"
---
# <a name="mci_realize-command"></a><span data-ttu-id="c00c8-105">\_Commande MCI réalise</span><span class="sxs-lookup"><span data-stu-id="c00c8-105">MCI\_REALIZE command</span></span>

<span data-ttu-id="c00c8-106">La \_ commande MCI réalise fait en sorte qu’un appareil graphique réalise sa palette dans un contexte de périphérique (DC).</span><span class="sxs-lookup"><span data-stu-id="c00c8-106">The MCI\_REALIZE command causes a graphic device to realize its palette into a device context (DC).</span></span> <span data-ttu-id="c00c8-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="c00c8-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="c00c8-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="c00c8-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
);
```



## <a name="parameters"></a><span data-ttu-id="c00c8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c00c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c00c8-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c00c8-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c00c8-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="c00c8-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c00c8-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c00c8-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c00c8-113">**MCI \_ NOTIFY**, **MCI \_ Wait** ou, pour les périphériques vidéo numériques, **\_ test MCI**.</span><span class="sxs-lookup"><span data-stu-id="c00c8-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="c00c8-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c00c8-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00c8-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span><span class="sxs-lookup"><span data-stu-id="c00c8-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span></span>
</dt> <dd>

<span data-ttu-id="c00c8-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c00c8-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="c00c8-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="c00c8-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c00c8-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c00c8-118">Return Value</span></span>

<span data-ttu-id="c00c8-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="c00c8-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c00c8-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c00c8-120">Remarks</span></span>

<span data-ttu-id="c00c8-121">Vous devez utiliser cette commande lorsque votre application reçoit le message [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) .</span><span class="sxs-lookup"><span data-stu-id="c00c8-121">You should use this command when your application receives the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message.</span></span>

<span data-ttu-id="c00c8-122">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil « Digitalvideo » :</span><span class="sxs-lookup"><span data-stu-id="c00c8-122">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="c00c8-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ réaliser \_ BKGD</span><span class="sxs-lookup"><span data-stu-id="c00c8-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI\_DGV\_REALIZE\_BKGD</span></span>
</dt> <dd>

<span data-ttu-id="c00c8-124">Réalise la palette sous forme de palette d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c00c8-124">Realizes the palette as a background palette.</span></span>

</dd> <dt>

<span data-ttu-id="c00c8-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI \_ DGV se \_ rendre \_ normal</span><span class="sxs-lookup"><span data-stu-id="c00c8-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI\_DGV\_REALIZE\_NORM</span></span>
</dt> <dd>

<span data-ttu-id="c00c8-126">Réalise une réalisation normale de la palette.</span><span class="sxs-lookup"><span data-stu-id="c00c8-126">Realizes the palette normally.</span></span> <span data-ttu-id="c00c8-127">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c00c8-127">This is the default.</span></span>

</dd> </dl>

<span data-ttu-id="c00c8-128">Pour les périphériques vidéo numériques, le paramètre *lpRealize* pointe vers une structure **MCI \_ \_** de réalisation.</span><span class="sxs-lookup"><span data-stu-id="c00c8-128">For digital-video devices, the *lpRealize* parameter points to an **MCI\_REALIZE\_PARMS** structure.</span></span> <span data-ttu-id="c00c8-129">Pour plus d’informations, consultez la section commentaires dans la structure des [**\_ \_ PARMS génériques MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c00c8-129">For more information, see comments in the [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c00c8-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c00c8-130">Requirements</span></span>



| <span data-ttu-id="c00c8-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c00c8-131">Requirement</span></span> | <span data-ttu-id="c00c8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c00c8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c00c8-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c00c8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c00c8-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c00c8-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c00c8-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c00c8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c00c8-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c00c8-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c00c8-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="c00c8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c00c8-138"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c00c8-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c00c8-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c00c8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c00c8-140">MCI</span><span class="sxs-lookup"><span data-stu-id="c00c8-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c00c8-141">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="c00c8-141">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

