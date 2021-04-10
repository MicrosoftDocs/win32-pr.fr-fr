---
title: Commande MCI_CAPTURE (mmsystem. h)
description: La \_ commande MCI capture capture le contenu de la mémoire tampon de trame et le stocke dans un fichier spécifié. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- Commande MCI_CAPTURE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942439"
---
# <a name="mci_capture-command"></a><span data-ttu-id="cc2f4-105">\_Commande de capture MCI</span><span class="sxs-lookup"><span data-stu-id="cc2f4-105">MCI\_CAPTURE command</span></span>

<span data-ttu-id="cc2f4-106">La \_ commande MCI capture capture le contenu de la mémoire tampon de trame et le stocke dans un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="cc2f4-106">The MCI\_CAPTURE command captures the contents of the frame buffer and stores it in a specified file.</span></span> <span data-ttu-id="cc2f4-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="cc2f4-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="cc2f4-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="cc2f4-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
);
```



## <a name="parameters"></a><span data-ttu-id="cc2f4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc2f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc2f4-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="cc2f4-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="cc2f4-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="cc2f4-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="cc2f4-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cc2f4-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cc2f4-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="cc2f4-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="cc2f4-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cc2f4-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc2f4-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span><span class="sxs-lookup"><span data-stu-id="cc2f4-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span></span>
</dt> <dd>

<span data-ttu-id="cc2f4-116">Pointeur vers une structure de [**\_ DGV de \_ capture \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="cc2f4-116">Pointer to an [**MCI\_DGV\_CAPTURE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc2f4-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc2f4-117">Return Value</span></span>

<span data-ttu-id="cc2f4-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="cc2f4-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc2f4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="cc2f4-119">Remarks</span></span>

<span data-ttu-id="cc2f4-120">Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :</span><span class="sxs-lookup"><span data-stu-id="cc2f4-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="cc2f4-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI \_ DGV \_ capture \_ en tant que</span><span class="sxs-lookup"><span data-stu-id="cc2f4-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI\_DGV\_CAPTURE\_AS</span></span>
</dt> <dd>

<span data-ttu-id="cc2f4-122">Le membre **lpstrFileName** de la structure identifiée par *lpCapture* contient l’adresse d’une mémoire tampon spécifiant le chemin d’accès et le nom de fichier de destination.</span><span class="sxs-lookup"><span data-stu-id="cc2f4-122">The **lpstrFileName** member of the structure identified by *lpCapture* contains an address of a buffer specifying the destination path and filename.</span></span> <span data-ttu-id="cc2f4-123">(Cet indicateur est obligatoire.)</span><span class="sxs-lookup"><span data-stu-id="cc2f4-123">(This flag is required.)</span></span>

</dd> <dt>

<span data-ttu-id="cc2f4-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>\_DGV \_ de la capture MCI \_ sur</span><span class="sxs-lookup"><span data-stu-id="cc2f4-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI\_DGV\_CAPTURE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="cc2f4-125">Le membre **RC** de la structure identifiée par *lpCapture* contient un rectangle valide.</span><span class="sxs-lookup"><span data-stu-id="cc2f4-125">The **rc** member of the structure identified by *lpCapture* contains a valid rectangle.</span></span> <span data-ttu-id="cc2f4-126">Le rectangle spécifie la zone rectangulaire dans la mémoire tampon de trame qui est rognée et enregistrée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="cc2f4-126">The rectangle specifies the rectangular region within the frame buffer that is cropped and saved to disk.</span></span> <span data-ttu-id="cc2f4-127">En cas d’omission, la zone rognée est définie par défaut sur le rectangle spécifié ou par défaut sur une commande [ \_ put précédente MCI](mci-put.md) qui spécifie la zone source pour cette instance du pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="cc2f4-127">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [MCI\_PUT](mci-put.md) command that specifies the source area for this instance of the device driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc2f4-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc2f4-128">Requirements</span></span>



| <span data-ttu-id="cc2f4-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc2f4-129">Requirement</span></span> | <span data-ttu-id="cc2f4-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc2f4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2f4-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc2f4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cc2f4-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc2f4-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cc2f4-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc2f4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cc2f4-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc2f4-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cc2f4-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc2f4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc2f4-136"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc2f4-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc2f4-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc2f4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc2f4-138">MCI</span><span class="sxs-lookup"><span data-stu-id="cc2f4-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cc2f4-139">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="cc2f4-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

