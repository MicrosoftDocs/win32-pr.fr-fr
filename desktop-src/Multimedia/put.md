---
title: commande put
description: La commande put définit la zone de l’image source et de la fenêtre de destination utilisées pour l’affichage. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- commande put Windows multimédia
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105706"
---
# <a name="put-command"></a><span data-ttu-id="8c894-105">commande put</span><span class="sxs-lookup"><span data-stu-id="8c894-105">put command</span></span>

<span data-ttu-id="8c894-106">La commande put définit la zone de l’image source et de la fenêtre de destination utilisées pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="8c894-106">The put command defines the area of the source image and destination window used for display.</span></span> <span data-ttu-id="8c894-107">Les appareils vidéo et vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="8c894-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="8c894-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="8c894-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="8c894-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c894-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c894-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8c894-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8c894-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="8c894-111">Identifier of an MCI device.</span></span> <span data-ttu-id="8c894-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="8c894-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="8c894-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span><span class="sxs-lookup"><span data-stu-id="8c894-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span></span>
</dt> <dd>

<span data-ttu-id="8c894-114">Indicateur pour la définition de la zone.</span><span class="sxs-lookup"><span data-stu-id="8c894-114">Flag for defining the area.</span></span> <span data-ttu-id="8c894-115">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande put et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="8c894-115">The following table lists device types that recognize the put command and the flags used by each type.</span></span>



| <span data-ttu-id="8c894-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c894-116">Value</span></span>        | <span data-ttu-id="8c894-117">Signification</span><span class="sxs-lookup"><span data-stu-id="8c894-117">Meaning</span></span>                                                                                      | <span data-ttu-id="8c894-118">Signification</span><span class="sxs-lookup"><span data-stu-id="8c894-118">Meaning</span></span>                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c894-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="8c894-119">digitalvideo</span></span> | <span data-ttu-id="8c894-120">destination de destination *au niveau* du frame du rectangle dans le rectangle *source source au* *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8c894-120">destination destination at *rectangle* frame frame at *rectangle* source source at *rectangle*</span></span> | <span data-ttu-id="8c894-121">vidéo vidéo dans la fenêtre *rectangle* fenêtre fenêtre du *rectangle* client fenêtre client au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8c894-121">video video at *rectangle* window window at *rectangle* window client window client at *rectangle*</span></span> |
| <span data-ttu-id="8c894-122">superposition</span><span class="sxs-lookup"><span data-stu-id="8c894-122">overlay</span></span>      | <span data-ttu-id="8c894-123">destination de destination au niveau du frame du *rectangle* dans le *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8c894-123">destination destination at *rectangle* frame frame at *rectangle*</span></span>                             | <span data-ttu-id="8c894-124">vidéo source de la vidéo du *rectangle* dans le *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8c894-124">source source at *rectangle* video video at *rectangle*</span></span>                                           |



 

<span data-ttu-id="8c894-125">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszRegions** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="8c894-125">The following table lists the flags that can be specified in the **lpszRegions** parameter and their meanings.</span></span>



