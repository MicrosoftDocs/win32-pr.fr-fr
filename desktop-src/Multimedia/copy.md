---
title: copier (commande)
description: La commande de copie copie les données dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- commande copier Windows Multimedia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740500"
---
# <a name="copy-command"></a><span data-ttu-id="a38e8-105">copier (commande)</span><span class="sxs-lookup"><span data-stu-id="a38e8-105">copy command</span></span>

<span data-ttu-id="a38e8-106">La commande de copie copie les données dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a38e8-106">The copy command copies data to the clipboard.</span></span> <span data-ttu-id="a38e8-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="a38e8-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="a38e8-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="a38e8-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a38e8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a38e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a38e8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a38e8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a38e8-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="a38e8-111">Identifier of an MCI device.</span></span> <span data-ttu-id="a38e8-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="a38e8-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a38e8-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="a38e8-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="a38e8-114">L’un des indicateurs suivants identifiant l’élément à copier.</span><span class="sxs-lookup"><span data-stu-id="a38e8-114">One of the following flags identifying the item to copy.</span></span>



| <span data-ttu-id="a38e8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a38e8-115">Value</span></span>                 | <span data-ttu-id="a38e8-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a38e8-116">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a38e8-117">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="a38e8-117">at *rectangle*</span></span>        | <span data-ttu-id="a38e8-118">Spécifie la partie de chaque frame qui sera copiée.</span><span class="sxs-lookup"><span data-stu-id="a38e8-118">Specifies the portion of each frame that will be copied.</span></span> <span data-ttu-id="a38e8-119">En cas d’omission, le paramètre par défaut est le cadre entier.</span><span class="sxs-lookup"><span data-stu-id="a38e8-119">If omitted, the default setting is the entire frame.</span></span>                                                                                                                             |
| <span data-ttu-id="a38e8-120">*flux* de flux audio</span><span class="sxs-lookup"><span data-stu-id="a38e8-120">audio stream *stream*</span></span> | <span data-ttu-id="a38e8-121">Spécifie le flux audio dans l’espace de travail affecté par la commande.</span><span class="sxs-lookup"><span data-stu-id="a38e8-121">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="a38e8-122">Si vous utilisez cet indicateur et que vous souhaitez également copier la vidéo, vous devez également utiliser l’indicateur « flux vidéo ».</span><span class="sxs-lookup"><span data-stu-id="a38e8-122">If you use this flag and also want to copy video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="a38e8-123">(Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont copiés.)</span><span class="sxs-lookup"><span data-stu-id="a38e8-123">(If neither flag is specified, all audio and video streams are copied.)</span></span> |
| <span data-ttu-id="a38e8-124">à partir de la *position*</span><span class="sxs-lookup"><span data-stu-id="a38e8-124">from *position*</span></span>       | <span data-ttu-id="a38e8-125">Spécifie le début de la plage copiée.</span><span class="sxs-lookup"><span data-stu-id="a38e8-125">Specifies the start of the range copied.</span></span> <span data-ttu-id="a38e8-126">En cas d’omission, le paramètre par défaut est la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="a38e8-126">If omitted, the default setting is the current position.</span></span>                                                                                                                                         |
| <span data-ttu-id="a38e8-127">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="a38e8-127">to *position*</span></span>         | <span data-ttu-id="a38e8-128">Spécifie la fin de la plage copiée.</span><span class="sxs-lookup"><span data-stu-id="a38e8-128">Specifies the end of the range copied.</span></span> <span data-ttu-id="a38e8-129">Les données audio et vidéo copiées sont exclusives à cette position.</span><span class="sxs-lookup"><span data-stu-id="a38e8-129">The audio and video data copied are exclusive of this position.</span></span> <span data-ttu-id="a38e8-130">En cas d’omission, le paramètre par défaut est la fin de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="a38e8-130">If omitted, the default setting is the end of the workspace.</span></span>                                                                       |
| <span data-ttu-id="a38e8-131">*flux* de flux vidéo</span><span class="sxs-lookup"><span data-stu-id="a38e8-131">video stream *stream*</span></span> | <span data-ttu-id="a38e8-132">Spécifie le flux vidéo dans l’espace de travail affecté par la commande.</span><span class="sxs-lookup"><span data-stu-id="a38e8-132">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="a38e8-133">Si vous utilisez cet indicateur et que vous souhaitez également copier l’audio, vous devez également utiliser l’indicateur « flux audio ».</span><span class="sxs-lookup"><span data-stu-id="a38e8-133">If you use this flag and also want to copy audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="a38e8-134">(Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont copiés.)</span><span class="sxs-lookup"><span data-stu-id="a38e8-134">(If neither flag is specified, all audio and video streams are copied.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="a38e8-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="a38e8-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a38e8-136">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="a38e8-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="a38e8-137">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a38e8-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a38e8-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a38e8-138">Return Value</span></span>

<span data-ttu-id="a38e8-139">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="a38e8-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a38e8-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a38e8-140">Requirements</span></span>



| <span data-ttu-id="a38e8-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a38e8-141">Requirement</span></span> | <span data-ttu-id="a38e8-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="a38e8-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a38e8-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a38e8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a38e8-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a38e8-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a38e8-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a38e8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a38e8-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a38e8-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a38e8-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a38e8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38e8-148">MCI</span><span class="sxs-lookup"><span data-stu-id="a38e8-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a38e8-149">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="a38e8-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

