---
title: Commande MCI_QUALITY (mmsystem. h)
description: La \_ commande MCI Quality définit un niveau de qualité personnalisé pour l’audio, la vidéo ou la compression des données d’image fixe. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- Commande MCI_QUALITY Windows multimédia
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383855"
---
# <a name="mci_quality-command"></a><span data-ttu-id="44f7c-105">\_Commande de qualité MCI</span><span class="sxs-lookup"><span data-stu-id="44f7c-105">MCI\_QUALITY command</span></span>

<span data-ttu-id="44f7c-106">La \_ commande MCI Quality définit un niveau de qualité personnalisé pour l’audio, la vidéo ou la compression des données d’image fixe.</span><span class="sxs-lookup"><span data-stu-id="44f7c-106">The MCI\_QUALITY command defines a custom quality level for audio, video, or still image data compression.</span></span> <span data-ttu-id="44f7c-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="44f7c-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="44f7c-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="44f7c-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
);
```



## <a name="parameters"></a><span data-ttu-id="44f7c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44f7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f7c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="44f7c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="44f7c-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="44f7c-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="44f7c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="44f7c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="44f7c-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="44f7c-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="44f7c-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="44f7c-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="44f7c-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span><span class="sxs-lookup"><span data-stu-id="44f7c-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span></span>
</dt> <dd>

<span data-ttu-id="44f7c-116">Pointeur vers une structure de [**\_ \_ qualité \_ MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="44f7c-116">Pointer to an [**MCI\_DGV\_QUALITY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f7c-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="44f7c-117">Return Value</span></span>

<span data-ttu-id="44f7c-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="44f7c-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f7c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="44f7c-119">Remarks</span></span>

<span data-ttu-id="44f7c-120">Le nom défini pour ce niveau de qualité peut être utilisé lors de la définition de l’audio, de la vidéo ou encore de la qualité avec les commandes [MCI \_ SETAUDIO](mci-setaudio.md) et [MCI \_ SETVIDEO](mci-setvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="44f7c-120">The name defined for this quality level can be used when setting the audio, video, or still quality with the [MCI\_SETAUDIO](mci-setaudio.md) and [MCI\_SETVIDEO](mci-setvideo.md) commands.</span></span>

<span data-ttu-id="44f7c-121">Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :</span><span class="sxs-lookup"><span data-stu-id="44f7c-121">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="44f7c-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI \_ Quality \_ ALG</span><span class="sxs-lookup"><span data-stu-id="44f7c-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI\_QUALITY\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="44f7c-123">Le membre **lpstrAlgorithm** de la structure identifiée par *lpQuality* contient l’adresse d’une mémoire tampon contenant le nom de l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="44f7c-123">The **lpstrAlgorithm** member of the structure identified by *lpQuality* contains an address of a buffer containing the name of the algorithm.</span></span> <span data-ttu-id="44f7c-124">Cet algorithme doit être pris en charge par le pilote de périphérique et doit être compatible avec le descripteur audio, Persist ou Video utilisé.</span><span class="sxs-lookup"><span data-stu-id="44f7c-124">This algorithm must be supported by the device driver, and must be compatible with the audio, still, or video descriptor that is used.</span></span> <span data-ttu-id="44f7c-125">Si cet indicateur est omis, l’algorithme actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="44f7c-125">If this flag is omitted, the current algorithm is used.</span></span>

</dd> <dt>

<span data-ttu-id="44f7c-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_boîte de \_ dialogue qualité MCI</span><span class="sxs-lookup"><span data-stu-id="44f7c-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI\_QUALITY\_DIALOG</span></span>
</dt> <dd>

<span data-ttu-id="44f7c-127">Le pilote de périphérique doit afficher une boîte de dialogue permettant de spécifier le niveau de qualité.</span><span class="sxs-lookup"><span data-stu-id="44f7c-127">The device driver should display a dialog box for specifying the quality level.</span></span> <span data-ttu-id="44f7c-128">La boîte de dialogue contient des champs spécifiques à l’algorithme utilisés en interne par le pilote de périphérique pour créer une structure décrivant un niveau de qualité spécifique.</span><span class="sxs-lookup"><span data-stu-id="44f7c-128">The dialog box has algorithm-specific fields used internally by the device driver to create a structure describing a specific quality level.</span></span>

</dd> <dt>

<span data-ttu-id="44f7c-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>\_handle de qualité MCI \_</span><span class="sxs-lookup"><span data-stu-id="44f7c-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI\_QUALITY\_HANDLE</span></span>
</dt> <dd>

<span data-ttu-id="44f7c-130">Le membre **dwHandle** de la structure identifiée par *lpQuality* contient un handle vers une structure.</span><span class="sxs-lookup"><span data-stu-id="44f7c-130">The **dwHandle** member of the structure identified by *lpQuality* contains a handle to a structure.</span></span> <span data-ttu-id="44f7c-131">La structure contient des données algorithmiques qui décrivent le niveau de qualité spécifique.</span><span class="sxs-lookup"><span data-stu-id="44f7c-131">The structure contains algorithmic-specific data describing the specific quality level.</span></span> <span data-ttu-id="44f7c-132">Le format des structures pour les algorithmes dépend du périphérique.</span><span class="sxs-lookup"><span data-stu-id="44f7c-132">The format of the structures for the algorithms is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="44f7c-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_élément de qualité MCI \_</span><span class="sxs-lookup"><span data-stu-id="44f7c-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI\_QUALITY\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="44f7c-134">Constante indiquant que le type d’algorithme est inclus dans le membre **dwItem** de la structure identifiée par *lpQuality*.</span><span class="sxs-lookup"><span data-stu-id="44f7c-134">A constant indicating the type of algorithm is included in the **dwItem** member of the structure identified by *lpQuality*.</span></span>

</dd> <dt>

<span data-ttu-id="44f7c-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>nom de la \_ qualité MCI \_</span><span class="sxs-lookup"><span data-stu-id="44f7c-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>MCI\_QUALITY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="44f7c-136">Le membre **lpstrName** de la structure identifiée par *lpQuality* contient l’adresse d’une mémoire tampon contenant le descripteur de qualité.</span><span class="sxs-lookup"><span data-stu-id="44f7c-136">The **lpstrName** member of the structure identified by *lpQuality* contains an address of a buffer containing the quality descriptor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44f7c-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44f7c-137">Requirements</span></span>



| <span data-ttu-id="44f7c-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44f7c-138">Requirement</span></span> | <span data-ttu-id="44f7c-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="44f7c-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44f7c-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44f7c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="44f7c-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44f7c-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="44f7c-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44f7c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="44f7c-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44f7c-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="44f7c-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="44f7c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="44f7c-145"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44f7c-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44f7c-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44f7c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f7c-147">MCI</span><span class="sxs-lookup"><span data-stu-id="44f7c-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="44f7c-148">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="44f7c-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

