---
title: Commande MCI_WHERE (mmsystem. h)
description: La \_ commande MCI qui obtient le rectangle de découpage du périphérique vidéo.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- Commande MCI_WHERE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942186"
---
# <a name="mci_where-command"></a><span data-ttu-id="5127f-104">\_Commande MCI Where</span><span class="sxs-lookup"><span data-stu-id="5127f-104">MCI\_WHERE command</span></span>

<span data-ttu-id="5127f-105">La \_ commande MCI qui obtient le rectangle de découpage du périphérique vidéo.</span><span class="sxs-lookup"><span data-stu-id="5127f-105">The MCI\_WHERE command obtains the clipping rectangle for the video device.</span></span> <span data-ttu-id="5127f-106">Les appareils vidéo et vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="5127f-106">Digital-video, and video-overlay devices recognize this command.</span></span> <span data-ttu-id="5127f-107">Les membres **supérieur** et **gauche** du [Rect](/previous-versions//ms536136(v=vs.85)) retourné contiennent l’origine du rectangle de découpage, et les membres de **droite** et du **bas** contiennent la largeur et la hauteur du rectangle de découpage.</span><span class="sxs-lookup"><span data-stu-id="5127f-107">The **top** and **left** members of the returned [RECT](/previous-versions//ms536136(v=vs.85)) contain the origin of the clipping rectangle, and the **right** and **bottom** members contain the width and height of the clipping rectangle.</span></span> <span data-ttu-id="5127f-108">(Il ne s’agit pas de l’utilisation standard des membres **droits** et **inférieurs** .)</span><span class="sxs-lookup"><span data-stu-id="5127f-108">(This is not the standard use of the **right** and **bottom** members.)</span></span>

<span data-ttu-id="5127f-109">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="5127f-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
);
```



## <a name="parameters"></a><span data-ttu-id="5127f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5127f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5127f-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5127f-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5127f-112">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="5127f-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5127f-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5127f-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5127f-114">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="5127f-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="5127f-115">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5127f-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5127f-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span><span class="sxs-lookup"><span data-stu-id="5127f-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span></span>
</dt> <dd>

<span data-ttu-id="5127f-117">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="5127f-117">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="5127f-118">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="5127f-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5127f-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5127f-119">Return Value</span></span>

<span data-ttu-id="5127f-120">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="5127f-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5127f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="5127f-121">Remarks</span></span>

<span data-ttu-id="5127f-122">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="5127f-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5127f-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>\_DGV MCI \_ où \_ destination</span><span class="sxs-lookup"><span data-stu-id="5127f-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI\_DGV\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="5127f-124">Obtient une description de la zone rectangulaire utilisée pour afficher la vidéo et les images dans la zone cliente de la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="5127f-124">Obtains a description of the rectangular region used to display video and images in the client area of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="5127f-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI \_ DGV \_ où \_ Frame</span><span class="sxs-lookup"><span data-stu-id="5127f-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI\_DGV\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="5127f-126">Obtient une description de la zone rectangulaire de la mémoire tampon de trame dans laquelle les images du rectangle vidéo sont mises à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="5127f-126">Obtains a description of the rectangular region of the frame buffer into which images from the video rectangle are scaled.</span></span> <span data-ttu-id="5127f-127">Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="5127f-127">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="5127f-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>DGV MCI, \_ \_ où \_ Max</span><span class="sxs-lookup"><span data-stu-id="5127f-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI\_DGV\_WHERE\_MAX</span></span>
</dt> <dd>

<span data-ttu-id="5127f-129">En cas d’utilisation avec MCI \_ DGV \_ où \_ destination ou MCI \_ DGV \_ où \_ source, le rectangle retourné indique la largeur et la hauteur maximales de la région spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5127f-129">When used with MCI\_DGV\_WHERE\_DESTINATION or MCI\_DGV\_WHERE\_SOURCE, the rectangle returned indicates the maximum width and height of the specified region.</span></span> <span data-ttu-id="5127f-130">Lorsqu’il est utilisé avec MCI \_ DGV \_ \_ , le rectangle retourné indique la taille de l’affichage entier.</span><span class="sxs-lookup"><span data-stu-id="5127f-130">When used with MCI\_DGV\_WHERE\_WINDOW, the rectangle returned indicates the size of the entire display.</span></span>

</dd> <dt>

<span data-ttu-id="5127f-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV \_ où \_ source</span><span class="sxs-lookup"><span data-stu-id="5127f-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI\_DGV\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="5127f-132">Obtient une description de la zone rectangulaire (rognée de la mémoire tampon de frame) qui est étirée pour s’ajuster au rectangle de destination sur l’affichage.</span><span class="sxs-lookup"><span data-stu-id="5127f-132">Obtains a description of the rectangular region (cropped from the frame buffer) that is stretched to fit the destination rectangle on the display.</span></span>

</dd> <dt>

<span data-ttu-id="5127f-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI \_ DGV \_ où \_ vidéo</span><span class="sxs-lookup"><span data-stu-id="5127f-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI\_DGV\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="5127f-134">Obtient une description de la zone rectangulaire rognée de la source de présentation pour remplir le rectangle de cadre dans la mémoire tampon de frame.</span><span class="sxs-lookup"><span data-stu-id="5127f-134">Obtains a description of the rectangular region cropped from the presentation source to fill the frame rectangle in the frame buffer.</span></span> <span data-ttu-id="5127f-135">Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="5127f-135">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="5127f-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI \_ DGV \_ où \_ fenêtre</span><span class="sxs-lookup"><span data-stu-id="5127f-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI\_DGV\_WHERE\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="5127f-137">Obtient une description du frame de fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5127f-137">Obtains a description of the display-window frame.</span></span>

</dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="5127f-138">Pour les périphériques vidéo numériques, le paramètre *lpQuery* pointe vers un **MCI \_ DGV \_ où \_** la structure PARMS.</span><span class="sxs-lookup"><span data-stu-id="5127f-138">For digital-video devices, the *lpQuery* parameter points to an **MCI\_DGV\_WHERE\_PARMS** structure.</span></span> <span data-ttu-id="5127f-139">La structure **MCI \_ DGV \_ où \_ parms** est identique à la structure [**MCI \_ DGV \_ rect \_ parms**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="5127f-139">The **MCI\_DGV\_WHERE\_PARMS** structure is identical to the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="5127f-140">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique de **superposition** :</span><span class="sxs-lookup"><span data-stu-id="5127f-140">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5127f-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>\_OVLY MCI \_ où \_ destination</span><span class="sxs-lookup"><span data-stu-id="5127f-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI\_OVLY\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="5127f-142">Obtient le rectangle d’affichage de la destination.</span><span class="sxs-lookup"><span data-stu-id="5127f-142">Obtains the destination display rectangle.</span></span> <span data-ttu-id="5127f-143">Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="5127f-143">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="5127f-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI \_ OVLY \_ où \_ Frame</span><span class="sxs-lookup"><span data-stu-id="5127f-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI\_OVLY\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="5127f-145">Obtient le rectangle de frame de superposition.</span><span class="sxs-lookup"><span data-stu-id="5127f-145">Obtains the overlay frame rectangle.</span></span> <span data-ttu-id="5127f-146">Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="5127f-146">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="5127f-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ où \_ source</span><span class="sxs-lookup"><span data-stu-id="5127f-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI\_OVLY\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="5127f-148">Obtient le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="5127f-148">Obtains the source rectangle.</span></span> <span data-ttu-id="5127f-149">Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="5127f-149">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="5127f-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI \_ OVLY \_ où \_ vidéo</span><span class="sxs-lookup"><span data-stu-id="5127f-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI\_OVLY\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="5127f-151">Obtient le rectangle vidéo.</span><span class="sxs-lookup"><span data-stu-id="5127f-151">Obtains the video rectangle.</span></span> <span data-ttu-id="5127f-152">Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="5127f-152">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> </dl>

<span data-ttu-id="5127f-153">Pour les périphériques de superposition vidéo, le paramètre *lpQuery* pointe vers une structure [**MCI \_ OVLY \_ rect \_ PARMS**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="5127f-153">For video-overlay devices, the *lpQuery* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5127f-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5127f-154">Requirements</span></span>



| <span data-ttu-id="5127f-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5127f-155">Requirement</span></span> | <span data-ttu-id="5127f-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="5127f-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5127f-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5127f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="5127f-158">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5127f-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5127f-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5127f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="5127f-160">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5127f-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5127f-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="5127f-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="5127f-162"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5127f-162"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5127f-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5127f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5127f-164">MCI</span><span class="sxs-lookup"><span data-stu-id="5127f-164">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5127f-165">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="5127f-165">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

