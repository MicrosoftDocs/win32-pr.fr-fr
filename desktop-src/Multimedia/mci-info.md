---
title: Commande MCI_INFO (mmsystem. h)
description: La \_ commande MCI info récupère les informations de chaîne d’un appareil.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- Commande MCI_INFO Windows multimédia
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105709"
---
# <a name="mci_info-command"></a><span data-ttu-id="838d6-104">\_Commande MCI info</span><span class="sxs-lookup"><span data-stu-id="838d6-104">MCI\_INFO command</span></span>

<span data-ttu-id="838d6-105">La \_ commande MCI info récupère les informations de chaîne d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="838d6-105">The MCI\_INFO command retrieves string information from a device.</span></span> <span data-ttu-id="838d6-106">Tous les appareils reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="838d6-106">All devices recognize this command.</span></span> <span data-ttu-id="838d6-107">Les informations sont retournées dans le membre **lpstrReturn** de la structure identifiée par *lpInfo*.</span><span class="sxs-lookup"><span data-stu-id="838d6-107">Information is returned in the **lpstrReturn** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="838d6-108">Le membre **dwRetSize** spécifie la longueur de la mémoire tampon pour les données retournées.</span><span class="sxs-lookup"><span data-stu-id="838d6-108">The **dwRetSize** member specifies the buffer length for the returned data.</span></span>

