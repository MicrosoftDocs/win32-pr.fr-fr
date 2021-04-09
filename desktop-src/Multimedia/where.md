---
title: commande Where
description: La commande WHERE récupère le rectangle spécifiant la zone source ou de destination. Ce rectangle a été spécifié à l’aide de la commande put. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- commande Windows multimédia
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942686"
---
# <a name="where-command"></a><span data-ttu-id="a0b7a-106">commande Where</span><span class="sxs-lookup"><span data-stu-id="a0b7a-106">where command</span></span>

<span data-ttu-id="a0b7a-107">La commande WHERE récupère le rectangle spécifiant la zone source ou de destination.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-107">The where command retrieves the rectangle specifying the source or destination area.</span></span> <span data-ttu-id="a0b7a-108">Ce rectangle a été spécifié à l’aide de la commande [put](put.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b7a-108">This rectangle was specified using the [put](put.md) command.</span></span> <span data-ttu-id="a0b7a-109">Les appareils vidéo et vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-109">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="a0b7a-110">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a0b7a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0b7a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0b7a-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a0b7a-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a0b7a-113">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-113">Identifier of an MCI device.</span></span> <span data-ttu-id="a0b7a-114">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a0b7a-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span><span class="sxs-lookup"><span data-stu-id="a0b7a-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span></span>
</dt> <dd>

<span data-ttu-id="a0b7a-116">Indicateur qui identifie le rectangle dont les dimensions sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-116">Flag that identifies the rectangle whose dimensions are retrieved.</span></span> <span data-ttu-id="a0b7a-117">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Where** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-117">The following table lists device types that recognize the **where** command and the flags used by each type.</span></span>



| <span data-ttu-id="a0b7a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0b7a-118">Value</span></span>        | <span data-ttu-id="a0b7a-119">Signification</span><span class="sxs-lookup"><span data-stu-id="a0b7a-119">Meaning</span></span>                                                       | <span data-ttu-id="a0b7a-120">Signification</span><span class="sxs-lookup"><span data-stu-id="a0b7a-120">Meaning</span></span>                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="a0b7a-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="a0b7a-121">digitalvideo</span></span> | <span data-ttu-id="a0b7a-122">destinationdestination [**Max**](max.md)frameFrame maxsource</span><span class="sxs-lookup"><span data-stu-id="a0b7a-122">destinationdestination [**max**](max.md)frameframe maxsource</span></span> | <span data-ttu-id="a0b7a-123">maxvideovideo source maxwindowwindow Max</span><span class="sxs-lookup"><span data-stu-id="a0b7a-123">source maxvideovideo maxwindowwindow max</span></span> |
| <span data-ttu-id="a0b7a-124">superposition</span><span class="sxs-lookup"><span data-stu-id="a0b7a-124">overlay</span></span>      | <span data-ttu-id="a0b7a-125">destinationframe</span><span class="sxs-lookup"><span data-stu-id="a0b7a-125">destinationframe</span></span>                                              | <span data-ttu-id="a0b7a-126">sourcevideo</span><span class="sxs-lookup"><span data-stu-id="a0b7a-126">sourcevideo</span></span>                              |



 

<span data-ttu-id="a0b7a-127">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszRequestRect** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-127">The following table lists the flags that can be specified in the **lpszRequestRect** parameter and their meanings.</span></span>



