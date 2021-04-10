---
title: Reserve, commande
description: La commande Reserve alloue de l’espace disque contigu à l’espace de travail de l’instance de périphérique. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- commande de réserve Windows Multimedia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941691"
---
# <a name="reserve-command"></a><span data-ttu-id="c253f-105">Reserve, commande</span><span class="sxs-lookup"><span data-stu-id="c253f-105">reserve command</span></span>

<span data-ttu-id="c253f-106">La commande Reserve alloue de l’espace disque contigu à l’espace de travail de l’instance de périphérique.</span><span class="sxs-lookup"><span data-stu-id="c253f-106">The reserve command allocates contiguous disk space for the device instance's workspace.</span></span> <span data-ttu-id="c253f-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="c253f-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="c253f-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="c253f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c253f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c253f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c253f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c253f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c253f-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="c253f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c253f-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="c253f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c253f-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span><span class="sxs-lookup"><span data-stu-id="c253f-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span></span>
</dt> <dd>

<span data-ttu-id="c253f-114">Un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="c253f-114">One or more of the following flags.</span></span>



| <span data-ttu-id="c253f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c253f-115">Value</span></span>           | <span data-ttu-id="c253f-116">Signification</span><span class="sxs-lookup"><span data-stu-id="c253f-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c253f-117">dans le *chemin*</span><span class="sxs-lookup"><span data-stu-id="c253f-117">in *path*</span></span>       | <span data-ttu-id="c253f-118">Spécifie le lecteur et le chemin d’accès au répertoire (mais pas le nom) d’un fichier temporaire utilisé pour contenir les données enregistrées.</span><span class="sxs-lookup"><span data-stu-id="c253f-118">Specifies the drive and directory path (but not the name) of a temporary file used to hold recorded data.</span></span> <span data-ttu-id="c253f-119">Le nom de ce fichier est spécifié par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c253f-119">The name of this file is specified by the device.</span></span> <span data-ttu-id="c253f-120">Le fichier temporaire est supprimé lorsque l’appareil est fermé.</span><span class="sxs-lookup"><span data-stu-id="c253f-120">The temporary file is deleted when the device is closed.</span></span> <span data-ttu-id="c253f-121">Si cet indicateur est omis, le périphérique spécifie l’emplacement de l’espace disque.</span><span class="sxs-lookup"><span data-stu-id="c253f-121">If this flag is omitted, the device specifies the location of the disk space.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c253f-122">*durée* de la taille</span><span class="sxs-lookup"><span data-stu-id="c253f-122">size *duration*</span></span> | <span data-ttu-id="c253f-123">Spécifie la quantité approximative d’espace disque à réserver dans l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="c253f-123">Specifies the approximate amount of disk space to reserve in the workspace.</span></span> <span data-ttu-id="c253f-124">La valeur de *durée* est spécifiée dans le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="c253f-124">The *duration* value is specified in the current time format.</span></span> <span data-ttu-id="c253f-125">L’appareil base son estimation de l’espace disque requis sur les paramètres suivants : l’heure demandée, le format de fichier, l’algorithme de compression vidéo et audio et les valeurs de qualité de compression en vigueur.</span><span class="sxs-lookup"><span data-stu-id="c253f-125">The device bases its estimate of the required disk space on the following parameters: the requested time, the file format, the video and audio compression algorithm, and the compression quality values in effect.</span></span> <span data-ttu-id="c253f-126">Si [setvideo](setvideo.md) « record » est « OFF », l’espace est réservé uniquement à l’audio.</span><span class="sxs-lookup"><span data-stu-id="c253f-126">If [setvideo](setvideo.md) "record" is "off", then space is reserved only for audio.</span></span> <span data-ttu-id="c253f-127">Si [SetAudio](setaudio.md) « record » est « OFF », l’espace est réservé uniquement pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="c253f-127">If [setaudio](setaudio.md) "record" is "off", then space is reserved only for video.</span></span> <span data-ttu-id="c253f-128">Si les deux sont « OFF », ou si *Duration* est égal à zéro, aucun espace n’est réservé et tout espace réservé existant est libéré.</span><span class="sxs-lookup"><span data-stu-id="c253f-128">If both are "off", or if *duration* is zero, then no space is reserved and any existing reserved space is deallocated.</span></span> <span data-ttu-id="c253f-129">Si cet indicateur est omis, l’appareil utilise une valeur par défaut définie par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c253f-129">If this flag is omitted, the device will use a device-defined default.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c253f-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c253f-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c253f-131">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="c253f-131">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="c253f-132">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c253f-132">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c253f-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c253f-133">Return Value</span></span>

