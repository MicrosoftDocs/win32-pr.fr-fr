---
title: libérer la commande
description: La commande dégeler réactive l’acquisition vidéo dans la mémoire tampon de trame une fois qu’elle a été désactivée par la commande Freeze. Les périphériques numériques vidéo, VCR et vidéo reconnaissent cette commande.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- libérer la commande multimédia Windows
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743557"
---
# <a name="unfreeze-command"></a><span data-ttu-id="0b9c5-105">libérer la commande</span><span class="sxs-lookup"><span data-stu-id="0b9c5-105">unfreeze command</span></span>

<span data-ttu-id="0b9c5-106">La commande dégeler réactive l’acquisition vidéo dans la mémoire tampon de trame une fois qu’elle a été désactivée par la commande [Freeze](freeze.md) .</span><span class="sxs-lookup"><span data-stu-id="0b9c5-106">The unfreeze command reenables video acquisition to the frame buffer after it has been disabled by the [freeze](freeze.md) command.</span></span> <span data-ttu-id="0b9c5-107">Les périphériques numériques vidéo, VCR et vidéo reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="0b9c5-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0b9c5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b9c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b9c5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0b9c5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0b9c5-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0b9c5-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0b9c5-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span><span class="sxs-lookup"><span data-stu-id="0b9c5-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="0b9c5-114">Indicateur pour la réactivation de l’acquisition vidéo dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-114">Flag for reenabling video acquisition to the frame buffer.</span></span> <span data-ttu-id="0b9c5-115">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **dégeler** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-115">The following table lists device types that recognize the **unfreeze** command and the flags used by each type.</span></span>



| <span data-ttu-id="0b9c5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b9c5-116">Value</span></span>        | <span data-ttu-id="0b9c5-117">Signification</span><span class="sxs-lookup"><span data-stu-id="0b9c5-117">Meaning</span></span>        |
|--------------|----------------|
| <span data-ttu-id="0b9c5-118">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="0b9c5-118">digitalvideo</span></span> | <span data-ttu-id="0b9c5-119">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="0b9c5-119">at *rectangle*</span></span> |
| <span data-ttu-id="0b9c5-120">superposition</span><span class="sxs-lookup"><span data-stu-id="0b9c5-120">overlay</span></span>      | <span data-ttu-id="0b9c5-121">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="0b9c5-121">at *rectangle*</span></span> |
| <span data-ttu-id="0b9c5-122">vidéo</span><span class="sxs-lookup"><span data-stu-id="0b9c5-122">vcr</span></span>          | <span data-ttu-id="0b9c5-123">sortie d’entrée</span><span class="sxs-lookup"><span data-stu-id="0b9c5-123">input output</span></span>   |



 

<span data-ttu-id="0b9c5-124">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszUnfreeze** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-124">The following table lists the flags that can be specified in the **lpszUnfreeze** parameter and their meanings.</span></span>



| <span data-ttu-id="0b9c5-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b9c5-125">Value</span></span>          | <span data-ttu-id="0b9c5-126">Signification</span><span class="sxs-lookup"><span data-stu-id="0b9c5-126">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9c5-127">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="0b9c5-127">at *rectangle*</span></span> | <span data-ttu-id="0b9c5-128">Spécifie la région pour laquelle l’acquisition de vidéos sera réactivée.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-128">Specifies the region that will have video acquisition reenabled.</span></span> <span data-ttu-id="0b9c5-129">Le rectangle est relatif à l’origine de la mémoire tampon vidéo et est spécifié comme *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-129">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="0b9c5-130">Les coordonnées *x1 Y1* spécifient l’angle supérieur gauche du rectangle, tandis que les coordonnées *x2 Y2* spécifient la largeur et la hauteur.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-130">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="0b9c5-131">entrée</span><span class="sxs-lookup"><span data-stu-id="0b9c5-131">input</span></span>          | <span data-ttu-id="0b9c5-132">Libérez l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-132">Unfreeze the input image.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0b9c5-133">sortie</span><span class="sxs-lookup"><span data-stu-id="0b9c5-133">output</span></span>         | <span data-ttu-id="0b9c5-134">Libérez l’image de sortie.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-134">Unfreeze the output image.</span></span> <span data-ttu-id="0b9c5-135">Si aucune « entrée » ni « sortie » n’est indiquée, la « sortie » est supposée.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-135">If neither "input" nor "output" is given, "output" is assumed.</span></span>                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="0b9c5-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0b9c5-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0b9c5-137">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-137">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="0b9c5-138">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="0b9c5-138">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="0b9c5-139">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0b9c5-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b9c5-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0b9c5-140">Return Value</span></span>

<span data-ttu-id="0b9c5-141">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="0b9c5-142">Exemples</span><span class="sxs-lookup"><span data-stu-id="0b9c5-142">Examples</span></span>

<span data-ttu-id="0b9c5-143">La commande suivante libère une région de la mémoire tampon vidéo.</span><span class="sxs-lookup"><span data-stu-id="0b9c5-143">The following command unfreezes a region of the video buffer.</span></span>

``` syntax
unfreeze vboard at 10 20 90 165
```

## <a name="requirements"></a><span data-ttu-id="0b9c5-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b9c5-144">Requirements</span></span>



| <span data-ttu-id="0b9c5-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b9c5-145">Requirement</span></span> | <span data-ttu-id="0b9c5-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b9c5-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0b9c5-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b9c5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0b9c5-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b9c5-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0b9c5-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b9c5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0b9c5-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b9c5-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0b9c5-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b9c5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9c5-152">MCI</span><span class="sxs-lookup"><span data-stu-id="0b9c5-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0b9c5-153">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="0b9c5-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="0b9c5-154">antigel</span><span class="sxs-lookup"><span data-stu-id="0b9c5-154">freeze</span></span>](freeze.md)
</dt> </dl>

 

