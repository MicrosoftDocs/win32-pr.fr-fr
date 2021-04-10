---
title: Commande MCI_LOAD (mmsystem. h)
description: La \_ commande de chargement MCI charge un fichier. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- Commande MCI_LOAD Windows multimédia
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941653"
---
# <a name="mci_load-command"></a><span data-ttu-id="2a3e2-105">\_Commande de chargement MCI</span><span class="sxs-lookup"><span data-stu-id="2a3e2-105">MCI\_LOAD command</span></span>

<span data-ttu-id="2a3e2-106">La \_ commande de chargement MCI charge un fichier.</span><span class="sxs-lookup"><span data-stu-id="2a3e2-106">The MCI\_LOAD command loads a file.</span></span> <span data-ttu-id="2a3e2-107">Les appareils vidéo et vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="2a3e2-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="2a3e2-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="2a3e2-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
);
```



## <a name="parameters"></a><span data-ttu-id="2a3e2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a3e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a3e2-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2a3e2-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2a3e2-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="2a3e2-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2a3e2-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2a3e2-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2a3e2-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="2a3e2-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="2a3e2-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2a3e2-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a3e2-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span><span class="sxs-lookup"><span data-stu-id="2a3e2-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span></span>
</dt> <dd>

<span data-ttu-id="2a3e2-116">Pointeur vers une structure de gestion de [**\_ \_ charge MCI**](mci-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="2a3e2-116">Pointer to an [**MCI\_LOAD\_PARMS**](mci-load-parms.md) structure.</span></span> <span data-ttu-id="2a3e2-117">(Les appareils avec des paramètres supplémentaires peuvent remplacer cette structure par une structure spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a3e2-117">(Devices with additional parameters might replace this structure with a device-specific structure.</span></span> <span data-ttu-id="2a3e2-118">Pour les périphériques vidéo numériques, le paramètre **lpLoad** pointe vers une structure [**MCI \_ DGV \_ load \_ PARMS**](/previous-versions//dd743391(v=vs.85)) .)</span><span class="sxs-lookup"><span data-stu-id="2a3e2-118">For digital-video devices, the **lpLoad** parameter points to an [**MCI\_DGV\_LOAD\_PARMS**](/previous-versions//dd743391(v=vs.85)) structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a3e2-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2a3e2-119">Return Value</span></span>

<span data-ttu-id="2a3e2-120">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="2a3e2-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a3e2-121">Notes</span><span class="sxs-lookup"><span data-stu-id="2a3e2-121">Remarks</span></span>

<span data-ttu-id="2a3e2-122">L’indicateur supplémentaire suivant s’applique à tous les appareils prenant en charge la \_ charge MCI :</span><span class="sxs-lookup"><span data-stu-id="2a3e2-122">The following additional flag applies to all devices supporting MCI\_LOAD:</span></span>

<dl> <dt>

<span data-ttu-id="2a3e2-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_charger le \_ fichier MCI</span><span class="sxs-lookup"><span data-stu-id="2a3e2-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI\_LOAD\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="2a3e2-124">Le membre **lpFileName** de la structure identifiée par *lpLoad* contient l’adresse d’une mémoire tampon contenant le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="2a3e2-124">The **lpfilename** member of the structure identified by *lpLoad* contains an address of a buffer containing the filename.</span></span>

</dd> </dl>

<span data-ttu-id="2a3e2-125">L’indicateur supplémentaire suivant est utilisé avec le type de périphérique de **superposition** :</span><span class="sxs-lookup"><span data-stu-id="2a3e2-125">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="2a3e2-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="2a3e2-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="2a3e2-127">Le membre **RC** de la structure identifiée par *lpLoad* contient un rectangle d’affichage valide qui identifie la zone de la mémoire tampon vidéo à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="2a3e2-127">The **rc** member of the structure identified by *lpLoad* contains a valid display rectangle that identifies the area of the video buffer to update.</span></span>

</dd> </dl>

<span data-ttu-id="2a3e2-128">Pour les périphériques de superposition vidéo, le paramètre *lpLoad* pointe vers une structure de paramètres de [**\_ \_ charge \_ MCI OVLY**](mci-ovly-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="2a3e2-128">For video-overlay devices, the *lpLoad* parameter points to an [**MCI\_OVLY\_LOAD\_PARMS**](mci-ovly-load-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a3e2-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a3e2-129">Requirements</span></span>



| <span data-ttu-id="2a3e2-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a3e2-130">Requirement</span></span> | <span data-ttu-id="2a3e2-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a3e2-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3e2-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a3e2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3e2-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a3e2-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2a3e2-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a3e2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3e2-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a3e2-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2a3e2-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a3e2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a3e2-137"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a3e2-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a3e2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a3e2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a3e2-139">MCI</span><span class="sxs-lookup"><span data-stu-id="2a3e2-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2a3e2-140">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="2a3e2-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