<span data-ttu-id="c253f-134">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="c253f-134">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c253f-135">Notes</span><span class="sxs-lookup"><span data-stu-id="c253f-135">Remarks</span></span>

<span data-ttu-id="c253f-136">Si nécessaire, les commandes [enregistrer ou](record.md) [Enregistrer](save.md) suivantes utilisent l’espace réservé par cette commande.</span><span class="sxs-lookup"><span data-stu-id="c253f-136">If needed, subsequent [record](record.md) or [save](save.md) commands use the space reserved by this command.</span></span> <span data-ttu-id="c253f-137">Si l’espace de travail contient des données non enregistrées, les données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="c253f-137">If the workspace contains unsaved data, the data is lost.</span></span> <span data-ttu-id="c253f-138">Certains appareils ne nécessitent pas de réserve et l’ignorent.</span><span class="sxs-lookup"><span data-stu-id="c253f-138">Some devices do not require reserve and ignore it.</span></span> <span data-ttu-id="c253f-139">Si l’espace disque n’est pas réservé avant l’enregistrement, la commande d’enregistrement effectue une réservation implicite avec des indicateurs par défaut spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c253f-139">If disk space is not reserved prior to recording, the record command performs an implied reserve with device-specific default flags.</span></span> <span data-ttu-id="c253f-140">Utilisez une commande de réserve explicite si vous souhaitez mieux contrôler quand l’allocation de disque se produit, le contrôle de la quantité d’espace alloué et le contrôle de l’emplacement où l’espace disque est alloué.</span><span class="sxs-lookup"><span data-stu-id="c253f-140">Use an explicit reserve command if you want better control of when the delay for disk allocation occurs, control of how much space is allocated, and control of where the disk space is allocated.</span></span> <span data-ttu-id="c253f-141">Votre application peut modifier la quantité et l’emplacement de l’espace disque précédemment réservé avec les commandes de réserve suivantes.</span><span class="sxs-lookup"><span data-stu-id="c253f-141">Your application can change the amount and location of previously reserved disk space with subsequent reserve commands.</span></span> <span data-ttu-id="c253f-142">Tout espace disque alloué et toujours inutilisé n’est pas libéré tant que les données enregistrées ne sont pas enregistrées ou que l’instance d’appareil n’est pas fermée.</span><span class="sxs-lookup"><span data-stu-id="c253f-142">Any allocated and still unused disk space is not deallocated until any recorded data is saved, or until the device instance is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c253f-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c253f-143">Requirements</span></span>



| <span data-ttu-id="c253f-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c253f-144">Requirement</span></span> | <span data-ttu-id="c253f-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="c253f-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c253f-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c253f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c253f-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c253f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c253f-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c253f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c253f-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c253f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c253f-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c253f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c253f-151">MCI</span><span class="sxs-lookup"><span data-stu-id="c253f-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c253f-152">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="c253f-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c253f-153">enregistrement</span><span class="sxs-lookup"><span data-stu-id="c253f-153">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="c253f-154">enregistrer</span><span class="sxs-lookup"><span data-stu-id="c253f-154">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="c253f-155">setaudio</span><span class="sxs-lookup"><span data-stu-id="c253f-155">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="c253f-156">setvideo</span><span class="sxs-lookup"><span data-stu-id="c253f-156">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