| <span data-ttu-id="a0b7a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0b7a-128">Value</span></span>                          | <span data-ttu-id="a0b7a-129">Signification</span><span class="sxs-lookup"><span data-stu-id="a0b7a-129">Meaning</span></span>                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b7a-130">destination</span><span class="sxs-lookup"><span data-stu-id="a0b7a-130">destination</span></span>                    | <span data-ttu-id="a0b7a-131">Récupère l’étendue et le décalage de destination.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-131">Retrieves the destination offset and extent.</span></span> <span data-ttu-id="a0b7a-132">Pour les périphériques de superposition vidéo, le rectangle de destination définit la zone de la zone cliente de la fenêtre d’affichage qui affiche les données de l’image à partir de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-132">For video-overlay devices, the destination rectangle defines the area of the display window client area that displays the image data from the frame buffer.</span></span>                                                                                             |
| <span data-ttu-id="a0b7a-133">maximum de la destination [ ](max.md)</span><span class="sxs-lookup"><span data-stu-id="a0b7a-133">destination [**max**](max.md)</span></span> | <span data-ttu-id="a0b7a-134">Récupère la taille actuelle du rectangle client.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-134">Retrieves the current size of the client rectangle.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a0b7a-135">frame</span><span class="sxs-lookup"><span data-stu-id="a0b7a-135">frame</span></span>                          | <span data-ttu-id="a0b7a-136">Récupère le décalage et l’étendue du rectangle de la mémoire tampon de frame.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-136">Retrieves the offset and extent of the frame buffer rectangle.</span></span> <span data-ttu-id="a0b7a-137">Le rectangle de la mémoire tampon de frame définit la zone de la mémoire tampon de trame qui reçoit les données vidéo entrantes.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-137">The frame buffer rectangle defines the area of the frame buffer that receives incoming video data.</span></span> <span data-ttu-id="a0b7a-138">Les images du rectangle « Video » sont mises à l’échelle dans cette région.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-138">Images from the "video" rectangle are scaled into this region.</span></span>                                                                     |
| <span data-ttu-id="a0b7a-139">[ **nombre maximal** de frames](max.md)</span><span class="sxs-lookup"><span data-stu-id="a0b7a-139">frame [**max**](max.md)</span></span>       | <span data-ttu-id="a0b7a-140">Retourne la taille maximale de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-140">Returns the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a0b7a-141">source</span><span class="sxs-lookup"><span data-stu-id="a0b7a-141">source</span></span>                         | <span data-ttu-id="a0b7a-142">Récupère l’étendue et le décalage de la source.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-142">Retrieves the source offset and extent.</span></span> <span data-ttu-id="a0b7a-143">Pour les périphériques de superposition vidéo, le rectangle source définit la région de la mémoire tampon de trame qui s’affiche dans la fenêtre de destination.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-143">For video-overlay devices, the source rectangle defines the region of the frame buffer that is displayed in the destination window.</span></span> <span data-ttu-id="a0b7a-144">L’appareil utilise ce rectangle pour rogner l’image avant qu’elle ne soit étirée pour s’ajuster au rectangle de destination sur l’affichage.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-144">The device uses this rectangle to crop the image before it is stretched to fit the destination rectangle on the display.</span></span> |
| <span data-ttu-id="a0b7a-145">[ **Max** source](max.md)</span><span class="sxs-lookup"><span data-stu-id="a0b7a-145">source [**max**](max.md)</span></span>      | <span data-ttu-id="a0b7a-146">Récupère la taille maximale de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-146">Retrieves the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a0b7a-147">video</span><span class="sxs-lookup"><span data-stu-id="a0b7a-147">video</span></span>                          | <span data-ttu-id="a0b7a-148">Récupère le décalage et l’étendue du rectangle vidéo.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-148">Retrieves the offset and extent of the video rectangle.</span></span> <span data-ttu-id="a0b7a-149">Le rectangle vidéo définit la région des données vidéo entrantes qui sont transférées vers la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-149">The video rectangle defines the region of the incoming video data that is transferred to the frame buffer.</span></span>                                                                                                                                   |
| <span data-ttu-id="a0b7a-150">[ **Max** . vidéo](max.md)</span><span class="sxs-lookup"><span data-stu-id="a0b7a-150">video [**max**](max.md)</span></span>       | <span data-ttu-id="a0b7a-151">Retourne la taille maximale de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-151">Returns the maximum size of the input.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a0b7a-152">window</span><span class="sxs-lookup"><span data-stu-id="a0b7a-152">window</span></span>                         | <span data-ttu-id="a0b7a-153">Récupère la taille et la position actuelles du frame de fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-153">Retrieves the current size and position of the display-window frame.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="a0b7a-154">maximum de la fenêtre [ ](max.md)</span><span class="sxs-lookup"><span data-stu-id="a0b7a-154">window [**max**](max.md)</span></span>      | <span data-ttu-id="a0b7a-155">Récupère la taille de l’affichage entier.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-155">Retrieves the size of the entire display.</span></span>                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="a0b7a-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="a0b7a-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a0b7a-157">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-157">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="a0b7a-158">Pour les appareils vidéo numériques, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="a0b7a-158">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="a0b7a-159">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a0b7a-159">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0b7a-160">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a0b7a-160">Return Value</span></span>

<span data-ttu-id="a0b7a-161">Retourne un rectangle dans le paramètre *lpszReturnString* de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a0b7a-161">Returns a rectangle in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="a0b7a-162">Le rectangle décrit la zone spécifiée dans le paramètre *lpszRequestRect* de cette commande.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-162">The rectangle describes the area specified in the *lpszRequestRect* parameter of this command.</span></span> <span data-ttu-id="a0b7a-163">Le rectangle est spécifié en tant que *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-163">The rectangle is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="a0b7a-164">Les coordonnées *x1 Y1* spécifient l’angle supérieur gauche du rectangle, tandis que les coordonnées *x2 Y2* spécifient la largeur et la hauteur.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-164">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span>

## <a name="examples"></a><span data-ttu-id="a0b7a-165">Exemples</span><span class="sxs-lookup"><span data-stu-id="a0b7a-165">Examples</span></span>

<span data-ttu-id="a0b7a-166">La commande suivante renvoie le rectangle d’affichage de l’appareil « Movie ».</span><span class="sxs-lookup"><span data-stu-id="a0b7a-166">The following command returns the display rectangle of the "movie" device.</span></span>

``` syntax
where movie destination
```

## <a name="requirements"></a><span data-ttu-id="a0b7a-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0b7a-167">Requirements</span></span>



| <span data-ttu-id="a0b7a-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0b7a-168">Requirement</span></span> | <span data-ttu-id="a0b7a-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0b7a-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a0b7a-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0b7a-170">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b7a-171">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0b7a-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a0b7a-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0b7a-172">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b7a-173">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0b7a-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a0b7a-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0b7a-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b7a-175">MCI</span><span class="sxs-lookup"><span data-stu-id="a0b7a-175">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a0b7a-176">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="a0b7a-176">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="a0b7a-177">posé</span><span class="sxs-lookup"><span data-stu-id="a0b7a-177">put</span></span>](put.md)
</dt> </dl>

 

