---
title: Commande MCI_STATUS (mmsystem. h)
description: La \_ commande d’État MCI récupère des informations sur un périphérique MCI. Tous les appareils reconnaissent cette commande. Les informations sont retournées dans le membre dwReturn de la structure identifiée par le paramètre lpStatus.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- Commande MCI_STATUS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/12/2021
ms.locfileid: "104321253"
---
# <a name="mci_status-command"></a><span data-ttu-id="6eaed-106">\_Commande d’État MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-106">MCI\_STATUS command</span></span>

> [!NOTE]
> <span data-ttu-id="6eaed-107">Communication sans biais Microsoft prend en charge un environnement diversifié et un environnement d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="6eaed-107">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="6eaed-108">Dans ce document, il existe des références au mot « esclave ».</span><span class="sxs-lookup"><span data-stu-id="6eaed-108">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="6eaed-109">Le [Guide de style de Microsoft pour les Communications Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconnaît cela comme un mot d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="6eaed-109">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="6eaed-110">Ce libellé est utilisé, car il s’agit actuellement de la formulation utilisée dans les commandes.</span><span class="sxs-lookup"><span data-stu-id="6eaed-110">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="6eaed-111">Pour des fins de cohérence, ce document contient ce mot.</span><span class="sxs-lookup"><span data-stu-id="6eaed-111">For consistency, this document contains this word.</span></span> <span data-ttu-id="6eaed-112">Lorsque ce mot est modifié dans les commandes, nous allons corriger ce document pour qu’il soit aligné.</span><span class="sxs-lookup"><span data-stu-id="6eaed-112">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="6eaed-113">La \_ commande d’État MCI récupère des informations sur un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="6eaed-113">The MCI\_STATUS command retrieves information about an MCI device.</span></span> <span data-ttu-id="6eaed-114">Tous les appareils reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="6eaed-114">All devices recognize this command.</span></span> <span data-ttu-id="6eaed-115">Les informations sont retournées dans le membre **dwReturn** de la structure identifiée par le paramètre *lpStatus* .</span><span class="sxs-lookup"><span data-stu-id="6eaed-115">Information is returned in the **dwReturn** member of the structure identified by the *lpStatus* parameter.</span></span>

<span data-ttu-id="6eaed-116">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="6eaed-116">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
);
```



## <a name="parameters"></a><span data-ttu-id="6eaed-117">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6eaed-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eaed-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6eaed-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-119">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="6eaed-119">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6eaed-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-121">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="6eaed-121">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="6eaed-122">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6eaed-122">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span><span class="sxs-lookup"><span data-stu-id="6eaed-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-124">Pointeur vers une structure d' [**\_ \_ État MCI**](mci-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-124">Pointer to an [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure.</span></span> <span data-ttu-id="6eaed-125">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="6eaed-125">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eaed-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6eaed-126">Return Value</span></span>

<span data-ttu-id="6eaed-127">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="6eaed-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eaed-128">Notes</span><span class="sxs-lookup"><span data-stu-id="6eaed-128">Remarks</span></span>

<span data-ttu-id="6eaed-129">Les indicateurs standard et spécifiques à la commande suivants s’appliquent à tous les appareils prenant en charge l' \_ État MCI :</span><span class="sxs-lookup"><span data-stu-id="6eaed-129">The following additional standard and command-specific flags apply to all devices supporting MCI\_STATUS:</span></span>

<dl> <dt>

<span data-ttu-id="6eaed-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>\_élément d’État MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI\_STATUS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-131">Spécifie que le membre **dwItem** de la structure identifiée par *lpStatus* contient une constante qui spécifie l’élément d’État à obtenir.</span><span class="sxs-lookup"><span data-stu-id="6eaed-131">Specifies that the **dwItem** member of the structure identified by *lpStatus* contains a constant specifying which status item to obtain.</span></span> <span data-ttu-id="6eaed-132">Les constantes suivantes définissent l’élément d’État à retourner dans le membre **dwReturn** de la structure :</span><span class="sxs-lookup"><span data-stu-id="6eaed-132">The following constants define which status item to return in the **dwReturn** member of the structure:</span></span>

<span data-ttu-id="6eaed-133">\_ \_ piste active de l’État MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-133">MCI\_STATUS\_CURRENT\_TRACK</span></span>

<span data-ttu-id="6eaed-134">Le membre **dwReturn** est défini sur le numéro de suivi actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-134">The **dwReturn** member is set to the current track number.</span></span> <span data-ttu-id="6eaed-135">MCI utilise des numéros de pistes continus.</span><span class="sxs-lookup"><span data-stu-id="6eaed-135">MCI uses continuous track numbers.</span></span>

<span data-ttu-id="6eaed-136">longueur de l' \_ État MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-136">MCI\_STATUS\_LENGTH</span></span>

<span data-ttu-id="6eaed-137">Le membre **dwReturn** est défini sur la longueur totale du média.</span><span class="sxs-lookup"><span data-stu-id="6eaed-137">The **dwReturn** member is set to the total media length.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_mode d’État MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-139">Le membre **dwReturn** est défini sur le mode actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6eaed-139">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="6eaed-140">Les modes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6eaed-140">The modes include the following:</span></span>

-   <span data-ttu-id="6eaed-141">\_mode MCI \_ non \_ prêt</span><span class="sxs-lookup"><span data-stu-id="6eaed-141">MCI\_MODE\_NOT\_READY</span></span>
-   <span data-ttu-id="6eaed-142">\_pause en mode MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-142">MCI\_MODE\_PAUSE</span></span>
-   <span data-ttu-id="6eaed-143">\_lecture en mode MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-143">MCI\_MODE\_PLAY</span></span>
-   <span data-ttu-id="6eaed-144">\_arrêt en mode MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-144">MCI\_MODE\_STOP</span></span>
-   <span data-ttu-id="6eaed-145">\_mode MCI \_ ouvert</span><span class="sxs-lookup"><span data-stu-id="6eaed-145">MCI\_MODE\_OPEN</span></span>
-   <span data-ttu-id="6eaed-146">\_enregistrement en mode MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-146">MCI\_MODE\_RECORD</span></span>
-   <span data-ttu-id="6eaed-147">\_recherche en mode MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-147">MCI\_MODE\_SEEK</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>\_ \_ nombre d’États MCI \_ des \_ pistes</span><span class="sxs-lookup"><span data-stu-id="6eaed-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI\_STATUS\_NUMBER\_OF\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-149">Le membre **dwReturn** est défini sur le nombre total de pistes lisibles.</span><span class="sxs-lookup"><span data-stu-id="6eaed-149">The **dwReturn** member is set to the total number of playable tracks.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>POSITION de l' \_ État MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI\_STATUS\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-151">Le membre **dwReturn** est défini à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="6eaed-151">The **dwReturn** member is set to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>\_État MCI \_ prêt</span><span class="sxs-lookup"><span data-stu-id="6eaed-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI\_STATUS\_READY</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-153">Le membre **dwReturn** a la valeur **true** si l’appareil est prêt ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-153">The **dwReturn** member is set to **TRUE** if the device is ready; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>FORMAT de l’heure de l' \_ État MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI\_STATUS\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-155">Le membre **dwReturn** est défini sur le format d’heure actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6eaed-155">The **dwReturn** member is set to the current time format of the device.</span></span> <span data-ttu-id="6eaed-156">Les formats d’heure sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6eaed-156">The time formats include:</span></span>

-   <span data-ttu-id="6eaed-157">\_octets au format MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-157">MCI\_FORMAT\_BYTES</span></span>
-   <span data-ttu-id="6eaed-158">\_images au format MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-158">MCI\_FORMAT\_FRAMES</span></span>
-   <span data-ttu-id="6eaed-159">\_format MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="6eaed-159">MCI\_FORMAT\_HMS</span></span>
-   <span data-ttu-id="6eaed-160">FORMAT MCI en \_ \_ millisecondes</span><span class="sxs-lookup"><span data-stu-id="6eaed-160">MCI\_FORMAT\_MILLISECONDS</span></span>
-   <span data-ttu-id="6eaed-161">FORMAT MCI ( \_ \_ MSF)</span><span class="sxs-lookup"><span data-stu-id="6eaed-161">MCI\_FORMAT\_MSF</span></span>
-   <span data-ttu-id="6eaed-162">\_exemples de format MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-162">MCI\_FORMAT\_SAMPLES</span></span>
-   <span data-ttu-id="6eaed-163">\_format MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="6eaed-163">MCI\_FORMAT\_TMSF</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>démarrage de l' \_ État MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI\_STATUS\_START</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-165">Obtient la position de départ du média.</span><span class="sxs-lookup"><span data-stu-id="6eaed-165">Obtains the starting position of the media.</span></span> <span data-ttu-id="6eaed-166">Pour atteindre la position de départ, associez cet indicateur à l' \_ élément d’État MCI \_ et définissez le membre **dwItem** de la structure identifiée par *lpStatus* sur la position d' \_ État MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="6eaed-166">To get the starting position, combine this flag with MCI\_STATUS\_ITEM and set the **dwItem** member of the structure identified by *lpStatus* to MCI\_STATUS\_POSITION.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>\_piste MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-168">Indique qu’un paramètre de suivi d’État est inclus dans le membre **dwTrack** de la structure identifiée par *lpStatus*.</span><span class="sxs-lookup"><span data-stu-id="6eaed-168">Indicates a status track parameter is included in the **dwTrack** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="6eaed-169">Vous devez utiliser cet indicateur avec les \_ \_ constantes position d’État MCI ou \_ longueur d’État MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="6eaed-169">You must use this flag with the MCI\_STATUS\_POSITION or MCI\_STATUS\_LENGTH constants.</span></span> <span data-ttu-id="6eaed-170">Lorsqu’elle est utilisée avec la \_ position d’État MCI \_ , \_ la piste MCI obtient la position de départ de la piste spécifiée. Lorsqu’elle est utilisée avec la \_ \_ durée d’État MCI, \_ la piste MCI obtient la longueur de la piste spécifiée. MCI utilise des numéros de pistes continus.</span><span class="sxs-lookup"><span data-stu-id="6eaed-170">When used with MCI\_STATUS\_POSITION, MCI\_TRACK obtains the starting position of the specified track. When used with MCI\_STATUS\_LENGTH, MCI\_TRACK obtains the length of the specified track. MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="6eaed-171">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **cdaudio** .</span><span class="sxs-lookup"><span data-stu-id="6eaed-171">The following additional flags are used with the **cdaudio** device type.</span></span> <span data-ttu-id="6eaed-172">Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6eaed-172">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="6eaed-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>\_piste de \_ type d’État MCI CDA \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI\_CDA\_STATUS\_TYPE\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-174">Le membre **dwReturn** est défini sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6eaed-174">The **dwReturn** member is set to one of the following values:</span></span>

-   <span data-ttu-id="6eaed-175">MCI \_ CDA \_ piste \_ audio</span><span class="sxs-lookup"><span data-stu-id="6eaed-175">MCI\_CDA\_TRACK\_AUDIO</span></span>
-   <span data-ttu-id="6eaed-176">MCI \_ CDA- \_ piste \_ autre</span><span class="sxs-lookup"><span data-stu-id="6eaed-176">MCI\_CDA\_TRACK\_OTHER</span></span>

<span data-ttu-id="6eaed-177">Pour utiliser cet indicateur, l' \_ indicateur de piste MCI doit être défini et le membre **dwTrack** de la structure identifié par *lpStatus* doit contenir un numéro de suivi valide.</span><span class="sxs-lookup"><span data-stu-id="6eaed-177">To use this flag, the MCI\_TRACK flag must be set, and the **dwTrack** member of the structure identified by *lpStatus* must contain a valid track number.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent</span><span class="sxs-lookup"><span data-stu-id="6eaed-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-179">Le membre **dwReturn** a la valeur **true** si le média est inséré dans l’appareil ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-179">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="6eaed-180">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="6eaed-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="6eaed-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>\_DGV d' \_ état \_ MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI\_DGV\_STATUS\_DISKSPACE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-182">Le membre **lpstrDrive** de la structure identifiée par *lpStatus* spécifie un lecteur de disque ou, dans certaines implémentations, un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="6eaed-182">The **lpstrDrive** member of the structure identified by *lpStatus* specifies a disk drive or, in some implementations, a path.</span></span> <span data-ttu-id="6eaed-183">La \_ commande d’État MCI retourne la quantité approximative d’espace disque qui peut être obtenue par la commande de [ \_ réserve MCI](mci-reserve.md) dans le membre **dwReturn** de la structure identifiée par *lpStatus*.</span><span class="sxs-lookup"><span data-stu-id="6eaed-183">The MCI\_STATUS command returns the approximate amount of disk space that could be obtained by the [MCI\_RESERVE](mci-reserve.md) command in the **dwReturn** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="6eaed-184">L’espace disque est mesuré en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-184">The disk space is measured in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>\_ \_ entrée d’État MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI\_DGV\_STATUS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-186">La constante spécifiée par le membre **dwItem** de la structure identifiée par *lpStatus* s’applique à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-186">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the input.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>État de DGV MCI à \_ \_ \_ gauche</span><span class="sxs-lookup"><span data-stu-id="6eaed-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>MCI\_DGV\_STATUS\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-188">La constante spécifiée par le membre **dwItem** de la structure identifiée par *lpStatus* s’applique au canal audio de gauche.</span><span class="sxs-lookup"><span data-stu-id="6eaed-188">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>\_ \_ état \_ nominal de MCI DGV</span><span class="sxs-lookup"><span data-stu-id="6eaed-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI\_DGV\_STATUS\_NOMINAL</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-190">La constante spécifiée par le membre **dwItem** de la structure identifiée par *lpStatus* demande la valeur nominale plutôt que la valeur actuelle.</span><span class="sxs-lookup"><span data-stu-id="6eaed-190">The constant specified by the **dwItem** member of the structure identified by *lpStatus* requests the nominal value rather than the current value.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>sortie de l' \_ État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI\_DGV\_STATUS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-192">La constante spécifiée par le membre **dwItem** de la structure identifiée par *lpStatus* s’applique à la sortie.</span><span class="sxs-lookup"><span data-stu-id="6eaed-192">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the output.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>\_enregistrement d' \_ État MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI\_DGV\_STATUS\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-194">La fréquence d’images renvoyée pour l' \_ indicateur de fréquence d’images d’État MCI DGV \_ \_ \_ est le taux utilisé pour la compression.</span><span class="sxs-lookup"><span data-stu-id="6eaed-194">The frame rate returned for the MCI\_DGV\_STATUS\_FRAME\_RATE flag is the rate used for compression.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>informations de référence sur l' \_ État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI\_DGV\_STATUS\_REFERENCE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-196">Le membre **dwReturn** de la structure identifiée par *lpStatus* retourne l’image de l’image clé la plus proche qui précède le frame spécifié dans le membre **dwReference** .</span><span class="sxs-lookup"><span data-stu-id="6eaed-196">The **dwReturn** member of the structure identified by *lpStatus* returns the nearest key-frame image that precedes the frame specified in the **dwReference** member.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>État de DGV MCI- \_ \_ \_ droit</span><span class="sxs-lookup"><span data-stu-id="6eaed-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI\_DGV\_STATUS\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-198">La constante spécifiée par le membre **dwItem** de la structure identifiée par *lpStatus* s’applique au canal audio approprié.</span><span class="sxs-lookup"><span data-stu-id="6eaed-198">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the right audio channel.</span></span>

</dd> </dl>

<span data-ttu-id="6eaed-199">Les constantes suivantes sont utilisées avec le type d’appareil **Digitalvideo** dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6eaed-199">The following constants are used with the **digitalvideo** device type in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="6eaed-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>\_ \_ \_ sauts audio d’État AVI \_ MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI\_AVI\_STATUS\_AUDIO\_BREAKS</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-201">Le membre **dwReturn** retourne le nombre de fois que la partie audio de la dernière séquence AVI est tombée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-201">The **dwReturn** member returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="6eaed-202">Le système compte un saut audio chaque fois qu’il tente d’écrire des données audio sur le pilote de périphérique et découvre que le pilote a déjà lu toutes les données disponibles.</span><span class="sxs-lookup"><span data-stu-id="6eaed-202">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="6eaed-203">Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="6eaed-203">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>\_images d' \_ État AVI MCI \_ \_ ignorées</span><span class="sxs-lookup"><span data-stu-id="6eaed-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>MCI\_AVI\_STATUS\_FRAMES\_SKIPPED</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-205">Le membre **dwReturn** retourne le nombre d’images qui n’ont pas été dessinées lorsque la dernière séquence AVI a été lue.</span><span class="sxs-lookup"><span data-stu-id="6eaed-205">The **dwReturn** member returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="6eaed-206">Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="6eaed-206">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>\_vitesse de \_ \_ lecture du dernier État AVI \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI\_AVI\_STATUS\_LAST\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-208">Le membre **dwReturn** retourne une valeur représentant le degré de précision de la durée de l’exécution réelle de la dernière séquence AVI correspondant à la durée d’exécution de la cible.</span><span class="sxs-lookup"><span data-stu-id="6eaed-208">The **dwReturn** member returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="6eaed-209">La valeur 1000 indique que l’heure cible et l’heure réelle étaient les mêmes.</span><span class="sxs-lookup"><span data-stu-id="6eaed-209">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="6eaed-210">Une valeur de 2000, par exemple, indique que la séquence AVI prenait deux fois plus de temps que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-210">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="6eaed-211">Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="6eaed-211">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>\_ \_ État audio MCI \_ DGV</span><span class="sxs-lookup"><span data-stu-id="6eaed-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI\_DGV\_STATUS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-213">Le membre **dwReturn** retourne la valeur MCI \_ on ou MCI \_ off selon l’option MCI Set audio la plus récente \_ \_ pour la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-213">The **dwReturn** member returns MCI\_ON or MCI\_OFF depending on the most recent MCI\_SET\_AUDIO option for the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="6eaed-214">Elle retourne MCI \_ sur si l’un ou l’autre ou les deux enceintes sont activées, et l' \_ option MCI désactivée dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-214">It returns MCI\_ON if either or both speakers are enabled, and MCI\_OFF otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>\_ \_ \_ entrée audio d’État MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI\_DGV\_STATUS\_AUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-216">Le membre **dwReturn** retourne le niveau audio instantané approximatif du signal audio analogique.</span><span class="sxs-lookup"><span data-stu-id="6eaed-216">The **dwReturn** member returns the approximate instantaneous audio level of the analog audio signal.</span></span> <span data-ttu-id="6eaed-217">Une valeur supérieure à 1000 signifie qu’il y a une distorsion de découpage.</span><span class="sxs-lookup"><span data-stu-id="6eaed-217">A value greater than 1000 implies there is clipping distortion.</span></span> <span data-ttu-id="6eaed-218">Certains appareils peuvent déterminer cette valeur uniquement lors de l’enregistrement audio.</span><span class="sxs-lookup"><span data-stu-id="6eaed-218">Some devices can determine this value only while recording audio.</span></span> <span data-ttu-id="6eaed-219">Cette valeur d’État n’a pas de commande **MCI \_ Set** ou [MCI \_ SETAUDIO](mci-setaudio.md) associée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-219">This status value has no associated **MCI\_SET** or [MCI\_SETAUDIO](mci-setaudio.md) command.</span></span> <span data-ttu-id="6eaed-220">Cette valeur est associée à, mais normalisée différemment de, le niveau d’état de l’onde MCI Wave de commande Waveform Audio \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6eaed-220">This value is related to, but normalized differently from, the waveform-audio command MCI\_WAVE\_STATUS\_LEVEL.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>\_ \_ enregistrement audio d’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI\_DGV\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-222">Le membre **dwReturn** retourne la \_ valeur MCI on ou MCI en \_ reflétant l’état défini par l' \_ \_ indicateur d’enregistrement MCI DGV SETAUDIO \_ de la commande **MCI \_ SETAUDIO** .</span><span class="sxs-lookup"><span data-stu-id="6eaed-222">The **dwReturn** member returns MCI\_ON or MCI\_OFF reflecting the state set by the MCI\_DGV\_SETAUDIO\_RECORD flag of the **MCI\_SETAUDIO** command.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>\_ \_ source audio d’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI\_DGV\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-224">Le membre **dwReturn** retourne la source de digitaliseur audio actuelle :</span><span class="sxs-lookup"><span data-stu-id="6eaed-224">The **dwReturn** member returns the current audio digitizer source:</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>\_moyenne de \_ SETAUDIO \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI\_DGV\_SETAUDIO\_AVERAGE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-226">Spécifie la moyenne des canaux audio de gauche et de droite.</span><span class="sxs-lookup"><span data-stu-id="6eaed-226">Specifies the average of the left and right audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ SETAUDIO \_ gauche</span><span class="sxs-lookup"><span data-stu-id="6eaed-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-228">Spécifie le canal audio de gauche.</span><span class="sxs-lookup"><span data-stu-id="6eaed-228">Specifies the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ Right</span><span class="sxs-lookup"><span data-stu-id="6eaed-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-230">Spécifie le canal audio approprié.</span><span class="sxs-lookup"><span data-stu-id="6eaed-230">Specifies the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ SETAUDIO \_ stéréo</span><span class="sxs-lookup"><span data-stu-id="6eaed-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI\_DGV\_SETAUDIO\_STEREO</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-232">Spécifie le stéréo.</span><span class="sxs-lookup"><span data-stu-id="6eaed-232">Specifies stereo.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>\_ \_ flux audio d’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI\_DGV\_STATUS\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-234">Le membre **dwReturn** retourne le numéro de flux audio actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-234">The **dwReturn** member returns the current audio-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>\_État DGV \_ MCI \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="6eaed-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI\_DGV\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-236">Le membre **dwReturn** retourne le nombre moyen d’octets par seconde utilisés pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eaed-236">The **dwReturn** member returns the average number of bytes per second used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>\_État DGV MCI- \_ \_ basses</span><span class="sxs-lookup"><span data-stu-id="6eaed-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI\_DGV\_STATUS\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-238">Le membre **dwReturn** retourne le niveau de basses audio actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-238">The **dwReturn** member returns the current audio bass level.</span></span> <span data-ttu-id="6eaed-239">Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.</span><span class="sxs-lookup"><span data-stu-id="6eaed-239">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>\_État DGV \_ MCI \_ BITSPERPEL</span><span class="sxs-lookup"><span data-stu-id="6eaed-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI\_DGV\_STATUS\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-241">Le membre **dwReturn** retourne le nombre de bits par pixel utilisé pour enregistrer les données capturées ou enregistrées.</span><span class="sxs-lookup"><span data-stu-id="6eaed-241">The **dwReturn** member returns the number of bits per pixel used for saving captured or recorded data.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>\_État DGV \_ MCI \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="6eaed-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI\_DGV\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-243">Le membre **dwReturn** retourne le nombre de bits par échantillon que l’appareil utilise pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eaed-243">The **dwReturn** member returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="6eaed-244">Cela s’applique uniquement aux appareils prenant en charge le format PCM.</span><span class="sxs-lookup"><span data-stu-id="6eaed-244">This applies only to devices supporting the PCM format.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>\_État DGV \_ MCI \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="6eaed-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI\_DGV\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-246">Le membre **dwReturn** retourne l’alignement des blocs de données par rapport au début de la forme d’onde d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-246">The **dwReturn** member returns the alignment of data blocks relative to the start of the input waveform.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>luminosité de l' \_ État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI\_DGV\_STATUS\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-248">Le membre **dwReturn** retourne le niveau de luminosité vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-248">The **dwReturn** member returns the current video brightness level.</span></span> <span data-ttu-id="6eaed-249">Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.</span><span class="sxs-lookup"><span data-stu-id="6eaed-249">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>\_couleur d' \_ État MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI\_DGV\_STATUS\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-251">Le membre **dwReturn** retourne le niveau de couleur actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-251">The **dwReturn** member returns the current color level.</span></span> <span data-ttu-id="6eaed-252">Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.</span><span class="sxs-lookup"><span data-stu-id="6eaed-252">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>contraste de l' \_ État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI\_DGV\_STATUS\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-254">Le membre **dwReturn** retourne le niveau de contraste actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-254">The **dwReturn** member returns the current contrast level.</span></span> <span data-ttu-id="6eaed-255">Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.</span><span class="sxs-lookup"><span data-stu-id="6eaed-255">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>\_État d’DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI\_DGV\_STATUS\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-257">Le membre **dwReturn** retourne le format de fichier actuel pour l’enregistrement ou l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eaed-257">The **dwReturn** member returns the current file format for recording or saving.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>\_mode de \_ fichier d’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI\_DGV\_STATUS\_FILE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-259">Le membre **dwReturn** retourne l’état de l’opération de fichier :</span><span class="sxs-lookup"><span data-stu-id="6eaed-259">The **dwReturn** member returns the state of the file operation:</span></span>

<span data-ttu-id="6eaed-260">\_modification du \_ mode de fichier DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-260">MCI\_DGV\_FILE\_MODE\_EDITING</span></span>

<span data-ttu-id="6eaed-261">Renvoyé pendant les opérations couper, copier, supprimer, coller et annuler.</span><span class="sxs-lookup"><span data-stu-id="6eaed-261">Returned during cut, copy, delete, paste, and undo operations.</span></span>

<span data-ttu-id="6eaed-262">\_mode de \_ fichier DGV MCI \_ \_ inactif</span><span class="sxs-lookup"><span data-stu-id="6eaed-262">MCI\_DGV\_FILE\_MODE\_IDLE</span></span>

<span data-ttu-id="6eaed-263">Renvoyé lorsque le fichier est prêt pour l’opération suivante.</span><span class="sxs-lookup"><span data-stu-id="6eaed-263">Returned when the file is ready for the next operation.</span></span>

<span data-ttu-id="6eaed-264">\_ \_ \_ chargement en mode de fichier DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-264">MCI\_DGV\_FILE\_MODE\_LOADING</span></span>

<span data-ttu-id="6eaed-265">Retourné lors du chargement du fichier.</span><span class="sxs-lookup"><span data-stu-id="6eaed-265">Returned while the file is being loaded.</span></span>

<span data-ttu-id="6eaed-266">\_ \_ \_ enregistrement en mode de fichier DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-266">MCI\_DGV\_FILE\_MODE\_SAVING</span></span>

<span data-ttu-id="6eaed-267">Retourné lors de l’enregistrement du fichier.</span><span class="sxs-lookup"><span data-stu-id="6eaed-267">Returned while the file is being saved.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>\_exécution du \_ fichier d’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI\_DGV\_STATUS\_FILE\_COMPLETION</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-269">Le membre **dwReturn** retourne le pourcentage estimé pendant lequel l’opération de chargement, d’enregistrement, de capture, de couper, de copier, de suppression, de collage ou d’annulation a progressé.</span><span class="sxs-lookup"><span data-stu-id="6eaed-269">The **dwReturn** member returns the estimated percentage a load, save, capture, cut, copy, delete, paste, or undo operation has progressed.</span></span> <span data-ttu-id="6eaed-270">(Les applications peuvent l’utiliser pour fournir un indicateur visuel de la progression.) Cet indicateur n’est pas pris en charge par tous les périphériques vidéo numériques.</span><span class="sxs-lookup"><span data-stu-id="6eaed-270">(Applications can use this to provide a visual indicator of progress.) This flag is not supported by all digital-video devices.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>\_État de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI\_DGV\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-272">Le membre **dwReturn** retourne la **valeur true** si la direction de l’appareil est vers l’avant ou si l’appareil n’est pas en train de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="6eaed-272">The **dwReturn** member returns **TRUE** if the device direction is forward or the device is not playing.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>\_fréquence d' \_ images d’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI\_DGV\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-274">Le membre **dwReturn** doit être utilisé avec l' \_ État DGV de l' \_ état \_ nominal, MCI \_ DGV \_ \_ , ou les deux.</span><span class="sxs-lookup"><span data-stu-id="6eaed-274">The **dwReturn** member must be used with MCI\_DGV\_STATUS\_NOMINAL, MCI\_DGV\_STATUS\_RECORD, or both.</span></span> <span data-ttu-id="6eaed-275">Lorsqu' \_ il est utilisé avec \_ l’enregistrement d’État MCI DGV \_ , la fréquence d’images actuelle utilisée pour l’enregistrement est retournée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-275">When used with MCI\_DGV\_STATUS\_RECORD, the current frame rate used for recording is returned.</span></span> <span data-ttu-id="6eaed-276">En cas d’utilisation avec les \_ enregistrements d’État MCI DGV et les \_ \_ \_ États MCI DGV \_ \_ , la fréquence d’images nominale associée au signal vidéo d’entrée est retournée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-276">When used with both MCI\_DGV\_STATUS\_RECORD and MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the input video signal is returned.</span></span> <span data-ttu-id="6eaed-277">Lorsqu' \_ il est utilisé avec \_ l’État nominal de l’DGV MCI \_ , la fréquence d’images nominale associée au fichier est retournée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-277">When used with MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the file is returned.</span></span> <span data-ttu-id="6eaed-278">Dans tous les cas, les unités sont en images par seconde multiplié par 1000.</span><span class="sxs-lookup"><span data-stu-id="6eaed-278">In all cases the units are in frames per second multiplied by 1000.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>\_ \_ État gamma des DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI\_DGV\_STATUS\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-280">Le membre **dwReturn** retourne la valeur gamma actuelle.</span><span class="sxs-lookup"><span data-stu-id="6eaed-280">The **dwReturn** member returns the current gamma value.</span></span> <span data-ttu-id="6eaed-281">Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.</span><span class="sxs-lookup"><span data-stu-id="6eaed-281">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>\_État DGV \_ MCI \_ HPAL</span><span class="sxs-lookup"><span data-stu-id="6eaed-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI\_DGV\_STATUS\_HPAL</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-283">Le membre **dwReturn** retourne la valeur décimale ASCII pour le handle de palette actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-283">The **dwReturn** member returns the ASCII decimal value for the current palette handle.</span></span> <span data-ttu-id="6eaed-284">Le descripteur est contenu dans le mot de poids faible de la valeur retournée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-284">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>\_HWND DGV \_ état \_ HWND</span><span class="sxs-lookup"><span data-stu-id="6eaed-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI\_DGV\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-286">Le membre **dwReturn** retourne la valeur décimale ASCII pour le handle de fenêtre explicite ou par défaut actuellement associé à cette instance de pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="6eaed-286">The **dwReturn** member returns the ASCII decimal value for the current explicit or default window handle associated with this device driver instance.</span></span> <span data-ttu-id="6eaed-287">Le descripteur est contenu dans le mot de poids faible de la valeur retournée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-287">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>couleur de la clé d’État MCI \_ DGV \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI\_DGV\_STATUS\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-289">Le membre **dwReturn** retourne la valeur de la couleur de la clé actuelle.</span><span class="sxs-lookup"><span data-stu-id="6eaed-289">The **dwReturn** member returns the current key-color value.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>INDEX de la clé d’État MCI \_ DGV \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI\_DGV\_STATUS\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-291">Le membre **dwReturn** retourne la valeur actuelle de l’index de clé.</span><span class="sxs-lookup"><span data-stu-id="6eaed-291">The **dwReturn** member returns the current key-index value.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>\_moniteur d' \_ État MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MCI\_DGV\_STATUS\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-293">Le membre **dwReturn** retourne une constante indiquant la source de la présentation actuelle.</span><span class="sxs-lookup"><span data-stu-id="6eaed-293">The **dwReturn** member returns a constant indicating the source of the current presentation.</span></span> <span data-ttu-id="6eaed-294">Les constantes suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="6eaed-294">The following constants are defined:</span></span>

<span data-ttu-id="6eaed-295">\_fichier d' \_ analyse \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-295">MCI\_DGV\_MONITOR\_FILE</span></span>

<span data-ttu-id="6eaed-296">Un fichier est la source.</span><span class="sxs-lookup"><span data-stu-id="6eaed-296">A file is the source.</span></span>

<span data-ttu-id="6eaed-297">\_entrée du \_ moniteur MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-297">MCI\_DGV\_MONITOR\_INPUT</span></span>

<span data-ttu-id="6eaed-298">L’entrée est la source.</span><span class="sxs-lookup"><span data-stu-id="6eaed-298">The input is the source.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>\_méthode du \_ moniteur d’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI\_DGV\_STATUS\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-300">Le membre **dwReturn** retourne une constante indiquant la méthode utilisée pour la surveillance d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-300">The **dwReturn** member returns a constant indicating the method used for input monitoring.</span></span> <span data-ttu-id="6eaed-301">Les constantes suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="6eaed-301">The following constants are defined:</span></span>

<span data-ttu-id="6eaed-302">\_ \_ mode direct MCI \_ DGV</span><span class="sxs-lookup"><span data-stu-id="6eaed-302">MCI\_DGV\_METHOD\_DIRECT</span></span>

<span data-ttu-id="6eaed-303">Surveillance directe des entrées.</span><span class="sxs-lookup"><span data-stu-id="6eaed-303">Direct input monitoring.</span></span>

<span data-ttu-id="6eaed-304">publication de la \_ méthode DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-304">MCI\_DGV\_METHOD\_POST</span></span>

<span data-ttu-id="6eaed-305">Surveillance après entrée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-305">Post-input monitoring.</span></span>

<span data-ttu-id="6eaed-306">\_pré- \_ méthode \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-306">MCI\_DGV\_METHOD\_PRE</span></span>

<span data-ttu-id="6eaed-307">Surveillance de pré-entrée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-307">Pre-input monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>\_ \_ \_ mode pause de l’État MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI\_DGV\_STATUS\_PAUSE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-309">Le membre **dwReturn** retourne le \_ mode \_ lecture MCI si l’appareil a été interrompu lors de la lecture et retourne l' \_ enregistrement en mode MCI \_ si l’appareil a été mis en pause pendant l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eaed-309">The **dwReturn** member returns MCI\_MODE\_PLAY if the device was paused while playing and returns MCI\_MODE\_RECORD if the device was paused while recording.</span></span> <span data-ttu-id="6eaed-310">La commande retourne la \_ \_ fonction non applicable MCIERR comme une erreur de retour si l’appareil n’est pas suspendu.</span><span class="sxs-lookup"><span data-stu-id="6eaed-310">The command returns MCIERR\_NONAPPLICABLE\_FUNCTION as an error return if the device is not paused.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>\_État DGV \_ MCI \_ SAMPLESPERSECOND</span><span class="sxs-lookup"><span data-stu-id="6eaed-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI\_DGV\_STATUS\_SAMPLESPERSECOND</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-312">Le membre **dwReturn** retourne le nombre d’échantillons par seconde enregistrés.</span><span class="sxs-lookup"><span data-stu-id="6eaed-312">The **dwReturn** member returns the number of samples per second recorded.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>\_État de DGV MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI\_DGV\_STATUS\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-314">Le membre **dwReturn** retourne **true** ou **false** indiquant si le format Seek exact est défini.</span><span class="sxs-lookup"><span data-stu-id="6eaed-314">The **dwReturn** member returns **TRUE** or **FALSE** indicating whether or not the seek exactly format is set.</span></span> <span data-ttu-id="6eaed-315">(Les applications peuvent définir ce format à l’aide de la commande [MCI \_ Set](mci-set.md) avec l' \_ indicateur MCI DGV \_ Set \_ Seek \_ exact.)</span><span class="sxs-lookup"><span data-stu-id="6eaed-315">(Applications can set this format by using the [MCI\_SET](mci-set.md) command with the MCI\_DGV\_SET\_SEEK\_EXACTLY flag.)</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>\_netteté de l’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI\_DGV\_STATUS\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-317">Le membre **dwReturn** retourne le niveau de netteté actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-317">The **dwReturn** member returns the current sharpness level.</span></span> <span data-ttu-id="6eaed-318">Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.</span><span class="sxs-lookup"><span data-stu-id="6eaed-318">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>taille de l' \_ État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI\_DGV\_STATUS\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-320">Le membre **dwReturn** retourne la durée de lecture approximative des données compressées que l’espace de travail réservé contiendra.</span><span class="sxs-lookup"><span data-stu-id="6eaed-320">The **dwReturn** member returns the approximate playback duration of compressed data that the reserved workspace will hold.</span></span> <span data-ttu-id="6eaed-321">Les unités de durée sont au format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-321">The duration units are in the current time format.</span></span> <span data-ttu-id="6eaed-322">Elle retourne zéro s’il n’y a pas d’espace disque réservé.</span><span class="sxs-lookup"><span data-stu-id="6eaed-322">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="6eaed-323">La taille retournée est approximative, car l’espace disque précis pour les données compressées ne peut pas, en général, être prédit tant que les données n’ont pas été compressées.</span><span class="sxs-lookup"><span data-stu-id="6eaed-323">The size returned is approximate since the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>\_État DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI\_DGV\_STATUS\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-325">Le membre **dwReturn** retourne le code de temps SMPTE associé à la position actuelle dans l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="6eaed-325">The **dwReturn** member returns the SMPTE time code associated with the current position in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>Vitesse d’état de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI\_DGV\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-327">Le membre **dwReturn** retourne la vitesse de lecture actuelle.</span><span class="sxs-lookup"><span data-stu-id="6eaed-327">The **dwReturn** member returns the current playback speed.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>\_État de DGV MCI \_ \_ toujours \_ en cours</span><span class="sxs-lookup"><span data-stu-id="6eaed-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI\_DGV\_STATUS\_STILL\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-329">Le membre **dwReturn** retourne le format de fichier actuel pour la commande de [ \_ capture MCI](mci-capture.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-329">The **dwReturn** member returns the current file format for the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>\_teinte de l’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI\_DGV\_STATUS\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-331">Le membre **dwReturn** retourne le niveau de teinte vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-331">The **dwReturn** member returns the current video tint level.</span></span> <span data-ttu-id="6eaed-332">Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.</span><span class="sxs-lookup"><span data-stu-id="6eaed-332">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>\_État des \_ \_ aigus MCI DGV</span><span class="sxs-lookup"><span data-stu-id="6eaed-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI\_DGV\_STATUS\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-334">Le membre **dwReturn** retourne le niveau de aigu audio actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-334">The **dwReturn** member returns the current audio treble level.</span></span> <span data-ttu-id="6eaed-335">Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.</span><span class="sxs-lookup"><span data-stu-id="6eaed-335">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>\_État de DGV MCI \_ \_ non enregistré</span><span class="sxs-lookup"><span data-stu-id="6eaed-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>MCI\_DGV\_STATUS\_UNSAVED</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-337">Le **membre dwReturn** retourne la **valeur true** s’il y a des données enregistrées dans l’espace de travail qui peuvent être perdues suite à une [ \_ fermeture MCI](mci-close.md), une [ \_ charge MCI](mci-load.md), un [ \_ enregistrement MCI](mci-record.md), une [ \_ réservation MCI](mci-reserve.md), une [ \_ coupure](mci-cut.md)MCI, une [ \_ suppression MCI](mci-delete.md)ou une commande de [ \_ Collage MCI](mci-paste.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-337">The **dwReturn** member returns **TRUE** if there is recorded data in the workspace that might be lost as a result of a [MCI\_CLOSE](mci-close.md), [MCI\_LOAD](mci-load.md), [MCI\_RECORD](mci-record.md), [MCI\_RESERVE](mci-reserve.md), [MCI\_CUT](mci-cut.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="6eaed-338">Dans le cas contraire, le membre retourne la **valeur false** .</span><span class="sxs-lookup"><span data-stu-id="6eaed-338">The member returns **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>\_vidéo d' \_ État MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>MCI\_DGV\_STATUS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-340">Le membre **dwReturn** retourne MCI \_ si la vidéo est activée ou MCI \_ si elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-340">The **dwReturn** member returns MCI\_ON if video is enabled or MCI\_OFF if it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>\_ \_ enregistrement vidéo d’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI\_DGV\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-342">Le membre **dwReturn** retourne \_ la valeur MCI on ou MCI, en \_ reflétant l’état défini par l' \_ \_ indicateur d’enregistrement MCI DGV SETVIDEO \_ de la commande [MCI \_ SETVIDEO](mci-setvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-342">The **dwReturn** member returns MCI\_ON or MCI\_OFF, reflecting the state set by the MCI\_DGV\_SETVIDEO\_RECORD flag of the [MCI\_SETVIDEO](mci-setvideo.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>\_ \_ source vidéo d’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI\_DGV\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-344">Le membre **dwReturn** retourne une constante indiquant le type de source vidéo défini par l' \_ indicateur de source MCI DGV \_ SETVIDEO \_ de la commande **MCI \_ SETVIDEO** .</span><span class="sxs-lookup"><span data-stu-id="6eaed-344">The **dwReturn** member returns a constant indicating the type of video source set by the MCI\_DGV\_SETVIDEO\_SOURCE flag of the **MCI\_SETVIDEO** command.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>\_vidéo d’État MCI DGV \_ \_ \_ src \_ num</span><span class="sxs-lookup"><span data-stu-id="6eaed-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI\_DGV\_STATUS\_VIDEO\_SRC\_NUM</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-346">Le membre **dwReturn** retourne le nombre dans son type de source d’entrée vidéo actuellement actif.</span><span class="sxs-lookup"><span data-stu-id="6eaed-346">The **dwReturn** member returns the number within its type of the video-input source currently active.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>\_ \_ flux vidéo d’État MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI\_DGV\_STATUS\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-348">Le membre **dwReturn** retourne le numéro de flux vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-348">The **dwReturn** member returns the current video-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>\_volume d' \_ État MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI\_DGV\_STATUS\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-350">Le membre **dwReturn** retourne la moyenne du volume aux haut-parleurs gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="6eaed-350">The **dwReturn** member returns the average of the volume to the left and right speakers.</span></span> <span data-ttu-id="6eaed-351">Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.</span><span class="sxs-lookup"><span data-stu-id="6eaed-351">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>\_fenêtre d' \_ État MCI DGV \_ \_ visible</span><span class="sxs-lookup"><span data-stu-id="6eaed-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>MCI\_DGV\_STATUS\_WINDOW\_VISIBLE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-353">Le membre **dwReturn** retourne la **valeur true** si la fenêtre n’est pas masquée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-353">The **dwReturn** member returns **TRUE** if the window is not hidden.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>\_fenêtre d' \_ État MCI DGV \_ \_ réduite</span><span class="sxs-lookup"><span data-stu-id="6eaed-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>MCI\_DGV\_STATUS\_WINDOW\_MINIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-355">Le membre **dwReturn** retourne la **valeur true** si la fenêtre est réduite.</span><span class="sxs-lookup"><span data-stu-id="6eaed-355">The **dwReturn** member returns **TRUE** if the window is minimized.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>\_fenêtre d’État MCI DGV \_ \_ \_ agrandie</span><span class="sxs-lookup"><span data-stu-id="6eaed-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>MCI\_DGV\_STATUS\_WINDOW\_MAXIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-357">Le membre **dwReturn** retourne la **valeur true** si la fenêtre est agrandie.</span><span class="sxs-lookup"><span data-stu-id="6eaed-357">The **dwReturn** member returns **TRUE** if the window is maximized.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent</span><span class="sxs-lookup"><span data-stu-id="6eaed-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-359">Le membre **dwReturn** retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="6eaed-359">The **dwReturn** member returns **TRUE**.</span></span>

</dd> </dl>

<span data-ttu-id="6eaed-360">Pour les périphériques vidéo numériques, le paramètre *lpStatus* pointe vers une structure de paramètres d' [**\_ \_ état \_ DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-360">For digital-video devices, the *lpStatus* parameter points to an [**MCI\_DGV\_STATUS\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) structure.</span></span>

<span data-ttu-id="6eaed-361">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Sequencer** .</span><span class="sxs-lookup"><span data-stu-id="6eaed-361">The following additional flags are used with the **sequencer** device type.</span></span> <span data-ttu-id="6eaed-362">Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6eaed-362">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="6eaed-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>\_ \_ DIVTYPE état de l’MCI Seq \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI\_SEQ\_STATUS\_DIVTYPE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-364">Le membre **dwReturn** est défini sur l’une des valeurs suivantes indiquant le type de division actuel d’une séquence :</span><span class="sxs-lookup"><span data-stu-id="6eaed-364">The **dwReturn** member is set to one of the following values indicating the current division type of a sequence:</span></span>

-   <span data-ttu-id="6eaed-365">MCI \_ Seq \_ div \_ PPQN</span><span class="sxs-lookup"><span data-stu-id="6eaed-365">MCI\_SEQ\_DIV\_PPQN</span></span>
-   <span data-ttu-id="6eaed-366">MCI \_ Seq \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="6eaed-366">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>
-   <span data-ttu-id="6eaed-367">MCI \_ Seq \_ div \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="6eaed-367">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>
-   <span data-ttu-id="6eaed-368">MCI \_ Seq \_ div \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="6eaed-368">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>
-   <span data-ttu-id="6eaed-369">MCI \_ Seq \_ div \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="6eaed-369">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>\_contrôleur d' \_ État MCI Seq \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI\_SEQ\_STATUS\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-371">Le membre **dwReturn** est défini sur le type de synchronisation utilisé pour l’opération maître.</span><span class="sxs-lookup"><span data-stu-id="6eaed-371">The **dwReturn** member is set to the synchronization type used for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>décalage de l' \_ État MCI Seq \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>MCI\_SEQ\_STATUS\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-373">Le membre **dwReturn** est défini sur le décalage SMPTE actuel d’une séquence.</span><span class="sxs-lookup"><span data-stu-id="6eaed-373">The **dwReturn** member is set to the current SMPTE offset of a sequence.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>\_port d' \_ État MCI Seq \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI\_SEQ\_STATUS\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-375">Le membre **dwReturn** est défini sur l’identificateur d’appareil MIDI pour le port actuel utilisé par la séquence.</span><span class="sxs-lookup"><span data-stu-id="6eaed-375">The **dwReturn** member is set to the MIDI device identifier for the current port used by the sequence.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>\_État esclave de l’État MCI Seq \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI\_SEQ\_STATUS\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-377">Le membre **dwReturn** est défini sur le type de synchronisation utilisé pour l’opération subordonnée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-377">The **dwReturn** member is set to the synchronization type used for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>TEMPO d’État du MCI \_ Seq \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI\_SEQ\_STATUS\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-379">Le membre **dwReturn** est défini sur le tempo actuel d’une séquence MIDI en temps par minute pour les fichiers PPQN, ou les images par seconde pour les fichiers SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eaed-379">The **dwReturn** member is set to the current tempo of a MIDI sequence in beats per minute for PPQN files, or frames per second for SMPTE files.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent</span><span class="sxs-lookup"><span data-stu-id="6eaed-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-381">Le membre **dwReturn** a la valeur **true** si le média est inséré dans l’appareil ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-381">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="6eaed-382">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** .</span><span class="sxs-lookup"><span data-stu-id="6eaed-382">The following additional flags are used with the **vcr** device type.</span></span> <span data-ttu-id="6eaed-383">Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6eaed-383">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="6eaed-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent</span><span class="sxs-lookup"><span data-stu-id="6eaed-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-385">Le membre **dwReturn** a la valeur **true** si le média est inséré dans l’appareil ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-385">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>\_enregistrement d' \_ État de magnétoscope \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI\_VCR\_STATUS\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-387">Le membre **dwReturn** a la valeur **true** si le mode assembler est activé ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-387">The **dwReturn** member is set to **TRUE** if assemble mode is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>\_ \_ moniteur audio d’état de magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-389">Le membre **dwReturn** est défini sur une constante, indiquant le type de moniteur audio actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6eaed-389">The **dwReturn** member is set to a constant, indicating the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>\_numéro du \_ \_ moniteur audio \_ \_ de l’état du magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-391">Le membre **dwReturn** est défini sur le numéro du type de moniteur audio actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6eaed-391">The **dwReturn** member is set to the number of the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>\_ \_ enregistrement audio d’État magnétoscope \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI\_VCR\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-393">Le membre **dwReturn** a la valeur **true** si l’audio est enregistré lorsque la commande d’enregistrement suivante est donnée ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-393">The **dwReturn** member is set to **TRUE** if audio will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="6eaed-394">Si vous spécifiez MCI \_ Track dans le paramètre *dwFlags* de cette commande, **dwTrack** contient le suivi auquel s’applique cette requête.</span><span class="sxs-lookup"><span data-stu-id="6eaed-394">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>\_ \_ source audio d’État MCI VCR \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-396">Le membre **dwReturn** est défini sur une constante, indiquant le type de source audio en cours.</span><span class="sxs-lookup"><span data-stu-id="6eaed-396">The **dwReturn** member is set to a constant, indicating the current audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>\_numéro de \_ \_ source audio \_ \_ de l’état du magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-398">Le membre **dwReturn** est défini sur le numéro du type de source audio actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6eaed-398">The **dwReturn** member is set to the number of the currently selected audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>horloge de l' \_ État MCI VCR \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI\_VCR\_STATUS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-400">Le membre **dwReturn** est défini sur la valeur d’horloge actuelle, dans le nombre total d’incréments d’horloge.</span><span class="sxs-lookup"><span data-stu-id="6eaed-400">The **dwReturn** member is set to the current clock value, in total clock increments.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>ID d’horloge de l' \_ État de magnétoscope MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI\_VCR\_STATUS\_CLOCK\_ID</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-402">Le membre **dwReturn** est défini sur un nombre qui décrit de façon unique l’horloge en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6eaed-402">The **dwReturn** member is set to a number which uniquely describes the clock in use.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>FORMAT du compteur de l' \_ État du magnétoscope MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI\_VCR\_STATUS\_COUNTER\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-404">Le membre **dwReturn** est défini sur une constante décrivant le format de compteur actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-404">The **dwReturn** member is set to a constant describing the current counter format.</span></span> <span data-ttu-id="6eaed-405">Pour plus d’informations, consultez l' \_ \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-405">For more information, see the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>\_résolution de \_ compteur d’état de magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>MCI\_VCR\_STATUS\_COUNTER\_RESOLUTION</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-407">Le membre **dwReturn** est défini sur une constante décrivant la résolution du compteur et est l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6eaed-407">The **dwReturn** member is set to a constant describing the resolution of the counter, and is one of the following values:</span></span>

-   <span data-ttu-id="6eaed-408">\_ \_ \_ Images de compteur de magnétoscope MCI : le \_ compteur a une résolution de frames.</span><span class="sxs-lookup"><span data-stu-id="6eaed-408">MCI\_VCR\_COUNTER\_RES\_FRAMES: Counter has resolution of frames.</span></span>
-   <span data-ttu-id="6eaed-409">\_Compteur de magnétoscopes MCI \_ \_ res \_ secondes : le compteur a une résolution de secondes.</span><span class="sxs-lookup"><span data-stu-id="6eaed-409">MCI\_VCR\_COUNTER\_RES\_SECONDS: Counter has resolution of seconds.</span></span>
-   <span data-ttu-id="6eaed-410">\_Valeur du \_ compteur d’État du magnétoscope MCI \_ \_ : le membre **dwReturn** est défini sur le compteur en cours de lecture, dans le format au moment du compteur actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-410">MCI\_VCR\_STATUS\_COUNTER\_VALUE: The **dwReturn** member is set to the current counter reading, in the current counter-time format.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>\_fréquence des \_ \_ trames d’état de magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI\_VCR\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-412">Le membre **dwReturn** est défini sur la fréquence d’images Native actuelle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6eaed-412">The **dwReturn** member is set to the current native frame rate of the device.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>\_index d' \_ état \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI\_VCR\_STATUS\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-414">Le membre **dwReturn** est défini sur une constante, décrivant le contenu actuel de l’affichage à l’écran et est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6eaed-414">The **dwReturn** member is set to a constant, describing the current contents of the on-screen display, and is one of the following:</span></span>

-   <span data-ttu-id="6eaed-415">\_compteur d' \_ index \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-415">MCI\_VCR\_INDEX\_COUNTER</span></span>
-   <span data-ttu-id="6eaed-416">\_Date d' \_ index \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-416">MCI\_VCR\_INDEX\_DATE</span></span>
-   <span data-ttu-id="6eaed-417">\_heure d' \_ index \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-417">MCI\_VCR\_INDEX\_TIME</span></span>
-   <span data-ttu-id="6eaed-418">\_code temporel de l’index magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-418">MCI\_VCR\_INDEX\_TIMECODE</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_ \_ \_ index d’état de magnétoscope MCI \_ activé</span><span class="sxs-lookup"><span data-stu-id="6eaed-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI\_VCR\_STATUS\_INDEX\_ON</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-420">Le membre **dwReturn** a la valeur **true** si l’affichage à l’écran est activé ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-420">The **dwReturn** member is set to **TRUE** if the on-screen display is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>\_type de \_ média d’État magnétoscope \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI\_VCR\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-422">Le membre **dwReturn** est défini sur l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6eaed-422">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="6eaed-423">\_Média magnétoscope \_ MCI \_ 8 mm</span><span class="sxs-lookup"><span data-stu-id="6eaed-423">MCI\_VCR\_MEDIA\_8MM</span></span>
-   <span data-ttu-id="6eaed-424">\_Hi8 de \_ média \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-424">MCI\_VCR\_MEDIA\_HI8</span></span>
-   <span data-ttu-id="6eaed-425">MCI \_ magnétoscope \_ - \_ VHS</span><span class="sxs-lookup"><span data-stu-id="6eaed-425">MCI\_VCR\_MEDIA\_VHS</span></span>
-   <span data-ttu-id="6eaed-426">\_SVHS de \_ média \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-426">MCI\_VCR\_MEDIA\_SVHS</span></span>
-   <span data-ttu-id="6eaed-427">MCI \_ VCR \_ Media \_ bêta</span><span class="sxs-lookup"><span data-stu-id="6eaed-427">MCI\_VCR\_MEDIA\_BETA</span></span>
-   <span data-ttu-id="6eaed-428">\_EDBETA de \_ média \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-428">MCI\_VCR\_MEDIA\_EDBETA</span></span>
-   <span data-ttu-id="6eaed-429">\_média magnétoscope \_ MCI \_ autre</span><span class="sxs-lookup"><span data-stu-id="6eaed-429">MCI\_VCR\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>\_numéro d' \_ État du magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI\_VCR\_STATUS\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-431">Le membre **dwNumber** est défini sur le numéro de tuner logique lorsque vous utilisez cet indicateur avec l' \_ indicateur de \_ canal tuner d’état de magnétoscope MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6eaed-431">The **dwNumber** member is set to the logical-tuner number when you use this flag with the MCI\_VCR\_STATUS\_TUNER\_CHANNEL flag.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_ \_ État du magnétoscope \_ MCI \_ nombre \_ de \_ pistes audio</span><span class="sxs-lookup"><span data-stu-id="6eaed-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_AUDIO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-433">Le membre **dwReturn** est défini sur le nombre de pistes audio qui peuvent être sélectionnées de manière indépendante.</span><span class="sxs-lookup"><span data-stu-id="6eaed-433">The **dwReturn** member is set to the number of audio tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_ \_ État du magnétoscope \_ MCI \_ nombre \_ de \_ pistes vidéo</span><span class="sxs-lookup"><span data-stu-id="6eaed-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_VIDEO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-435">Le membre **dwReturn** est défini sur le nombre de pistes vidéo qui peuvent être sélectionnées de manière indépendante.</span><span class="sxs-lookup"><span data-stu-id="6eaed-435">The **dwReturn** member is set to the number of video tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>délai de pause de l' \_ État de magnétoscope MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI\_VCR\_STATUS\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-437">Le membre **dwReturn** est défini sur la durée maximale, en millisecondes, d’une commande pause.</span><span class="sxs-lookup"><span data-stu-id="6eaed-437">The **dwReturn** member is set to the maximum duration, in milliseconds, of a pause command.</span></span> <span data-ttu-id="6eaed-438">La valeur de retour de zéro indique qu’aucun délai d’attente n’a lieu.</span><span class="sxs-lookup"><span data-stu-id="6eaed-438">The return value of zero indicates that no time-out will occur.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>FORMAT de lecture de l' \_ État MCI VCR \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI\_VCR\_STATUS\_PLAY\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-440">Le membre **dwReturn** est défini sur l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6eaed-440">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="6eaed-441">\_format VCR \_ MCI \_ EP</span><span class="sxs-lookup"><span data-stu-id="6eaed-441">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="6eaed-442">\_format de magnétoscope MCI \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="6eaed-442">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="6eaed-443">\_format VCR \_ MCI \_ autre</span><span class="sxs-lookup"><span data-stu-id="6eaed-443">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="6eaed-444">MCI \_ magnétoscope \_ au format \_ SP</span><span class="sxs-lookup"><span data-stu-id="6eaed-444">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>\_ \_ \_ durée Postroll de l’état de magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>MCI\_VCR\_STATUS\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-446">Le membre **dwReturn** est défini sur la longueur de la bande vidéo qui est lue après l’emplacement où il a été arrêté, dans le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-446">The **dwReturn** member is set to the length of the videotape that will play after the spot at which it was stopped, in the current time format.</span></span> <span data-ttu-id="6eaed-447">Cela est nécessaire pour freiner le transport de bandes VCR à partir d’une commande Stop ou pause.</span><span class="sxs-lookup"><span data-stu-id="6eaed-447">This is needed to brake the VCR tape transport from a stop or pause command.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>\_ \_ État de l' \_ alimentation MCI magnétoscope \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI\_VCR\_STATUS\_POWER\_ON</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-449">Le membre **dwReturn** a la valeur **true** si l’alimentation est activée ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-449">The **dwReturn** member is set to **TRUE** if the power is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>\_durée du \_ préroll d’État du magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>MCI\_VCR\_STATUS\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-451">Le membre **dwReturn** est défini sur la longueur de la bande vidéo qui doit être lue avant l’emplacement où il a été démarré, dans le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-451">The **dwReturn** member is set to the length of the videotape that will play before the spot at which it was started, in the current time format.</span></span> <span data-ttu-id="6eaed-452">Cela est nécessaire pour stabiliser la sortie du magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="6eaed-452">This is needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>\_format d' \_ enregistrement d’État magnétoscope \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI\_VCR\_STATUS\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-454">Le membre **dwReturn** est défini sur l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6eaed-454">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="6eaed-455">\_format VCR \_ MCI \_ EP</span><span class="sxs-lookup"><span data-stu-id="6eaed-455">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="6eaed-456">\_format de magnétoscope MCI \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="6eaed-456">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="6eaed-457">\_format VCR \_ MCI \_ autre</span><span class="sxs-lookup"><span data-stu-id="6eaed-457">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="6eaed-458">MCI \_ magnétoscope \_ au format \_ SP</span><span class="sxs-lookup"><span data-stu-id="6eaed-458">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>\_Vitesse d' \_ État du magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI\_VCR\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-460">Le membre **dwReturn** est défini sur la vitesse actuelle.</span><span class="sxs-lookup"><span data-stu-id="6eaed-460">The **dwReturn** member is set to the current speed.</span></span> <span data-ttu-id="6eaed-461">Pour plus d’informations, consultez l' \_ \_ indicateur de vitesse du jeu de magnétoscopes MCI \_ de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-461">For more information, see the MCI\_VCR\_SET\_SPEED flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MODE de temps de l' \_ État des magnétoscopes MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI\_VCR\_STATUS\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-463">Le membre **dwReturn** est défini sur l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6eaed-463">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="6eaed-464">\_compteur de \_ temps MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-464">MCI\_VCR\_TIME\_COUNTER</span></span>
-   <span data-ttu-id="6eaed-465">détection de l' \_ heure du magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-465">MCI\_VCR\_TIME\_DETECT</span></span>
-   <span data-ttu-id="6eaed-466">\_code temporel de l’heure MCI magnétoscope \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-466">MCI\_VCR\_TIME\_TIMECODE</span></span>

<span data-ttu-id="6eaed-467">Pour plus d’informations, consultez l' \_ indicateur MCI magnétoscope \_ Set \_ Time \_ mode de la commande [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-467">For more information, see the MCI\_VCR\_SET\_TIME\_MODE flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>TYPE de temps de l' \_ État du magnétoscope MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI\_VCR\_STATUS\_TIME\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-469">Le membre **dwReturn** est défini sur une constante décrivant le type d’heure actuel en cours d’utilisation (utilisé par [Play](play.md), [Record](record.md), [Seek](seek.md), etc.), et est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6eaed-469">The **dwReturn** member is set to a constant describing the current time type in use (used by [play](play.md), [record](record.md), [seek](seek.md), and so on), and is one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_compteur de \_ temps MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-471">Compteur en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6eaed-471">Counter is in use.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_code temporel de l’heure MCI magnétoscope \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-473">Le code temporel est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6eaed-473">Timecode is in use.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>\_ \_ code temporel MCI État du magnétoscope \_ \_ présent</span><span class="sxs-lookup"><span data-stu-id="6eaed-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>MCI\_VCR\_STATUS\_TIMECODE\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-475">Le membre **dwReturn** a la valeur **true** si le code temporel est présent à la position actuelle dans le contenu ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-475">The **dwReturn** member is set to **TRUE** if timecode is present at the current position in the content; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>\_enregistrement du \_ \_ code temporel \_ MCI de l’État magnétoscope</span><span class="sxs-lookup"><span data-stu-id="6eaed-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI\_VCR\_STATUS\_TIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-477">Le membre **dwReturn** a la valeur **true** si le code temporel sera enregistré lorsque la commande d’enregistrement suivante est donnée ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-477">The **dwReturn** member is set to **TRUE** if the timecode will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>TYPE de code de l' \_ État magnétoscope MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI\_VCR\_STATUS\_TIMECODE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-479">Le membre **dwReturn** est défini sur une constante, décrivant le type de code temporel qui est directement pris en charge par l’appareil, et est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6eaed-479">The **dwReturn** member is set to a constant, describing the type of timecode that is directly supported by the device, and is one of the following:</span></span>

-   <span data-ttu-id="6eaed-480">\_ \_ Type de code temporel de magnétoscope MCI \_ \_ aucun : cet appareil n’utilise pas de code temporel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-480">MCI\_VCR\_TIMECODE\_TYPE\_NONE: This device does not use a timecode.</span></span>
-   <span data-ttu-id="6eaed-481">\_Type de \_ code temporel MCI magnétoscope \_ \_ autre : cet appareil utilise un code temporel non spécifié.</span><span class="sxs-lookup"><span data-stu-id="6eaed-481">MCI\_VCR\_TIMECODE\_TYPE\_OTHER: This device uses an unspecified timecode.</span></span>
-   <span data-ttu-id="6eaed-482">\_Type de \_ code temporel MCI magnétoscope \_ \_ SMPTE : cet appareil utilise le code temporel SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eaed-482">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE: This device uses SMPTE timecode.</span></span>
-   <span data-ttu-id="6eaed-483">\_ \_ Suppression SMPTE du type de code temporel de magnétoscope MCI \_ \_ \_ : cet appareil utilise le code temporel de suppression SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eaed-483">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE\_DROP: This device uses SMPTE drop timecode.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>\_canal du \_ tuner d’État MCI VCR \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI\_VCR\_STATUS\_TUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-485">Le membre **dwReturn** est défini sur le numéro de canal actuel.</span><span class="sxs-lookup"><span data-stu-id="6eaed-485">The **dwReturn** member is set to the current channel number.</span></span> <span data-ttu-id="6eaed-486">Si vous spécifiez \_ le numéro d’État du magnétoscope MCI \_ \_ dans le paramètre *dwFlags* de cette commande, **dwNumber** contient le numéro de tuner logique auquel cette commande s’applique.</span><span class="sxs-lookup"><span data-stu-id="6eaed-486">If you specify MCI\_VCR\_STATUS\_NUMBER in the *dwFlags* parameter of this command, **dwNumber** contains the logical-tuner number this command applies to.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>\_ \_ moniteur vidéo d’État magnétoscope \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-488">Le membre **dwReturn** est défini sur une constante, indiquant le type de moniteur vidéo actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6eaed-488">The **dwReturn** member is set to a constant, indicating the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_numéro de \_ \_ moniteur vidéo \_ d’État magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-490">Le membre **dwReturn** est défini sur le numéro du type de moniteur vidéo actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6eaed-490">The **dwReturn** member is set to the number of the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_ \_ enregistrement vidéo d’État magnétoscope \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>MCI\_VCR\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-492">Le membre **dwReturn** a la valeur **true** si la vidéo est enregistrée lorsque la commande d’enregistrement suivante est donnée ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-492">The **dwReturn** member is set to **TRUE** if video will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="6eaed-493">Si vous spécifiez MCI \_ Track dans le paramètre *dwFlags* de cette commande, **dwTrack** contient le suivi auquel s’applique cette requête.</span><span class="sxs-lookup"><span data-stu-id="6eaed-493">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>\_ \_ source vidéo d’état de magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-495">Le membre **dwReturn** est défini sur une constante indiquant le type de source vidéo actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6eaed-495">The **dwReturn** member is set to a constant indicating the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>\_numéro de \_ \_ source vidéo \_ \_ de l’État MCI VCR</span><span class="sxs-lookup"><span data-stu-id="6eaed-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-497">Le membre **dwReturn** est défini sur le numéro du type de source vidéo actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6eaed-497">The **dwReturn** member is set to the number of the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>\_État du magnétoscope MCI \_ \_ protégé en écriture \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI\_VCR\_STATUS\_WRITE\_PROTECTED</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-499">Le membre **dwReturn** a la valeur **true** si le média est protégé en écriture ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-499">The **dwReturn** member is set to **TRUE** if the media is write-protected; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="6eaed-500">Pour les périphériques VCR, le paramètre *lpStatus* pointe vers une structure d' [**\_ \_ état \_ de magnétoscope MCI**](mci-vcr-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-500">For VCR devices, the *lpStatus* parameter points to an [**MCI\_VCR\_STATUS\_PARMS**](mci-vcr-status-parms.md) structure.</span></span>

<span data-ttu-id="6eaed-501">L’utilisation \_ de l' \_ indicateur de longueur d’État MCI pour déterminer la longueur du média retourne toujours 2 heures pour les périphériques VCR, sauf si la longueur a été explicitement modifiée à l’aide de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-501">Using the MCI\_STATUS\_LENGTH flag to determine the length of the media always returns 2 hours for VCR devices, unless the length has been explicitly changed using the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="6eaed-502">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique de **superposition** .</span><span class="sxs-lookup"><span data-stu-id="6eaed-502">The following additional flags are used with the **overlay** device type.</span></span> <span data-ttu-id="6eaed-503">Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6eaed-503">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="6eaed-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>\_HWND OVLY \_ état \_ HWND</span><span class="sxs-lookup"><span data-stu-id="6eaed-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI\_OVLY\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-505">Le membre **dwReturn** est défini sur le handle de la fenêtre associée à l’appareil de superposition vidéo.</span><span class="sxs-lookup"><span data-stu-id="6eaed-505">The **dwReturn** member is set to the handle of the window associated with the video-overlay device.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>\_extension d' \_ État MCI OVLY \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI\_OVLY\_STATUS\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-507">Le membre **dwReturn** a la valeur **true** si l’étirement est activé ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-507">The **dwReturn** member is set to **TRUE** if stretching is enabled; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent</span><span class="sxs-lookup"><span data-stu-id="6eaed-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-509">Le membre **dwReturn** a la valeur **true** si le média est inséré dans l’appareil ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-509">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="6eaed-510">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **videodisc** .</span><span class="sxs-lookup"><span data-stu-id="6eaed-510">The following additional flags are used with the **videodisc** device type.</span></span> <span data-ttu-id="6eaed-511">Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6eaed-511">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="6eaed-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent</span><span class="sxs-lookup"><span data-stu-id="6eaed-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-513">Le membre **dwReturn** a la valeur **true** si le média est inséré dans l’appareil ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-513">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_mode d’État MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-515">Le membre **dwReturn** est défini sur le mode actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6eaed-515">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="6eaed-516">Les appareils Videodisc peuvent retourner la \_ \_ constante de parking en mode VD MCI \_ , en plus des constantes que tout appareil peut retourner, comme indiqué dans le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6eaed-516">Videodisc devices can return the MCI\_VD\_MODE\_PARK constant, in addition to the constants any device can return, as documented with the *dwFlags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>\_taille du \_ disque d’état \_ \_ MCI MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI\_VD\_STATUS\_DISC\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-518">Le membre **dwReturn** est défini sur la taille du disque chargé, en pouces (8 ou 12).</span><span class="sxs-lookup"><span data-stu-id="6eaed-518">The **dwReturn** member is set to the size of the loaded disc in inches (8 or 12).</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>État du MCI MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI\_VD\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-520">Le membre **dwReturn** a la valeur **true** en cas de progression ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6eaed-520">The **dwReturn** member is set to **TRUE** if playing forward; it is set to **FALSE** otherwise.</span></span>

<span data-ttu-id="6eaed-521">L’appareil MCI videodisc ne prend pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eaed-521">The MCI videodisc device does not support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>\_type de \_ média d’État MCI VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI\_VD\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-523">Le membre **dwReturn** est défini sur le type de média du média inséré.</span><span class="sxs-lookup"><span data-stu-id="6eaed-523">The **dwReturn** member is set to the media type of the inserted media.</span></span> <span data-ttu-id="6eaed-524">Les types de média suivants peuvent être retournés :</span><span class="sxs-lookup"><span data-stu-id="6eaed-524">The following media types can be returned:</span></span>

<span data-ttu-id="6eaed-525">\_ \_ CAV multimédia VD \_ MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-525">MCI\_VD\_MEDIA\_CAV</span></span>

<span data-ttu-id="6eaed-526">\_ \_ CLV multimédia VD \_ MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-526">MCI\_VD\_MEDIA\_CLV</span></span>

<span data-ttu-id="6eaed-527">\_média MCI \_ VD \_ autre</span><span class="sxs-lookup"><span data-stu-id="6eaed-527">MCI\_VD\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>\_ \_ côté État MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="6eaed-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI\_VD\_STATUS\_SIDE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-529">Le membre **dwReturn** a la valeur 1 ou 2 pour indiquer le côté du disque chargé.</span><span class="sxs-lookup"><span data-stu-id="6eaed-529">The **dwReturn** member is set to 1 or 2 to indicate which side of the disc is loaded.</span></span> <span data-ttu-id="6eaed-530">Tous les appareils videodisc ne prennent pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eaed-530">Not all videodisc devices support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>Vitesse de l' \_ État MCI VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI\_VD\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-532">Le membre **dwReturn** est défini sur la vitesse de lecture en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="6eaed-532">The **dwReturn** member is set to the play speed in frames per second.</span></span> <span data-ttu-id="6eaed-533">MCIPIONR. Le pilote de périphérique DRV retourne une \_ fonction non prise en charge MCIERR \_ .</span><span class="sxs-lookup"><span data-stu-id="6eaed-533">The MCIPIONR.DRV device driver returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> </dl>

<span data-ttu-id="6eaed-534">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="6eaed-534">The following additional flags are used with the **waveaudio** device type.</span></span> <span data-ttu-id="6eaed-535">Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6eaed-535">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="6eaed-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>\_FORMATTAG Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI\_WAVE\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-537">Le membre **dwReturn** est défini sur la balise de format actuelle utilisée pour la diffusion, l’enregistrement et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eaed-537">The **dwReturn** member is set to the current format tag used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrée MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-539">Le membre **dwReturn** est défini sur l’appareil d’entrée Wave utilisé pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eaed-539">The **dwReturn** member is set to the wave input device used for recording.</span></span> <span data-ttu-id="6eaed-540">Si aucun appareil n’est en cours d’utilisation et qu’aucun appareil n’a été défini explicitement, l’erreur renvoyée est MCIERR \_ Wave \_ INPUTUNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="6eaed-540">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_INPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_sortie MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-542">Le membre **dwReturn** est défini sur le périphérique de sortie Wave utilisé pour la diffusion.</span><span class="sxs-lookup"><span data-stu-id="6eaed-542">The **dwReturn** member is set to the wave output device used for playing.</span></span> <span data-ttu-id="6eaed-543">Si aucun appareil n’est en cours d’utilisation et qu’aucun appareil n’a été défini explicitement, l’erreur renvoyée est MCIERR \_ Wave \_ OUTPUTUNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="6eaed-543">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_OUTPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>État de l' \_ onde MCI \_ \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="6eaed-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI\_WAVE\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-545">Le membre **dwReturn** est défini sur le nombre d’octets par seconde actuels utilisé pour la diffusion, l’enregistrement et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eaed-545">The **dwReturn** member is set to the current bytes per second used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>État de l' \_ onde MCI \_ \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="6eaed-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI\_WAVE\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-547">Le membre **dwReturn** est défini sur le nombre actuel de bits par échantillon utilisé pour la diffusion, l’enregistrement et l’enregistrement des données au format PCM.</span><span class="sxs-lookup"><span data-stu-id="6eaed-547">The **dwReturn** member is set to the current bits per sample used for playing, recording, and saving PCM formatted data.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>État de l' \_ onde MCI \_ \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="6eaed-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI\_WAVE\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-549">Le membre **dwReturn** est défini sur l’alignement de bloc actuel utilisé pour la diffusion, l’enregistrement et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eaed-549">The **dwReturn** member is set to the current block alignment used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>\_canaux d' \_ État des Wave MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI\_WAVE\_STATUS\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-551">Le membre **dwReturn** est défini sur le nombre de canaux actuel utilisé pour la diffusion, l’enregistrement et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eaed-551">The **dwReturn** member is set to the current channel count used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>niveau d’état de l' \_ onde MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI\_WAVE\_STATUS\_LEVEL</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-553">Le membre **dwReturn** est défini sur l’enregistrement actuel ou sur le niveau de lecture des données au format PCM.</span><span class="sxs-lookup"><span data-stu-id="6eaed-553">The **dwReturn** member is set to the current record or playback level of PCM formatted data.</span></span> <span data-ttu-id="6eaed-554">La valeur est retournée sous la forme d’une valeur de 8 ou 16 bits, en fonction de la taille de l’échantillon utilisée.</span><span class="sxs-lookup"><span data-stu-id="6eaed-554">The value is returned as an 8- or 16-bit value, depending on the sample size used.</span></span> <span data-ttu-id="6eaed-555">Le niveau de canal droit ou mono est retourné dans le mot de poids faible.</span><span class="sxs-lookup"><span data-stu-id="6eaed-555">The right or mono channel level is returned in the low-order word.</span></span> <span data-ttu-id="6eaed-556">Le niveau de canal gauche est retourné dans le mot de poids fort.</span><span class="sxs-lookup"><span data-stu-id="6eaed-556">The left channel level is returned in the high-order word.</span></span>

</dd> <dt>

<span data-ttu-id="6eaed-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>État de l' \_ onde MCI \_ \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="6eaed-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI\_WAVE\_STATUS\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="6eaed-558">Le membre **dwReturn** est défini sur les échantillons actuels par seconde utilisés pour la diffusion, l’enregistrement et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eaed-558">The **dwReturn** member is set to the current samples per second used for playing, recording, and saving.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6eaed-559">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6eaed-559">Requirements</span></span>



| <span data-ttu-id="6eaed-560">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6eaed-560">Requirement</span></span> | <span data-ttu-id="6eaed-561">Valeur</span><span class="sxs-lookup"><span data-stu-id="6eaed-561">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eaed-562">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eaed-562">Minimum supported client</span></span><br/> | <span data-ttu-id="6eaed-563">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eaed-563">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6eaed-564">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eaed-564">Minimum supported server</span></span><br/> | <span data-ttu-id="6eaed-565">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eaed-565">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6eaed-566">En-tête</span><span class="sxs-lookup"><span data-stu-id="6eaed-566">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eaed-567"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6eaed-567"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eaed-568">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6eaed-568">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eaed-569">MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-569">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6eaed-570">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-570">MCI Commands</span></span>](mci-commands.md)
</dt> <dt>

[<span data-ttu-id="6eaed-571">\_raccourcis MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-571">MCI\_CUT</span></span>](mci-cut.md)
</dt> <dt>

[<span data-ttu-id="6eaed-572">suppression de MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-572">MCI\_DELETE</span></span>](mci-delete.md)
</dt> <dt>

[<span data-ttu-id="6eaed-573">\_Collage MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-573">MCI\_PASTE</span></span>](mci-paste.md)
</dt> <dt>

[<span data-ttu-id="6eaed-574">\_réserve MCI</span><span class="sxs-lookup"><span data-stu-id="6eaed-574">MCI\_RESERVE</span></span>](mci-reserve.md)
</dt> <dt>

[<span data-ttu-id="6eaed-575">jeu de MCI \_</span><span class="sxs-lookup"><span data-stu-id="6eaed-575">MCI\_SET</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="6eaed-576">répétition</span><span class="sxs-lookup"><span data-stu-id="6eaed-576">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="6eaed-577">enregistrement</span><span class="sxs-lookup"><span data-stu-id="6eaed-577">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="6eaed-578">Demandez</span><span class="sxs-lookup"><span data-stu-id="6eaed-578">seek</span></span>](seek.md)
</dt> </dl>

 

