---
title: commande capture
description: La commande capture copie le contenu de la mémoire tampon de frame et le stocke dans le fichier spécifié. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- commande de capture multimédia Windows
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105919"
---
# <a name="capture-command"></a><span data-ttu-id="d76ce-105">commande capture</span><span class="sxs-lookup"><span data-stu-id="d76ce-105">capture command</span></span>

<span data-ttu-id="d76ce-106">La commande capture copie le contenu de la mémoire tampon de frame et le stocke dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="d76ce-106">The capture command copies the contents of the frame buffer and stores it in the specified file.</span></span> <span data-ttu-id="d76ce-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="d76ce-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d76ce-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="d76ce-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d76ce-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d76ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76ce-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d76ce-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d76ce-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="d76ce-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d76ce-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="d76ce-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d76ce-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span><span class="sxs-lookup"><span data-stu-id="d76ce-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span></span>
</dt> <dd>

<span data-ttu-id="d76ce-114">Un ou plusieurs des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="d76ce-114">One or more of the following flags:</span></span>



| <span data-ttu-id="d76ce-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d76ce-115">Value</span></span>          | <span data-ttu-id="d76ce-116">Signification</span><span class="sxs-lookup"><span data-stu-id="d76ce-116">Meaning</span></span>                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76ce-117">comme *chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="d76ce-117">as *pathname*</span></span>  | <span data-ttu-id="d76ce-118">Spécifie le chemin d’accès et le nom de fichier de destination de l’image capturée.</span><span class="sxs-lookup"><span data-stu-id="d76ce-118">Specifies the destination path and filename for the captured image.</span></span> <span data-ttu-id="d76ce-119">Cet indicateur est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d76ce-119">This flag is required.</span></span>                                                                                                                                                                |
| <span data-ttu-id="d76ce-120">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="d76ce-120">at *rectangle*</span></span> | <span data-ttu-id="d76ce-121">Spécifie la zone rectangulaire dans la mémoire tampon de trame que l’appareil rogne et enregistre sur le disque.</span><span class="sxs-lookup"><span data-stu-id="d76ce-121">Specifies the rectangular region within the frame buffer that the device crops and saves to disk.</span></span> <span data-ttu-id="d76ce-122">En cas d’omission, la zone rognée est définie par défaut sur le rectangle spécifié ou par défaut sur une commande [put](put.md) « source » précédente pour cette instance d’appareil.</span><span class="sxs-lookup"><span data-stu-id="d76ce-122">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [put](put.md) "source" command for this device instance.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d76ce-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d76ce-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d76ce-124">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="d76ce-124">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="d76ce-125">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d76ce-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d76ce-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d76ce-126">Return Value</span></span>

<span data-ttu-id="d76ce-127">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="d76ce-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d76ce-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d76ce-128">Remarks</span></span>

<span data-ttu-id="d76ce-129">Cette commande peut échouer si l’appareil est en train de visionner des vidéos animées ou d’exécuter d’autres opérations gourmandes en ressources.</span><span class="sxs-lookup"><span data-stu-id="d76ce-129">This command might fail if the device is currently playing motion video or executing some other resource-intensive operation.</span></span> <span data-ttu-id="d76ce-130">Si la mémoire tampon de trame est mise à jour en temps réel, la mise à jour s’interrompt momentanément afin qu’une image complète soit capturée.</span><span class="sxs-lookup"><span data-stu-id="d76ce-130">If the frame buffer is being updated in real time, the updating momentarily pauses so that a complete image is captured.</span></span> <span data-ttu-id="d76ce-131">Si l’appareil interrompt la mise à jour, il peut y avoir un effet visuel ou audible.</span><span class="sxs-lookup"><span data-stu-id="d76ce-131">If the device pauses the updating, there might be a visual or audible effect.</span></span> <span data-ttu-id="d76ce-132">Si le format de fichier, l’algorithme de compression et les niveaux de qualité n’ont pas été définis, leurs valeurs par défaut sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="d76ce-132">If the file format, compression algorithm, and quality levels have not been set, their defaults are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d76ce-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d76ce-133">Requirements</span></span>



| <span data-ttu-id="d76ce-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d76ce-134">Requirement</span></span> | <span data-ttu-id="d76ce-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d76ce-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d76ce-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d76ce-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d76ce-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d76ce-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d76ce-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d76ce-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d76ce-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d76ce-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d76ce-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d76ce-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d76ce-141">MCI</span><span class="sxs-lookup"><span data-stu-id="d76ce-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d76ce-142">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="d76ce-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="d76ce-143">posé</span><span class="sxs-lookup"><span data-stu-id="d76ce-143">put</span></span>](put.md)
</dt> </dl>

 

