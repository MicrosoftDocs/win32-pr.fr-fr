---
title: Commande MCI_SET (mmsystem. h)
description: La \_ commande Set MCI définit les informations de l’appareil. Les périphériques CD audio, numérique-vidéo, MIDI Sequencer, VCR, videodisc, vidéo-overlay et Waveform-Audio reconnaissent cette commande.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- Commande MCI_SET Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/12/2021
ms.locfileid: "106535724"
---
# <a name="mci_set-command"></a><span data-ttu-id="9ca5a-105">\_Commande Set MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-105">MCI\_SET command</span></span>

> [!NOTE]
> <span data-ttu-id="9ca5a-106">Communication sans biais Microsoft prend en charge un environnement diversifié et un environnement d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="9ca5a-107">Dans ce document, il existe des références au mot « esclave ».</span><span class="sxs-lookup"><span data-stu-id="9ca5a-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="9ca5a-108">Le [Guide de style de Microsoft pour les Communications Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconnaît cela comme un mot d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="9ca5a-109">Ce libellé est utilisé, car il s’agit actuellement de la formulation utilisée dans les commandes.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="9ca5a-110">Pour des fins de cohérence, ce document contient ce mot.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="9ca5a-111">Lorsque ce mot est modifié dans les commandes, nous allons corriger ce document pour qu’il soit aligné.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="9ca5a-112">La \_ commande Set MCI définit les informations de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-112">The MCI\_SET command sets device information.</span></span> <span data-ttu-id="9ca5a-113">Les périphériques CD audio, numérique-vidéo, MIDI Sequencer, VCR, videodisc, vidéo-overlay et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="9ca5a-114">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-114">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
);
```



## <a name="parameters"></a><span data-ttu-id="9ca5a-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ca5a-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ca5a-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="9ca5a-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-117">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-117">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="9ca5a-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-119">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-119">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="9ca5a-120">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9ca5a-120">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span><span class="sxs-lookup"><span data-stu-id="9ca5a-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-122">Pointeur vers une [**structure \_ Set \_ PARMS de MCI**](mci-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-122">Pointer to an [**MCI\_SET\_PARMS**](mci-set-parms.md) structure.</span></span> <span data-ttu-id="9ca5a-123">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="9ca5a-123">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ca5a-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ca5a-124">Return Value</span></span>

<span data-ttu-id="9ca5a-125">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca5a-126">Notes</span><span class="sxs-lookup"><span data-stu-id="9ca5a-126">Remarks</span></span>

<span data-ttu-id="9ca5a-127">Les indicateurs supplémentaires suivants s’appliquent à tous les appareils prenant en charge l' \_ ensemble MCI :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-127">The following additional flags apply to all devices supporting MCI\_SET:</span></span>

<dl> <dt>

<span data-ttu-id="9ca5a-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ définir le \_ son</span><span class="sxs-lookup"><span data-stu-id="9ca5a-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI\_SET\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-129">Un numéro de canal audio est inclus dans le membre dwAudio de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-129">An audio channel number is included in the dwAudio member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="9ca5a-130">Cet indicateur doit être utilisé avec l’option MCI activée \_ \_ ou \_ activée \_ .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-130">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="9ca5a-131">Utilisez l’une des constantes suivantes pour indiquer le numéro de canal :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-131">Use one of the following constants to indicate the channel number:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI- \_ définir l' \_ audio \_ tout</span><span class="sxs-lookup"><span data-stu-id="9ca5a-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI\_SET\_AUDIO\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-133">Tous les canaux audio.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-133">All audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI- \_ définir l' \_ audio à \_ gauche</span><span class="sxs-lookup"><span data-stu-id="9ca5a-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI\_SET\_AUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-135">Canal gauche.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-135">Left channel.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ - \_ définir \_ le son</span><span class="sxs-lookup"><span data-stu-id="9ca5a-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI\_SET\_AUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-137">Canal droit.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-137">Right channel.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>porte de l' \_ ensemble MCI \_ \_ fermée</span><span class="sxs-lookup"><span data-stu-id="9ca5a-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI\_SET\_DOOR\_CLOSED</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-139">Ferme le support multimédia (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="9ca5a-139">Closes the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>porte de l' \_ ensemble MCI \_ \_ ouverte</span><span class="sxs-lookup"><span data-stu-id="9ca5a-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI\_SET\_DOOR\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-141">Ouvre la couverture du support (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="9ca5a-141">Opens the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="9ca5a-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-143">Désactive le canal vidéo ou audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-143">Disables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-145">Active le canal vidéo ou audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-145">Enables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>FORMAT d’heure de l' \_ ensemble MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI\_SET\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-147">Un paramètre de format d’heure est inclus dans le membre **dwTimeFormat** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-147">A time format parameter is included in the **dwTimeFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="9ca5a-148">Les indicateurs suivants sont utilisés avec cet indicateur :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-148">The following flags are used with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>\_octets au format MCI \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI\_FORMAT\_BYTES</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-150">Dans un format de données PCM (Pulse Code Modulation), modifie la description du membre de temps en octets pour l’entrée ou la sortie.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-150">Within a PCM (Pulse Code Modulation) data format, changes the time member description to bytes for input or output.</span></span> <span data-ttu-id="9ca5a-151">Reconnu par le type d’appareil **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-151">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>\_images au format MCI \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI\_FORMAT\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-153">Les commandes suivantes utilisent des frames.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-153">Subsequent commands will use frames.</span></span> <span data-ttu-id="9ca5a-154">Reconnu par les types d’appareils **Digitalvideo**, **VCR** et **videodisc** .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-154">Recognized by the **digitalvideo**, **vcr**, and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>\_format MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="9ca5a-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI\_FORMAT\_HMS</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-156">Modifie le format d’heure en heures, minutes et secondes.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-156">Changes the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="9ca5a-157">Reconnu par les types de périphérique **VCR** et **videodisc** .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-157">Recognized by the **vcr** and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>FORMAT MCI en \_ \_ millisecondes</span><span class="sxs-lookup"><span data-stu-id="9ca5a-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI\_FORMAT\_MILLISECONDS</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-159">Modifie le format d’heure en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-159">Changes the time format to milliseconds.</span></span> <span data-ttu-id="9ca5a-160">Reconnu par tous les types d’appareils.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-160">Recognized by all device types.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>FORMAT MCI ( \_ \_ MSF)</span><span class="sxs-lookup"><span data-stu-id="9ca5a-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI\_FORMAT\_MSF</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-162">Change le format d’heure en minutes, secondes et frames.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-162">Changes the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="9ca5a-163">Reconnu par les types d’appareils **cdaudio** et **VCR** .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-163">Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>\_exemples de format MCI \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI\_FORMAT\_SAMPLES</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-165">Remplace le format d’heure par des exemples d’entrée ou de sortie.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-165">Changes the time format to samples for input or output.</span></span> <span data-ttu-id="9ca5a-166">Reconnu par le type d’appareil **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-166">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>\_Format MCI \_ SMPTE \_ 24, \_ format MCI \_ SMPTE \_ 25 et format MCI \_ , \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="9ca5a-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI\_FORMAT\_SMPTE\_24, MCI\_FORMAT\_SMPTE\_25, and MCI\_FORMAT\_SMPTE\_30</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-168">Définit le format d’heure sur 24, 25 et 30 images SMPTE (société de mouvement et ingénieurs de télévision), respectivement.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-168">Sets the time format to 24, 25, and 30 frame SMPTE (Society of Motion Picture and Television Engineers), respectively.</span></span> <span data-ttu-id="9ca5a-169">Reconnus par les types de périphérique **Sequencer** et **VCR** .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-169">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>\_Format MCI \_ \_ 30DROP SMPTE</span><span class="sxs-lookup"><span data-stu-id="9ca5a-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI\_FORMAT\_SMPTE\_30DROP</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-171">Définit le format d’heure sur 30 SMPTE de dépôt.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-171">Sets the time format to 30 drop-frame SMPTE.</span></span> <span data-ttu-id="9ca5a-172">Reconnus par les types de périphérique **Sequencer** et **VCR** .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-172">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>\_format MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="9ca5a-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI\_FORMAT\_TMSF</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-174">Modifie le format d’heure en pistes, minutes, secondes et frames.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-174">Changes the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="9ca5a-175">(MCI utilise des numéros de pistes continus.) Reconnu par les types d’appareils **cdaudio** et **VCR** .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-175">(MCI uses continuous track numbers.) Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>\_vidéo Set \_ MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI\_SET\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-177">Définit le signal vidéo activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-177">Sets the video signal on or off.</span></span> <span data-ttu-id="9ca5a-178">Cet indicateur doit être utilisé avec l’option MCI activée ou l’option \_ \_ MCI \_ \_ désactivée.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-178">This flag must be used with either MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="9ca5a-179">Les appareils qui n’ont pas de vidéo retournent une fonction MCIERR non \_ prise en charge \_ .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-179">Devices that do not have video return MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="9ca5a-180">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="9ca5a-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ Set \_ FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="9ca5a-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI\_DGV\_SET\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-182">Un paramètre de format de fichier est inclus dans le membre **dwFileFormat** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-182">A file format parameter is included in the **dwFileFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="9ca5a-183">Pour les périphériques vidéo numériques, le format de fichier est utilisé pour les commandes d’enregistrement ou de capture.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-183">For digital-video devices, the file format is used for save or capture commands.</span></span> <span data-ttu-id="9ca5a-184">En cas d’omission, il peut s’agit d’un format défini par défaut pour le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-184">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="9ca5a-185">Si le format de fichier spécifié est en conflit avec l’algorithme et la qualité actuellement sélectionnés, ils sont remplacés par les valeurs par défaut pour le format de fichier.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-185">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="9ca5a-186">Les constantes de format de fichier suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-186">The following file format constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI\_DGV\_FF\_AVI</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-188">Format AVI.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-188">AVI format.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ avss</span><span class="sxs-lookup"><span data-stu-id="9ca5a-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI\_DGV\_FF\_AVSS</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-190">Format AVSS.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-190">AVSS format.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ DGV \_ FF \_ DIB</span><span class="sxs-lookup"><span data-stu-id="9ca5a-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI\_DGV\_FF\_DIB</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-192">Format DIB.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-192">DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF</span><span class="sxs-lookup"><span data-stu-id="9ca5a-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI\_DGV\_FF\_JFIF</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-194">Format JFIF.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-194">JFIF format.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG</span><span class="sxs-lookup"><span data-stu-id="9ca5a-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI\_DGV\_FF\_JPEG</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-196">Format JPEG.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-196">JPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG</span><span class="sxs-lookup"><span data-stu-id="9ca5a-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI\_DGV\_FF\_MPEG</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-198">Format MPEG.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-198">MPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB</span><span class="sxs-lookup"><span data-stu-id="9ca5a-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI\_DGV\_FF\_RDIB</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-200">Format DIB RLE.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-200">RLE DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG</span><span class="sxs-lookup"><span data-stu-id="9ca5a-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI\_DGV\_FF\_RJPEG</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-202">Format RJPEG.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-202">RJPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>configuration de la recherche MCI \_ DGV \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI\_DGV\_SET\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-204">Définit le format utilisé pour le positionnement.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-204">Sets the format used for positioning.</span></span> <span data-ttu-id="9ca5a-205">Cet indicateur doit être utilisé avec l’option MCI activée \_ \_ ou \_ activée \_ .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-205">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="9ca5a-206">Si \_ l’option MCI activée \_ est spécifiée, la fonction de jeu ou d’enregistrement accède précisément à la trame spécifiée avec l' \_ indicateur MCI.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-206">If MCI\_SET\_ON is specified, playing or recording precisely accesses the frame specified with the MCI\_FROM flag.</span></span> <span data-ttu-id="9ca5a-207">Cela peut ajouter un délai supplémentaire si la trame demandée n’est pas une image clé.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-207">This might add some extra delay if the requested frame is not a key frame.</span></span> <span data-ttu-id="9ca5a-208">Si \_ la valeur \_ OFF est spécifiée pour MCI, l’appareil recherche une image d’image clé qui précède le frame demandé.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-208">If MCI\_SET\_OFF is specified, the device will seek to a key-frame image that precedes the requested frame.</span></span> <span data-ttu-id="9ca5a-209">Pour certains fichiers et périphériques, il peut s’agir de la première image du fichier.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-209">For some files and devices, this might be the first frame of the file.</span></span> <span data-ttu-id="9ca5a-210">La valeur par défaut de cet indicateur dépend de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-210">The default for this flag is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>\_vitesse de \_ définition de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI\_DGV\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-212">Un paramètre de vitesse est inclus dans le membre **dwSpeed** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-212">A speed parameter is included in the **dwSpeed** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="9ca5a-213">La vitesse est spécifiée comme un ratio entre la fréquence d’images nominale et la fréquence d’images souhaitée où la fréquence d’images nominale est désignée comme 1000.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-213">Speed is specified as a ratio between the nominal frame rate and the desired frame rate where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="9ca5a-214">Une demi-vitesse est de 500 et la double vitesse est de 2000.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-214">Half speed is 500 and double speed is 2000.</span></span> <span data-ttu-id="9ca5a-215">La plage de vitesse autorisée dépend également du périphérique et éventuellement du fichier.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-215">The allowable speed range is dependent on the device and possibly the file, too.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_jeu de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI\_DGV\_SET\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-217">Lorsqu’il est utilisé avec MCI \_ DGV \_ Set \_ FILEFORMAT, MCI \_ Set définit le format de fichier utilisé pour les commandes de capture.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-217">When used with MCI\_DGV\_SET\_FILEFORMAT, MCI\_SET sets the file format used for capture commands.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="9ca5a-218">Pour les périphériques vidéo numériques, le paramètre *lpSet* pointe vers une structure [**MCI \_ DGV \_ Set \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-218">For digital-video devices, the *lpSet* parameter points to an [**MCI\_DGV\_SET\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) structure.</span></span>

<span data-ttu-id="9ca5a-219">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Sequencer** :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-219">The following additional flags are used with the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="9ca5a-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI \_ Seq \_ format \_ SONGPTR</span><span class="sxs-lookup"><span data-stu-id="9ca5a-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI\_SEQ\_FORMAT\_SONGPTR</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-221">Définit le format d’heure sur les unités du pointeur de la chanson.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-221">Sets the time format to song pointer units.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>\_contrôleur d’ensemble de séquences MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI\_SEQ\_SET\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-223">Définit Sequencer comme source de données de synchronisation et indique que le type de synchronisation est spécifié dans le membre **dwMaster** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-223">Sets the sequencer as a source of synchronization data and indicates that the type of synchronization is specified in the **dwMaster** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="9ca5a-224">MCISEQ retourne une \_ fonction non prise en charge MCIERR \_ .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-224">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="9ca5a-225">Les constantes suivantes sont définies pour le type de synchronisation :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-225">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ midi</span><span class="sxs-lookup"><span data-stu-id="9ca5a-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-227">Sequencer enverra les données de synchronisation au format MIDI.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-227">The sequencer will send MIDI format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="9ca5a-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-229">Sequencer enverra les données de synchronisation au format SMPTE.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-229">The sequencer will send SMPTE format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ aucun</span><span class="sxs-lookup"><span data-stu-id="9ca5a-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-231">Sequencer n’enverra pas de données de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-231">The sequencer will not send synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>décalage de l' \_ ensemble de séquences MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI\_SEQ\_SET\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-233">Remplace le décalage SMPTE d’une séquence par celui spécifié par le membre **dwOffset** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-233">Changes the SMPTE offset of a sequence to that specified by the **dwOffset** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="9ca5a-234">Cela affecte uniquement les séquences avec un type de division SMPTE.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-234">This affects only sequences with a SMPTE division type.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>\_port MCI Seq \_ Set \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI\_SEQ\_SET\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-236">Définit le port MIDI de sortie d’une séquence sur celui spécifié par l’identificateur d’appareil MIDI dans le membre **dwPort** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-236">Sets the output MIDI port of a sequence to that specified by the MIDI device identifier in the **dwPort** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="9ca5a-237">L’appareil ferme le port précédent (le cas échéant) et tente d’ouvrir et d’utiliser le nouveau port.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-237">The device closes the previous port (if any), and attempts to open and use the new port.</span></span> <span data-ttu-id="9ca5a-238">Si elle échoue, elle retourne une erreur et ouvre à nouveau le port précédemment utilisé (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="9ca5a-238">If it fails, it returns an error and reopens the previously used port (if any).</span></span> <span data-ttu-id="9ca5a-239">Les constantes suivantes sont définies pour les ports :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-239">The following constants are defined for the ports:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ aucun</span><span class="sxs-lookup"><span data-stu-id="9ca5a-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-241">Ferme le port précédemment utilisé (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="9ca5a-241">Closes the previously used port (if any).</span></span> <span data-ttu-id="9ca5a-242">Sequencer se comporte exactement comme si un port était ouvert, à l’exception du fait qu’aucun message MIDI n’est envoyé.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-242">The sequencer behaves exactly the same as if a port were open, except no MIDI message is sent.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>\_Mappeur midi</span><span class="sxs-lookup"><span data-stu-id="9ca5a-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI\_MAPPER</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-244">Définit le port ouvert sur le Mappeur MIDI.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-244">Sets the port opened to the MIDI mapper.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ Seq \_ Set \_ esclave</span><span class="sxs-lookup"><span data-stu-id="9ca5a-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI\_SEQ\_SET\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-246">Définit Sequencer pour recevoir des données de synchronisation et indique que le type de synchronisation est spécifié dans le membre **dwSlave** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-246">Sets the sequencer to receive synchronization data and indicates that the type of synchronization is specified in the **dwSlave** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="9ca5a-247">MCISEQ retourne une \_ fonction non prise en charge MCIERR \_ .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-247">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="9ca5a-248">Les constantes suivantes sont définies pour le type de synchronisation :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-248">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>\_fichier séquence \_ MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI\_SEQ\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-250">Définit le séquenceur pour qu’il reçoive les données de synchronisation contenues dans le fichier MIDI.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-250">Sets the sequencer to receive synchronization data contained in the MIDI file.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ midi</span><span class="sxs-lookup"><span data-stu-id="9ca5a-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-252">Définit le séquenceur pour qu’il reçoive les données de synchronisation MIDI.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-252">Sets the sequencer to receive MIDI synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ aucun</span><span class="sxs-lookup"><span data-stu-id="9ca5a-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-254">Définit le Sequencer pour qu’il ignore les données de synchronisation dans un flux MIDI.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-254">Sets the sequencer to ignore synchronization data in a MIDI stream.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="9ca5a-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-256">Définit le séquenceur pour qu’il reçoive les données de synchronisation SMPTE.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-256">Sets the sequencer to receive SMPTE synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>\_tempo d’ensemble de séquences MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI\_SEQ\_SET\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-258">Remplace le tempo de la séquence MIDI par celui spécifié par le membre **dwTempo** de la structure vers laquelle pointe *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-258">Changes the tempo of the MIDI sequence to that specified by the **dwTempo** member of the structure pointed to by *lpSet*.</span></span> <span data-ttu-id="9ca5a-259">Pour les séquences avec le type de division PPQN, le tempo est spécifié en temps par minute. pour les séquences avec le type de division SMPTE, le tempo est spécifié en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-259">For sequences with division type PPQN, tempo is specified in beats per minute; for sequences with division type SMPTE, tempo is specified in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="9ca5a-260">Pour les appareils Sequencer, le paramètre *lpSet* pointe vers une structure [**MCI \_ Seq \_ Set \_ PARMS**](mci-seq-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-260">For sequencer devices, the *lpSet* parameter points to an [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure.</span></span>

<span data-ttu-id="9ca5a-261">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-261">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="9ca5a-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>\_jeu d' \_ \_ enregistrements d’assemblage de magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI\_VCR\_SET\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-263">Définit l’appareil à enregistrer dans les modes assembleur ou insertion (lorsque l’option assembler est désactivée, l’insertion est activée et vice versa).</span><span class="sxs-lookup"><span data-stu-id="9ca5a-263">Sets the device to record in assemble or insert modes (when assemble is off, insert is on, and vice-versa).</span></span> <span data-ttu-id="9ca5a-264">Utilisez avec l’un des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-264">Use with one of the following flag:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-266">Définit l’enregistrement d’assemblage sur et désactive l’enregistrement d’insertion.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-266">Sets assemble record on, and turns insert record off.</span></span> <span data-ttu-id="9ca5a-267">Enregistre toutes les pistes vidéo, audio et de code temporel.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-267">Records all video, audio and timecode tracks.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="9ca5a-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-269">Définit l’enregistrement d’assemblage OFF et active l’enregistrement d’insertion sur.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-269">Sets assemble record off, and turns insert record on.</span></span> <span data-ttu-id="9ca5a-270">Lorsque l’option assembler l’enregistrement est désactivée, les pistes individuelles de la vidéo, de l’audio et du code temporel peuvent être sélectionnées pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-270">When assemble record is off, individual tracks of video, audio, and timecode can be selected for recording.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>\_horloge du jeu de magnétoscopes MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI\_VCR\_SET\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-272">Le membre **dwClock** de la structure identifiée par *lpSet* contient la nouvelle heure de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-272">The **dwClock** member of the structure identified by *lpSet* contains the new clock time.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>\_format du \_ compteur de jeu de magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI\_VCR\_SET\_COUNTER\_FORMA</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-274">Le membre **dwCounterFormat** de la structure identifiée par *lpSet* contient une constante qui spécifie le nouveau format de compteur à utiliser par le compteur d’État.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-274">The **dwCounterFormat** member of the structure identified by *lpSet* contains a constant specifying the new counter-time format to be used by the status counter.</span></span> <span data-ttu-id="9ca5a-275">Pour obtenir la liste des constantes valides, \_ consultez \_ format d’heure Set MCI \_ dans la liste des indicateurs supplémentaires pour cette commande.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-275">For a list of valid constants, see MCI\_SET\_TIME\_FORMAT in the list of additional flags for this command.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>valeur du compteur de l' \_ ensemble de magnétoscopes MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI\_VCR\_SET\_COUNTER\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-277">Le membre **dwCounterValue** de la structure identifiée par *lpSet* contient la nouvelle valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-277">The **dwCounterValue** member of the structure identified by *lpSet* contains the new counter value.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>\_jeu d' \_ \_ index magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI\_VCR\_SET\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-279">Le membre **dwIndex** de la structure identifiée par *lpSet* contient une constante indiquant le contenu de l’affichage à l’écran et doit être l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-279">The **dwIndex** member of the structure identified by *lpSet* contains a constant indicating the contents of the on-screen display and must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>\_compteur d' \_ index \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI\_VCR\_INDEX\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-281">Affiche le compteur.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-281">Displays counter.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>\_Date d' \_ index \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI\_VCR\_INDEX\_DATE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-283">Affiche la date.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-283">Displays date.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>\_heure d' \_ index \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI\_VCR\_INDEX\_TIME</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-285">Affiche l’heure.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-285">Displays time.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>\_code temporel de l’index magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI\_VCR\_INDEX\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-287">Affiche le code temporel.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-287">Displays timecode.</span></span>

<span data-ttu-id="9ca5a-288">Pour plus d’informations, consultez la commande d' [ \_ index MCI](mci-index.md) .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-288">For more information, see the [MCI\_INDEX](mci-index.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>\_délai de \_ \_ pause \_ du jeu de magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI\_VCR\_SET\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-290">Le membre **dwPauseTimeout** de la structure identifiée par *lpSet* contient la durée maximale, en millisecondes, d’une commande pause.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-290">The **dwPauseTimeout** member of the structure identified by *lpSet* contains the maximum duration, in milliseconds, of a pause command.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>durée de l' \_ ensemble des magnétoscopes MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI\_VCR\_SET\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-292">Le membre **dwPostrollDuration** de la structure identifiée par *lpSet* contient la longueur des cassettes vidéo, au format de l’heure actuelle, nécessaire pour freiner le transport du magnétoscope lors de l’émission d’une commande Stop ou pause.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-292">The **dwPostrollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to brake the VCR transport when a stop or pause command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>\_alimentation du jeu de magnétoscopes MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI\_VCR\_SET\_POWER</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-294">Définit la mise sous tension ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-294">Sets the power on or off.</span></span> <span data-ttu-id="9ca5a-295">Doit être utilisé avec l’un des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-295">Must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="9ca5a-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-297">Désactive l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-297">Turns power off.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-299">Active la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-299">Turns power on.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>\_durée du \_ préroll du jeu de magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>MCI\_VCR\_SET\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-301">Le membre **dwPrerollDuration** de la structure identifiée par *lpSet* contient la longueur des cassettes vidéo, au format de l’heure actuelle, nécessaire pour stabiliser la sortie du magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-301">The **dwPrerollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>\_format d' \_ enregistrement du jeu de magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI\_VCR\_SET\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-303">Le membre **dwRecordFormat** de la structure identifiée par *lpSet* contient une constante décrivant la vitesse des enregistrements, qui doit être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-303">The **dwRecordFormat** member of the structure identified by *lpSet* contains a constant describing the record speed, which must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>\_format VCR \_ MCI \_ EP</span><span class="sxs-lookup"><span data-stu-id="9ca5a-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI\_VCR\_FORMAT\_EP</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-305">Enregistrements à vitesse lente.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-305">Records at slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>\_format de magnétoscope MCI \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="9ca5a-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI\_VCR\_FORMAT\_LP</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-307">Enregistrements à vitesse moyenne lente.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-307">Records at medium-slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI \_ magnétoscope \_ au format \_ SP</span><span class="sxs-lookup"><span data-stu-id="9ca5a-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI\_VCR\_FORMAT\_SP</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-309">Enregistrements à la vitesse standard.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-309">Records at standard speed.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>\_ \_ vitesse définie pour magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI\_VCR\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-311">Le membre **dwSpeed** de la structure identifiée par *lpSet* contient le nouveau paramètre de vitesse, où 1000 correspond à la vitesse normale, 2000 à la vitesse et 500 à mi-vitesse, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-311">The **dwSpeed** member of the structure identified by *lpSet* contains the new speed setting, where 1000 is normal speed, 2000 is double speed, and 500 is half speed, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>\_longueur de \_ bande du jeu de MAGNÉTOSCOPEs MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI\_VCR\_SET\_TAPE\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-313">Le membre **dwTapeLength** de la structure identifiée par *lpSet* contient la nouvelle longueur de la bande, à condition que la longueur de la bande ne soit pas détectable.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-313">The **dwTapeLength** member of the structure identified by *lpSet* contains the new length of the tape, provided that the length of the tape is undetectable.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>magnétoscope MCI- \_ \_ définir le \_ \_ mode temporel</span><span class="sxs-lookup"><span data-stu-id="9ca5a-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI\_VCR\_SET\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-315">Le membre **dwTimeMode** de la structure identifiée par *lpSet* contient une constante indiquant le nouveau mode de temps de position.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-315">The **dwTimeMode** member of the structure identified by *lpSet* contains a constant indicating the new positional time mode.</span></span> <span data-ttu-id="9ca5a-316">Les constantes suivantes sont valides :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-316">The following constants are valid:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_compteur de \_ temps MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-318">Force l’appareil à utiliser le compteur exclusivement.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-318">Forces the device to use counter exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>détection de l' \_ heure du magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI\_VCR\_TIME\_DETECT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-320">Chaque fois qu’une nouvelle bande vidéo est insérée dans l’appareil ou que le mode passe de non prêt à prêt, l’appareil doit tenter de déterminer si un code temporel est disponible sur la bande vidéo.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-320">Each time a new videotape is inserted into the device, or the mode changes from not ready to ready, the device should attempt to determine if there is timecode available on the videotape.</span></span> <span data-ttu-id="9ca5a-321">Si le code temporel est disponible, utilisez le code temporel dans toutes les commandes suivantes qui spécifient des positions.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-321">If timecode is available, use timecode in all subsequent commands that specify positions.</span></span> <span data-ttu-id="9ca5a-322">Dans le cas contraire, utilisez le compteur.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-322">Otherwise, use the counter.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_code temporel de l’heure MCI magnétoscope \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-324">Force l’appareil à utiliser le code temporel exclusivement.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-324">Forces the device to use timecode exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>\_suivi du jeu de magnétoscopes MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI\_VCR\_SET\_TRACKING</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-326">Ajuste la vitesse du transport de bande VCR avec un ajustement précis et doit être utilisé avec l’un des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-326">Tunes the speed of the VCR tape transport with a fine adjustment, and must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>\_magnétoscope MCI \_ plus</span><span class="sxs-lookup"><span data-stu-id="9ca5a-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI\_VCR\_PLUS</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-328">Augmente la vitesse de transport de bande.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-328">Increases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>\_magnétoscope MCI \_ moins</span><span class="sxs-lookup"><span data-stu-id="9ca5a-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI\_VCR\_MINUS</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-330">Diminue la vitesse du transport sur bande.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-330">Decreases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>\_réinitialisation de magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI\_VCR\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-332">Retourne l’ajustement de suivi à zéro.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-332">Returns the tracking adjustment to zero.</span></span>

</dd> </dl>

<span data-ttu-id="9ca5a-333">Pour les périphériques VCR, le paramètre *lpSet* pointe vers une structure d' [**\_ \_ ensemble \_ de magnétoscopes MCI**](mci-vcr-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-333">For VCR devices, the *lpSet* parameter points to an [**MCI\_VCR\_SET\_PARMS**](mci-vcr-set-parms.md) structure.</span></span>

<span data-ttu-id="9ca5a-334">L’indicateur supplémentaire suivant est utilisé avec le type d’appareil **videodisc** :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-334">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="9ca5a-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>\_piste de \_ format MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI\_VD\_FORMAT\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-336">Modifie le format d’heure en pistes.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-336">Changes the time format to tracks.</span></span> <span data-ttu-id="9ca5a-337">MCI utilise des numéros de pistes continus.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-337">MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="9ca5a-338">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-338">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="9ca5a-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrée MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-340">Définit l’entrée utilisée pour l’enregistrement dans le membre **wInput** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-340">Sets the input used for recording to the **wInput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_sortie MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="9ca5a-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-342">Définit la sortie utilisée pour la diffusion dans le membre **wOutput** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-342">Sets the output used for playing to the **wOutput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>\_jeu Wave \_ MCI \_ ANYINPUT</span><span class="sxs-lookup"><span data-stu-id="9ca5a-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI\_WAVE\_SET\_ANYINPUT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-344">Toutes les entrées Wave compatibles avec le format actuel peuvent être utilisées pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-344">Any wave input compatible with the current format can be used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>\_jeu Wave \_ MCI \_ ANYOUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ca5a-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI\_WAVE\_SET\_ANYOUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-346">Toutes les sorties Wave compatibles avec le format actuel peuvent être utilisées pour la diffusion.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-346">Any wave output compatible with the current format can be used for playing.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>\_jeu Wave \_ MCI \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="9ca5a-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-348">Définit le nombre d’octets par seconde utilisé pour la diffusion, l’enregistrement et l’enregistrement dans le membre **nAvgBytesPerSec** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-348">Sets the bytes per second used for playing, recording, and saving to the **nAvgBytesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>\_jeu Wave \_ MCI \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="9ca5a-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-350">Définit le nombre de bits par échantillon utilisé pour la diffusion, l’enregistrement et l’enregistrement dans le membre **nBitsPerSample** du format de données PCM identifié par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-350">Sets the bits per sample used for playing, recording, and saving to the **nBitsPerSample** member of the PCM data format identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>\_jeu Wave \_ MCI \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="9ca5a-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-352">Définit l’alignement de bloc utilisé pour la diffusion, l’enregistrement et l’enregistrement dans le membre **nBlockAlign** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-352">Sets the block alignment used for playing, recording, and saving to the **nBlockAlign** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>\_canaux de \_ jeu \_ Wave MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI\_WAVE\_SET\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-354">Le nombre de canaux est indiqué dans le membre **nChannels** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-354">The number of channels is indicated in the **nChannels** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>\_jeu Wave \_ MCI \_ FORMATTAG</span><span class="sxs-lookup"><span data-stu-id="9ca5a-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI\_WAVE\_SET\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-356">Définit le type de format utilisé pour la diffusion, l’enregistrement et l’enregistrement dans le membre **wFormatTag** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-356">Sets the format type used for playing, recording, and saving to the **wFormatTag** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="9ca5a-357">La spécification \_ du format Wave \_ PCM change le format en PCM.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-357">Specifying WAVE\_FORMAT\_PCM changes the format to PCM.</span></span>

</dd> <dt>

<span data-ttu-id="9ca5a-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>\_jeu Wave \_ MCI \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="9ca5a-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="9ca5a-359">Définit les échantillons par seconde utilisés pour la diffusion, l’enregistrement et l’enregistrement dans le membre **nSamplesPerSec** de la structure identifiée par *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-359">Sets the samples per second used for playing, recording, and saving to the **nSamplesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> </dl>

<span data-ttu-id="9ca5a-360">Pour les périphériques audio Waveform, le paramètre *lpSet* pointe vers une structure de paramètres [**\_ Wave \_ \_ MCI**](mci-wave-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="9ca5a-360">For waveform-audio devices, the *lpSet* parameter points to an [**MCI\_WAVE\_SET\_PARMS**](mci-wave-set-parms.md) structure.</span></span>

<span data-ttu-id="9ca5a-361">Plusieurs propriétés des données Waveform-Audio sont définies lors de la création du fichier de stockage des données.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-361">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="9ca5a-362">Ces propriétés décrivent comment les données sont structurées dans le fichier et ne peuvent pas être modifiées une fois l’enregistrement commencé.</span><span class="sxs-lookup"><span data-stu-id="9ca5a-362">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="9ca5a-363">La liste d’indicateurs suivante identifie ces propriétés :</span><span class="sxs-lookup"><span data-stu-id="9ca5a-363">The following list of flags identifies these properties:</span></span>

-   <span data-ttu-id="9ca5a-364">\_jeu Wave \_ MCI \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="9ca5a-364">MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
-   <span data-ttu-id="9ca5a-365">\_jeu Wave \_ MCI \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="9ca5a-365">MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
-   <span data-ttu-id="9ca5a-366">\_jeu Wave \_ MCI \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="9ca5a-366">MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
-   <span data-ttu-id="9ca5a-367">\_canaux de \_ jeu \_ Wave MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-367">MCI\_WAVE\_SET\_CHANNELS</span></span>
-   <span data-ttu-id="9ca5a-368">\_jeu Wave \_ MCI \_ FORMATTAG</span><span class="sxs-lookup"><span data-stu-id="9ca5a-368">MCI\_WAVE\_SET\_FORMATTAG</span></span>
-   <span data-ttu-id="9ca5a-369">\_jeu Wave \_ MCI \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="9ca5a-369">MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca5a-370">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ca5a-370">Requirements</span></span>



| <span data-ttu-id="9ca5a-371">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ca5a-371">Requirement</span></span> | <span data-ttu-id="9ca5a-372">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ca5a-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca5a-373">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ca5a-373">Minimum supported client</span></span><br/> | <span data-ttu-id="9ca5a-374">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ca5a-374">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9ca5a-375">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ca5a-375">Minimum supported server</span></span><br/> | <span data-ttu-id="9ca5a-376">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ca5a-376">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9ca5a-377">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ca5a-377">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ca5a-378"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ca5a-378"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ca5a-379">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ca5a-379">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca5a-380">MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-380">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9ca5a-381">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="9ca5a-381">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

