---
title: Commande MCI_BREAK (mmsystem. h)
description: La \_ commande MCI Break définit une clé d’arrêt pour un appareil MCI. MCI prend en charge cette commande directement au lieu de la transmettre à l’appareil. Toute application MCI peut utiliser cette commande.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- Commande MCI_BREAK Windows multimédia
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464990"
---
# <a name="mci_break-command"></a><span data-ttu-id="301dd-106">\_Commande MCI Break</span><span class="sxs-lookup"><span data-stu-id="301dd-106">MCI\_BREAK command</span></span>

<span data-ttu-id="301dd-107">La \_ commande MCI Break définit une clé d’arrêt pour un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="301dd-107">The MCI\_BREAK command sets a break key for an MCI device.</span></span> <span data-ttu-id="301dd-108">MCI prend en charge cette commande directement au lieu de la transmettre à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="301dd-108">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="301dd-109">Toute application MCI peut utiliser cette commande.</span><span class="sxs-lookup"><span data-stu-id="301dd-109">Any MCI application can use this command.</span></span>

<span data-ttu-id="301dd-110">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="301dd-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
);
```



## <a name="parameters"></a><span data-ttu-id="301dd-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="301dd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="301dd-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="301dd-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="301dd-113">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="301dd-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="301dd-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="301dd-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="301dd-115">MCI \_ Notify, MCI \_ Wait ou, pour les appareils Digital-Video et Video-cassette Recorder (magnétoscope), \_ test MCI.</span><span class="sxs-lookup"><span data-stu-id="301dd-115">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and video-cassette recorder (VCR) devices, MCI\_TEST.</span></span> <span data-ttu-id="301dd-116">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="301dd-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="301dd-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span><span class="sxs-lookup"><span data-stu-id="301dd-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span></span>
</dt> <dd>

<span data-ttu-id="301dd-118">Pointeur vers une structure de [**\_ \_ sauts MCI**](mci-break-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="301dd-118">Pointer to an [**MCI\_ BREAK\_PARMS**](mci-break-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="301dd-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="301dd-119">Return Value</span></span>

<span data-ttu-id="301dd-120">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="301dd-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="301dd-121">Notes</span><span class="sxs-lookup"><span data-stu-id="301dd-121">Remarks</span></span>

<span data-ttu-id="301dd-122">Vous devrez peut-être appuyer plusieurs fois sur la touche pause pour interrompre une opération d’attente.</span><span class="sxs-lookup"><span data-stu-id="301dd-122">You might have to press the break key multiple times to interrupt a wait operation.</span></span> <span data-ttu-id="301dd-123">Le fait d’appuyer sur la touche Attn après l’annulation d’un appareil peut envoyer la pause à une application.</span><span class="sxs-lookup"><span data-stu-id="301dd-123">Pressing the break key after a device wait is canceled can send the break to an application.</span></span> <span data-ttu-id="301dd-124">Si une application a une action définie pour le code de clé virtuelle, elle peut répondre par inadvertance à l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="301dd-124">If an application has an action defined for the virtual-key code, then it can inadvertently respond to the break.</span></span> <span data-ttu-id="301dd-125">Par exemple, une application utilisant VK \_ Annuler pour une touche accélérateur peut répondre à la touche CTRL + ATTN par défaut si elle est appuyée après l’annulation d’une attente.</span><span class="sxs-lookup"><span data-stu-id="301dd-125">For example, an application using VK\_CANCEL for an accelerator key can respond to the default CTRL+BREAK key if it is pressed after a wait is canceled.</span></span>

<span data-ttu-id="301dd-126">Les indicateurs supplémentaires suivants s’appliquent à tous les appareils :</span><span class="sxs-lookup"><span data-stu-id="301dd-126">The following additional flags apply to all devices:</span></span>

<dl> <dt>

<span data-ttu-id="301dd-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>\_HWND de pause MCI \_</span><span class="sxs-lookup"><span data-stu-id="301dd-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI\_BREAK\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="301dd-128">Le membre **hwndBreak** de la structure identifiée par *lpBreak* contient un handle de fenêtre qui doit être la fenêtre active afin d’activer la détection de rupture pour ce périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="301dd-128">The **hwndBreak** member of the structure identified by *lpBreak* contains a window handle that must be the current window in order to enable break detection for that MCI device.</span></span> <span data-ttu-id="301dd-129">Il s’agit généralement de la fenêtre principale de l’application.</span><span class="sxs-lookup"><span data-stu-id="301dd-129">This is usually the application's main window.</span></span> <span data-ttu-id="301dd-130">En cas d’omission, MCI ne vérifie pas le handle de fenêtre de la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="301dd-130">If omitted, MCI does not check the window handle of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="301dd-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>\_touche pause \_ MCI</span><span class="sxs-lookup"><span data-stu-id="301dd-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI\_BREAK\_KEY</span></span>
</dt> <dd>

<span data-ttu-id="301dd-132">Le membre **nVirtKey** de la structure identifiée par *lpBreak* spécifie le code de touche virtuelle utilisé pour la touche Attn.</span><span class="sxs-lookup"><span data-stu-id="301dd-132">The **nVirtKey** member of the structure identified by *lpBreak* specifies the virtual-key code used for the break key.</span></span> <span data-ttu-id="301dd-133">Par défaut, MCI attribue la touche d’arrêt CTRL + ATTN.</span><span class="sxs-lookup"><span data-stu-id="301dd-133">By default, MCI assigns CTRL+BREAK as the break key.</span></span> <span data-ttu-id="301dd-134">Cet indicateur est requis si la \_ \_ déconnexion MCI n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="301dd-134">This flag is required if MCI\_BREAK\_OFF is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="301dd-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>\_Pause MCI \_</span><span class="sxs-lookup"><span data-stu-id="301dd-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI\_BREAK\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="301dd-136">Désactive toute clé d’arrêt existante pour l’appareil indiqué.</span><span class="sxs-lookup"><span data-stu-id="301dd-136">Disables any existing break key for the indicated device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="301dd-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="301dd-137">Requirements</span></span>



| <span data-ttu-id="301dd-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="301dd-138">Requirement</span></span> | <span data-ttu-id="301dd-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="301dd-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="301dd-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="301dd-140">Minimum supported client</span></span><br/> | <span data-ttu-id="301dd-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="301dd-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="301dd-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="301dd-142">Minimum supported server</span></span><br/> | <span data-ttu-id="301dd-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="301dd-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="301dd-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="301dd-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="301dd-145"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="301dd-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="301dd-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="301dd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301dd-147">MCI</span><span class="sxs-lookup"><span data-stu-id="301dd-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="301dd-148">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="301dd-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

