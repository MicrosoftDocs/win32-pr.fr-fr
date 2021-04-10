---
title: Commande MCI_PUT (mmsystem. h)
description: La \_ commande MCI put définit les rectangles de la source, de la destination et du frame. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- Commande MCI_PUT Windows multimédia
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106537"
---
# <a name="mci_put-command"></a><span data-ttu-id="f4ddb-105">\_Commande put MCI</span><span class="sxs-lookup"><span data-stu-id="f4ddb-105">MCI\_PUT command</span></span>

<span data-ttu-id="f4ddb-106">La \_ commande MCI put définit les rectangles de la source, de la destination et du frame.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-106">The MCI\_PUT command sets the source, destination, and frame rectangles.</span></span> <span data-ttu-id="f4ddb-107">Les appareils vidéo et vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="f4ddb-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="f4ddb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4ddb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ddb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f4ddb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f4ddb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="f4ddb-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="f4ddb-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f4ddb-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span><span class="sxs-lookup"><span data-stu-id="f4ddb-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f4ddb-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="f4ddb-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="f4ddb-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ddb-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f4ddb-118">Return Value</span></span>

<span data-ttu-id="f4ddb-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ddb-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f4ddb-120">Remarks</span></span>

<span data-ttu-id="f4ddb-121">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="f4ddb-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f4ddb-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>\_client MCI DGV \_ put \_</span><span class="sxs-lookup"><span data-stu-id="f4ddb-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI\_DGV\_PUT\_CLIENT</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-123">Le rectangle défini pour MCI \_ DGV \_ Rect s’applique à la position de la fenêtre cliente.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-123">The rectangle defined for MCI\_DGV\_RECT applies to the position of the client window.</span></span> <span data-ttu-id="f4ddb-124">Le rectangle spécifié est relatif à la fenêtre parente de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-124">The rectangle specified is relative to the parent window of the display window.</span></span> <span data-ttu-id="f4ddb-125">\_ \_ La fenêtre put DGV MCI \_ doit être définie simultanément avec cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-125">MCI\_DGV\_PUT\_WINDOW must be set concurrently with this flag.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>DGV de mise en place de la \_ \_ \_ destination MCI</span><span class="sxs-lookup"><span data-stu-id="f4ddb-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI\_DGV\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-127">Le rectangle défini pour MCI \_ DGV \_ rect spécifie un rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-127">The rectangle defined for MCI\_DGV\_RECT specifies a destination rectangle.</span></span> <span data-ttu-id="f4ddb-128">Le rectangle de destination spécifie la partie de la fenêtre cliente associée à cette instance de pilote de périphérique qui affiche l’image ou la vidéo.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-128">The destination rectangle specifies the portion of the client window associated with this device driver instance that shows the image or video.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>\_ \_ image put DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f4ddb-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI\_DGV\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-130">Le rectangle défini pour MCI \_ DGV \_ Rect s’applique au rectangle de cadre.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-130">The rectangle defined for MCI\_DGV\_RECT applies to the frame rectangle.</span></span> <span data-ttu-id="f4ddb-131">Le rectangle de frame spécifie la partie de la mémoire tampon de trame utilisée comme destination des images vidéo obtenues à partir du rectangle vidéo.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-131">The frame rectangle specifies the portion of the frame buffer used as the destination of the video images obtained from the video rectangle.</span></span> <span data-ttu-id="f4ddb-132">La vidéo doit être mise à l’échelle pour s’ajuster au rectangle de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-132">The video should be scaled to fit within the frame buffer rectangle.</span></span>

