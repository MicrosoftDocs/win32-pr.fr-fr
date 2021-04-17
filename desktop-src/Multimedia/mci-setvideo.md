---
title: Commande MCI_SETVIDEO (mmsystem. h)
description: La \_ commande MCI SETVIDEO définit les valeurs associées à la lecture vidéo. Les appareils vidéo numériques et VCR reconnaissent cette commande.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- Commande MCI_SETVIDEO Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465418"
---
# <a name="mci_setvideo-command"></a><span data-ttu-id="b7f48-105">\_Commande MCI SETVIDEO</span><span class="sxs-lookup"><span data-stu-id="b7f48-105">MCI\_SETVIDEO command</span></span>

<span data-ttu-id="b7f48-106">La \_ commande MCI SETVIDEO définit les valeurs associées à la lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="b7f48-106">The MCI\_SETVIDEO command sets values associated with video playback.</span></span> <span data-ttu-id="b7f48-107">Les appareils vidéo numériques et VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="b7f48-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="b7f48-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="b7f48-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
);
```



## <a name="parameters"></a><span data-ttu-id="b7f48-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7f48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7f48-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b7f48-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="b7f48-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b7f48-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-113">**MCI \_ NOTIFY**, **l' \_ attente MCI** ou **le \_ test MCI**.</span><span class="sxs-lookup"><span data-stu-id="b7f48-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or **MCI\_TEST**.</span></span> <span data-ttu-id="b7f48-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b7f48-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span><span class="sxs-lookup"><span data-stu-id="b7f48-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="b7f48-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="b7f48-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="b7f48-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7f48-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b7f48-118">Return Value</span></span>

<span data-ttu-id="b7f48-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="b7f48-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7f48-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b7f48-120">Remarks</span></span>

<span data-ttu-id="b7f48-121">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil « Digitalvideo » :</span><span class="sxs-lookup"><span data-stu-id="b7f48-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="b7f48-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ SETVIDEO \_ ALG</span><span class="sxs-lookup"><span data-stu-id="b7f48-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI\_DGV\_SETVIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-123">Le membre **lpstrAlgorithm** de la structure identifiée par *lpSetVideo* contient l’adresse d’une mémoire tampon contenant le nom d’un algorithme de compression vidéo.</span><span class="sxs-lookup"><span data-stu-id="b7f48-123">The **lpstrAlgorithm** member of the structure identified by *lpSetVideo* contains an address of a buffer containing the name of a video compression algorithm.</span></span> <span data-ttu-id="b7f48-124">L’algorithme de compression est utilisé par les commandes de [ \_ réserve MCI](mci-reserve.md) ou d' [ \_ enregistrement MCI](mci-record.md) suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7f48-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="b7f48-125">Les algorithmes disponibles dépendent du périphérique.</span><span class="sxs-lookup"><span data-stu-id="b7f48-125">The available algorithms are device dependent.</span></span>

<span data-ttu-id="b7f48-126">Si l’algorithme spécifié est incompatible avec le format de fichier actuel, le format de fichier est remplacé par le format par défaut de l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="b7f48-126">If the specified algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ SETVIDEO \_ CLOCKTIME</span><span class="sxs-lookup"><span data-stu-id="b7f48-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI\_DGV\_SETVIDEO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-128">Lorsqu’il est utilisé avec **MCI \_ DGV \_ SETVIDEO \_ sur**, indique que l’heure est spécifiée en millisecondes et est l’heure absolue.</span><span class="sxs-lookup"><span data-stu-id="b7f48-128">When used with **MCI\_DGV\_SETVIDEO\_OVER**, indicates time is specified in milliseconds and is absolute time.</span></span> <span data-ttu-id="b7f48-129">(Cette heure n’est pas à l’étape de la diffusion de l’espace de travail.)</span><span class="sxs-lookup"><span data-stu-id="b7f48-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>\_entrée MCI DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI\_DGV\_SETVIDEO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-131">Modifie la **\_ \_ \_ teinte** **MCI \_ DGV \_ SETVIDEO \_ Brightness**, **MCI \_ DGV \_ SETVIDEO \_ Color**, **MCI \_ DGV \_ SETVIDEO \_ Contrast**, **MCI \_ DGV \_ SETVIDEO \_ gamma**, **MCI \_ DGV \_ SETVIDEO \_ net** ou MCI DGV SETVIDEO, afin qu’elle affecte le signal d’entrée et modifie ce qui est enregistré.</span><span class="sxs-lookup"><span data-stu-id="b7f48-131">Modifies the **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="b7f48-132">Si possible, il s’agit de la valeur par défaut lors de l’analyse de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="b7f48-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>\_ \_ élément SETVIDEO DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI\_DGV\_SETVIDEO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-134">Une constante vidéo est spécifiée dans le membre **dwItem** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-134">A video constant is specified in the **dwItem** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-135">La constante identifie la valeur qui est définie.</span><span class="sxs-lookup"><span data-stu-id="b7f48-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="b7f48-136">Vous pouvez spécifier les constantes suivantes avec cet indicateur :</span><span class="sxs-lookup"><span data-stu-id="b7f48-136">You can specify the following constants with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>\_procédure de dessin MCI AVI \_ SETVIDEO \_ \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI\_AVI\_SETVIDEO\_DRAW\_PROCEDURE</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-138">Une nouvelle adresse de procédure de dessin est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-138">A new drawing procedure address is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-139">Vous pouvez spécifier une nouvelle procédure de dessin uniquement lorsque l’appareil est inactif.</span><span class="sxs-lookup"><span data-stu-id="b7f48-139">You can specify a new drawing procedure only when the device is idle.</span></span> <span data-ttu-id="b7f48-140">Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="b7f48-140">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="b7f48-141">Il n’existe aucun équivalent à cet indicateur dans l’interface de commande de chaîne.</span><span class="sxs-lookup"><span data-stu-id="b7f48-141">There is no equivalent to this flag in the string command interface.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>\_couleur de \_ la \_ palette SETVIDEO AVI \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-143">Une nouvelle couleur de palette est spécifiée dans les membres **dwOver** et **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-143">A new palette color is specified in the **dwOver** and **dwValue** members of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-144">Le membre **dwOver** spécifie l’index de palette de la couleur à modifier et le membre **dwValue** spécifie la nouvelle couleur, sous la forme d’une valeur RVB.</span><span class="sxs-lookup"><span data-stu-id="b7f48-144">The **dwOver** member specifies the palette index of the color to be changed and the **dwValue** member specifies the new color, as an RGB value.</span></span> <span data-ttu-id="b7f48-145">Vous devez également spécifier les indicateurs de **\_ \_ \_ valeur** **MCI \_ DGV \_ SETVIDEO \_ sur** et MCI DGV avec **l' \_ \_ \_ élément MCI DGV SETVIDEO** lorsque vous utilisez cette constante.</span><span class="sxs-lookup"><span data-stu-id="b7f48-145">You must also specify the **MCI\_DGV\_SETVIDEO\_OVER** and **MCI\_DGV\_SETVIDEO\_VALUE** flags with **MCI\_DGV\_SETVIDEO\_ITEM** when you use this constant.</span></span> <span data-ttu-id="b7f48-146">Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="b7f48-146">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>\_demi- \_ \_ \_ teinte de la palette SETVIDEO AVI MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_HALFTONE</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-148">Indique que la palette de demi-teintes doit être utilisée au lieu de la palette par défaut.</span><span class="sxs-lookup"><span data-stu-id="b7f48-148">Indicates that the halftone palette should be used, instead of the default palette.</span></span> <span data-ttu-id="b7f48-149">Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="b7f48-149">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ SETVIDEO \_ BITSPERPEL</span><span class="sxs-lookup"><span data-stu-id="b7f48-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI\_DGV\_SETVIDEO\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-151">Le nombre de bits par pixel est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-151">The number of bits per pixel is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-152">Le nombre de bits par pixel est utilisé pour enregistrer les données capturées ou enregistrées</span><span class="sxs-lookup"><span data-stu-id="b7f48-152">The number of bits per pixel is used for saving captured or recorded data</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>\_luminosité de \_ SETVIDEO \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI\_DGV\_SETVIDEO\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-154">Le niveau de luminosité de la vidéo est spécifié en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-154">The video brightness level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>\_couleur MCI DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI\_DGV\_SETVIDEO\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-156">Le niveau de saturation de la couleur vidéo est spécifié en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-156">The video color saturation level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>\_ \_ contraste SETVIDEO DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI\_DGV\_SETVIDEO\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-158">Le niveau de contraste vidéo est spécifié en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-158">The video contrast level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>\_fréquence d’images MCI DGV \_ SETVIDEO \_ \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI\_DGV\_SETVIDEO\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-160">Une fréquence d’images est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-160">A frame rate is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-161">Le taux est spécifié en unités d’images par seconde (1000).</span><span class="sxs-lookup"><span data-stu-id="b7f48-161">The rate is specified in units of frames per second times 1000.</span></span> <span data-ttu-id="b7f48-162">Par exemple, 29,97 images par seconde sont spécifiées sous la forme 29970.</span><span class="sxs-lookup"><span data-stu-id="b7f48-162">For example, 29.97 frames per second is specified as 29970.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>\_DGV MCI \_ SETVIDEO \_ gamma</span><span class="sxs-lookup"><span data-stu-id="b7f48-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI\_DGV\_SETVIDEO\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-164">Une valeur d’exposant de correction gamma est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-164">A gamma correction exponent value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-165">La correction gamma ajuste le mappage entre l’intensité encodée dans la source de présentation et la luminosité affichée.</span><span class="sxs-lookup"><span data-stu-id="b7f48-165">Gamma correction adjusts the mapping between the intensity encoded in the presentation source and the displayed brightness.</span></span> <span data-ttu-id="b7f48-166">La valeur est l’exposant multiplié par 1000.</span><span class="sxs-lookup"><span data-stu-id="b7f48-166">The value is the exponent multiplied by 1000.</span></span> <span data-ttu-id="b7f48-167">Par exemple, 2200 indique un exposant de 2,2.</span><span class="sxs-lookup"><span data-stu-id="b7f48-167">For example, 2200 indicates an exponent of 2.2.</span></span> <span data-ttu-id="b7f48-168">Une valeur de 1000 indique un exposant de 1, qui n’applique aucune correction gamma.</span><span class="sxs-lookup"><span data-stu-id="b7f48-168">A value of 1000 indicates an exponent of 1, which applies no gamma correction.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>\_couleur de \_ \_ clé SETVIDEO DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI\_DGV\_SETVIDEO\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-170">Une couleur de clé est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-170">A key color is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-171">La couleur de la clé est une valeur RVB.</span><span class="sxs-lookup"><span data-stu-id="b7f48-171">The key color is an RGB value.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>\_index de \_ \_ clé SETVIDEO DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI\_DGV\_SETVIDEO\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-173">Une valeur d’index de clé est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-173">A key index value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-174">Le paramètre d’index est un index de palette physique.</span><span class="sxs-lookup"><span data-stu-id="b7f48-174">The index parameter is a physical palette index.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ SETVIDEO \_ PALHANDLE</span><span class="sxs-lookup"><span data-stu-id="b7f48-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI\_DGV\_SETVIDEO\_PALHANDLE</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-176">Un descripteur de palette est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-176">A palette handle is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-177">Le descripteur de palette est contenu dans le mot de poids faible.</span><span class="sxs-lookup"><span data-stu-id="b7f48-177">The palette handle is contained in the low-order word.</span></span> <span data-ttu-id="b7f48-178">Les périphériques vidéo numériques ne doivent pas libérer la palette transmise avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="b7f48-178">Digital-video devices should not free the palette passed with this command.</span></span> <span data-ttu-id="b7f48-179">Les applications doivent le libérer après avoir fermé l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b7f48-179">Applications should free it after they close the device.</span></span> <span data-ttu-id="b7f48-180">Cet indicateur est pris en charge uniquement par les appareils qui utilisent des palettes.</span><span class="sxs-lookup"><span data-stu-id="b7f48-180">This flag is supported only by devices that use palettes.</span></span> <span data-ttu-id="b7f48-181">Si le handle de palette spécifié est égal à zéro, la palette par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="b7f48-181">If this specified palette handle is zero, then the default palette is used.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>\_ \_ netteté MCI DGV SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI\_DGV\_SETVIDEO\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-183">Une valeur de netteté vidéo est spécifiée en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-183">A video sharpness value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>\_source MCI DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI\_DGV\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-185">Une constante qui spécifie la source de l’entrée vidéo est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-185">A constant specifying the source of the video input is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-186">Les constantes suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="b7f48-186">The following constants are defined:</span></span>

-   <span data-ttu-id="b7f48-187">**MCI \_ DGV \_ SETVIDEO \_ src \_ NTSC**: télévision NTSC.</span><span class="sxs-lookup"><span data-stu-id="b7f48-187">**MCI\_DGV\_SETVIDEO\_SRC\_NTSC**: NTSC television.</span></span>
-   <span data-ttu-id="b7f48-188">MCI \_ DGV \_ SETVIDEO \_ src \_ PAL : PAL Television.</span><span class="sxs-lookup"><span data-stu-id="b7f48-188">MCI\_DGV\_SETVIDEO\_SRC\_PAL: PAL television.</span></span>
-   <span data-ttu-id="b7f48-189">MCI \_ DGV \_ SETVIDEO \_ src \_ RGB : vidéo RVB.</span><span class="sxs-lookup"><span data-stu-id="b7f48-189">MCI\_DGV\_SETVIDEO\_SRC\_RGB: RGB video.</span></span>
-   <span data-ttu-id="b7f48-190">MCI \_ DGV \_ SETVIDEO \_ src \_ SECAM : SECAM Television.</span><span class="sxs-lookup"><span data-stu-id="b7f48-190">MCI\_DGV\_SETVIDEO\_SRC\_SECAM: SECAM television.</span></span>
-   <span data-ttu-id="b7f48-191">MCI \_ DGV \_ SETVIDEO \_ src \_ SVIDEO : S-Video.</span><span class="sxs-lookup"><span data-stu-id="b7f48-191">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO: S-Video.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>\_flux MCI DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI\_DGV\_SETVIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-193">Un flux vidéo est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-193">A video stream is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-194">La valeur entière spécifie le flux vidéo lu de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="b7f48-194">The integer value specifies the video stream played back from the workspace.</span></span> <span data-ttu-id="b7f48-195">Si le flux n’est pas spécifié et que le format de fichier ne définit pas de flux par défaut, le premier flux vidéo entrelacé physiquement est lu.</span><span class="sxs-lookup"><span data-stu-id="b7f48-195">If the stream is not specified and the file format does not define a default stream, the first physically interleaved video stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>\_ \_ teinte MCI DGV SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI\_DGV\_SETVIDEO\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-197">Une valeur de teinte vidéo est spécifiée en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-197">A video tint value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-198">En règle générale, cet ajustement est modélisé après le contrôle de la teinte de nombreux jeux de télévision couleur, avec 250 défini en vert, 750 défini en rouge et 0 (ou 1000) défini en bleu.</span><span class="sxs-lookup"><span data-stu-id="b7f48-198">Typically, this adjustment is modeled after the tint control of many color television sets, with 250 defined as green, 750 defined as red, and 0 (or 1000) defined as blue.</span></span> <span data-ttu-id="b7f48-199">La valeur nominale est toujours 500.</span><span class="sxs-lookup"><span data-stu-id="b7f48-199">The nominal value is always 500.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>\_sortie MCI DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI\_DGV\_SETVIDEO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-201">La **couleur \_ MCI \_ DGV SETVIDEO \_ Brightness**, **MCI \_ DGV \_ SETVIDEO \_ Color**, **MCI \_ DGV \_ SETVIDEO \_ Contrast**, **MCI \_ DGV \_ SETVIDEO \_ gamma**, **MCI \_ DGV \_ SETVIDEO \_ net** ou **MCI \_ DGV \_ SETVIDEO \_** est modifiée de sorte qu’elle affecte uniquement le signal affiché et non ce qui est enregistré.</span><span class="sxs-lookup"><span data-stu-id="b7f48-201">The **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** flag is modified so that it affects only the displayed signal and not what is recorded.</span></span> <span data-ttu-id="b7f48-202">Si possible, il s’agit de la valeur par défaut lors de l’analyse d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="b7f48-202">If possible, this is the default when monitoring a file.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI\_DGV\_SETVIDEO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-204">Un paramètre de longueur de transition est inclus dans le membre **dwOver** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-204">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-205">La longueur de transition spécifie la durée (dans le format d’heure actuel) à appliquer pour apporter une modification.</span><span class="sxs-lookup"><span data-stu-id="b7f48-205">The transition length specifies how long (in the current time format) it should take to make a change.</span></span> <span data-ttu-id="b7f48-206">Si cet indicateur n’est pas utilisé, la modification se produit immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b7f48-206">If this flag is not used, the change occurs immediately.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>\_DGV MCI \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI\_DGV\_SETVIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-208">Le membre **lpstrQuality** de la structure identifiée par *lpSetVideo* contient l’adresse d’une mémoire tampon décrivant la qualité de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="b7f48-208">The **lpstrQuality** member of the structure identified by *lpSetVideo* contains an address of a buffer describing the video quality.</span></span> <span data-ttu-id="b7f48-209">Une chaîne de texte dans la mémoire tampon spécifie les caractéristiques de l’algorithme de compression vidéo.</span><span class="sxs-lookup"><span data-stu-id="b7f48-209">A text-string in the buffer specifies the characteristics of the video compression algorithm.</span></span>

<span data-ttu-id="b7f48-210">L’indicateur **MCI \_ DGV \_ SETVIDEO \_ ALG** peut être utilisé pour sélectionner un descripteur de qualité pour l’algorithme spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7f48-210">The **MCI\_DGV\_SETVIDEO\_ALG** flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="b7f48-211">Si cet indicateur est omis, l’algorithme actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b7f48-211">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="b7f48-212">Les algorithmes et les noms de descripteurs disponibles dépendent du périphérique.</span><span class="sxs-lookup"><span data-stu-id="b7f48-212">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="b7f48-213">Chaque appareil fournit de la documentation pour les algorithmes disponibles et une description des noms de descripteur applicables.</span><span class="sxs-lookup"><span data-stu-id="b7f48-213">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="b7f48-214">La commande [MCI \_ Quality](mci-quality.md) peut définir des noms de descripteurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b7f48-214">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span> <span data-ttu-id="b7f48-215">Tous les appareils prennent en charge les descripteurs « Low », « medium » et « High ».</span><span class="sxs-lookup"><span data-stu-id="b7f48-215">All devices support the descriptors "low", "medium", and "high".</span></span> <span data-ttu-id="b7f48-216">La valeur par défaut est spécifique au pilote.</span><span class="sxs-lookup"><span data-stu-id="b7f48-216">The default is driver specific.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>\_enregistrement MCI DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI\_DGV\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-218">Spécifie si l’enregistrement inclut ou exclut les données vidéo.</span><span class="sxs-lookup"><span data-stu-id="b7f48-218">Specifies whether recording includes or excludes video data.</span></span> <span data-ttu-id="b7f48-219">Lorsqu’elles sont combinées avec **MCI \_ \_** activé, les données vidéo sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="b7f48-219">When combined with **MCI\_SET\_ON**, video data is recorded.</span></span> <span data-ttu-id="b7f48-220">Lorsqu’elle est associée à l' **\_ \_ option MCI désactivée**, les données vidéo sont exclues.</span><span class="sxs-lookup"><span data-stu-id="b7f48-220">When combined with **MCI\_SET\_OFF**, video data is excluded.</span></span> <span data-ttu-id="b7f48-221">La valeur par défaut comprend les données vidéo.</span><span class="sxs-lookup"><span data-stu-id="b7f48-221">The default includes video data.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>\_ \_ numéro SRC du SETVIDEO DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI\_DGV\_SETVIDEO\_SRC\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-223">Un nombre pour la source vidéo est spécifié dans le membre **dwSourceNumber** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-223">A number for the video source is specified in the **dwSourceNumber** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-224">S’il existe plusieurs entrées du type spécifié par la **\_ \_ \_ valeur SETVIDEO de MCI DGV**, la valeur sélectionne l’entrée.</span><span class="sxs-lookup"><span data-stu-id="b7f48-224">If there is more than one input of the type specified by **MCI\_DGV\_SETVIDEO\_VALUE**, the value selects the input.</span></span> <span data-ttu-id="b7f48-225">Cet indicateur doit toujours être utilisé avec **la \_ \_ \_ source MCI DGV SETVIDEO**.</span><span class="sxs-lookup"><span data-stu-id="b7f48-225">This flag must always be used with **MCI\_DGV\_SETVIDEO\_SOURCE**.</span></span> <span data-ttu-id="b7f48-226">Toutefois, si la **\_ \_ \_ valeur de SETVIDEO DGV MCI** est omise, le numéro de source spécifié indique la source absolue à utiliser comme indiqué dans la commande de [ \_ liste MCI](mci-list.md) .</span><span class="sxs-lookup"><span data-stu-id="b7f48-226">If **MCI\_DGV\_SETVIDEO\_VALUE** is omitted, however, the specified source number indicates the absolute source to use as specified in the [MCI\_LIST](mci-list.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI \_ DGV \_ SETVIDEO \_ toujours</span><span class="sxs-lookup"><span data-stu-id="b7f48-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI\_DGV\_SETVIDEO\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-228">Le nom de l’algorithme ou la valeur de qualité spécifiée s’applique aux images fixes.</span><span class="sxs-lookup"><span data-stu-id="b7f48-228">The algorithm name or quality value specified applies to still images.</span></span>

<span data-ttu-id="b7f48-229">Chaque pilote de périphérique doit prendre en charge l’algorithme « None », ce qui signifie qu’aucune compression n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b7f48-229">Every device driver must support an algorithm of "none", which means no compression.</span></span> <span data-ttu-id="b7f48-230">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b7f48-230">This is the default.</span></span> <span data-ttu-id="b7f48-231">Dans ce cas, les périphériques vidéo numériques enregistrent des images fixes sous forme de bitmaps indépendantes des appareils RVB (DIB).</span><span class="sxs-lookup"><span data-stu-id="b7f48-231">In this case, digital-video devices save still images as RGB device-independent bitmaps (DIBs).</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>\_ \_ valeur SETVIDEO de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI\_DGV\_SETVIDEO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-233">Une valeur est incluse dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="b7f48-233">A value is included in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="b7f48-234">La signification de la valeur est spécifiée par l’indicateur **MCI \_ DGV \_ SETVIDEO \_ Item** .</span><span class="sxs-lookup"><span data-stu-id="b7f48-234">The meaning of the value is specified by the **MCI\_DGV\_SETVIDEO\_ITEM** flag.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="b7f48-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-236">Désactive la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="b7f48-236">Disables video output.</span></span> <span data-ttu-id="b7f48-237">Pour les périphériques vidéo numériques, la désactivation de la vidéo définit les pixels du rectangle de destination défini par la commande [ \_ put de MCI](mci-put.md) (ou la région cliente de la fenêtre active) sur une couleur unie, mais elle n’a aucun effet sur la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="b7f48-237">For digital-video devices, disabling video sets the pixels in the destination rectangle defined by the [MCI\_PUT](mci-put.md) command (or its default, the client region of the current window) to a solid color, but it has no effect on the frame buffer.</span></span> <span data-ttu-id="b7f48-238">Si vous le souhaitez, vous pouvez masquer la fenêtre avec la commande de [ \_ fenêtre MCI](mci-window.md) .</span><span class="sxs-lookup"><span data-stu-id="b7f48-238">You can hide the window with the [MCI\_WINDOW](mci-window.md) command if desired.</span></span> <span data-ttu-id="b7f48-239">La source de vidéo, qu’il s’agisse de l’espace de travail ou d’une entrée externe, peut continuer à stocker de nouvelles images dans la mémoire tampon de trame, mais elles ne sont pas affichées tant que la vidéo n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="b7f48-239">The source of video, whether it's the workspace or an external input, might continue to store new images in the frame buffer, but they are not displayed until the video is enabled.</span></span> <span data-ttu-id="b7f48-240">Alors que les applications doivent utiliser la \_ commande MCI SETVIDEO pour contrôler cette fonction, les appareils vidéo numériques doivent toujours prendre en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="b7f48-240">While applications should use the MCI\_SETVIDEO command to control this function, digital-video devices must still support this flag.</span></span> <span data-ttu-id="b7f48-241">La valeur par défaut après une ouverture est activée.</span><span class="sxs-lookup"><span data-stu-id="b7f48-241">The default value after an open is on.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_</span><span class="sxs-lookup"><span data-stu-id="b7f48-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-243">Active la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="b7f48-243">Enables video output.</span></span>

</dd> </dl>

<span data-ttu-id="b7f48-244">Pour les périphériques vidéo numériques, le paramètre *lpSetVideo* pointe vers une structure [**MCI \_ DGV \_ SETVIDEO \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="b7f48-244">For digital-video devices, the *lpSetVideo* parameter points to an [**MCI\_DGV\_SETVIDEO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) structure.</span></span>

<span data-ttu-id="b7f48-245">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil « VCR » :</span><span class="sxs-lookup"><span data-stu-id="b7f48-245">The following additional flags are used with the "vcr" device type:</span></span>

<dl> <dt>

<span data-ttu-id="b7f48-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>\_ \_ enregistrement SETVIDEO magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI\_VCR\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-247">Définit l’enregistrement vidéo sur on ou OFF.</span><span class="sxs-lookup"><span data-stu-id="b7f48-247">Sets the video recording to on or off.</span></span> <span data-ttu-id="b7f48-248">Utilisé conjointement avec l’un des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="b7f48-248">Used in conjunction with one of following flags:</span></span>

-   <span data-ttu-id="b7f48-249">**MCI \_ DÉFINI \_ sur**.</span><span class="sxs-lookup"><span data-stu-id="b7f48-249">**MCI\_SET\_ON**.</span></span> <span data-ttu-id="b7f48-250">Enregistrement vidéo activé.</span><span class="sxs-lookup"><span data-stu-id="b7f48-250">Video recording on.</span></span>
-   <span data-ttu-id="b7f48-251">**MCI \_ \_désactivée**.</span><span class="sxs-lookup"><span data-stu-id="b7f48-251">**MCI\_SET\_OFF**.</span></span> <span data-ttu-id="b7f48-252">Enregistrement vidéo désactivé.</span><span class="sxs-lookup"><span data-stu-id="b7f48-252">Video recording off.</span></span> <span data-ttu-id="b7f48-253">Il peut être nécessaire de désactiver d’abord l’enregistrement de l’assembly (à l’aide de la commande [ \_ Set MCI](mci-set.md) avec l’indicateur de l' **\_ \_ \_ \_ enregistrement assembler** de l’ensemble magnétoscope MCI défini sur OFF) avant que l’enregistrement vidéo puisse être désactivé.</span><span class="sxs-lookup"><span data-stu-id="b7f48-253">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the **MCI\_VCR\_SET\_ASSEMBLE\_RECORD** flag set to off) before the video recording can be turned off.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>\_piste MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-255">Le membre **dwTrack** de la structure identifiée par *lpSetVideo* spécifie la piste qui est affectée par la commande.</span><span class="sxs-lookup"><span data-stu-id="b7f48-255">The **dwTrack** member of the structure identified by *lpSetVideo* specifies which track is affected by the command.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>\_ \_ source SETVIDEO magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI\_VCR\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-257">Définit la source vidéo et doit être utilisé avec le **magnétoscope MCI \_ \_ SETVIDEO \_ pour** signaler.</span><span class="sxs-lookup"><span data-stu-id="b7f48-257">Sets the video source, and must be used with the **MCI\_VCR\_SETVIDEO\_TO** flag.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>\_ \_ moniteur SETVIDEO magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI\_VCR\_SETVIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-259">Définit le moniteur de source vidéo et doit être utilisé avec le \_ magnétoscope MCI \_ SETVIDEO \_ pour signaler.</span><span class="sxs-lookup"><span data-stu-id="b7f48-259">Sets the video source monitor, and must be used with the MCI\_VCR\_SETVIDEO\_TO flag.</span></span>

</dd> <dt>

<span data-ttu-id="b7f48-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>\_magnétoscope MCI \_ SETVIDEO \_ à</span><span class="sxs-lookup"><span data-stu-id="b7f48-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI\_VCR\_SETVIDEO\_TO</span></span>
</dt> <dd>

<span data-ttu-id="b7f48-261">Le membre **dwTo** de la structure identifiée par *lpSetVideo* contient l’une des constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7f48-261">The **dwTo** member of the structure identified by *lpSetVideo* contains one of the following constants:</span></span>

<dl> <dd><span data-ttu-id="b7f48-262">**\_tuner de \_ \_ type SRC magnétoscope MCI \_**</span><span class="sxs-lookup"><span data-stu-id="b7f48-262">**MCI\_VCR\_SRC\_TYPE\_TUNER**</span></span></dd> <dd><span data-ttu-id="b7f48-263">**\_ligne de \_ \_ type SRC magnétoscope MCI \_**</span><span class="sxs-lookup"><span data-stu-id="b7f48-263">**MCI\_VCR\_SRC\_TYPE\_LINE**</span></span></dd> <dd><span data-ttu-id="b7f48-264">**\_magnétoscope MCI \_ type de source \_ \_ aux**</span><span class="sxs-lookup"><span data-stu-id="b7f48-264">**MCI\_VCR\_SRC\_TYPE\_AUX**</span></span></dd> <dd><span data-ttu-id="b7f48-265">**\_type de source de magnétoscope MCI \_ \_ \_ générique**</span><span class="sxs-lookup"><span data-stu-id="b7f48-265">**MCI\_VCR\_SRC\_TYPE\_GENERIC**</span></span></dd> <dd><span data-ttu-id="b7f48-266">**\_type de source de magnétoscope MCI \_ \_ \_ muet**</span><span class="sxs-lookup"><span data-stu-id="b7f48-266">**MCI\_VCR\_SRC\_TYPE\_MUTE**</span></span></dd> <dd><span data-ttu-id="b7f48-267">**\_sortie de \_ \_ type SRC magnétoscope MCI \_**</span><span class="sxs-lookup"><span data-stu-id="b7f48-267">**MCI\_VCR\_SRC\_TYPE\_OUTPUT**</span></span></dd> <dd><span data-ttu-id="b7f48-268">**\_type de source de magnétoscope MCI \_ \_ \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="b7f48-268">**MCI\_VCR\_SRC\_TYPE\_RGB**</span></span></dd> <dd><span data-ttu-id="b7f48-269">**\_ \_ numéro SETVIDEO magnétoscope \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="b7f48-269">**MCI\_VCR\_SETVIDEO\_NUMBER**</span></span></dd> </dl>

<span data-ttu-id="b7f48-270">Le membre **dwNumber** de la structure identifiée par *lpSetVideo* contient l’entrée vidéo (du type spécifié dans le membre **dwTo** ) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b7f48-270">The **dwNumber** member of the structure identified by *lpSetVideo* contains the video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

<span data-ttu-id="b7f48-271">Pour les périphériques VCR, le paramètre *lpSetVideo* pointe vers une structure [**MCI \_ VCR \_ SETVIDEO \_ PARMS**](mci-vcr-setvideo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="b7f48-271">For VCR devices, the *lpSetVideo* parameter points to an [**MCI\_VCR\_SETVIDEO\_PARMS**](mci-vcr-setvideo-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f48-272">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7f48-272">Requirements</span></span>



| <span data-ttu-id="b7f48-273">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7f48-273">Requirement</span></span> | <span data-ttu-id="b7f48-274">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7f48-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f48-275">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7f48-275">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f48-276">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7f48-276">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b7f48-277">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7f48-277">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f48-278">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7f48-278">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b7f48-279">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7f48-279">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7f48-280"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7f48-280"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f48-281">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7f48-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f48-282">MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-282">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b7f48-283">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="b7f48-283">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