| <span data-ttu-id="8c894-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c894-126">Value</span></span>                        | <span data-ttu-id="8c894-127">Signification</span><span class="sxs-lookup"><span data-stu-id="8c894-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c894-128">destination</span><span class="sxs-lookup"><span data-stu-id="8c894-128">destination</span></span>                  | <span data-ttu-id="8c894-129">Sélectionne la zone cliente entière de la fenêtre de destination pour afficher les données.</span><span class="sxs-lookup"><span data-stu-id="8c894-129">Selects the entire client area of the destination window to display the data.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8c894-130">destination au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8c894-130">destination at *rectangle*</span></span>   | <span data-ttu-id="8c894-131">Sélectionne une partie de la zone cliente de la fenêtre de destination utilisée pour afficher l’image.</span><span class="sxs-lookup"><span data-stu-id="8c894-131">Selects a portion of the client area of the destination window used to display the image.</span></span> <span data-ttu-id="8c894-132">Lorsqu’une zone de la fenêtre d’affichage est spécifiée et que l’appareil prend en charge l’étirement, l’image source est étirée jusqu’à l’offset et l’étendue de destination.</span><span class="sxs-lookup"><span data-stu-id="8c894-132">When an area of the display window is specified and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                     |
| <span data-ttu-id="8c894-133">frame</span><span class="sxs-lookup"><span data-stu-id="8c894-133">frame</span></span>                        | <span data-ttu-id="8c894-134">Sélectionne la mémoire tampon de frame entière pour recevoir les images vidéo entrantes.</span><span class="sxs-lookup"><span data-stu-id="8c894-134">Selects the entire frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8c894-135">Frame au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8c894-135">frame at *rectangle*</span></span>         | <span data-ttu-id="8c894-136">Sélectionne une partie de la mémoire tampon de trame pour recevoir les images vidéo entrantes.</span><span class="sxs-lookup"><span data-stu-id="8c894-136">Selects a portion of the frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8c894-137">source</span><span class="sxs-lookup"><span data-stu-id="8c894-137">source</span></span>                       | <span data-ttu-id="8c894-138">Sélectionne la totalité de l’image à afficher dans la fenêtre de destination.</span><span class="sxs-lookup"><span data-stu-id="8c894-138">Selects the entire image for display in the destination window.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="8c894-139">source au *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8c894-139">source at *rectangle*</span></span>        | <span data-ttu-id="8c894-140">Sélectionne une partie de l’image à afficher dans la fenêtre de destination.</span><span class="sxs-lookup"><span data-stu-id="8c894-140">Selects a portion of the image to display in the destination window.</span></span> <span data-ttu-id="8c894-141">Lorsqu’une zone de l’image source est spécifiée et que l’appareil prend en charge l’étirement, l’image source est étirée jusqu’au décalage et à l’étendue de destination.</span><span class="sxs-lookup"><span data-stu-id="8c894-141">When an area of the source image is specified, and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                                           |
| <span data-ttu-id="8c894-142">video</span><span class="sxs-lookup"><span data-stu-id="8c894-142">video</span></span>                        | <span data-ttu-id="8c894-143">Sélectionne la totalité de l’image vidéo entrante à capturer dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="8c894-143">Selects the entire incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8c894-144">vidéo au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8c894-144">video at *rectangle*</span></span>         | <span data-ttu-id="8c894-145">Sélectionne une partie de l’image vidéo entrante à capturer dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="8c894-145">Selects a portion of the incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8c894-146">window</span><span class="sxs-lookup"><span data-stu-id="8c894-146">window</span></span>                       | <span data-ttu-id="8c894-147">Restaure la taille initiale de la fenêtre à l’écran.</span><span class="sxs-lookup"><span data-stu-id="8c894-147">Restores the initial window size on the display.</span></span> <span data-ttu-id="8c894-148">Cette commande affiche également la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8c894-148">This command also displays the window.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8c894-149">fenêtre au *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8c894-149">window at *rectangle*</span></span>        | <span data-ttu-id="8c894-150">Modifie la taille et l’emplacement de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8c894-150">Changes the size and location of the display window.</span></span> <span data-ttu-id="8c894-151">Le rectangle spécifié est relatif à la fenêtre parente de la fenêtre d’affichage (généralement le bureau) si l’indicateur « style Child » a été utilisé pour la commande [Open](open.md) .</span><span class="sxs-lookup"><span data-stu-id="8c894-151">The specified rectangle is relative to the parent window of the display window (usually the desktop) if the "style child" flag has been used for the [open](open.md) command.</span></span> <span data-ttu-id="8c894-152">Pour modifier l’emplacement de la fenêtre sans modifier sa hauteur ou sa largeur, spécifiez une valeur égale à zéro pour la hauteur et la largeur.</span><span class="sxs-lookup"><span data-stu-id="8c894-152">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span> |
| <span data-ttu-id="8c894-153">client Windows</span><span class="sxs-lookup"><span data-stu-id="8c894-153">window client</span></span>                | <span data-ttu-id="8c894-154">Restaure la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8c894-154">Restores the client area of the window.</span></span>                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8c894-155">client Windows au *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8c894-155">window client at *rectangle*</span></span> | <span data-ttu-id="8c894-156">Modifie la taille et l’emplacement de la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8c894-156">Changes the size and location of the client area of the window.</span></span> <span data-ttu-id="8c894-157">Le rectangle spécifié est relatif à la fenêtre parente de la fenêtre cliente.</span><span class="sxs-lookup"><span data-stu-id="8c894-157">The specified rectangle is relative to the parent window of the client window.</span></span> <span data-ttu-id="8c894-158">Pour modifier l’emplacement de la fenêtre sans modifier sa hauteur ou sa largeur, spécifiez une valeur égale à zéro pour la hauteur et la largeur.</span><span class="sxs-lookup"><span data-stu-id="8c894-158">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span>                                                                                      |



 

<span data-ttu-id="8c894-159">Lorsqu’un indicateur comprend un rectangle, les coordonnées des rectangles sont relatives à l’origine de la fenêtre ou à l’origine de l’image, selon le cas, et sont spécifiées comme **x1 Y1 x2 Y2**.</span><span class="sxs-lookup"><span data-stu-id="8c894-159">When a flag includes a rectangle, the rectangle coordinates are relative to the window origin or the image origin, as appropriate, and are specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="8c894-160">Les coordonnées **X1Y1** spécifient l’angle supérieur gauche, tandis que les coordonnées **X2Y2** spécifient la largeur et la hauteur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="8c894-160">The coordinates **X1Y1** specify the upper left corner, and the coordinates **X2Y2** specify the width and height of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="8c894-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="8c894-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8c894-162">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="8c894-162">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="8c894-163">Pour les appareils vidéo numériques, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="8c894-163">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="8c894-164">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8c894-164">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c894-165">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8c894-165">Return Value</span></span>

