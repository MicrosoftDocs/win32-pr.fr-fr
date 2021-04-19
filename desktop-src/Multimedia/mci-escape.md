---
title: Commande MCI_ESCAPE (mmsystem. h)
description: La \_ commande d’échappement MCI envoie une chaîne directement à l’appareil. Les appareils Videodisc reconnaissent cette commande.
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- Commande MCI_ESCAPE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510542"
---
# <a name="mci_escape-command"></a><span data-ttu-id="8f819-105">\_Commande d’échappement MCI</span><span class="sxs-lookup"><span data-stu-id="8f819-105">MCI\_ESCAPE command</span></span>

<span data-ttu-id="8f819-106">La \_ commande d’échappement MCI envoie une chaîne directement à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f819-106">The MCI\_ESCAPE command sends a string directly to the device.</span></span> <span data-ttu-id="8f819-107">Les appareils Videodisc reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="8f819-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="8f819-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="8f819-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
);
```



## <a name="parameters"></a><span data-ttu-id="8f819-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f819-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f819-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8f819-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8f819-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="8f819-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="8f819-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8f819-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8f819-113">\_Attente MCI Notify ou MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="8f819-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="8f819-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8f819-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f819-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span><span class="sxs-lookup"><span data-stu-id="8f819-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span></span>
</dt> <dd>

<span data-ttu-id="8f819-116">Pointeur vers une structure d' [**\_ \_ échappement \_ MCI VD**](mci-vd-escape-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8f819-116">Pointer to an [**MCI\_VD\_ESCAPE\_PARMS**](mci-vd-escape-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f819-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8f819-117">Return Value</span></span>

<span data-ttu-id="8f819-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="8f819-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f819-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8f819-119">Remarks</span></span>

<span data-ttu-id="8f819-120">Les données envoyées avec l' \_ échappement MCI sont dépendantes de l’appareil et sont généralement transmises directement au matériel associé à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f819-120">The data sent with MCI\_ESCAPE is device-dependent and is usually passed directly to the hardware associated with the device.</span></span>

<span data-ttu-id="8f819-121">L’indicateur supplémentaire suivant s’applique aux appareils videodisc :</span><span class="sxs-lookup"><span data-stu-id="8f819-121">The following additional flag applies to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="8f819-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>\_chaîne d' \_ échappement \_ VD MCI</span><span class="sxs-lookup"><span data-stu-id="8f819-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>MCI\_VD\_ESCAPE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="8f819-123">Une chaîne de commande est spécifiée dans le membre **lpstrCommand** de la structure identifiée par *lpEscape*.</span><span class="sxs-lookup"><span data-stu-id="8f819-123">A command string is specified in the **lpstrCommand** member of the structure identified by *lpEscape*.</span></span> <span data-ttu-id="8f819-124">Cet indicateur est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8f819-124">This flag is required.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f819-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f819-125">Requirements</span></span>



| <span data-ttu-id="8f819-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f819-126">Requirement</span></span> | <span data-ttu-id="8f819-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f819-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f819-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f819-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8f819-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f819-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8f819-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f819-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8f819-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f819-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8f819-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f819-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f819-133"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f819-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f819-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f819-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f819-135">MCI</span><span class="sxs-lookup"><span data-stu-id="8f819-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8f819-136">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="8f819-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

