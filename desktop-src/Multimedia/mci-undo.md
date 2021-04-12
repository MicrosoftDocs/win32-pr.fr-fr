---
title: Commande MCI_UNDO (mmsystem. h)
description: La commande d’annulation de la commande MCI annule \_ la dernière opération de collage MCI, de \_ copie MCI, de la \_ suppression MCI ou de la \_ \_ commande de collage MCI. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 1593457a-e680-4732-a89e-00f4eff7605a
keywords:
- Commande MCI_UNDO Windows multimédia
topic_type:
- apiref
api_name:
- MCI_UNDO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d099d95159afee8d91acb77eb64e8e80bee5425d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032473"
---
# <a name="mci_undo-command"></a><span data-ttu-id="03ab0-105">\_Commande d’annulation MCI</span><span class="sxs-lookup"><span data-stu-id="03ab0-105">MCI\_UNDO command</span></span>

<span data-ttu-id="03ab0-106">La commande d’annulation de la commande MCI annule \_ la dernière opération de collage [MCI \_ ](mci-cut.md), de [ \_ copie MCI](mci-copy.md), de la [ \_ suppression MCI](mci-delete.md)ou de la commande de [ \_ Collage MCI](mci-paste.md) .</span><span class="sxs-lookup"><span data-stu-id="03ab0-106">The MCI\_UNDO command reverses the most recent successful [MCI\_CUT](mci-cut.md), [MCI\_COPY](mci-copy.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="03ab0-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="03ab0-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="03ab0-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="03ab0-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNDO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUndo
);
```



## <a name="parameters"></a><span data-ttu-id="03ab0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03ab0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ab0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="03ab0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="03ab0-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="03ab0-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="03ab0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="03ab0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="03ab0-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="03ab0-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="03ab0-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="03ab0-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ab0-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span><span class="sxs-lookup"><span data-stu-id="03ab0-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span></span>
</dt> <dd>

<span data-ttu-id="03ab0-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="03ab0-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="03ab0-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="03ab0-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ab0-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03ab0-118">Return Value</span></span>

<span data-ttu-id="03ab0-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="03ab0-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="03ab0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03ab0-120">Requirements</span></span>



| <span data-ttu-id="03ab0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03ab0-121">Requirement</span></span> | <span data-ttu-id="03ab0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="03ab0-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ab0-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03ab0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="03ab0-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03ab0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="03ab0-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03ab0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="03ab0-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03ab0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="03ab0-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="03ab0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="03ab0-128"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03ab0-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03ab0-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03ab0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ab0-130">MCI</span><span class="sxs-lookup"><span data-stu-id="03ab0-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="03ab0-131">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="03ab0-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

