---
title: Commande MCI_RESTORE (mmsystem. h)
description: La \_ commande de restauration MCI copie une image bitmap d’un fichier vers la mémoire tampon de trame. Les périphériques vidéo numériques reconnaissent cette commande. Cette commande effectue l’action inverse de la \_ commande de capture MCI.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- Commande MCI_RESTORE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742812"
---
# <a name="mci_restore-command"></a><span data-ttu-id="6a896-106">\_Commande de restauration MCI</span><span class="sxs-lookup"><span data-stu-id="6a896-106">MCI\_RESTORE command</span></span>

<span data-ttu-id="6a896-107">La \_ commande de restauration MCI copie une image bitmap d’un fichier vers la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="6a896-107">The MCI\_RESTORE command copies a bitmap from a file to the frame buffer.</span></span> <span data-ttu-id="6a896-108">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="6a896-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="6a896-109">Cette commande effectue l’action inverse de la commande de [ \_ capture MCI](mci-capture.md) .</span><span class="sxs-lookup"><span data-stu-id="6a896-109">This command performs the opposite action of the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

<span data-ttu-id="6a896-110">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="6a896-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
);
```



## <a name="parameters"></a><span data-ttu-id="6a896-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a896-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a896-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6a896-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6a896-113">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="6a896-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6a896-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6a896-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6a896-115">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="6a896-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="6a896-116">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6a896-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a896-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span><span class="sxs-lookup"><span data-stu-id="6a896-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span></span>
</dt> <dd>

<span data-ttu-id="6a896-118">Pointeur vers une structure de [**\_ paramètres de \_ restauration \_ DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="6a896-118">Pointer to an [**MCI\_DGV\_RESTORE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a896-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a896-119">Return Value</span></span>

<span data-ttu-id="6a896-120">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="6a896-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a896-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6a896-121">Remarks</span></span>

<span data-ttu-id="6a896-122">L’implémentation peut reconnaître un grand nombre de formats d’image, mais une image bitmap indépendante du périphérique (DIB) Windows est toujours acceptée.</span><span class="sxs-lookup"><span data-stu-id="6a896-122">The implementation can recognize a variety of image formats, but a Windows device-independent bitmap (DIB) is always accepted.</span></span>

<span data-ttu-id="6a896-123">Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :</span><span class="sxs-lookup"><span data-stu-id="6a896-123">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="6a896-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>\_ \_ restauration \_ à partir de MCI DGV</span><span class="sxs-lookup"><span data-stu-id="6a896-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI\_DGV\_RESTORE\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="6a896-125">Le membre **lpstrFileName** de la structure identifiée par *lpRestore* contient l’adresse d’une mémoire tampon contenant le nom du fichier source.</span><span class="sxs-lookup"><span data-stu-id="6a896-125">The **lpstrFileName** member of the structure identified by *lpRestore* contains an address of a buffer containing the source filename.</span></span> <span data-ttu-id="6a896-126">Le nom de fichier est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6a896-126">The filename is required.</span></span>

</dd> <dt>

<span data-ttu-id="6a896-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>\_ \_ restauration de DGV MCI \_ sur</span><span class="sxs-lookup"><span data-stu-id="6a896-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI\_DGV\_RESTORE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="6a896-128">Le membre **RC** de la structure identifiée par *lpRestore* contient un rectangle valide.</span><span class="sxs-lookup"><span data-stu-id="6a896-128">The **rc** member of the structure identified by *lpRestore* contains a valid rectangle.</span></span> <span data-ttu-id="6a896-129">Le rectangle spécifie une région de la mémoire tampon de trame par rapport à son origine.</span><span class="sxs-lookup"><span data-stu-id="6a896-129">The rectangle specifies a region of the frame buffer relative to its origin.</span></span> <span data-ttu-id="6a896-130">La première paire de coordonnées spécifie l’angle supérieur gauche du rectangle. la deuxième paire spécifie la largeur et la hauteur.</span><span class="sxs-lookup"><span data-stu-id="6a896-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="6a896-131">Si cet indicateur n’est pas spécifié, l’image est copiée dans l’angle supérieur gauche de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="6a896-131">If this flag is not specified, the image is copied to the upper left corner of the frame buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a896-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a896-132">Requirements</span></span>



| <span data-ttu-id="6a896-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a896-133">Requirement</span></span> | <span data-ttu-id="6a896-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a896-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a896-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a896-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6a896-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a896-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6a896-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a896-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6a896-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a896-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6a896-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a896-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a896-140"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a896-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a896-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a896-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a896-142">MCI</span><span class="sxs-lookup"><span data-stu-id="6a896-142">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6a896-143">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="6a896-143">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