<span data-ttu-id="8c894-166">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="8c894-166">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c894-167">Notes</span><span class="sxs-lookup"><span data-stu-id="8c894-167">Remarks</span></span>

<span data-ttu-id="8c894-168">La commande put définit un ou plusieurs des rectangles suivants lorsque vous travaillez avec des appareils de superposition vidéo :</span><span class="sxs-lookup"><span data-stu-id="8c894-168">The put command defines one or more of the following rectangles when working with video-overlay devices:</span></span>

-   <span data-ttu-id="8c894-169">Le rectangle vidéo définit la région de l’image vidéo entrante à capturer.</span><span class="sxs-lookup"><span data-stu-id="8c894-169">The video rectangle defines the region of the incoming video image to capture.</span></span>
-   <span data-ttu-id="8c894-170">Le rectangle de cadre définit la région de la mémoire tampon de trame qui reçoit l’image vidéo entrante.</span><span class="sxs-lookup"><span data-stu-id="8c894-170">The frame rectangle defines the region of the frame buffer that receives the incoming video image.</span></span>
-   <span data-ttu-id="8c894-171">Le rectangle source définit la région de la mémoire tampon de trame qui est copiée dans le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="8c894-171">The source rectangle defines which region of the frame buffer is copied to the destination rectangle.</span></span>
-   <span data-ttu-id="8c894-172">Le rectangle de destination définit la région de la zone cliente de la fenêtre d’affichage qui reçoit l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="8c894-172">The destination rectangle defines the region of the display window client area that receives the video image.</span></span>

<span data-ttu-id="8c894-173">Le rectangle vidéo est lié au rectangle de cadre de la même façon que le rectangle source est lié au rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="8c894-173">The video rectangle is related to the frame rectangle in the same way the source rectangle is related to the destination rectangle.</span></span> <span data-ttu-id="8c894-174">L’étirement peut se produire du rectangle vidéo vers le rectangle de frame et du rectangle source vers le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="8c894-174">Stretching can occur from the video rectangle to the frame rectangle and from the source rectangle to the destination rectangle.</span></span> <span data-ttu-id="8c894-175">Tous les appareils ne prennent pas en charge l’étirement et l’étirement doit être activé (à l’aide de la commande [Set](set.md) ).</span><span class="sxs-lookup"><span data-stu-id="8c894-175">Not all devices support stretching, and stretching must be enabled (by using the [set](set.md) command).</span></span>

<span data-ttu-id="8c894-176">La commande suivante définit trois régions pour la vidéo, le frame et la source.</span><span class="sxs-lookup"><span data-stu-id="8c894-176">The following command defines three regions for the video, frame, and source.</span></span>

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

<span data-ttu-id="8c894-177">Les régions de cet exemple sont définies comme suit :</span><span class="sxs-lookup"><span data-stu-id="8c894-177">The regions in this example are defined as follows:</span></span>

-   <span data-ttu-id="8c894-178">Une région de 200 x 200 pixels des données vidéo entrantes, en commençant à l’origine 120 pixels de l’angle supérieur gauche, sera capturée dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="8c894-178">A 200- by 200-pixel region of the incoming video data, starting at an origin 120 pixels from the upper left corner, will be captured to the frame buffer.</span></span>
-   <span data-ttu-id="8c894-179">Les données vidéo seront placées dans une région de 200 par 200 pixels dans le coin supérieur gauche de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="8c894-179">The video data will be placed in a 200- by 200-pixel region at the upper left corner of the frame buffer.</span></span>
-   <span data-ttu-id="8c894-180">Les transferts sont effectués à partir de la région 200-par 200-pixels située dans le coin supérieur gauche de la mémoire tampon de trame vers la fenêtre de destination.</span><span class="sxs-lookup"><span data-stu-id="8c894-180">Transfers are made from the 200- by 200-pixel region at the upper left corner of the frame buffer to the destination window.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c894-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c894-181">Requirements</span></span>



| <span data-ttu-id="8c894-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c894-182">Requirement</span></span> | <span data-ttu-id="8c894-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c894-183">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8c894-184">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c894-184">Minimum supported client</span></span><br/> | <span data-ttu-id="8c894-185">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c894-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8c894-186">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c894-186">Minimum supported server</span></span><br/> | <span data-ttu-id="8c894-187">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c894-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8c894-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c894-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c894-189">MCI</span><span class="sxs-lookup"><span data-stu-id="8c894-189">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8c894-190">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="8c894-190">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="8c894-191">open</span><span class="sxs-lookup"><span data-stu-id="8c894-191">open</span></span>](open.md)
</dt> <dt>

[<span data-ttu-id="8c894-192">set</span><span class="sxs-lookup"><span data-stu-id="8c894-192">set</span></span>](set.md)
</dt> </dl>

 

