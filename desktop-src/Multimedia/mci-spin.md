---
title: Commande MCI_SPIN (mmsystem. h)
description: La \_ commande MCI spin démarre l’appareil en la faisant pivoter vers le haut ou vers le haut. Les appareils Videodisc reconnaissent cette commande.
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- Commande MCI_SPIN Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SPIN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b154d9a2f54248ac6174e71a24d4afe74918d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384475"
---
# <a name="mci_spin-command"></a><span data-ttu-id="15929-105">\_Commande spin MCI</span><span class="sxs-lookup"><span data-stu-id="15929-105">MCI\_SPIN command</span></span>

<span data-ttu-id="15929-106">La \_ commande MCI spin démarre l’appareil en la faisant pivoter vers le haut ou vers le haut.</span><span class="sxs-lookup"><span data-stu-id="15929-106">The MCI\_SPIN command starts the device spinning up or down.</span></span> <span data-ttu-id="15929-107">Les appareils Videodisc reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="15929-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="15929-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="15929-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SPIN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSpin
);
```



## <a name="parameters"></a><span data-ttu-id="15929-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15929-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15929-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="15929-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="15929-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="15929-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="15929-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="15929-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="15929-113">\_Attente MCI Notify ou MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="15929-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="15929-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="15929-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="15929-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span><span class="sxs-lookup"><span data-stu-id="15929-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span></span>
</dt> <dd>

<span data-ttu-id="15929-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="15929-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="15929-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="15929-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15929-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="15929-118">Return Value</span></span>

<span data-ttu-id="15929-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="15929-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="15929-120">Notes</span><span class="sxs-lookup"><span data-stu-id="15929-120">Remarks</span></span>

<span data-ttu-id="15929-121">Les indicateurs supplémentaires suivants s’appliquent aux appareils videodisc :</span><span class="sxs-lookup"><span data-stu-id="15929-121">The following additional flags apply to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="15929-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI \_ VD \_ spin \_ Down</span><span class="sxs-lookup"><span data-stu-id="15929-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI\_VD\_SPIN\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="15929-123">Arrête la rotation du disque.</span><span class="sxs-lookup"><span data-stu-id="15929-123">Stops the disc spinning.</span></span>

</dd> <dt>

<span data-ttu-id="15929-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI \_ VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="15929-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI\_VD\_SPIN\_UP</span></span>
</dt> <dd>

<span data-ttu-id="15929-125">Démarre le disque en rotation.</span><span class="sxs-lookup"><span data-stu-id="15929-125">Starts the disc spinning.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15929-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15929-126">Requirements</span></span>



| <span data-ttu-id="15929-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15929-127">Requirement</span></span> | <span data-ttu-id="15929-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="15929-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15929-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15929-129">Minimum supported client</span></span><br/> | <span data-ttu-id="15929-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15929-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15929-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15929-131">Minimum supported server</span></span><br/> | <span data-ttu-id="15929-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15929-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="15929-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="15929-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="15929-134"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15929-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15929-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15929-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15929-136">MCI</span><span class="sxs-lookup"><span data-stu-id="15929-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="15929-137">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="15929-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

