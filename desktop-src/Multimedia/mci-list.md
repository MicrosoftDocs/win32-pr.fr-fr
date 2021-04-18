---
title: Commande MCI_LIST (mmsystem. h)
description: La \_ commande MCI List obtient des informations sur le nombre et les types d’entrées disponibles pour l’appareil. Les appareils vidéo numériques et VCR reconnaissent cette commande.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- Commande MCI_LIST Windows multimédia
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509414"
---
# <a name="mci_list-command"></a><span data-ttu-id="ef60c-105">\_Commande de liste MCI</span><span class="sxs-lookup"><span data-stu-id="ef60c-105">MCI\_LIST command</span></span>

<span data-ttu-id="ef60c-106">La \_ commande MCI List obtient des informations sur le nombre et les types d’entrées disponibles pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ef60c-106">The MCI\_LIST command obtains information about the number and types of inputs available to the device.</span></span> <span data-ttu-id="ef60c-107">Les appareils vidéo numériques et VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="ef60c-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="ef60c-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="ef60c-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
);
```



## <a name="parameters"></a><span data-ttu-id="ef60c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef60c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef60c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ef60c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="ef60c-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ef60c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="ef60c-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="ef60c-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ef60c-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span><span class="sxs-lookup"><span data-stu-id="ef60c-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ef60c-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="ef60c-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="ef60c-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef60c-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ef60c-118">Return Value</span></span>

<span data-ttu-id="ef60c-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="ef60c-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef60c-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ef60c-120">Remarks</span></span>

<span data-ttu-id="ef60c-121">Les indicateurs supplémentaires suivants s’appliquent au type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="ef60c-121">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ef60c-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI \_ DGV \_ List \_ ALG</span><span class="sxs-lookup"><span data-stu-id="ef60c-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI\_DGV\_LIST\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-123">Le membre **lpstrAlgorithm** de la structure identifiée par *lpList* contient l’adresse d’une mémoire tampon contenant le nom d’un algorithme.</span><span class="sxs-lookup"><span data-stu-id="ef60c-123">The **lpstrAlgorithm** member of the structure identified by *lpList* contains an address of a buffer containing the name of an algorithm.</span></span> <span data-ttu-id="ef60c-124">Le nom est utilisé pour récupérer les types de descripteurs de qualité associés à un algorithme.</span><span class="sxs-lookup"><span data-stu-id="ef60c-124">The name is used to retrieve the types of quality descriptors associated with an algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>\_nombre de \_ listes MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI\_DGV\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-126">Retourne le nombre d’options du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="ef60c-126">Returns the number of options of the specified type.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>\_élément de \_ liste \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="ef60c-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI\_DGV\_LIST\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-128">Une constante indiquant que le type de liste est inclus dans le membre **dwItem** de la structure identifiée par *lpList*.</span><span class="sxs-lookup"><span data-stu-id="ef60c-128">A constant indicating the list type is included in the **dwItem** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="ef60c-129">Cet indicateur est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ef60c-129">This flag is required.</span></span> <span data-ttu-id="ef60c-130">Utilisez l’une des constantes suivantes pour indiquer le type de liste :</span><span class="sxs-lookup"><span data-stu-id="ef60c-130">Use one of the following constants to indicate the list type:</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ liste de l' \_ \_ ALG audio</span><span class="sxs-lookup"><span data-stu-id="ef60c-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI\_DGV\_LIST\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-132">La commande doit récupérer les noms des algorithmes audio.</span><span class="sxs-lookup"><span data-stu-id="ef60c-132">The command should retrieve names of audio algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>\_ \_ \_ qualité audio de la liste DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI\_DGV\_LIST\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-134">La commande doit récupérer des niveaux de qualité audio.</span><span class="sxs-lookup"><span data-stu-id="ef60c-134">The command should retrieve audio quality levels.</span></span> <span data-ttu-id="ef60c-135">Les niveaux renvoyés sont associés à l’algorithme référencé par le membre **lpstrAlgorithm** de la structure identifiée par *lpList*.</span><span class="sxs-lookup"><span data-stu-id="ef60c-135">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="ef60c-136">Si ce membre est spécifié à l’aide de la chaîne « Current », les qualités associées à l’algorithme actuel sont retournées.</span><span class="sxs-lookup"><span data-stu-id="ef60c-136">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>\_ \_ flux audio de liste DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI\_DGV\_LIST\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-138">La commande doit récupérer les noms des flux audio.</span><span class="sxs-lookup"><span data-stu-id="ef60c-138">The command should retrieve names of audio streams.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>\_liste de DGV MCI \_ \_ toujours \_ al</span><span class="sxs-lookup"><span data-stu-id="ef60c-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI\_DGV\_LIST\_STILL\_AL</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-140">La commande doit récupérer les noms des algorithmes toujours.</span><span class="sxs-lookup"><span data-stu-id="ef60c-140">The command should retrieve names of still algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>qualité de la \_ liste de DGV MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI\_DGV\_LIST\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-142">La commande doit récupérer des niveaux de qualité.</span><span class="sxs-lookup"><span data-stu-id="ef60c-142">The command should retrieve quality levels.</span></span> <span data-ttu-id="ef60c-143">Les niveaux renvoyés sont associés à l’algorithme référencé par le membre **lpstrAlgorithm** de la structure identifiée par *lpList*.</span><span class="sxs-lookup"><span data-stu-id="ef60c-143">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="ef60c-144">Si ce membre est spécifié à l’aide de la chaîne « Current », les qualités associées à l’algorithme actuel sont retournées.</span><span class="sxs-lookup"><span data-stu-id="ef60c-144">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>\_vidéo de \_ liste MCI DGV \_ \_ ALG</span><span class="sxs-lookup"><span data-stu-id="ef60c-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI\_DGV\_LIST\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-146">La commande doit récupérer les noms des algorithmes vidéo.</span><span class="sxs-lookup"><span data-stu-id="ef60c-146">The command should retrieve names of video algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>\_ \_ \_ qualité vidéo de la liste DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI\_DGV\_LIST\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-148">La commande doit récupérer des niveaux de qualité vidéo.</span><span class="sxs-lookup"><span data-stu-id="ef60c-148">The command should retrieve video quality levels.</span></span> <span data-ttu-id="ef60c-149">Les niveaux renvoyés sont associés à l’algorithme référencé par le membre **lpstrAlgorithm** de la structure identifiée par *lpList*.</span><span class="sxs-lookup"><span data-stu-id="ef60c-149">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="ef60c-150">Si ce membre est spécifié à l’aide de la chaîne « Current », les qualités associées à l’algorithme actuel sont retournées.</span><span class="sxs-lookup"><span data-stu-id="ef60c-150">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>\_ \_ \_ source vidéo de la liste DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI\_DGV\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-152">La commande doit retourner des informations sur les sources vidéo.</span><span class="sxs-lookup"><span data-stu-id="ef60c-152">The command should return information about the video sources.</span></span> <span data-ttu-id="ef60c-153">En cas d’utilisation \_ avec \_ \_ le nombre de listes MCI DGV, la commande retourne le nombre de sources vidéo.</span><span class="sxs-lookup"><span data-stu-id="ef60c-153">When used with MCI\_DGV\_LIST\_COUNT, the command returns the number of video sources.</span></span> <span data-ttu-id="ef60c-154">Lorsqu’elle est utilisée \_ avec \_ \_ le numéro de liste MCI DGV, la commande retourne le type d’une source vidéo.</span><span class="sxs-lookup"><span data-stu-id="ef60c-154">When used with MCI\_DGV\_LIST\_NUMBER, the command returns the type of a video source.</span></span> <span data-ttu-id="ef60c-155">MCI définit les types suivants :</span><span class="sxs-lookup"><span data-stu-id="ef60c-155">MCI defines the following types:</span></span>

-   <span data-ttu-id="ef60c-156">\_ \_ \_ Generic SETVIDEO SRC \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="ef60c-156">MCI\_DGV\_SETVIDEO\_SRC\_GENERIC</span></span>
-   <span data-ttu-id="ef60c-157">MCI \_ DGV \_ SETVIDEO \_ src \_ NTSC</span><span class="sxs-lookup"><span data-stu-id="ef60c-157">MCI\_DGV\_SETVIDEO\_SRC\_NTSC</span></span>
-   <span data-ttu-id="ef60c-158">\_PAL DGV \_ SETVIDEO \_ src \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-158">MCI\_DGV\_SETVIDEO\_SRC\_PAL</span></span>
-   <span data-ttu-id="ef60c-159">MCI \_ DGV \_ SETVIDEO \_ src \_ RGB</span><span class="sxs-lookup"><span data-stu-id="ef60c-159">MCI\_DGV\_SETVIDEO\_SRC\_RGB</span></span>
-   <span data-ttu-id="ef60c-160">MCI \_ DGV \_ SETVIDEO \_ src \_ SECAM</span><span class="sxs-lookup"><span data-stu-id="ef60c-160">MCI\_DGV\_SETVIDEO\_SRC\_SECAM</span></span>
-   <span data-ttu-id="ef60c-161">MCI \_ DGV \_ SETVIDEO \_ src \_ Svideo</span><span class="sxs-lookup"><span data-stu-id="ef60c-161">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO</span></span>

<span data-ttu-id="ef60c-162">Plusieurs sources de chaque type peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="ef60c-162">There might be more than one source of each type returned.</span></span> <span data-ttu-id="ef60c-163">Le type de source générique est utilisé lorsque plus un type de signal est autorisé pour ce connecteur.</span><span class="sxs-lookup"><span data-stu-id="ef60c-163">The generic source type is used when more then one type of signal is allowed for that connector.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>\_ \_ flux vidéo de liste DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI\_DGV\_LIST\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-165">La commande doit récupérer les noms des flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="ef60c-165">The command should retrieve names of video streams.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>\_numéro de \_ liste \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="ef60c-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI\_DGV\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-167">Un index est spécifié dans le membre **dwNumber** de la structure identifiée par *lpList*.</span><span class="sxs-lookup"><span data-stu-id="ef60c-167">An index is specified in the **dwNumber** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="ef60c-168">L’index doit être un entier compris entre 1 et la valeur retournée pour \_ l' \_ indicateur de nombre de listes MCI DGV \_ .</span><span class="sxs-lookup"><span data-stu-id="ef60c-168">The index must be an integer between 1 and the value returned for the MCI\_DGV\_LIST\_COUNT flag.</span></span>

</dd> </dl>

<span data-ttu-id="ef60c-169">Pour les périphériques vidéo numériques, *lpList* pointe vers une structure [**MCI \_ DGV \_ List \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="ef60c-169">For digital-video devices, *lpList* points to an [**MCI\_DGV\_LIST\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) structure.</span></span>

<span data-ttu-id="ef60c-170">Les indicateurs supplémentaires suivants s’appliquent au type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="ef60c-170">The following additional flags apply to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ef60c-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>\_ \_ source audio de liste de MAGNÉTOSCOPEs MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>MCI\_VCR\_LIST\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-172">Répertorier les entrées ou les types audio.</span><span class="sxs-lookup"><span data-stu-id="ef60c-172">List audio inputs or types.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>\_nombre de listes de magnétoscopes MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI\_VCR\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-174">Définit le membre **dwReturn** de la structure identifiée par *lpList* sur le nombre total d’entrées vidéo ou audio.</span><span class="sxs-lookup"><span data-stu-id="ef60c-174">Sets the **dwReturn** member of the structure identified by *lpList* to the total number of video or audio inputs.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>Numéro de la \_ liste magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI\_VCR\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-176">Définit le membre **dwReturn** de la structure identifiée par *lpList* sur le type de l’entrée vidéo ou audio spécifiée par le membre **dwNumber** .</span><span class="sxs-lookup"><span data-stu-id="ef60c-176">Sets the **dwReturn** member of the structure identified by *lpList* to the type of the video or audio input specified by the **dwNumber** member.</span></span>

</dd> <dt>

<span data-ttu-id="ef60c-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>\_ \_ source vidéo de liste de MAGNÉTOSCOPEs MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ef60c-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>MCI\_VCR\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="ef60c-178">Répertorier les entrées ou les types vidéo.</span><span class="sxs-lookup"><span data-stu-id="ef60c-178">List video inputs or types.</span></span>

</dd> </dl>

<span data-ttu-id="ef60c-179">Pour les périphériques VCR, *lpList* pointe vers une structure de [**\_ \_ liste \_ de magnétoscopes MCI**](mci-vcr-list-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ef60c-179">For VCR devices, *lpList* points to an [**MCI\_VCR\_LIST\_PARMS**](mci-vcr-list-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef60c-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef60c-180">Requirements</span></span>



| <span data-ttu-id="ef60c-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef60c-181">Requirement</span></span> | <span data-ttu-id="ef60c-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef60c-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef60c-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef60c-183">Minimum supported client</span></span><br/> | <span data-ttu-id="ef60c-184">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef60c-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ef60c-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef60c-185">Minimum supported server</span></span><br/> | <span data-ttu-id="ef60c-186">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef60c-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ef60c-187">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef60c-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef60c-188"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef60c-188"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef60c-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef60c-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef60c-190">MCI</span><span class="sxs-lookup"><span data-stu-id="ef60c-190">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ef60c-191">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="ef60c-191">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

