---
title: Commande MCI_MARK (mmsystem. h)
description: La \_ commande de marque MCI enregistre ou efface les marques qui peuvent être utilisées avec la \_ commande MCI Seek pour les recherches à grande vitesse. Les périphériques VCR reconnaissent cette commande.
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- Commande MCI_MARK Windows multimédia
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032551"
---
# <a name="mci_mark-command"></a><span data-ttu-id="dca95-105">\_Commande MCI Mark</span><span class="sxs-lookup"><span data-stu-id="dca95-105">MCI\_MARK command</span></span>

<span data-ttu-id="dca95-106">La \_ commande de marque MCI enregistre ou efface les marques qui peuvent être utilisées avec la commande [MCI \_ Seek](mci-seek.md) pour les recherches à grande vitesse.</span><span class="sxs-lookup"><span data-stu-id="dca95-106">The MCI\_MARK command records or erases marks that can be used with the [MCI\_SEEK](mci-seek.md) command for high-speed searches.</span></span> <span data-ttu-id="dca95-107">Les périphériques VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="dca95-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="dca95-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="dca95-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
);
```



## <a name="parameters"></a><span data-ttu-id="dca95-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dca95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dca95-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="dca95-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="dca95-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="dca95-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="dca95-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="dca95-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="dca95-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="dca95-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="dca95-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="dca95-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="dca95-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span><span class="sxs-lookup"><span data-stu-id="dca95-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span></span>
</dt> <dd>

<span data-ttu-id="dca95-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="dca95-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="dca95-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="dca95-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dca95-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dca95-118">Return Value</span></span>

<span data-ttu-id="dca95-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="dca95-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dca95-120">Notes</span><span class="sxs-lookup"><span data-stu-id="dca95-120">Remarks</span></span>

<span data-ttu-id="dca95-121">Les indicateurs supplémentaires suivants s’appliquent aux périphériques VCR :</span><span class="sxs-lookup"><span data-stu-id="dca95-121">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="dca95-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>\_ \_ effacement des marques MCI magnétoscope \_</span><span class="sxs-lookup"><span data-stu-id="dca95-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI\_VCR\_MARK\_ERASE</span></span>
</dt> <dd>

<span data-ttu-id="dca95-123">Efface une marque à la position actuelle, si elle existe.</span><span class="sxs-lookup"><span data-stu-id="dca95-123">Erases a mark at the current position if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="dca95-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>\_écriture de \_ marquage \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="dca95-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI\_VCR\_MARK\_WRITE</span></span>
</dt> <dd>

<span data-ttu-id="dca95-125">Écrit une marque à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="dca95-125">Writes a mark at the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dca95-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dca95-126">Requirements</span></span>



| <span data-ttu-id="dca95-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dca95-127">Requirement</span></span> | <span data-ttu-id="dca95-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="dca95-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dca95-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dca95-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dca95-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dca95-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dca95-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dca95-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dca95-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dca95-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dca95-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="dca95-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dca95-134"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dca95-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dca95-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dca95-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca95-136">MCI</span><span class="sxs-lookup"><span data-stu-id="dca95-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="dca95-137">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="dca95-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

