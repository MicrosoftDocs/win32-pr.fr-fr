---
title: Commande MCI_SETTUNER (mmsystem. h)
description: La \_ commande MCI SETTUNER définit le canal actuel sur le tuner. Les périphériques VCR reconnaissent cette commande.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- Commande MCI_SETTUNER Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5774a927e1f41cf5d3bf42d6e93e532e0c2961a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033237"
---
# <a name="mci_settuner-command"></a><span data-ttu-id="11cd7-105">\_Commande MCI SETTUNER</span><span class="sxs-lookup"><span data-stu-id="11cd7-105">MCI\_SETTUNER command</span></span>

<span data-ttu-id="11cd7-106">La \_ commande MCI SETTUNER définit le canal actuel sur le tuner.</span><span class="sxs-lookup"><span data-stu-id="11cd7-106">The MCI\_SETTUNER command sets the current channel on the tuner.</span></span> <span data-ttu-id="11cd7-107">Les périphériques VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="11cd7-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="11cd7-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="11cd7-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
);
```



## <a name="parameters"></a><span data-ttu-id="11cd7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11cd7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11cd7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="11cd7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="11cd7-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="11cd7-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="11cd7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="11cd7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="11cd7-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="11cd7-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="11cd7-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="11cd7-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="11cd7-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span><span class="sxs-lookup"><span data-stu-id="11cd7-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span></span>
</dt> <dd>

<span data-ttu-id="11cd7-116">Pointeur vers une [**structure \_ \_ SETTUNER \_ PARMS de magnétoscope MCI**](mci-vcr-settuner-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="11cd7-116">Pointer to an [**MCI\_VCR\_SETTUNER\_PARMS**](mci-vcr-settuner-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11cd7-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="11cd7-117">Return Value</span></span>

<span data-ttu-id="11cd7-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="11cd7-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="11cd7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="11cd7-119">Remarks</span></span>

<span data-ttu-id="11cd7-120">Les indicateurs supplémentaires suivants s’appliquent aux périphériques VCR :</span><span class="sxs-lookup"><span data-stu-id="11cd7-120">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="11cd7-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>\_ \_ canal SETTUNER magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="11cd7-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI\_VCR\_SETTUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="11cd7-122">Le membre **dwChannel** de la structure identifiée par *lpSetTuner* contient le nouveau numéro de canal.</span><span class="sxs-lookup"><span data-stu-id="11cd7-122">The **dwChannel** member of the structure identified by *lpSetTuner* contains the new channel number.</span></span>

</dd> <dt>

<span data-ttu-id="11cd7-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>\_ \_ canal SETTUNER MCI \_ VCR \_</span><span class="sxs-lookup"><span data-stu-id="11cd7-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="11cd7-124">Décrémente le canal du tuner.</span><span class="sxs-lookup"><span data-stu-id="11cd7-124">Decrements the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="11cd7-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>\_SETTUNER de \_ canal \_ de \_ recherche \_ MCI VCR</span><span class="sxs-lookup"><span data-stu-id="11cd7-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="11cd7-126">Recherche un canal valide dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="11cd7-126">Searches for a valid channel in the reverse direction.</span></span>

</dd> <dt>

<span data-ttu-id="11cd7-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>\_magnétoscope MCI \_ SETTUNER \_ canal de \_ recherche \_</span><span class="sxs-lookup"><span data-stu-id="11cd7-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_UP</span></span>
</dt> <dd>

<span data-ttu-id="11cd7-128">Recherche un canal valide dans la direction vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="11cd7-128">Searches for a valid channel in the forward direction.</span></span>

</dd> <dt>

<span data-ttu-id="11cd7-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>\_ \_ canal SETTUNER MCI \_ VCR \_</span><span class="sxs-lookup"><span data-stu-id="11cd7-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_UP</span></span>
</dt> <dd>

<span data-ttu-id="11cd7-130">Incrémente le canal du tuner.</span><span class="sxs-lookup"><span data-stu-id="11cd7-130">Increments the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="11cd7-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>\_ \_ numéro SETTUNER magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="11cd7-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI\_VCR\_SETTUNER\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="11cd7-132">Le membre **dwNumber** de la structure identifiée par *lpSetTuner* spécifie le tuner logique à affecter avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="11cd7-132">The **dwNumber** member of the structure identified by *lpSetTuner* specifies which logical tuner to affect with this command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11cd7-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11cd7-133">Requirements</span></span>



| <span data-ttu-id="11cd7-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11cd7-134">Requirement</span></span> | <span data-ttu-id="11cd7-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="11cd7-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11cd7-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11cd7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="11cd7-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11cd7-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="11cd7-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11cd7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="11cd7-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11cd7-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="11cd7-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="11cd7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="11cd7-141"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11cd7-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11cd7-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11cd7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11cd7-143">MCI</span><span class="sxs-lookup"><span data-stu-id="11cd7-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="11cd7-144">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="11cd7-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

