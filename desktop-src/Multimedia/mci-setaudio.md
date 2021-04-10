---
title: Commande MCI_SETAUDIO (mmsystem. h)
description: La \_ commande MCI SETAUDIO définit les valeurs associées à la lecture et à la capture audio. Les appareils vidéo numériques et VCR reconnaissent cette commande.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- Commande MCI_SETAUDIO Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20605ff78c62a8e688778692d5ca8f8e1342a968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200574"
---
# <a name="mci_setaudio-command"></a><span data-ttu-id="4ed52-105">\_Commande MCI SETAUDIO</span><span class="sxs-lookup"><span data-stu-id="4ed52-105">MCI\_SETAUDIO command</span></span>

<span data-ttu-id="4ed52-106">La \_ commande MCI SETAUDIO définit les valeurs associées à la lecture et à la capture audio.</span><span class="sxs-lookup"><span data-stu-id="4ed52-106">The MCI\_SETAUDIO command sets values associated with audio playback and capture.</span></span> <span data-ttu-id="4ed52-107">Les appareils vidéo numériques et VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="4ed52-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="4ed52-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="4ed52-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
);
```



## <a name="parameters"></a><span data-ttu-id="4ed52-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ed52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ed52-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4ed52-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="4ed52-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="4ed52-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="4ed52-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="4ed52-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4ed52-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span><span class="sxs-lookup"><span data-stu-id="4ed52-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="4ed52-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="4ed52-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="4ed52-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ed52-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4ed52-118">Return Value</span></span>

<span data-ttu-id="4ed52-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="4ed52-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ed52-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4ed52-120">Remarks</span></span>

<span data-ttu-id="4ed52-121">Les indicateurs suivants s’appliquent au type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="4ed52-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="4ed52-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ SETAUDIO \_ ALG</span><span class="sxs-lookup"><span data-stu-id="4ed52-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI\_DGV\_SETAUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-123">Le membre **lpstrAlgorithm** de la structure identifiée par *lpSetAudio* contient l’adresse d’une mémoire tampon contenant le nom d’un algorithme de compression audio.</span><span class="sxs-lookup"><span data-stu-id="4ed52-123">The **lpstrAlgorithm** member of the structure identified by *lpSetAudio* contains an address of a buffer containing the name of an audio compression algorithm.</span></span> <span data-ttu-id="4ed52-124">L’algorithme de compression est utilisé par les commandes de [ \_ réserve MCI](mci-reserve.md) ou d' [ \_ enregistrement MCI](mci-record.md) suivantes.</span><span class="sxs-lookup"><span data-stu-id="4ed52-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="4ed52-125">Les algorithmes disponibles dépendent du périphérique.</span><span class="sxs-lookup"><span data-stu-id="4ed52-125">The available algorithms are device dependent.</span></span> <span data-ttu-id="4ed52-126">Si l’algorithme est incompatible avec le format de fichier actuel, le format de fichier est remplacé par le format par défaut de l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="4ed52-126">If the algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ SETAUDIO \_ CLOCKTIME</span><span class="sxs-lookup"><span data-stu-id="4ed52-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI\_DGV\_SETAUDIO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-128">L’heure spécifiée est exprimée en millisecondes et est l’heure absolue quand elle est utilisée avec MCI \_ DGV \_ SETAUDIO \_ .</span><span class="sxs-lookup"><span data-stu-id="4ed52-128">The time specified is in milliseconds and is absolute time when used with MCI\_DGV\_SETAUDIO\_OVER.</span></span> <span data-ttu-id="4ed52-129">(Cette heure n’est pas à l’étape de la diffusion de l’espace de travail.)</span><span class="sxs-lookup"><span data-stu-id="4ed52-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>\_entrée MCI DGV \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI\_DGV\_SETAUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-131">Modifie l’indicateur Bass, aigus ou volume pour qu’il affecte le signal d’entrée et modifie ce qui est enregistré.</span><span class="sxs-lookup"><span data-stu-id="4ed52-131">Modifies the bass, treble, or volume flag so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="4ed52-132">Si possible, il s’agit de la valeur par défaut lors de l’analyse de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="4ed52-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>\_ \_ élément SETAUDIO DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI\_DGV\_SETAUDIO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-134">Une constante audio est spécifiée dans le membre **dwItem** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-134">An audio constant is specified in the **dwItem** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="4ed52-135">La constante identifie la valeur qui est définie.</span><span class="sxs-lookup"><span data-stu-id="4ed52-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="4ed52-136">Les constantes suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="4ed52-136">The following constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ SETAUDIO \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="4ed52-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI\_DGV\_SETAUDIO\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-138">Le nombre moyen d’octets est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-138">The average number of bytes is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="4ed52-139">Cette valeur définit le nombre moyen d’octets par seconde pour la diffusion ou l’enregistrement dans les formats PCM (Pulse Code Modulation) et ADPCM (Adaptive Differential Pulse Code Modulation).</span><span class="sxs-lookup"><span data-stu-id="4ed52-139">This value sets the average number of bytes per second for playing or recording in the PCM (Pulse Code Modulation) and ADPCM (Adaptive Differential Pulse Code Modulation) formats.</span></span> <span data-ttu-id="4ed52-140">Le fichier est enregistré dans ce format.</span><span class="sxs-lookup"><span data-stu-id="4ed52-140">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ DGV \_ SETAUDIO \_ Bass</span><span class="sxs-lookup"><span data-stu-id="4ed52-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI\_DGV\_SETAUDIO\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-142">Le niveau de fréquence basse audio est spécifié en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-142">The audio low frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ SETAUDIO \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="4ed52-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI\_DGV\_SETAUDIO\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-144">Le nombre de bits par échantillon est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-144">The number of bits per sample is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="4ed52-145">Cette valeur définit le nombre de bits par échantillon lu ou enregistré au format PCM.</span><span class="sxs-lookup"><span data-stu-id="4ed52-145">This value sets the number of bits per sample played or recorded in the PCM format.</span></span> <span data-ttu-id="4ed52-146">Le fichier est enregistré dans ce format.</span><span class="sxs-lookup"><span data-stu-id="4ed52-146">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ SETAUDIO \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="4ed52-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI\_DGV\_SETAUDIO\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-148">L’alignement du bloc de données est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-148">The data block alignment is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="4ed52-149">Cette valeur définit l’alignement des blocs de données par rapport au début des données de forme d’onde en entrée.</span><span class="sxs-lookup"><span data-stu-id="4ed52-149">This value sets the alignment of data blocks relative to the start of input waveform data.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ DGV \_ SETAUDIO \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="4ed52-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI\_DGV\_SETAUDIO\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-151">Le taux d’échantillonnage est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-151">The sample rate is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="4ed52-152">Cette valeur définit le taux d’échantillonnage pour la diffusion et l’enregistrement avec les algorithmes PCM et ADPCM.</span><span class="sxs-lookup"><span data-stu-id="4ed52-152">This value sets the sample rate for playing and recording with the PCM and ADPCM algorithms.</span></span> <span data-ttu-id="4ed52-153">Le fichier est enregistré dans ce format.</span><span class="sxs-lookup"><span data-stu-id="4ed52-153">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>\_source MCI DGV \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI\_DGV\_SETAUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-155">Une constante qui spécifie la source d’entrée audio est incluse dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-155">A constant specifying the source of audio input is included in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="4ed52-156">Les constantes suivantes sont définies pour les sources d’entrée audio :</span><span class="sxs-lookup"><span data-stu-id="4ed52-156">The following constants are defined for the audio input sources:</span></span>

<span data-ttu-id="4ed52-157">moyenne de la \_ source MCI DGV \_ SETAUDIO \_ \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-157">MCI\_DGV\_SETAUDIO\_SOURCE\_AVERAGE</span></span>

<span data-ttu-id="4ed52-158">Moyenne des canaux audio de gauche et de droite.</span><span class="sxs-lookup"><span data-stu-id="4ed52-158">The average of the left and right audio channels.</span></span>

<span data-ttu-id="4ed52-159">\_ \_ source SETAUDIO DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-159">MCI\_DGV\_SETAUDIO\_SOURCE\_LEFT</span></span>

<span data-ttu-id="4ed52-160">Canal audio de gauche.</span><span class="sxs-lookup"><span data-stu-id="4ed52-160">Left audio channel.</span></span>

<span data-ttu-id="4ed52-161">\_DGV \_ SETAUDIO \_ source \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-161">MCI\_DGV\_SETAUDIO\_SOURCE\_RIGHT</span></span>

<span data-ttu-id="4ed52-162">Canal audio approprié.</span><span class="sxs-lookup"><span data-stu-id="4ed52-162">Right audio channel.</span></span>

<span data-ttu-id="4ed52-163">\_ \_ \_ stéréo source SETAUDIO DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-163">MCI\_DGV\_SETAUDIO\_SOURCE\_STEREO</span></span>

<span data-ttu-id="4ed52-164">Enceintes.</span><span class="sxs-lookup"><span data-stu-id="4ed52-164">Stereo.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>\_flux MCI DGV \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI\_DGV\_SETAUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-166">Un flux audio est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-166">An audio-stream is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="4ed52-167">La valeur entière spécifie le flux audio lu à partir de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="4ed52-167">The integer value specifies the audio stream played back from the workspace.</span></span> <span data-ttu-id="4ed52-168">Si le flux n’est pas spécifié, le premier flux audio entrelacé physiquement est lu.</span><span class="sxs-lookup"><span data-stu-id="4ed52-168">If the stream is not specified, the first physically interleaved audio stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>\_DGV MCI \_ SETAUDIO \_ aigus</span><span class="sxs-lookup"><span data-stu-id="4ed52-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI\_DGV\_SETAUDIO\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-170">Le niveau haute fréquence audio est spécifié comme un facteur dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-170">The audio high-frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>\_ \_ volume SETAUDIO DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI\_DGV\_SETAUDIO\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-172">Le niveau audio d’un ou des deux canaux audio est spécifié en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-172">The audio level for one or both audio channels is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="4ed52-173">Si les volumes de gauche et de droite ont été définis sur des valeurs différentes, le rapport entre le volume de gauche et le volume de droite est approximativement inchangé.</span><span class="sxs-lookup"><span data-stu-id="4ed52-173">If the left and right volumes have been set to different values, then the ratio of left to right volume is approximately unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ SETAUDIO \_ gauche</span><span class="sxs-lookup"><span data-stu-id="4ed52-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-175">Active le canal audio de gauche lorsqu’il est utilisé avec MCI activé \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4ed52-175">Enables the left audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="4ed52-176">Désactive le canal audio de gauche lorsqu’il est utilisé avec \_ MCI \_ désactivé.</span><span class="sxs-lookup"><span data-stu-id="4ed52-176">Disables the left audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="4ed52-177">Lorsque cet indicateur est utilisé avec la combinaison de la \_ \_ valeur SETAUDIO MCI DGV \_ et du \_ volume MCI DGV \_ SETAUDIO \_ , il définit le volume du canal audio de gauche.</span><span class="sxs-lookup"><span data-stu-id="4ed52-177">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the left audio channel.</span></span> <span data-ttu-id="4ed52-178">Lorsque cet indicateur est utilisé avec la \_ source MCI DGV \_ SETAUDIO \_ , il spécifie le canal audio de gauche comme source pour le numériseur d’entrée audio.</span><span class="sxs-lookup"><span data-stu-id="4ed52-178">When this flag is used with MCI\_DGV\_SETAUDIO\_SOURCE, it specifies the left audio channel as the source for the audio input digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI\_DGV\_SETAUDIO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-180">Un paramètre de longueur de transition est inclus dans le membre **dwOver** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-180">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="4ed52-181">La valeur de longueur spécifie la durée (en unités du format d’heure actuel) à effectuer pour effectuer une modification qui utilise un facteur.</span><span class="sxs-lookup"><span data-stu-id="4ed52-181">The length value specifies how long (in units of the current time format) it should take to make a change that uses a factor.</span></span> <span data-ttu-id="4ed52-182">Si cet indicateur n’est pas utilisé, les modifications se produisent immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4ed52-182">If this flag is not used, changes occur immediately.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>\_DGV MCI \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI\_DGV\_SETAUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-184">Le membre **lpstrQuality** de la structure identifiée par *lpSetAudio* contient l’adresse d’une mémoire tampon définissant la qualité audio.</span><span class="sxs-lookup"><span data-stu-id="4ed52-184">The **lpstrQuality** member of the structure identified by *lpSetAudio* contains an address of a buffer defining the audio quality.</span></span> <span data-ttu-id="4ed52-185">Une chaîne de texte dans la mémoire tampon spécifie les caractéristiques de l’algorithme de compression audio.</span><span class="sxs-lookup"><span data-stu-id="4ed52-185">A text-string within the buffer specifies the characteristics of the audio compression algorithm.</span></span>

<span data-ttu-id="4ed52-186">L' \_ indicateur MCI DGV \_ SETAUDIO \_ ALG peut être utilisé pour sélectionner un descripteur de qualité pour l’algorithme spécifié.</span><span class="sxs-lookup"><span data-stu-id="4ed52-186">The MCI\_DGV\_SETAUDIO\_ALG flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="4ed52-187">Si cet indicateur est omis, l’algorithme actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4ed52-187">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="4ed52-188">Les algorithmes et les noms de descripteurs disponibles dépendent du périphérique.</span><span class="sxs-lookup"><span data-stu-id="4ed52-188">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="4ed52-189">Chaque appareil fournit de la documentation pour les algorithmes disponibles et une description des noms de descripteur applicables.</span><span class="sxs-lookup"><span data-stu-id="4ed52-189">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="4ed52-190">La commande [MCI \_ Quality](mci-quality.md) peut définir des noms de descripteurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4ed52-190">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>\_enregistrement MCI DGV \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI\_DGV\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-192">Spécifie si l’enregistrement inclut ou exclut les données audio.</span><span class="sxs-lookup"><span data-stu-id="4ed52-192">Specifies whether recording includes or excludes audio data.</span></span> <span data-ttu-id="4ed52-193">Lorsqu’elles sont combinées avec MCI activé \_ \_ , les données audio sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="4ed52-193">When combined with MCI\_SET\_ON, audio data is recorded.</span></span> <span data-ttu-id="4ed52-194">Lorsqu’elle est associée à l' \_ option MCI activée \_ , les données audio sont exclues.</span><span class="sxs-lookup"><span data-stu-id="4ed52-194">When combined with MCI\_SET\_OFF, audio data is excluded.</span></span> <span data-ttu-id="4ed52-195">La valeur par défaut comprend les données audio.</span><span class="sxs-lookup"><span data-stu-id="4ed52-195">The default includes audio data.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ Right</span><span class="sxs-lookup"><span data-stu-id="4ed52-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-197">Active le canal audio approprié lorsqu’il est utilisé avec MCI activé \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4ed52-197">Enables the right audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="4ed52-198">Désactive le canal audio approprié lorsqu’il est utilisé avec MCI \_ \_ désactivé.</span><span class="sxs-lookup"><span data-stu-id="4ed52-198">Disables the right audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="4ed52-199">Lorsque cet indicateur est utilisé avec la combinaison de la \_ \_ valeur SETAUDIO MCI DGV \_ et du \_ volume MCI DGV \_ SETAUDIO \_ , il définit le volume du canal audio approprié.</span><span class="sxs-lookup"><span data-stu-id="4ed52-199">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>\_ \_ valeur SETAUDIO de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI\_DGV\_SETAUDIO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-201">Une valeur est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="4ed52-201">A value is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="4ed52-202">La signification de la valeur est spécifiée par la constante définie pour l’indicateur de l' \_ \_ élément SETAUDIO MCI DGV \_ .</span><span class="sxs-lookup"><span data-stu-id="4ed52-202">The meaning of the value is specified by the constant defined for the MCI\_DGV\_SETAUDIO\_ITEM flag.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="4ed52-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-204">Désactive le canal audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="4ed52-204">Disables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-206">Active le canal audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="4ed52-206">Enables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="4ed52-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>\_sortie MCI SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI\_SETAUDIO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-208">Modifie l’indicateur Bass, aigus ou volume afin qu’il modifie uniquement le signal joué et non ce qui est enregistré.</span><span class="sxs-lookup"><span data-stu-id="4ed52-208">Modifies the bass, treble, or volume flag so that it modifies only the played signal and not what is recorded.</span></span> <span data-ttu-id="4ed52-209">Si possible, il s’agit de la valeur par défaut lors de l’analyse de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="4ed52-209">If possible, this is the default when monitoring the input.</span></span>

</dd> </dl>

<span data-ttu-id="4ed52-210">Pour les périphériques vidéo numériques, le paramètre *lpSetAudio* pointe vers une structure [**MCI \_ DGV \_ SETAUDIO \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="4ed52-210">For digital-video devices, the *lpSetAudio* parameter points to an [**MCI\_DGV\_SETAUDIO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) structure.</span></span>

<span data-ttu-id="4ed52-211">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="4ed52-211">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="4ed52-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>\_ \_ enregistrement SETAUDIO magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI\_VCR\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="4ed52-213">Définit l’enregistrement audio sur on ou OFF, qui est utilisé conjointement avec l’un des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="4ed52-213">Sets the audio recording to on or off, which is used in conjunction with one of following flags:</span></span>

<span data-ttu-id="4ed52-214">MCI \_ activé \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-214">MCI\_SET\_ON</span></span>

<span data-ttu-id="4ed52-215">Enregistrement audio activé.</span><span class="sxs-lookup"><span data-stu-id="4ed52-215">Audio recording on.</span></span>

<span data-ttu-id="4ed52-216">MCI \_ \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="4ed52-216">MCI\_SET\_OFF</span></span>

<span data-ttu-id="4ed52-217">Enregistrement audio désactivé.</span><span class="sxs-lookup"><span data-stu-id="4ed52-217">Audio recording off.</span></span> <span data-ttu-id="4ed52-218">Il peut être nécessaire de désactiver d’abord l’enregistrement de l’assembly (à l’aide de la commande [ \_ Set MCI](mci-set.md) avec l’indicateur de l' \_ \_ \_ enregistrement assembler de l’ensemble magnétoscope MCI \_ défini sur OFF) avant que l’enregistrement audio puisse être désactivé.</span><span class="sxs-lookup"><span data-stu-id="4ed52-218">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the MCI\_VCR\_SET\_ASSEMBLE\_RECORD flag set to off) before the audio recording can be turned off.</span></span>

<span data-ttu-id="4ed52-219">\_piste MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-219">MCI\_TRACK</span></span>

<span data-ttu-id="4ed52-220">Le membre **dwTrack** de la structure identifiée par *lpSetAudio* spécifie la piste qui est affectée par la commande.</span><span class="sxs-lookup"><span data-stu-id="4ed52-220">The **dwTrack** member of the structure identified by *lpSetAudio* specifies which track is affected by the command.</span></span>

<span data-ttu-id="4ed52-221">\_ \_ source SETAUDIO magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-221">MCI\_VCR\_SETAUDIO\_SOURCE</span></span>

<span data-ttu-id="4ed52-222">Définit la source audio.</span><span class="sxs-lookup"><span data-stu-id="4ed52-222">Sets the audio source.</span></span> <span data-ttu-id="4ed52-223">Cet indicateur doit être utilisé avec le \_ magnétoscope MCI \_ SETAUDIO \_ pour signaler.</span><span class="sxs-lookup"><span data-stu-id="4ed52-223">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="4ed52-224">\_ \_ moniteur SETAUDIO magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-224">MCI\_VCR\_SETAUDIO\_MONITOR</span></span>

<span data-ttu-id="4ed52-225">Définit le moniteur de la source audio.</span><span class="sxs-lookup"><span data-stu-id="4ed52-225">Sets the audio source monitor.</span></span> <span data-ttu-id="4ed52-226">Cet indicateur doit être utilisé avec le \_ magnétoscope MCI \_ SETAUDIO \_ pour signaler.</span><span class="sxs-lookup"><span data-stu-id="4ed52-226">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="4ed52-227">\_magnétoscope MCI \_ SETAUDIO \_ à</span><span class="sxs-lookup"><span data-stu-id="4ed52-227">MCI\_VCR\_SETAUDIO\_TO</span></span>

<span data-ttu-id="4ed52-228">Le membre **dwTo** de la structure identifiée par *lpSetAudio* contient une constante décrivant le type d’entrée ou d’entrée analysée.</span><span class="sxs-lookup"><span data-stu-id="4ed52-228">The **dwTo** member of the structure identified by *lpSetAudio* contains a constant describing the type of input or monitored input.</span></span> <span data-ttu-id="4ed52-229">Il doit s’agir de l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4ed52-229">It must be one of the following:</span></span>

<span data-ttu-id="4ed52-230"><dl> <dd></span><span class="sxs-lookup"><span data-stu-id="4ed52-230"><dl> <dd></span></span>

<span data-ttu-id="4ed52-231">\_tuner de \_ \_ type SRC magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-231">MCI\_VCR\_SRC\_TYPE\_TUNER</span></span>

<span data-ttu-id="4ed52-232">Type tuner.</span><span class="sxs-lookup"><span data-stu-id="4ed52-232">Type is tuner.</span></span>

</dd> <dd>

<span data-ttu-id="4ed52-233">\_ligne de \_ \_ type SRC magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-233">MCI\_VCR\_SRC\_TYPE\_LINE</span></span>

<span data-ttu-id="4ed52-234">Le type est Line.</span><span class="sxs-lookup"><span data-stu-id="4ed52-234">Type is line.</span></span>

</dd> <dd>

<span data-ttu-id="4ed52-235">\_magnétoscope MCI \_ type de source \_ \_ aux</span><span class="sxs-lookup"><span data-stu-id="4ed52-235">MCI\_VCR\_SRC\_TYPE\_AUX</span></span>

<span data-ttu-id="4ed52-236">Le type est auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="4ed52-236">Type is auxiliary.</span></span>

</dd> <dd>

<span data-ttu-id="4ed52-237">\_type de source de magnétoscope MCI \_ \_ \_ générique</span><span class="sxs-lookup"><span data-stu-id="4ed52-237">MCI\_VCR\_SRC\_TYPE\_GENERIC</span></span>

<span data-ttu-id="4ed52-238">Le type est Generic.</span><span class="sxs-lookup"><span data-stu-id="4ed52-238">Type is generic.</span></span>

</dd> <dd>

<span data-ttu-id="4ed52-239">\_type de source de magnétoscope MCI \_ \_ \_ muet</span><span class="sxs-lookup"><span data-stu-id="4ed52-239">MCI\_VCR\_SRC\_TYPE\_MUTE</span></span>

<span data-ttu-id="4ed52-240">Le type est muet.</span><span class="sxs-lookup"><span data-stu-id="4ed52-240">Type is mute.</span></span> <span data-ttu-id="4ed52-241">Cela ne peut être utilisé qu’avec l' \_ indicateur de source MCI VCR \_ SETAUDIO \_ .</span><span class="sxs-lookup"><span data-stu-id="4ed52-241">This can be used only with the MCI\_VCR\_SETAUDIO\_SOURCE flag.</span></span>

</dd> <dd>

<span data-ttu-id="4ed52-242">\_sortie de \_ \_ type SRC magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ed52-242">MCI\_VCR\_SRC\_TYPE\_OUTPUT</span></span>

<span data-ttu-id="4ed52-243">Le type est output.</span><span class="sxs-lookup"><span data-stu-id="4ed52-243">Type is output.</span></span>

</dd> <dd>

<span data-ttu-id="4ed52-244">\_ \_ numéro SETAUDIO magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-244">MCI\_VCR\_SETAUDIO\_NUMBER</span></span>

<span data-ttu-id="4ed52-245">Le membre dwNumber de la structure identifiée par lpSetAudio contient l’entrée audio (du type spécifié dans le membre dwTo) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4ed52-245">The dwNumber member of the structure identified by lpSetAudio contains the audio input (of the type specified in the dwTo member) to use.</span></span>

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="4ed52-246">Pour les périphériques VCR, le paramètre *lpSetAudio* pointe vers une structure [**MCI \_ VCR \_ SETAUDIO \_ PARMS**](mci-vcr-setaudio-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="4ed52-246">For VCR devices, the *lpSetAudio* parameter points to an [**MCI\_VCR\_SETAUDIO\_PARMS**](mci-vcr-setaudio-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed52-247">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ed52-247">Requirements</span></span>



| <span data-ttu-id="4ed52-248">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ed52-248">Requirement</span></span> | <span data-ttu-id="4ed52-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ed52-249">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed52-250">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ed52-250">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed52-251">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ed52-251">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4ed52-252">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ed52-252">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed52-253">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ed52-253">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4ed52-254">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ed52-254">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ed52-255"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ed52-255"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ed52-256">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ed52-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed52-257">MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-257">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4ed52-258">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="4ed52-258">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

