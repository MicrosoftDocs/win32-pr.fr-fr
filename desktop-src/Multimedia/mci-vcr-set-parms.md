---
title: Structure de MCI_VCR_SET_PARMS (VCR. h)
description: La structure de l' \_ ensemble de paramètres MCI magnétoscope \_ contient des \_ paramètres pour la \_ commande MCI Set pour les enregistreurs vidéo-cassettes.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- Structure de MCI_VCR_SET_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385139"
---
# <a name="mci_vcr_set_parms-structure"></a><span data-ttu-id="475a4-104">La \_ structure de l’ensemble de magnétoscopes MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="475a4-104">MCI\_VCR\_SET\_PARMS structure</span></span>

<span data-ttu-id="475a4-105">La structure de l’ensemble de paramètres **MCI \_ magnétoscope \_ \_** contient des paramètres pour la commande [**MCI \_ Set**](mci-set.md) pour les enregistreurs vidéo-cassettes.</span><span class="sxs-lookup"><span data-stu-id="475a4-105">The **MCI\_VCR\_SET\_PARMS** structure contains parameters for the [**MCI\_SET**](mci-set.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="475a4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="475a4-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="475a4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="475a4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="475a4-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="475a4-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="475a4-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="475a4-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-111">Format de l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="475a4-111">Current time format.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="475a4-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="475a4-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-114">**dwTimeMode**</span><span class="sxs-lookup"><span data-stu-id="475a4-114">**dwTimeMode**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-115">Constante qui spécifie la source de minutage utilisée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="475a4-115">Constant that specifies the timing source used by the device.</span></span> <span data-ttu-id="475a4-116">La source de minutage est soit un code temporel enregistré sur bande vidéo, soit les compteurs de l’appareil qui détectent le mouvement des cassettes vidéo.</span><span class="sxs-lookup"><span data-stu-id="475a4-116">The timing source is either a timecode recorded on videotape, or the counters in the device that sense videotape movement.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-117">**dwRecordFormat**</span><span class="sxs-lookup"><span data-stu-id="475a4-117">**dwRecordFormat**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-118">Taux d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="475a4-118">Recording rate.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-119">**dwCounterFormat**</span><span class="sxs-lookup"><span data-stu-id="475a4-119">**dwCounterFormat**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-120">Format d’une nouvelle valeur de temps de compteur.</span><span class="sxs-lookup"><span data-stu-id="475a4-120">Format of a new counter time value.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-121">**dwIndex**</span><span class="sxs-lookup"><span data-stu-id="475a4-121">**dwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-122">Contenu de l’affichage à l’écran.</span><span class="sxs-lookup"><span data-stu-id="475a4-122">Contents of on-screen display.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-123">**dwTracking**</span><span class="sxs-lookup"><span data-stu-id="475a4-123">**dwTracking**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-124">Réglage de la vitesse utilisé pour le suivi de la vitesse de lecture des MAGNÉTOSCOPEs.</span><span class="sxs-lookup"><span data-stu-id="475a4-124">Speed adjustment used when tracking the VCR playback rate.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-125">**dwSpeed**</span><span class="sxs-lookup"><span data-stu-id="475a4-125">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-126">Vitesse de lecture utilisée par l’appareil en tant qu’entier.</span><span class="sxs-lookup"><span data-stu-id="475a4-126">Playback speed used by the device as an integer.</span></span> <span data-ttu-id="475a4-127">La vitesse de lecture normale est de 1000, la double vitesse est de 2000, et la demi-vitesse est de 500.</span><span class="sxs-lookup"><span data-stu-id="475a4-127">Normal playback speed is 1000, double speed is 2000, and half speed is 500.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-128">**dwLength**</span><span class="sxs-lookup"><span data-stu-id="475a4-128">**dwLength**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-129">Longueur de bande vidéo lorsque la longueur n’est pas détectable par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="475a4-129">Videotape length when the length is undetectable by the device.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-130">**dwCounter**</span><span class="sxs-lookup"><span data-stu-id="475a4-130">**dwCounter**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-131">Nouvelle valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="475a4-131">New counter value.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-132">**dwClock**</span><span class="sxs-lookup"><span data-stu-id="475a4-132">**dwClock**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-133">Nouvelle heure de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="475a4-133">New clock time.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-134">**dwPauseTimeout**</span><span class="sxs-lookup"><span data-stu-id="475a4-134">**dwPauseTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-135">Nouvelle valeur de délai d’attente pour la commande pause.</span><span class="sxs-lookup"><span data-stu-id="475a4-135">New timeout value for pause command.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-136">**dwPrerollDuration**</span><span class="sxs-lookup"><span data-stu-id="475a4-136">**dwPrerollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-137">Longueur de bande vidéo nécessaire pour stabiliser la sortie du magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="475a4-137">Videotape length needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-138">**dwPostrollDuration**</span><span class="sxs-lookup"><span data-stu-id="475a4-138">**dwPostrollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="475a4-139">La longueur des cassettes vidéo est nécessaire pour freiner le transport du magnétoscope lors de l’émission d’une commande [**MCI \_ Stop**](mci-stop.md) ou [**MCI \_ Pause**](mci-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="475a4-139">Videotape length needed to brake the VCR transport when a [**MCI\_STOP**](mci-stop.md) or [**MCI\_PAUSE**](mci-pause.md) command is issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="475a4-140">Notes</span><span class="sxs-lookup"><span data-stu-id="475a4-140">Remarks</span></span>

<span data-ttu-id="475a4-141">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="475a4-141">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="475a4-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="475a4-142">Requirements</span></span>



| <span data-ttu-id="475a4-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="475a4-143">Requirement</span></span> | <span data-ttu-id="475a4-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="475a4-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="475a4-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="475a4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="475a4-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="475a4-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="475a4-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="475a4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="475a4-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="475a4-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="475a4-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="475a4-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="475a4-150"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="475a4-150"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="475a4-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="475a4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="475a4-152">**MCI**</span><span class="sxs-lookup"><span data-stu-id="475a4-152">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="475a4-153">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="475a4-153">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="475a4-154">**\_Pause MCI**</span><span class="sxs-lookup"><span data-stu-id="475a4-154">**MCI\_PAUSE**</span></span>](mci-pause.md)
</dt> <dt>

[<span data-ttu-id="475a4-155">**jeu de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="475a4-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="475a4-156">**\_arrêt MCI**</span><span class="sxs-lookup"><span data-stu-id="475a4-156">**MCI\_STOP**</span></span>](mci-stop.md)
</dt> <dt>

<span data-ttu-id="475a4-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="475a4-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

