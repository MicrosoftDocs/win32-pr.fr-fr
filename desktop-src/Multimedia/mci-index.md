---
title: Commande MCI_INDEX (mmsystem. h)
description: La \_ commande d’index MCI active ou désactive l’affichage à l’écran. Les périphériques VCR reconnaissent cette commande.
ms.assetid: c0f18f28-3578-4648-9b75-2d3ede68b3df
keywords:
- Commande MCI_INDEX Windows multimédia
topic_type:
- apiref
api_name:
- MCI_INDEX
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e93890b8c3db1150bc7224b0fd8b6ee7475ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106204"
---
# <a name="mci_index-command"></a><span data-ttu-id="605e6-105">\_Commande d’index MCI</span><span class="sxs-lookup"><span data-stu-id="605e6-105">MCI\_INDEX command</span></span>

<span data-ttu-id="605e6-106">La \_ commande d’index MCI active ou désactive l’affichage à l’écran.</span><span class="sxs-lookup"><span data-stu-id="605e6-106">The MCI\_INDEX command turns the on-screen display on or off.</span></span> <span data-ttu-id="605e6-107">Les périphériques VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="605e6-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="605e6-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="605e6-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INDEX, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpIndex
);
```



## <a name="parameters"></a><span data-ttu-id="605e6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="605e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="605e6-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="605e6-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="605e6-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="605e6-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="605e6-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="605e6-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="605e6-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="605e6-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="605e6-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="605e6-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="605e6-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span><span class="sxs-lookup"><span data-stu-id="605e6-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span></span>
</dt> <dd>

<span data-ttu-id="605e6-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="605e6-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="605e6-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="605e6-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="605e6-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="605e6-118">Return Value</span></span>

<span data-ttu-id="605e6-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="605e6-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="605e6-120">Notes</span><span class="sxs-lookup"><span data-stu-id="605e6-120">Remarks</span></span>

<span data-ttu-id="605e6-121">Les informations présentées dans l’affichage à l’écran sont contrôlées par l' \_ indicateur de jeu d’index magnétoscope MCI \_ \_ dans la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="605e6-121">The information presented in the on-screen display is controlled by the MCI\_VCR\_SET\_INDEX flag in the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="605e6-122">Les indicateurs supplémentaires suivants s’appliquent aux périphériques VCR :</span><span class="sxs-lookup"><span data-stu-id="605e6-122">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="605e6-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="605e6-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="605e6-124">Désactive l’affichage à l’écran.</span><span class="sxs-lookup"><span data-stu-id="605e6-124">Turns on-screen display off.</span></span>

</dd> <dt>

<span data-ttu-id="605e6-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_</span><span class="sxs-lookup"><span data-stu-id="605e6-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="605e6-126">Active l’affichage à l’écran.</span><span class="sxs-lookup"><span data-stu-id="605e6-126">Turns on-screen display on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="605e6-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="605e6-127">Requirements</span></span>



| <span data-ttu-id="605e6-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="605e6-128">Requirement</span></span> | <span data-ttu-id="605e6-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="605e6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605e6-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="605e6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="605e6-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="605e6-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="605e6-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="605e6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="605e6-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="605e6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="605e6-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="605e6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="605e6-135"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="605e6-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="605e6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="605e6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605e6-137">MCI</span><span class="sxs-lookup"><span data-stu-id="605e6-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="605e6-138">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="605e6-138">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