<span data-ttu-id="838d6-109">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="838d6-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
);
```



## <a name="parameters"></a><span data-ttu-id="838d6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="838d6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="838d6-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="838d6-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="838d6-112">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="838d6-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="838d6-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="838d6-114">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="838d6-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="838d6-115">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="838d6-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="838d6-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span><span class="sxs-lookup"><span data-stu-id="838d6-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span></span>
</dt> <dd>

<span data-ttu-id="838d6-117">Pointeur vers une structure d' [**\_ informations \_ sur MCI**](mci-info-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="838d6-117">Pointer to an [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure.</span></span> <span data-ttu-id="838d6-118">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="838d6-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="838d6-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="838d6-119">Return Value</span></span>

<span data-ttu-id="838d6-120">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="838d6-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="838d6-121">Notes</span><span class="sxs-lookup"><span data-stu-id="838d6-121">Remarks</span></span>

<span data-ttu-id="838d6-122">L’indicateur de code standard et spécifique à la commande suivant s’applique à tous les périphériques prenant en charge MCI \_ info :</span><span class="sxs-lookup"><span data-stu-id="838d6-122">The following additional standard and command-specific flag applies to all devices supporting MCI\_INFO:</span></span>

<dl> <dt>

<span data-ttu-id="838d6-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>\_produit MCI info \_</span><span class="sxs-lookup"><span data-stu-id="838d6-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI\_INFO\_PRODUCT</span></span>
</dt> <dd>

<span data-ttu-id="838d6-124">Obtient une description du matériel associé à un appareil.</span><span class="sxs-lookup"><span data-stu-id="838d6-124">Obtains a description of the hardware associated with a device.</span></span> <span data-ttu-id="838d6-125">Les appareils doivent fournir une description qui identifie le pilote et le matériel utilisés.</span><span class="sxs-lookup"><span data-stu-id="838d6-125">Devices should supply a description that identifies both the driver and the hardware used.</span></span>

</dd> </dl>

<span data-ttu-id="838d6-126">Les indicateurs supplémentaires suivants s’appliquent au type d’appareil **cdaudio** :</span><span class="sxs-lookup"><span data-stu-id="838d6-126">The following additional flags apply to the **cdaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="838d6-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>\_identité des \_ médias MCI info \_</span><span class="sxs-lookup"><span data-stu-id="838d6-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI\_INFO\_MEDIA\_IDENTITY</span></span>
</dt> <dd>

<span data-ttu-id="838d6-128">Produit un identificateur unique pour le CD audio actuellement chargé dans le lecteur interrogé.</span><span class="sxs-lookup"><span data-stu-id="838d6-128">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span> <span data-ttu-id="838d6-129">Cet indicateur retourne une chaîne de 16 chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="838d6-129">This flag returns a string of 16 hexadecimal digits.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI \_ info \_ Media \_ UPC</span><span class="sxs-lookup"><span data-stu-id="838d6-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI\_INFO\_MEDIA\_UPC</span></span>
</dt> <dd>

<span data-ttu-id="838d6-131">Produit le code UPC (Universal Product Code) encodé sur un CD audio.</span><span class="sxs-lookup"><span data-stu-id="838d6-131">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="838d6-132">Le UPC est une chaîne de chiffres.</span><span class="sxs-lookup"><span data-stu-id="838d6-132">The UPC is a string of digits.</span></span> <span data-ttu-id="838d6-133">Elle n’est peut-être pas disponible pour tous les CD.</span><span class="sxs-lookup"><span data-stu-id="838d6-133">It might not be available for all CDs.</span></span>

</dd> </dl>

<span data-ttu-id="838d6-134">Les indicateurs supplémentaires suivants s’appliquent au type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="838d6-134">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="838d6-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>\_élément d' \_ informations \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="838d6-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI\_DGV\_INFO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="838d6-136">Une constante indiquant les informations souhaitées est incluse dans le membre **dwItem** de la structure identifiée par *lpInfo*.</span><span class="sxs-lookup"><span data-stu-id="838d6-136">A constant indicating the information desired is included in the **dwItem** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="838d6-137">Les constantes suivantes sont définies pour les périphériques vidéo numériques :</span><span class="sxs-lookup"><span data-stu-id="838d6-137">The following constants are defined for digital-video devices:</span></span>

</dd> <dt>

<span data-ttu-id="838d6-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ info \_ audio \_ ALG</span><span class="sxs-lookup"><span data-stu-id="838d6-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI\_DGV\_INFO\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="838d6-139">Retourne le nom de l’algorithme de compression audio actuel.</span><span class="sxs-lookup"><span data-stu-id="838d6-139">Returns the name for the current audio compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI \_ DGV \_ info \_ audio- \_ qualité</span><span class="sxs-lookup"><span data-stu-id="838d6-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI\_DGV\_INFO\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="838d6-141">Retourne le nom du descripteur de qualité audio actuel.</span><span class="sxs-lookup"><span data-stu-id="838d6-141">Returns the name for the current audio quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>\_informations DGV \_ MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="838d6-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI\_DGV\_INFO\_STILL\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="838d6-143">Retourne le nom de l’algorithme de compression d’image continue actuel.</span><span class="sxs-lookup"><span data-stu-id="838d6-143">Returns the name for the current still image compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>la \_ qualité des informations DGV MCI est \_ \_ toujours \_</span><span class="sxs-lookup"><span data-stu-id="838d6-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI\_DGV\_INFO\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="838d6-145">Retourne le nom du descripteur de qualité d’image continue actuel.</span><span class="sxs-lookup"><span data-stu-id="838d6-145">Returns the name for the current still image quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>\_utilisation des \_ informations \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="838d6-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI\_DGV\_INFO\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="838d6-147">Retourne une chaîne qui décrit les restrictions d’utilisation qui peuvent être imposées par le propriétaire des données visuelles ou sonores dans l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="838d6-147">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audible data in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>\_vidéo d' \_ informations \_ DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="838d6-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI\_DGV\_INFO\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="838d6-149">Retourne le nom de l’algorithme de compression vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="838d6-149">Returns the name for the current video compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>\_ \_ qualité vidéo des informations DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="838d6-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI\_DGV\_INFO\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="838d6-151">Retourne le nom du descripteur de qualité vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="838d6-151">Returns the name for the current video quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>\_version d’informations MCI \_</span><span class="sxs-lookup"><span data-stu-id="838d6-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="838d6-153">Retourne le niveau de version du pilote de périphérique et du matériel.</span><span class="sxs-lookup"><span data-stu-id="838d6-153">Returns the release level of the device driver and hardware.</span></span> <span data-ttu-id="838d6-154">Les développeurs de pilotes de périphériques doivent documenter la syntaxe de la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="838d6-154">Device driver developers must document the syntax of the returned string.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>\_texte d' \_ informations \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="838d6-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI\_DGV\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="838d6-156">Obtient le titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="838d6-156">Obtains the window caption.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_fichier d’informations MCI \_</span><span class="sxs-lookup"><span data-stu-id="838d6-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="838d6-158">Obtient le chemin d’accès et le nom de fichier du dernier fichier spécifié avec la commande [MCI \_ Open](mci-open.md) ou [MCI \_ Load](mci-load.md) .</span><span class="sxs-lookup"><span data-stu-id="838d6-158">Obtains the path and filename of the last file specified with the [MCI\_OPEN](mci-open.md) or [MCI\_LOAD](mci-load.md) command.</span></span> <span data-ttu-id="838d6-159">Si un fichier n’a pas été spécifié, l’appareil retourne une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="838d6-159">If a file has not been specified, the device returns a null-terminated string.</span></span> <span data-ttu-id="838d6-160">Cet indicateur est pris en charge uniquement par les appareils qui retournent la **valeur true** à l' \_ indicateur MCI GETDEVCAPS \_ utilise \_ les fichiers de la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="838d6-160">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

<span data-ttu-id="838d6-161">Pour les périphériques vidéo numériques, *lpInfo* pointe vers une structure [**MCI \_ DGV \_ info \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="838d6-161">For digital-video devices, *lpInfo* points to an [**MCI\_DGV\_INFO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) structure.</span></span>

<span data-ttu-id="838d6-162">Les indicateurs supplémentaires suivants s’appliquent au type d’appareil **Sequencer** :</span><span class="sxs-lookup"><span data-stu-id="838d6-162">The following additional flags apply to the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="838d6-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>\_Copyright des informations MCI \_</span><span class="sxs-lookup"><span data-stu-id="838d6-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI\_INFO\_COPYRIGHT</span></span>
</dt> <dd>

<span data-ttu-id="838d6-164">Obtient l’avis de copyright du fichier MIDI à partir de l’événement de métadonnées de copyright.</span><span class="sxs-lookup"><span data-stu-id="838d6-164">Obtains the MIDI file copyright notice from the copyright meta event.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_fichier d’informations MCI \_</span><span class="sxs-lookup"><span data-stu-id="838d6-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="838d6-166">Obtient le nom du fichier actif.</span><span class="sxs-lookup"><span data-stu-id="838d6-166">Obtains the filename of the current file.</span></span> <span data-ttu-id="838d6-167">Cet indicateur est pris en charge uniquement par les appareils qui renvoient la **valeur true** lorsque vous appelez la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) avec l' \_ indicateur MCI GETDEVCAPS \_ utilise des \_ fichiers.</span><span class="sxs-lookup"><span data-stu-id="838d6-167">This flag is supported only by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>nom de l' \_ info MCI \_</span><span class="sxs-lookup"><span data-stu-id="838d6-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI\_INFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="838d6-169">Obtient le nom de la séquence à partir de l’événement de méta-nom de séquence/suivi.</span><span class="sxs-lookup"><span data-stu-id="838d6-169">Obtains the sequence name from the sequence/track name meta event.</span></span>

</dd> </dl>

<span data-ttu-id="838d6-170">L’indicateur supplémentaire suivant s’applique au type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="838d6-170">The following additional flag applies to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="838d6-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>\_version d' \_ informations \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="838d6-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI\_VCR\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="838d6-172">Définit le membre **lpstrReturn** de la structure d' [**\_ informations \_ sur MCI**](mci-info-parms.md) pour qu’il pointe vers le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="838d6-172">Sets **lpstrReturn** member of the [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure to point to the version number.</span></span> <span data-ttu-id="838d6-173">Définit également le membre **dwRetSize** égal à la longueur de la chaîne vers laquelle pointe.</span><span class="sxs-lookup"><span data-stu-id="838d6-173">Also sets the **dwRetSize** member equal to the length of the string pointed to.</span></span>

</dd> </dl>

<span data-ttu-id="838d6-174">Les indicateurs supplémentaires suivants s’appliquent au type de périphérique de **superposition** :</span><span class="sxs-lookup"><span data-stu-id="838d6-174">The following additional flags apply to the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="838d6-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_fichier d’informations MCI \_</span><span class="sxs-lookup"><span data-stu-id="838d6-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="838d6-176">Obtient le nom du fichier actif.</span><span class="sxs-lookup"><span data-stu-id="838d6-176">Obtains the filename of the current file.</span></span> <span data-ttu-id="838d6-177">Cet indicateur est pris en charge uniquement par les appareils qui retournent la **valeur true** à l' \_ indicateur MCI GETDEVCAPS \_ utilise \_ les fichiers de la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="838d6-177">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>\_texte d' \_ informations \_ OVLY MCI</span><span class="sxs-lookup"><span data-stu-id="838d6-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI\_OVLY\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="838d6-179">Obtient la légende de la fenêtre associée à l’appareil de superposition vidéo.</span><span class="sxs-lookup"><span data-stu-id="838d6-179">Obtains the caption of the window associated with the video-overlay device.</span></span>

</dd> </dl>

<span data-ttu-id="838d6-180">Les indicateurs supplémentaires suivants s’appliquent au type d’appareil **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="838d6-180">The following additional flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="838d6-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_fichier d’informations MCI \_</span><span class="sxs-lookup"><span data-stu-id="838d6-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="838d6-182">Obtient le nom du fichier actif.</span><span class="sxs-lookup"><span data-stu-id="838d6-182">Obtains the filename of the current file.</span></span> <span data-ttu-id="838d6-183">Cet indicateur est pris en charge par les appareils qui renvoient la **valeur true** lorsque vous appelez la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) avec l' \_ indicateur MCI GETDEVCAPS \_ utilise des \_ fichiers.</span><span class="sxs-lookup"><span data-stu-id="838d6-183">This flag is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrée MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="838d6-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="838d6-185">Obtient le nom de produit de l’entrée actuelle.</span><span class="sxs-lookup"><span data-stu-id="838d6-185">Obtains the product name of the current input.</span></span>

</dd> <dt>

<span data-ttu-id="838d6-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_sortie MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="838d6-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="838d6-187">Obtient le nom de produit de la sortie actuelle et sa valeur est spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="838d6-187">Obtains the product name of the current output and its value is device specific.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="838d6-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="838d6-188">Requirements</span></span>



| <span data-ttu-id="838d6-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="838d6-189">Requirement</span></span> | <span data-ttu-id="838d6-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="838d6-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838d6-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="838d6-191">Minimum supported client</span></span><br/> | <span data-ttu-id="838d6-192">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="838d6-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="838d6-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="838d6-193">Minimum supported server</span></span><br/> | <span data-ttu-id="838d6-194">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="838d6-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="838d6-195">En-tête</span><span class="sxs-lookup"><span data-stu-id="838d6-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="838d6-196"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="838d6-196"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="838d6-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="838d6-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838d6-198">MCI</span><span class="sxs-lookup"><span data-stu-id="838d6-198">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="838d6-199">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="838d6-199">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