<span data-ttu-id="f4ddb-133">Le rectangle est spécifié dans les coordonnées de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-133">The rectangle is specified in frame buffer coordinates.</span></span> <span data-ttu-id="f4ddb-134">Le rectangle par défaut est la mémoire tampon d’image complète.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-134">The default rectangle is the full frame buffer.</span></span> <span data-ttu-id="f4ddb-135">La spécification de ce rectangle permet à l’appareil de mettre l’image à l’échelle au fur et à mesure qu’elle numérise les données.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-135">Specifying this rectangle lets the device scale the image as it digitizes the data.</span></span> <span data-ttu-id="f4ddb-136">Les appareils qui ne peuvent pas mettre à l’échelle l’image rejettent cette commande avec une \_ fonction non prise en charge par MCIERR \_ .</span><span class="sxs-lookup"><span data-stu-id="f4ddb-136">Devices that cannot scale the image reject this command with MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="f4ddb-137">Vous pouvez utiliser l' \_ indicateur MCI GETDEVCAPS \_ peut \_ Stretch avec la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) pour déterminer si un appareil met à l’échelle l’image.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-137">You can use the MCI\_GETDEVCAPS\_CAN\_STRETCH flag with the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command to determine if a device scales the image.</span></span> <span data-ttu-id="f4ddb-138">Un appareil retourne la **valeur false** s’il ne peut pas mettre l’image à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-138">A device returns **FALSE** if it cannot scale the image.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>\_source MCI DGV \_ put \_</span><span class="sxs-lookup"><span data-stu-id="f4ddb-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI\_DGV\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-140">Le rectangle défini pour MCI \_ DGV \_ rect spécifie un rectangle source.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-140">The rectangle defined for MCI\_DGV\_RECT specifies a source rectangle.</span></span> <span data-ttu-id="f4ddb-141">Le rectangle source spécifie la partie de la mémoire tampon de trame à mettre à l’échelle pour s’ajuster au rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-141">The source rectangle specifies which portion of the frame buffer is to be scaled to fit into the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>\_vidéo MCI DGV \_ put \_</span><span class="sxs-lookup"><span data-stu-id="f4ddb-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI\_DGV\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-143">Le rectangle défini pour MCI \_ DGV \_ Rect s’applique au rectangle vidéo.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-143">The rectangle defined for MCI\_DGV\_RECT applies to the video rectangle.</span></span> <span data-ttu-id="f4ddb-144">Le rectangle vidéo spécifie la partie de la source de présentation actuelle qui est stockée dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-144">The video rectangle specifies which portion of the current presentation source is stored in the frame buffer.</span></span> <span data-ttu-id="f4ddb-145">Le rectangle est spécifié à l’aide des coordonnées naturelles de la source de présentation.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-145">The rectangle is specified using the natural coordinates of the presentation source.</span></span> <span data-ttu-id="f4ddb-146">Il permet la spécification du rognage qui se produit avant de stocker des images et des vidéos dans le tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-146">It allows the specification of cropping that occurs prior to storing images and video in the frame buffer.</span></span> <span data-ttu-id="f4ddb-147">Le rectangle par défaut est la zone de numérisation active complète ou les images et vidéos décompressées complètes.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-147">The default rectangle is the full active scan area or the full decompressed images and video.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>\_ \_ fenêtre put DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f4ddb-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI\_DGV\_PUT\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-149">Le rectangle défini pour MCI \_ DGV \_ Rect s’applique à la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-149">The rectangle defined for MCI\_DGV\_RECT applies to the display window.</span></span> <span data-ttu-id="f4ddb-150">Ce rectangle est relatif à la fenêtre parente de la fenêtre d’affichage (généralement le bureau).</span><span class="sxs-lookup"><span data-stu-id="f4ddb-150">This rectangle is relative to the parent window of the display window (usually the desktop).</span></span> <span data-ttu-id="f4ddb-151">Si la fenêtre n’est pas spécifiée, la taille et la position de la fenêtre initiale sont définies par défaut.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-151">If the window is not specified, it defaults to the initial window size and position.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="f4ddb-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-153">Le membre **RC** de la structure identifiée par *lpDest* contient un rectangle valide.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-153">The **rc** member of the structure identified by *lpDest* contains a valid rectangle.</span></span>

</dd> </dl>

