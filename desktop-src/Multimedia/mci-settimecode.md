---
title: Commande MCI_SETTIMECODE (mmsystem. h)
description: La \_ commande MCI SETTIMECODE active ou désactive l’enregistrement du code temporel pour un magnétoscope. Les périphériques VCR reconnaissent cette commande.
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- Commande MCI_SETTIMECODE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df0727f4386bad46b3fde7f2d816ce951850b8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513041"
---
# <a name="mci_settimecode-command"></a><span data-ttu-id="cf377-105">\_Commande MCI SETTIMECODE</span><span class="sxs-lookup"><span data-stu-id="cf377-105">MCI\_SETTIMECODE command</span></span>

<span data-ttu-id="cf377-106">La \_ commande MCI SETTIMECODE active ou désactive l’enregistrement du code temporel pour un magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="cf377-106">The MCI\_SETTIMECODE command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="cf377-107">Les périphériques VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="cf377-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="cf377-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="cf377-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
);
```



## <a name="parameters"></a><span data-ttu-id="cf377-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf377-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf377-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="cf377-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="cf377-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="cf377-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="cf377-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cf377-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cf377-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="cf377-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="cf377-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cf377-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf377-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span><span class="sxs-lookup"><span data-stu-id="cf377-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="cf377-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="cf377-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="cf377-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="cf377-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf377-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cf377-118">Return Value</span></span>

<span data-ttu-id="cf377-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="cf377-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf377-120">Notes</span><span class="sxs-lookup"><span data-stu-id="cf377-120">Remarks</span></span>

<span data-ttu-id="cf377-121">L’indicateur supplémentaire suivant s’applique aux périphériques VCR :</span><span class="sxs-lookup"><span data-stu-id="cf377-121">The following additional flag applies to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="cf377-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>\_ \_ enregistrement SETTIMECODE magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="cf377-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>MCI\_VCR\_SETTIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="cf377-123">Définit l’enregistrement du suivi du code temporel sur on ou OFF.</span><span class="sxs-lookup"><span data-stu-id="cf377-123">Sets the timecode track recording to on or off.</span></span> <span data-ttu-id="cf377-124">Cet indicateur est utilisé en association avec l’un des indicateurs supplémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="cf377-124">This flag is used in combination with one of the following additional flags:</span></span>

</dd> <dt>

<span data-ttu-id="cf377-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_</span><span class="sxs-lookup"><span data-stu-id="cf377-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="cf377-126">Enregistrement du code temporel sur.</span><span class="sxs-lookup"><span data-stu-id="cf377-126">Timecode recording on.</span></span>

</dd> <dt>

<span data-ttu-id="cf377-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="cf377-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="cf377-128">Enregistrement du code temporel désactivé.</span><span class="sxs-lookup"><span data-stu-id="cf377-128">Timecode recording off.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf377-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf377-129">Requirements</span></span>



| <span data-ttu-id="cf377-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf377-130">Requirement</span></span> | <span data-ttu-id="cf377-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf377-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf377-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf377-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cf377-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf377-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cf377-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf377-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cf377-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf377-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cf377-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf377-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf377-137"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf377-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf377-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf377-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf377-139">MCI</span><span class="sxs-lookup"><span data-stu-id="cf377-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cf377-140">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="cf377-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

