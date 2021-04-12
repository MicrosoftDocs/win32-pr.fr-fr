---
title: Commande MCI_UPDATE (mmsystem. h)
description: La \_ commande de mise à jour MCI met à jour le rectangle d’affichage. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- Commande MCI_UPDATE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105910"
---
# <a name="mci_update-command"></a><span data-ttu-id="1f2f4-105">\_Commande de mise à jour MCI</span><span class="sxs-lookup"><span data-stu-id="1f2f4-105">MCI\_UPDATE command</span></span>

<span data-ttu-id="1f2f4-106">La \_ commande de mise à jour MCI met à jour le rectangle d’affichage.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-106">The MCI\_UPDATE command updates the display rectangle.</span></span> <span data-ttu-id="1f2f4-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="1f2f4-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="1f2f4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f2f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f2f4-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1f2f4-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1f2f4-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="1f2f4-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1f2f4-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1f2f4-113">**MCI \_ NOTIFY**, **MCI \_ Wait** ou, pour les périphériques vidéo numériques, **\_ test MCI**.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="1f2f4-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1f2f4-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f2f4-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span><span class="sxs-lookup"><span data-stu-id="1f2f4-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="1f2f4-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1f2f4-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="1f2f4-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="1f2f4-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f2f4-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f2f4-118">Return Value</span></span>

<span data-ttu-id="1f2f4-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f2f4-120">Notes</span><span class="sxs-lookup"><span data-stu-id="1f2f4-120">Remarks</span></span>

<span data-ttu-id="1f2f4-121">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil « Digitalvideo » :</span><span class="sxs-lookup"><span data-stu-id="1f2f4-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="1f2f4-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI \_ DGV \_ mise à jour \_ HDC</span><span class="sxs-lookup"><span data-stu-id="1f2f4-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI\_DGV\_UPDATE\_HDC</span></span>
</dt> <dd>

<span data-ttu-id="1f2f4-123">Le membre **HDC** de la structure identifiée par *lpDest* contient une fenêtre valide du contrôleur de contenu à peindre.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-123">The **hDC** member of the structure identified by *lpDest* contains a valid window of the DC to paint.</span></span> <span data-ttu-id="1f2f4-124">Cet indicateur est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-124">This flag is required.</span></span>

</dd> <dt>

<span data-ttu-id="1f2f4-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="1f2f4-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="1f2f4-126">Le membre **RC** de la structure identifiée par *lpUnfreeze* contient un rectangle d’affichage valide.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-126">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="1f2f4-127">Le rectangle spécifie le rectangle de découpage par rapport au rectangle client.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-127">The rectangle specifies the clipping rectangle relative to the client rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="1f2f4-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>\_ \_ mise à jour de MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="1f2f4-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI\_DGV\_UPDATE\_PAINT</span></span>
</dt> <dd>

<span data-ttu-id="1f2f4-129">Une application utilise cet indicateur lorsqu’elle reçoit un message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) destiné à un contrôleur de périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-129">An application uses this flag when it receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message that is intended for a display DC.</span></span> <span data-ttu-id="1f2f4-130">En général, un périphérique de mémoire tampon de trame peint la couleur de la clé.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-130">A frame-buffer device usually paints the key color.</span></span> <span data-ttu-id="1f2f4-131">Si le périphérique d’affichage n’a pas de mémoire tampon de trame, il est possible qu’il ignore la \_ commande de mise à jour de MCI lorsque l’indicateur de **\_ peinture MCI DGV \_ \_ Update** est utilisé, car l’affichage est repeint au cours de l’opération de lecture.</span><span class="sxs-lookup"><span data-stu-id="1f2f4-131">If the display device does not have a frame buffer, it might ignore the MCI\_UPDATE command when the **MCI\_DGV\_UPDATE\_PAINT** flag is used because the display will be repainted during the playback operation.</span></span>

</dd> </dl>

<span data-ttu-id="1f2f4-132">Pour les périphériques vidéo numériques, le paramètre *lpDest* pointe vers une structure de [**\_ \_ mise \_ à jour MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) .</span><span class="sxs-lookup"><span data-stu-id="1f2f4-132">For digital-video devices, the *lpDest* parameter points to an [**MCI\_DGV\_UPDATE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2f4-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f2f4-133">Requirements</span></span>



| <span data-ttu-id="1f2f4-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f2f4-134">Requirement</span></span> | <span data-ttu-id="1f2f4-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f2f4-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2f4-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f2f4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1f2f4-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f2f4-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1f2f4-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f2f4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1f2f4-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f2f4-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1f2f4-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f2f4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f2f4-141"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f2f4-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f2f4-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f2f4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f2f4-143">MCI</span><span class="sxs-lookup"><span data-stu-id="1f2f4-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1f2f4-144">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="1f2f4-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

