---
title: commande Close (Corecrt \_ IO. h)
description: La commande fermer ferme l’appareil ou le fichier et toutes les ressources associées. MCI décharge un appareil lorsque toutes les instances de l’appareil ou tous les fichiers sont fermés. Tous les périphériques MCI reconnaissent cette commande.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- commande fermer Windows Multimedia
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942008"
---
# <a name="close-command"></a><span data-ttu-id="4a9f5-106">commande Close</span><span class="sxs-lookup"><span data-stu-id="4a9f5-106">close command</span></span>

<span data-ttu-id="4a9f5-107">La commande fermer ferme l’appareil ou le fichier et toutes les ressources associées.</span><span class="sxs-lookup"><span data-stu-id="4a9f5-107">The close command closes the device or file and any associated resources.</span></span> <span data-ttu-id="4a9f5-108">MCI décharge un appareil lorsque toutes les instances de l’appareil ou tous les fichiers sont fermés.</span><span class="sxs-lookup"><span data-stu-id="4a9f5-108">MCI unloads a device when all instances of the device or all files are closed.</span></span> <span data-ttu-id="4a9f5-109">Tous les périphériques MCI reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="4a9f5-109">All MCI devices recognize this command.</span></span>

<span data-ttu-id="4a9f5-110">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="4a9f5-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4a9f5-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a9f5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a9f5-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4a9f5-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4a9f5-113">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="4a9f5-113">Identifier of an MCI device.</span></span> <span data-ttu-id="4a9f5-114">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="4a9f5-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4a9f5-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="4a9f5-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4a9f5-116">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="4a9f5-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="4a9f5-117">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4a9f5-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a9f5-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4a9f5-118">Return Value</span></span>

<span data-ttu-id="4a9f5-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="4a9f5-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a9f5-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4a9f5-120">Remarks</span></span>

<span data-ttu-id="4a9f5-121">Pour fermer tous les appareils ouverts par votre application, spécifiez l’identificateur de périphérique « tous » pour le paramètre *lpszDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="4a9f5-121">To close all devices opened by your application, specify the "all" device identifier for the *lpszDeviceID* parameter.</span></span>

<span data-ttu-id="4a9f5-122">La fermeture de l’appareil **cdaudio** arrête la lecture audio.</span><span class="sxs-lookup"><span data-stu-id="4a9f5-122">Closing the **cdaudio** device stops audio playback.</span></span>

<span data-ttu-id="4a9f5-123">**Windows 2000/XP :** Si l’appareil **cdaudio** est en lecture, la fermeture de l’appareil **cdaudio** n’entraîne pas l’arrêt de la lecture de l’audio.</span><span class="sxs-lookup"><span data-stu-id="4a9f5-123">**Windows 2000/XP:** If the **cdaudio** device is playing, closing the **cdaudio** device does not cause the audio to stop playing.</span></span> <span data-ttu-id="4a9f5-124">Envoyez d’abord la commande [Stop](stop.md) .</span><span class="sxs-lookup"><span data-stu-id="4a9f5-124">Send the [stop](stop.md) command first.</span></span>

## <a name="examples"></a><span data-ttu-id="4a9f5-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="4a9f5-125">Examples</span></span>

<span data-ttu-id="4a9f5-126">La commande suivante ferme l’appareil « mySound ».</span><span class="sxs-lookup"><span data-stu-id="4a9f5-126">The following command closes the "mysound" device.</span></span>

``` syntax
close mysound
```

## <a name="requirements"></a><span data-ttu-id="4a9f5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a9f5-127">Requirements</span></span>



| <span data-ttu-id="4a9f5-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a9f5-128">Requirement</span></span> | <span data-ttu-id="4a9f5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a9f5-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a9f5-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a9f5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4a9f5-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a9f5-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a9f5-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a9f5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4a9f5-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a9f5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a9f5-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a9f5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a9f5-135"><dt>Corecrt \_ IO. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a9f5-135"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a9f5-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a9f5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a9f5-137">MCI</span><span class="sxs-lookup"><span data-stu-id="4a9f5-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4a9f5-138">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="4a9f5-138">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

