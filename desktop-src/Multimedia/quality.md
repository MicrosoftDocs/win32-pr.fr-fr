---
title: Quality (commande)
description: La commande Quality définit un niveau de qualité personnalisé pour la compression des données audio, vidéo ou d’images fixes. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- commande Quality Windows Multimedia
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513628"
---
# <a name="quality-command"></a><span data-ttu-id="e802e-105">Quality (commande)</span><span class="sxs-lookup"><span data-stu-id="e802e-105">quality command</span></span>

<span data-ttu-id="e802e-106">La commande Quality définit un niveau de qualité personnalisé pour la compression des données audio, vidéo ou d’images fixes.</span><span class="sxs-lookup"><span data-stu-id="e802e-106">The quality command defines a custom quality level for either audio, video or still image data compression.</span></span> <span data-ttu-id="e802e-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="e802e-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="e802e-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="e802e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e802e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e802e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e802e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e802e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e802e-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="e802e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="e802e-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e802e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e802e-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span><span class="sxs-lookup"><span data-stu-id="e802e-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span></span>
</dt> <dd>

<span data-ttu-id="e802e-114">Un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="e802e-114">One or more of the following flags.</span></span> <span data-ttu-id="e802e-115">(L’un des trois indicateurs « audio », « toujours » et « vidéo » doit être présent.)</span><span class="sxs-lookup"><span data-stu-id="e802e-115">(One of the three flags "audio", "still", and "video" must be present.)</span></span>



| <span data-ttu-id="e802e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e802e-116">Value</span></span>                 | <span data-ttu-id="e802e-117">Signification</span><span class="sxs-lookup"><span data-stu-id="e802e-117">Meaning</span></span>                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e802e-118">*algorithme* d’algorithme</span><span class="sxs-lookup"><span data-stu-id="e802e-118">algorithm *algorithm*</span></span> | <span data-ttu-id="e802e-119">Associe le niveau de qualité à l' *algorithme* spécifié.</span><span class="sxs-lookup"><span data-stu-id="e802e-119">Associates the quality level with the specified *algorithm*.</span></span> <span data-ttu-id="e802e-120">Cet *algorithme* doit être pris en charge par l’appareil et être compatible avec l’indicateur « audio », « toujours » ou « vidéo » utilisé.</span><span class="sxs-lookup"><span data-stu-id="e802e-120">This *algorithm* must be supported by the device and be compatible with the "audio", "still", or "video" flag that is used.</span></span> <span data-ttu-id="e802e-121">En cas d’omission, l’algorithme actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e802e-121">If omitted, the current algorithm is used.</span></span> |
| <span data-ttu-id="e802e-122">*nom* audio</span><span class="sxs-lookup"><span data-stu-id="e802e-122">audio *name*</span></span>          | <span data-ttu-id="e802e-123">Indique que cette commande spécifie un niveau de qualité « audio » identifié par le *nom*.</span><span class="sxs-lookup"><span data-stu-id="e802e-123">Indicates this command specifies an "audio" quality level identified with *name*.</span></span>                                                                                                                                                   |
| <span data-ttu-id="e802e-124">dialogue</span><span class="sxs-lookup"><span data-stu-id="e802e-124">dialog</span></span>                | <span data-ttu-id="e802e-125">Demande que l’appareil affiche une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e802e-125">Requests that the device display a dialog box.</span></span> <span data-ttu-id="e802e-126">Cette boîte de dialogue contient des champs spécifiques à l’algorithme qui sont utilisés en interne par l’appareil pour créer la structure décrivant un niveau de qualité spécifique.</span><span class="sxs-lookup"><span data-stu-id="e802e-126">This dialog box has algorithm-specific fields that are used internally by the device to create the structure describing a specific quality level.</span></span>                                    |
| <span data-ttu-id="e802e-127">handle *de handle*</span><span class="sxs-lookup"><span data-stu-id="e802e-127">handle *handle*</span></span>       | <span data-ttu-id="e802e-128">Spécifie un *handle* vers une structure qui contient des données algorithmiques qui décrivent un niveau de qualité spécifique.</span><span class="sxs-lookup"><span data-stu-id="e802e-128">Specifies a *handle* to a structure that contains algorithmic-specific data describing a specific quality level.</span></span> <span data-ttu-id="e802e-129">Les structures des données référencées par ce handle sont spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e802e-129">The structures for the data referenced by this handle are device specific.</span></span>                                         |
| <span data-ttu-id="e802e-130">*nom* toujours</span><span class="sxs-lookup"><span data-stu-id="e802e-130">still *name*</span></span>          | <span data-ttu-id="e802e-131">Indique que la commande spécifie un niveau de qualité « toujours » identifié par le *nom.*</span><span class="sxs-lookup"><span data-stu-id="e802e-131">Indicates the command specifies a "still" quality level identified with *name.*</span></span>                                                                                                                                                     |
| <span data-ttu-id="e802e-132">*nom* de la vidéo</span><span class="sxs-lookup"><span data-stu-id="e802e-132">video *name*</span></span>          | <span data-ttu-id="e802e-133">Indique que la commande spécifie un niveau de qualité « vidéo » identifié par le *nom*.</span><span class="sxs-lookup"><span data-stu-id="e802e-133">Indicates the command specifies a "video" quality level identified with *name*.</span></span>                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="e802e-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="e802e-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e802e-135">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="e802e-135">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="e802e-136">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e802e-136">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e802e-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e802e-137">Return Value</span></span>

<span data-ttu-id="e802e-138">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="e802e-138">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e802e-139">Notes</span><span class="sxs-lookup"><span data-stu-id="e802e-139">Remarks</span></span>

<span data-ttu-id="e802e-140">Cette commande définit un nom de chaîne pour le niveau de qualité, qui peut ensuite être utilisé dans une commande [setvideo](setvideo.md) "Quality", setvideo "Still Quality" ou [SetAudio](setaudio.md) "Quality" pour l’établir comme le niveau de qualité de la vidéo, du reste ou de la compression audio en cours.</span><span class="sxs-lookup"><span data-stu-id="e802e-140">This command defines a string name for the quality level, which can then be used in a [setvideo](setvideo.md) "quality", setvideo "still quality", or [setaudio](setaudio.md) "quality" command to establish it as the current video, still, or audio-compression quality level.</span></span>

## <a name="requirements"></a><span data-ttu-id="e802e-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e802e-141">Requirements</span></span>



| <span data-ttu-id="e802e-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e802e-142">Requirement</span></span> | <span data-ttu-id="e802e-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="e802e-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e802e-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e802e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="e802e-145">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e802e-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e802e-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e802e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="e802e-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e802e-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e802e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e802e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e802e-149">MCI</span><span class="sxs-lookup"><span data-stu-id="e802e-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e802e-150">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="e802e-150">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="e802e-151">setaudio</span><span class="sxs-lookup"><span data-stu-id="e802e-151">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="e802e-152">setvideo</span><span class="sxs-lookup"><span data-stu-id="e802e-152">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

