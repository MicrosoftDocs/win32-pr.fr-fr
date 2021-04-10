---
title: commande couper
description: La commande couper supprime les données de l’espace de travail et les copie dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- commande couper Windows multimédia
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942635"
---
# <a name="cut-command"></a><span data-ttu-id="ee3ce-105">commande couper</span><span class="sxs-lookup"><span data-stu-id="ee3ce-105">cut command</span></span>

<span data-ttu-id="ee3ce-106">La commande couper supprime les données de l’espace de travail et les copie dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-106">The cut command removes data from the workspace and copies it to the clipboard.</span></span> <span data-ttu-id="ee3ce-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="ee3ce-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="ee3ce-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee3ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee3ce-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ee3ce-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ee3ce-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-111">Identifier of an MCI device.</span></span> <span data-ttu-id="ee3ce-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="ee3ce-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="ee3ce-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="ee3ce-114">L’un des indicateurs suivants identifiant l’élément à couper.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-114">One of the following flags identifying the item to cut.</span></span>



| <span data-ttu-id="ee3ce-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee3ce-115">Value</span></span>                 | <span data-ttu-id="ee3ce-116">Signification</span><span class="sxs-lookup"><span data-stu-id="ee3ce-116">Meaning</span></span>                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3ce-117">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="ee3ce-117">at *rectangle*</span></span>        | <span data-ttu-id="ee3ce-118">Spécifie la partie de chaque coupe de cadre.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-118">Specifies the portion of each frame cut.</span></span> <span data-ttu-id="ee3ce-119">En cas d’omission, la valeur par défaut est le frame entier.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-119">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="ee3ce-120">Lorsque cet élément est spécifié, les cadres ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-120">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="ee3ce-121">Au lieu de cela, la zone à l’intérieur du rectangle devient noire.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-121">Instead the area inside the rectangle becomes black.</span></span>                                       |
| <span data-ttu-id="ee3ce-122">*flux* de flux audio</span><span class="sxs-lookup"><span data-stu-id="ee3ce-122">audio stream *stream*</span></span> | <span data-ttu-id="ee3ce-123">Spécifie le flux audio dans l’espace de travail affecté par la commande.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-123">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="ee3ce-124">Si vous utilisez cet indicateur et que vous souhaitez également couper la vidéo, vous devez également utiliser l’indicateur « flux vidéo ».</span><span class="sxs-lookup"><span data-stu-id="ee3ce-124">If you use this flag and also want to cut video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="ee3ce-125">(Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont coupés.)</span><span class="sxs-lookup"><span data-stu-id="ee3ce-125">(If neither flag is specified, all audio and video streams are cut.)</span></span> |
| <span data-ttu-id="ee3ce-126">à partir de la *position*</span><span class="sxs-lookup"><span data-stu-id="ee3ce-126">from *position*</span></span>       | <span data-ttu-id="ee3ce-127">Spécifie le début de la coupe de plage.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-127">Specifies the start of the range cut.</span></span> <span data-ttu-id="ee3ce-128">En cas d’omission, sa valeur par défaut est la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-128">If omitted, it defaults to the current position.</span></span>                                                                                                                                                |
| <span data-ttu-id="ee3ce-129">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="ee3ce-129">to *position*</span></span>         | <span data-ttu-id="ee3ce-130">Spécifie la fin de la coupe de plage.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-130">Specifies the end of the range cut.</span></span> <span data-ttu-id="ee3ce-131">La coupure des données audio et vidéo est exclusive à cette position.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-131">The audio and video data cut are exclusive of this position.</span></span> <span data-ttu-id="ee3ce-132">S’il est omis, la valeur par défaut est la fin de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-132">If omitted it defaults to the end of the workspace.</span></span>                                                                                  |
| <span data-ttu-id="ee3ce-133">*flux* de flux vidéo</span><span class="sxs-lookup"><span data-stu-id="ee3ce-133">video stream *stream*</span></span> | <span data-ttu-id="ee3ce-134">Spécifie le flux vidéo dans l’espace de travail affecté par la commande.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-134">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="ee3ce-135">Si vous utilisez cet indicateur et que vous souhaitez également couper le son, vous devez également utiliser l’indicateur « flux audio ».</span><span class="sxs-lookup"><span data-stu-id="ee3ce-135">If you use this flag and also want to cut audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="ee3ce-136">(Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont coupés.)</span><span class="sxs-lookup"><span data-stu-id="ee3ce-136">(If neither flag is specified, all audio and video streams are cut.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="ee3ce-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="ee3ce-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ee3ce-138">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-138">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="ee3ce-139">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ee3ce-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee3ce-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ee3ce-140">Return Value</span></span>

<span data-ttu-id="ee3ce-141">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee3ce-142">Notes</span><span class="sxs-lookup"><span data-stu-id="ee3ce-142">Remarks</span></span>

<span data-ttu-id="ee3ce-143">La modification devient permanente uniquement lorsque les données sont enregistrées de manière explicite ; Toutefois, la lecture agit comme si les données avaient été supprimées.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-143">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee3ce-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee3ce-144">Requirements</span></span>



| <span data-ttu-id="ee3ce-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee3ce-145">Requirement</span></span> | <span data-ttu-id="ee3ce-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee3ce-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ee3ce-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee3ce-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ee3ce-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee3ce-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ee3ce-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee3ce-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ee3ce-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee3ce-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ee3ce-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee3ce-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3ce-152">MCI</span><span class="sxs-lookup"><span data-stu-id="ee3ce-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ee3ce-153">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="ee3ce-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

