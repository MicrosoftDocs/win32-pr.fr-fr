---
title: Commande MCI_OPEN (mmsystem. h)
description: La \_ commande Open MCI Initialise un appareil ou un fichier. Tous les appareils reconnaissent cette commande.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- Commande MCI_OPEN Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843045"
---
# <a name="mci_open-command"></a><span data-ttu-id="27997-105">\_Commande d’ouverture MCI</span><span class="sxs-lookup"><span data-stu-id="27997-105">MCI\_OPEN command</span></span>

<span data-ttu-id="27997-106">La \_ commande Open MCI Initialise un appareil ou un fichier.</span><span class="sxs-lookup"><span data-stu-id="27997-106">The MCI\_OPEN command initializes a device or file.</span></span> <span data-ttu-id="27997-107">Tous les appareils reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="27997-107">All devices recognize this command.</span></span>

<span data-ttu-id="27997-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="27997-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
);
```



## <a name="parameters"></a><span data-ttu-id="27997-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27997-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27997-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="27997-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="27997-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="27997-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="27997-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="27997-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="27997-113">\_Attente MCI Notify ou MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="27997-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="27997-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="27997-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="27997-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span><span class="sxs-lookup"><span data-stu-id="27997-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span></span>
</dt> <dd>

<span data-ttu-id="27997-116">Pointeur désignant une structure de [**\_ \_ PARMS ouverte avec MCI**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="27997-116">Pointer to an [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span> <span data-ttu-id="27997-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="27997-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27997-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27997-118">Return Value</span></span>

<span data-ttu-id="27997-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="27997-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="27997-120">Notes</span><span class="sxs-lookup"><span data-stu-id="27997-120">Remarks</span></span>

<span data-ttu-id="27997-121">L' \_ indicateur de \_ type Open MCI doit être utilisé chaque fois qu’un appareil est spécifié dans la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="27997-121">The MCI\_OPEN\_TYPE flag must be used whenever a device is specified in the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="27997-122">Si vous ouvrez un appareil en spécifiant une constante de type d’appareil, vous devez spécifier \_ l' \_ indicateur MCI Open type \_ ID en plus du \_ type MCI Open \_ .</span><span class="sxs-lookup"><span data-stu-id="27997-122">If you open a device by specifying a device-type constant, you must specify the MCI\_OPEN\_TYPE\_ID flag in addition to MCI\_OPEN\_TYPE.</span></span> <span data-ttu-id="27997-123">Pour obtenir la liste des constantes de type d’appareil, consultez [types d’appareils MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="27997-123">For a list of device-type constants, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="27997-124">Si l' \_ indicateur de \_ partage ouvert MCI n’est pas spécifié lors de l’ouverture initiale d’un appareil ou d’un fichier, toutes les commandes Open MCI ultérieures \_ à l’appareil ou au fichier échoueront.</span><span class="sxs-lookup"><span data-stu-id="27997-124">If the MCI\_OPEN\_SHAREABLE flag is not specified when a device or file is initially opened, all subsequent MCI\_OPEN commands to the device or file will fail.</span></span> <span data-ttu-id="27997-125">Si l’appareil ou le fichier est déjà ouvert et que cet indicateur n’est pas spécifié, l’appel échoue même si la première commande ouverte a spécifié le \_ partage MCI ouvert \_ .</span><span class="sxs-lookup"><span data-stu-id="27997-125">If the device or file is already open and this flag is not specified, the call will fail even if the first open command specified MCI\_OPEN\_SHAREABLE.</span></span> <span data-ttu-id="27997-126">Fichiers ouverts pour MCISEQ. DRV et MCIWAVE. Les appareils DRV ne peuvent pas être partagés.</span><span class="sxs-lookup"><span data-stu-id="27997-126">Files opened for the MCISEQ.DRV and MCIWAVE.DRV devices are nonsharable.</span></span>

<span data-ttu-id="27997-127">La casse est ignorée dans le nom de l’appareil, mais il ne peut pas y avoir de espaces à gauche ou à droite.</span><span class="sxs-lookup"><span data-stu-id="27997-127">Case is ignored in the device name, but there cannot be leading or trailing blanks.</span></span>

<span data-ttu-id="27997-128">Pour utiliser la sélection automatique de type (via les entrées du registre), affectez le nom de fichier et l’extension de fichier au membre **lpstrElementName** de la structure identifiée par *lpOpen*, affectez la valeur **null** au membre **lpstrDeviceType** et définissez l' \_ indicateur d’élément Open MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="27997-128">To use automatic type selection (via the entries in the registry), assign the filename and file extension to the **lpstrElementName** member of the structure identified by *lpOpen*, set the **lpstrDeviceType** member to **NULL**, and set the MCI\_OPEN\_ELEMENT flag.</span></span>

<span data-ttu-id="27997-129">Les indicateurs supplémentaires suivants s’appliquent à tous les appareils prenant en charge MCI \_ Open :</span><span class="sxs-lookup"><span data-stu-id="27997-129">The following additional flags apply to all devices supporting MCI\_OPEN:</span></span>

<dl> <dt>

<span data-ttu-id="27997-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>\_alias d’ouverture MCI \_</span><span class="sxs-lookup"><span data-stu-id="27997-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI\_OPEN\_ALIAS</span></span>
</dt> <dd>

<span data-ttu-id="27997-131">Un alias est inclus dans le membre **lpstrAlias** de la structure identifiée par *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="27997-131">An alias is included in the **lpstrAlias** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="27997-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>\_ouvrir un \_ partage MCI</span><span class="sxs-lookup"><span data-stu-id="27997-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI\_OPEN\_SHAREABLE</span></span>
</dt> <dd>

<span data-ttu-id="27997-133">L’appareil ou le fichier doit être ouvert comme partageable.</span><span class="sxs-lookup"><span data-stu-id="27997-133">The device or file should be opened as sharable.</span></span>

</dd> <dt>

<span data-ttu-id="27997-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>\_type d’ouverture MCI \_</span><span class="sxs-lookup"><span data-stu-id="27997-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI\_OPEN\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="27997-135">Un nom ou une constante de type d’appareil est inclus dans le membre **lpstrDeviceType** de la structure identifiée par *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="27997-135">A device type name or constant is included in the **lpstrDeviceType** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="27997-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>\_ID de \_ type d’ouverture MCI \_</span><span class="sxs-lookup"><span data-stu-id="27997-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI\_OPEN\_TYPE\_ID</span></span>
</dt> <dd>

<span data-ttu-id="27997-137">Le mot de poids faible du membre **lpstrDeviceType** de la structure identifiée par *lpOpen* contient un identificateur de type d’appareil MCI standard et le mot de poids fort peut éventuellement contenir l’index ordinal de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="27997-137">The low-order word of the **lpstrDeviceType** member of the structure identified by *lpOpen* contains a standard MCI device type identifier and the high-order word optionally contains the ordinal index for the device.</span></span> <span data-ttu-id="27997-138">Utilisez cet indicateur avec l' \_ indicateur de \_ type Open MCI.</span><span class="sxs-lookup"><span data-stu-id="27997-138">Use this flag with the MCI\_OPEN\_TYPE flag.</span></span>

</dd> </dl>

<span data-ttu-id="27997-139">Les indicateurs supplémentaires suivants s’appliquent aux appareils composés :</span><span class="sxs-lookup"><span data-stu-id="27997-139">The following additional flags apply to compound devices:</span></span>

<dl> <dt>

<span data-ttu-id="27997-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI \_ Open ( \_ élément)</span><span class="sxs-lookup"><span data-stu-id="27997-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI\_OPEN\_ELEMENT</span></span>
</dt> <dd>

<span data-ttu-id="27997-141">Un nom de fichier est inclus dans le membre **lpstrElementName** de la structure identifiée par *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="27997-141">A filename is included in the **lpstrElementName** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="27997-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>\_ID d' \_ élément \_ Open MCI</span><span class="sxs-lookup"><span data-stu-id="27997-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI\_OPEN\_ELEMENT\_ID</span></span>
</dt> <dd>

<span data-ttu-id="27997-143">Le membre **lpstrElementName** de la structure identifiée par *lpOpen* est interprété comme une valeur **DWORD** et a une signification interne à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="27997-143">The **lpstrElementName** member of the structure identified by *lpOpen* is interpreted as a **DWORD** value and has meaning internal to the device.</span></span> <span data-ttu-id="27997-144">Utilisez cet indicateur avec l' \_ indicateur d' \_ élément Open MCI.</span><span class="sxs-lookup"><span data-stu-id="27997-144">Use this flag with the MCI\_OPEN\_ELEMENT flag.</span></span>

</dd> </dl>

<span data-ttu-id="27997-145">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="27997-145">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="27997-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ ouvrir \_ nostatic</span><span class="sxs-lookup"><span data-stu-id="27997-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI\_DGV\_OPEN\_NOSTATIC</span></span>
</dt> <dd>

<span data-ttu-id="27997-147">L’appareil doit réduire le nombre de couleurs (système) statiques dans la palette.</span><span class="sxs-lookup"><span data-stu-id="27997-147">The device should reduce the number of static (system) colors in the palette.</span></span> <span data-ttu-id="27997-148">Cela augmente le nombre de couleurs disponibles pour le rendu du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="27997-148">This increases the number of colors available for rendering the video stream.</span></span> <span data-ttu-id="27997-149">Cet indicateur s’applique uniquement aux appareils qui partagent une palette avec Windows.</span><span class="sxs-lookup"><span data-stu-id="27997-149">This flag applies only to devices that share a palette with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="27997-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>\_DGV \_ Open \_ parent de MCI</span><span class="sxs-lookup"><span data-stu-id="27997-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI\_DGV\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="27997-151">Le handle de la fenêtre parente est spécifié dans le membre **hwndParent** de la structure identifiée par *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="27997-151">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="27997-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ Open \_ WS</span><span class="sxs-lookup"><span data-stu-id="27997-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI\_DGV\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="27997-153">Un style de fenêtre est spécifié dans le membre **dwStyle** de la structure identifiée par *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="27997-153">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="27997-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ ouvrir le \_ 16 bits</span><span class="sxs-lookup"><span data-stu-id="27997-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI\_DGV\_OPEN\_16BIT</span></span>
</dt> <dd>

<span data-ttu-id="27997-155">Indique une préférence pour la prise en charge des appareils MCI 16 bits.</span><span class="sxs-lookup"><span data-stu-id="27997-155">Indicates a preference for 16-bit MCI device support.</span></span>

</dd> <dt>

<span data-ttu-id="27997-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ Open \_ 32 bits</span><span class="sxs-lookup"><span data-stu-id="27997-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI\_DGV\_OPEN\_32BIT</span></span>
</dt> <dd>

<span data-ttu-id="27997-157">Indique une préférence pour la prise en charge des appareils MCI 32 bits.</span><span class="sxs-lookup"><span data-stu-id="27997-157">Indicates a preference for 32-bit MCI device support.</span></span>

</dd> </dl>

<span data-ttu-id="27997-158">Pour les périphériques vidéo numériques, le paramètre *lpOpen* pointe vers une structure [**MCI \_ DGV \_ Open \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="27997-158">For digital-video devices, the *lpOpen* parameter points to an [**MCI\_DGV\_OPEN\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) structure.</span></span>

<span data-ttu-id="27997-159">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique de **superposition** :</span><span class="sxs-lookup"><span data-stu-id="27997-159">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="27997-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>\_OVLY \_ Open \_ parent de MCI</span><span class="sxs-lookup"><span data-stu-id="27997-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI\_OVLY\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="27997-161">Le handle de la fenêtre parente est spécifié dans le membre **hwndParent** de la structure identifiée par *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="27997-161">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="27997-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ Open \_ WS</span><span class="sxs-lookup"><span data-stu-id="27997-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI\_OVLY\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="27997-163">Un style de fenêtre est spécifié dans le membre **dwStyle** de la structure identifiée par *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="27997-163">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span> <span data-ttu-id="27997-164">La valeur **dwStyle** spécifie le style de la fenêtre que le pilote créera et affichera si l’application n’en fournit pas.</span><span class="sxs-lookup"><span data-stu-id="27997-164">The **dwStyle** value specifies the style of the window that the driver will create and display if the application does not provide one.</span></span> <span data-ttu-id="27997-165">Le paramètre style prend un entier qui définit le style de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="27997-165">The style parameter takes an integer that defines the window style.</span></span> <span data-ttu-id="27997-166">Ces constantes sont les mêmes que les styles de fenêtre standard (tels que WS \_ Child, WS \_ OVERLAPPEDWINDOW ou WS \_ popup).</span><span class="sxs-lookup"><span data-stu-id="27997-166">These constants are the same as the standard window styles (such as WS\_CHILD, WS\_OVERLAPPEDWINDOW, or WS\_POPUP).</span></span>

</dd> </dl>

<span data-ttu-id="27997-167">Pour les périphériques de superposition vidéo, le paramètre *lpOpen* pointe vers une structure de paramètres d' [**ouverture (MCI \_ OVLY \_ Open \_ PARMS**](mci-ovly-open-parms.md) ).</span><span class="sxs-lookup"><span data-stu-id="27997-167">For video-overlay devices, the *lpOpen* parameter points to an [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md) structure.</span></span>

<span data-ttu-id="27997-168">L’indicateur supplémentaire suivant est utilisé avec le type d’appareil **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="27997-168">The following additional flag is used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="27997-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>\_tampon d' \_ ouverture MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="27997-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI\_WAVE\_OPEN\_BUFFER</span></span>
</dt> <dd>

<span data-ttu-id="27997-170">Une longueur de tampon est spécifiée dans le membre **dwBufferSeconds** de la structure identifiée par *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="27997-170">A buffer length is specified in the **dwBufferSeconds** member of the structure identified by *lpOpen*.</span></span>

</dd> </dl>

<span data-ttu-id="27997-171">Pour les périphériques audio Waveform, le paramètre *lpOpen* pointe vers une structure de paramètres d’ouverture de l' [**\_ onde \_ \_ MCI**](mci-wave-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="27997-171">For waveform-audio devices, the *lpOpen* parameter points to an [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) structure.</span></span> <span data-ttu-id="27997-172">Le pilote MCIWAVE requiert un périphérique audio Wave asynchrone.</span><span class="sxs-lookup"><span data-stu-id="27997-172">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="27997-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27997-173">Requirements</span></span>



| <span data-ttu-id="27997-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27997-174">Requirement</span></span> | <span data-ttu-id="27997-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="27997-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27997-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27997-176">Minimum supported client</span></span><br/> | <span data-ttu-id="27997-177">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27997-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="27997-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27997-178">Minimum supported server</span></span><br/> | <span data-ttu-id="27997-179">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27997-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="27997-180">En-tête</span><span class="sxs-lookup"><span data-stu-id="27997-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="27997-181"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27997-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27997-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27997-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27997-183">MCI</span><span class="sxs-lookup"><span data-stu-id="27997-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="27997-184">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="27997-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

