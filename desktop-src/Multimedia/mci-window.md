---
title: Commande MCI_WINDOW (mmsystem. h)
description: La \_ commande de fenêtre MCI spécifie la fenêtre et les caractéristiques de la fenêtre pour les périphériques graphiques. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- Commande MCI_WINDOW Windows multimédia
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942274"
---
# <a name="mci_window-command"></a><span data-ttu-id="e5700-105">\_Commande de fenêtre MCI</span><span class="sxs-lookup"><span data-stu-id="e5700-105">MCI\_WINDOW command</span></span>

<span data-ttu-id="e5700-106">La \_ commande de fenêtre MCI spécifie la fenêtre et les caractéristiques de la fenêtre pour les périphériques graphiques.</span><span class="sxs-lookup"><span data-stu-id="e5700-106">The MCI\_WINDOW command specifies the window and the window characteristics for graphic devices.</span></span> <span data-ttu-id="e5700-107">Les appareils vidéo et vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="e5700-107">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="e5700-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="e5700-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
);
```



## <a name="parameters"></a><span data-ttu-id="e5700-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5700-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5700-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e5700-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e5700-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="e5700-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="e5700-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="e5700-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e5700-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="e5700-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="e5700-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e5700-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5700-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span><span class="sxs-lookup"><span data-stu-id="e5700-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span></span>
</dt> <dd>

<span data-ttu-id="e5700-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="e5700-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="e5700-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="e5700-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5700-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e5700-118">Return Value</span></span>

<span data-ttu-id="e5700-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="e5700-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5700-120">Notes</span><span class="sxs-lookup"><span data-stu-id="e5700-120">Remarks</span></span>

<span data-ttu-id="e5700-121">Les appareils graphiques doivent créer une fenêtre par défaut lorsqu’un appareil est ouvert, mais ne doivent pas l’afficher tant qu’ils n’ont pas reçu la commande [MCI \_ Play](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="e5700-121">Graphic devices should create a default window when a device is opened but should not display it until they receive the [MCI\_PLAY](mci-play.md) command.</span></span> <span data-ttu-id="e5700-122">La \_ commande de fenêtre MCI est utilisée pour fournir une fenêtre créée par l’application à l’appareil et pour modifier les caractéristiques d’affichage d’une fenêtre d’affichage définie par l’application ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="e5700-122">The MCI\_WINDOW command is used to supply an application-created window to the device and to change the display characteristics of an application-defined or default display window.</span></span> <span data-ttu-id="e5700-123">Si l’application fournit la fenêtre d’affichage, vous devez préparer la mise à jour d’un rectangle non valide dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e5700-123">If the application supplies the display window, it should be prepared to update an invalid rectangle on the window.</span></span>

<span data-ttu-id="e5700-124">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="e5700-124">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="e5700-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>\_HWND de \_ fenêtre \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="e5700-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI\_DGV\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="e5700-126">Le descripteur de la fenêtre nécessaire pour une utilisation comme destination est inclus dans le membre **HWND** de la structure identifiée par *lpWindow*.</span><span class="sxs-lookup"><span data-stu-id="e5700-126">The handle of the window needed for use as the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span>

</dd> <dt>

<span data-ttu-id="e5700-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>État de la \_ fenêtre DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="e5700-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>MCI\_DGV\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="e5700-128">Le membre **nCmdShow** de la structure identifiée par *lpWindow* contient des paramètres pour définir l’état de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e5700-128">The **nCmdShow** member of the structure identified by *lpWindow* contains parameters for setting the window state.</span></span>

</dd> <dt>

<span data-ttu-id="e5700-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>texte de la \_ fenêtre DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="e5700-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI\_DGV\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="e5700-130">Le membre **lpstrText** de la structure identifiée par *lpWindow* contient l’adresse d’une mémoire tampon contenant la légende utilisée dans la barre de titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e5700-130">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used in the window title bar.</span></span>

</dd> </dl>

<span data-ttu-id="e5700-131">Pour les périphériques vidéo numériques, le paramètre *lpWindow* pointe vers une structure de [**\_ \_ fenêtre \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="e5700-131">For digital-video devices, the *lpWindow* parameter points to an [**MCI\_DGV\_WINDOW\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) structure.</span></span>

<span data-ttu-id="e5700-132">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique de **superposition** :</span><span class="sxs-lookup"><span data-stu-id="e5700-132">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="e5700-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>\_fenêtre OVLY \_ MCI \_ désactiver \_ Stretch</span><span class="sxs-lookup"><span data-stu-id="e5700-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI\_OVLY\_WINDOW\_DISABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="e5700-134">Désactive l’étirement de l’image.</span><span class="sxs-lookup"><span data-stu-id="e5700-134">Disables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="e5700-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>\_fenêtre OVLY \_ MCI \_ activer \_ Stretch</span><span class="sxs-lookup"><span data-stu-id="e5700-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI\_OVLY\_WINDOW\_ENABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="e5700-136">Active l’étirement de l’image.</span><span class="sxs-lookup"><span data-stu-id="e5700-136">Enables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="e5700-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>\_HWND de \_ fenêtre \_ OVLY MCI</span><span class="sxs-lookup"><span data-stu-id="e5700-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI\_OVLY\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="e5700-138">Le descripteur de la fenêtre utilisée pour la destination est inclus dans le membre **HWND** de la structure identifiée par *lpWindow*.</span><span class="sxs-lookup"><span data-stu-id="e5700-138">The handle of the window used for the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span> <span data-ttu-id="e5700-139">Définissez cet indicateur sur MCI \_ OVLY \_ \_ par défaut pour revenir à la fenêtre par défaut.</span><span class="sxs-lookup"><span data-stu-id="e5700-139">Set this flag to MCI\_OVLY\_WINDOW\_DEFAULT to return to the default window.</span></span>

</dd> <dt>

<span data-ttu-id="e5700-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>État de la \_ fenêtre OVLY MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="e5700-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>MCI\_OVLY\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="e5700-141">Le membre **nCmdShow** de la structure *lpWindow* contient des paramètres pour définir l’état de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e5700-141">The **nCmdShow** member of the *lpWindow* structure contains parameters for setting the window state.</span></span> <span data-ttu-id="e5700-142">Cet indicateur revient à appeler [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) avec le paramètre *State* .</span><span class="sxs-lookup"><span data-stu-id="e5700-142">This flag is equivalent to calling [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) with the *state* parameter.</span></span> <span data-ttu-id="e5700-143">Les constantes sont les mêmes que celles définies dans les fenêtres. H (tels que SW \_ Hide, SW \_ Minimize ou SW \_ SHOWNORMAL).</span><span class="sxs-lookup"><span data-stu-id="e5700-143">The constants are the same as those defined in WINDOWS.H (such as SW\_HIDE, SW\_MINIMIZE, or SW\_SHOWNORMAL).</span></span>

</dd> <dt>

<span data-ttu-id="e5700-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>texte de la \_ fenêtre OVLY MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="e5700-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>MCI\_OVLY\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="e5700-145">Le membre **lpstrText** de la structure identifiée par *lpWindow* contient l’adresse d’une mémoire tampon contenant la légende utilisée pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e5700-145">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used for the window.</span></span>

</dd> </dl>

<span data-ttu-id="e5700-146">Pour les périphériques de superposition vidéo, le paramètre *lpWindow* pointe vers une structure de fenêtre d’affichage [**MCI \_ OVLY \_ \_**](mci-ovly-window-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="e5700-146">For video-overlay devices, the *lpWindow* parameter points to an [**MCI\_OVLY\_WINDOW\_PARMS**](mci-ovly-window-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5700-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5700-147">Requirements</span></span>



| <span data-ttu-id="e5700-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5700-148">Requirement</span></span> | <span data-ttu-id="e5700-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5700-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5700-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5700-150">Minimum supported client</span></span><br/> | <span data-ttu-id="e5700-151">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5700-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e5700-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5700-152">Minimum supported server</span></span><br/> | <span data-ttu-id="e5700-153">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5700-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e5700-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5700-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5700-155"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5700-155"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5700-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5700-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5700-157">MCI</span><span class="sxs-lookup"><span data-stu-id="e5700-157">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e5700-158">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="e5700-158">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