<span data-ttu-id="f4ddb-154">Pour les périphériques vidéo numériques, *lpDest* pointe vers une structure [**MCI \_ DGV \_ put \_ PARMS**](/previous-versions//dd743397(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f4ddb-154">For digital-video devices, *lpDest* points to an [**MCI\_DGV\_PUT\_PARMS**](/previous-versions//dd743397(v=vs.85)) structure.</span></span>

<span data-ttu-id="f4ddb-155">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique de **superposition** :</span><span class="sxs-lookup"><span data-stu-id="f4ddb-155">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f4ddb-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>OVLY de mise en place de la \_ \_ \_ destination MCI</span><span class="sxs-lookup"><span data-stu-id="f4ddb-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI\_OVLY\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-157">Le rectangle défini pour MCI \_ OVLY \_ rect spécifie la zone de la fenêtre cliente utilisée pour afficher une image.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-157">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the client window used to display an image.</span></span> <span data-ttu-id="f4ddb-158">Le rectangle contient le décalage et l’étendue visible de l’image par rapport à l’origine de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-158">The rectangle contains the offset and visible extent of the image relative to the window origin.</span></span> <span data-ttu-id="f4ddb-159">Si le frame est étiré, la source est étirée sur le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-159">If the frame is being stretched, the source is stretched to the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>\_ \_ image put OVLY \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f4ddb-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI\_OVLY\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-161">Le rectangle défini pour MCI \_ OVLY \_ rect spécifie la zone de la mémoire tampon vidéo utilisée pour recevoir l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-161">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used to receive the video image.</span></span> <span data-ttu-id="f4ddb-162">Le rectangle contient le décalage et l’étendue de la zone de mémoire tampon par rapport à l’origine de la mémoire tampon vidéo.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-162">The rectangle contains the offset and extent of the buffer area relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>\_source MCI OVLY \_ put \_</span><span class="sxs-lookup"><span data-stu-id="f4ddb-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI\_OVLY\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-164">Le rectangle défini pour MCI \_ OVLY \_ rect spécifie la zone de la mémoire tampon vidéo utilisée comme source de l’image numérique.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-164">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used as the source of the digital image.</span></span> <span data-ttu-id="f4ddb-165">Le rectangle contient le décalage et l’étendue du rectangle de découpage pour la mémoire tampon vidéo par rapport à son origine.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-165">The rectangle contains the offset and extent of the clipping rectangle for the video buffer relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>\_vidéo MCI OVLY \_ put \_</span><span class="sxs-lookup"><span data-stu-id="f4ddb-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI\_OVLY\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-167">Le rectangle défini pour MCI \_ OVLY \_ rect spécifie la zone de la capture de la source vidéo par la mémoire tampon vidéo.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-167">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video source capture by the video buffer.</span></span> <span data-ttu-id="f4ddb-168">Le rectangle contient le décalage et l’étendue du rectangle de découpage pour la source vidéo par rapport à son origine.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-168">The rectangle contains the offset and extent of the clipping rectangle for the video source relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="f4ddb-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="f4ddb-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="f4ddb-170">Le membre **RC** de la structure identifiée par *lpDest* contient un rectangle d’affichage valide.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-170">The **rc** member of the structure identified by *lpDest* contains a valid display rectangle.</span></span> <span data-ttu-id="f4ddb-171">Si cet indicateur n’est pas spécifié, le rectangle par défaut correspond aux coordonnées du tampon vidéo ou de la fenêtre qui est découpée.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-171">If this flag is not specified, the default rectangle matches the coordinates of the video buffer or window being clipped.</span></span>

</dd> </dl>

<span data-ttu-id="f4ddb-172">Pour les périphériques de superposition vidéo, *lpDest* pointe vers une structure [**MCI \_ OVLY \_ rect \_ PARMS**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f4ddb-172">For video-overlay devices, *lpDest* points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ddb-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4ddb-173">Requirements</span></span>



| <span data-ttu-id="f4ddb-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4ddb-174">Requirement</span></span> | <span data-ttu-id="f4ddb-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4ddb-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ddb-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4ddb-176">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ddb-177">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4ddb-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f4ddb-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4ddb-178">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ddb-179">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4ddb-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f4ddb-180">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4ddb-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4ddb-181"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4ddb-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ddb-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4ddb-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ddb-183">MCI</span><span class="sxs-lookup"><span data-stu-id="f4ddb-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f4ddb-184">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="f4ddb-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

