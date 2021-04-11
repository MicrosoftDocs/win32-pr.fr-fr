---
title: Commande MCI_RESERVE (mmsystem. h)
description: La \_ commande de réserve MCI alloue de l’espace disque contigu à l’espace de travail de l’instance de pilote de périphérique afin de l’utiliser lors de l’enregistrement suivant. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- Commande MCI_RESERVE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942594"
---
# <a name="mci_reserve-command"></a><span data-ttu-id="63d58-105">\_Commande de réserve MCI</span><span class="sxs-lookup"><span data-stu-id="63d58-105">MCI\_RESERVE command</span></span>

<span data-ttu-id="63d58-106">La \_ commande de réserve MCI alloue de l’espace disque contigu à l’espace de travail de l’instance de pilote de périphérique afin de l’utiliser lors de l’enregistrement suivant.</span><span class="sxs-lookup"><span data-stu-id="63d58-106">The MCI\_RESERVE command allocates contiguous disk space for the workspace of the device driver instance for use with subsequent recording.</span></span> <span data-ttu-id="63d58-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="63d58-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="63d58-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="63d58-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
);
```



## <a name="parameters"></a><span data-ttu-id="63d58-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63d58-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63d58-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="63d58-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="63d58-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="63d58-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="63d58-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="63d58-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="63d58-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="63d58-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="63d58-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="63d58-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="63d58-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span><span class="sxs-lookup"><span data-stu-id="63d58-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span></span>
</dt> <dd>

<span data-ttu-id="63d58-116">Pointeur vers une structure de [**\_ \_ réserves \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="63d58-116">Pointer to an [**MCI\_DGV\_RESERVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63d58-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="63d58-117">Return Value</span></span>

<span data-ttu-id="63d58-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="63d58-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="63d58-119">Notes</span><span class="sxs-lookup"><span data-stu-id="63d58-119">Remarks</span></span>

<span data-ttu-id="63d58-120">Si l’espace de travail contient des données non enregistrées, ces données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="63d58-120">If the workspace contains unsaved data, this data is lost.</span></span> <span data-ttu-id="63d58-121">Si l’espace disque n’est pas réservé avant l’enregistrement, la commande [MCI \_ Record](mci-record.md) effectue une réservation implicite avec des paramètres par défaut spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="63d58-121">If disk space is not reserved prior to recording, the [MCI\_RECORD](mci-record.md) command performs an implied reserve with device-specific default parameters.</span></span> <span data-ttu-id="63d58-122">Sur certaines implémentations, la réserve n’est pas obligatoire et peut être ignorée par le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="63d58-122">On some implementations, reserve is not required and might be ignored by the device driver.</span></span> <span data-ttu-id="63d58-123">La réservation explicite d’espace vous permet de mieux contrôler le moment où se produit l’allocation de disque, la quantité d’espace allouée et l’emplacement où l’espace disque est alloué.</span><span class="sxs-lookup"><span data-stu-id="63d58-123">Explicitly reserving space gives you better control over when the delay for disk allocation occurs, how much space is allocated, and where the disk space is allocated.</span></span> <span data-ttu-id="63d58-124">La quantité et l’emplacement de l’espace disque déjà réservé pour cette instance d’appareil peuvent être modifiés par l’émission d' \_ une nouvelle réserve MCI.</span><span class="sxs-lookup"><span data-stu-id="63d58-124">The amount and location of disk space already reserved for this device instance can be changed by issuing MCI\_RESERVE again.</span></span> <span data-ttu-id="63d58-125">Tout espace disque alloué et toujours inutilisé n’est pas libéré tant que les données enregistrées ne sont pas enregistrées ou que l’instance de pilote de périphérique n’est pas fermée.</span><span class="sxs-lookup"><span data-stu-id="63d58-125">Any allocated and still unused disk space is not deallocated until any recorded data is saved or until the device driver instance is closed.</span></span>

<span data-ttu-id="63d58-126">Si la vidéo est désactivée avec l' \_ indicateur MCI désactivé de la commande [ \_ SETVIDEO MCI](mci-setvideo.md) , l’espace réservé n’inclut aucune vidéo.</span><span class="sxs-lookup"><span data-stu-id="63d58-126">If video is turned off with the MCI\_OFF flag of the [MCI\_SETVIDEO](mci-setvideo.md) command, the space reserved does not include any video.</span></span> <span data-ttu-id="63d58-127">Si le son est désactivé avec l' \_ indicateur MCI désactivé de la [commande \_ SETAUDIO MCI](mci-setaudio.md) , l’espace réservé n’inclut aucun audio.</span><span class="sxs-lookup"><span data-stu-id="63d58-127">If audio is turned off with the MCI\_OFF flag of the [MCI\_SETAUDIO](mci-setaudio.md) command, the space reserved does not include any audio.</span></span> <span data-ttu-id="63d58-128">Si les données audio et vidéo sont désactivées ou si la taille demandée est égale à zéro, aucun espace n’est réservé et tout espace réservé existant est libéré.</span><span class="sxs-lookup"><span data-stu-id="63d58-128">If both audio and video are turned off or if the requested size is zero, no space is reserved and any existing reserved space is deallocated.</span></span>

<span data-ttu-id="63d58-129">Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :</span><span class="sxs-lookup"><span data-stu-id="63d58-129">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="63d58-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>\_réservation DGV \_ MCI \_ dans</span><span class="sxs-lookup"><span data-stu-id="63d58-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI\_DGV\_RESERVE\_IN</span></span>
</dt> <dd>

<span data-ttu-id="63d58-131">Le membre **lpstrPath** de la structure identifiée par *lpReserve* contient l’adresse d’une mémoire tampon contenant l’emplacement d’un fichier temporaire.</span><span class="sxs-lookup"><span data-stu-id="63d58-131">The **lpstrPath** member of the structure identified by *lpReserve* contains an address of a buffer containing the location of a temporary file.</span></span> <span data-ttu-id="63d58-132">La mémoire tampon contient uniquement le chemin d’accès du lecteur et du répertoire du fichier utilisé pour contenir les données enregistrées ; le nom de fichier est spécifié par le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="63d58-132">The buffer contains only the drive and directory path of the file used to hold recorded data; the filename is specified by the device driver.</span></span> <span data-ttu-id="63d58-133">Ce fichier temporaire est supprimé lorsque l’instance d’appareil est fermée, sauf si elle est enregistrée explicitement.</span><span class="sxs-lookup"><span data-stu-id="63d58-133">This temporary file is deleted when the device instance is closed unless it is explicitly saved.</span></span> <span data-ttu-id="63d58-134">Si cet indicateur est omis, le pilote de périphérique spécifie l’emplacement d’allocation de l’espace disque.</span><span class="sxs-lookup"><span data-stu-id="63d58-134">If this flag is omitted, the device driver specifies where disk space is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="63d58-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>\_taille de \_ réserve \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="63d58-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI\_DGV\_RESERVE\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="63d58-136">Le membre **dwSize nul** de la structure identifiée par *lpReserve* spécifie la quantité approximative d’espace disque à réserver dans l’espace de travail pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="63d58-136">The **dwSize** member of the structure identified by *lpReserve* specifies the approximate amount of disk space to reserve in the workspace for recording.</span></span> <span data-ttu-id="63d58-137">La valeur est spécifiée dans le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="63d58-137">The value is specified in the current time format.</span></span> <span data-ttu-id="63d58-138">La quantité d’espace disque est estimée à partir de l’heure demandée et à partir de laquelle le format de fichier et l’algorithme vidéo et audio et les valeurs de qualité sont en vigueur.</span><span class="sxs-lookup"><span data-stu-id="63d58-138">The amount of disk space is estimated from the requested time and from which file format and video and audio algorithm and quality values are in effect.</span></span> <span data-ttu-id="63d58-139">Si cet indicateur est omis, le pilote de périphérique peut utiliser une valeur par défaut qu’il définit.</span><span class="sxs-lookup"><span data-stu-id="63d58-139">If this flag is omitted, the device driver might use a default value it defines.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63d58-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63d58-140">Requirements</span></span>



| <span data-ttu-id="63d58-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63d58-141">Requirement</span></span> | <span data-ttu-id="63d58-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="63d58-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d58-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63d58-143">Minimum supported client</span></span><br/> | <span data-ttu-id="63d58-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63d58-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="63d58-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63d58-145">Minimum supported server</span></span><br/> | <span data-ttu-id="63d58-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63d58-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="63d58-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="63d58-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="63d58-148"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63d58-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63d58-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63d58-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d58-150">MCI</span><span class="sxs-lookup"><span data-stu-id="63d58-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="63d58-151">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="63d58-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

