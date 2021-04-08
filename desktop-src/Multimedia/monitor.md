---
title: commande Monitor
description: La commande Monitor spécifie la source de la présentation. (La source de présentation par défaut est l’espace de travail.) Le fait de basculer la source de présentation change tous les flux audio et vidéo dans la source. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- commande surveiller Windows Multimedia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741428"
---
# <a name="monitor-command"></a><span data-ttu-id="606a5-106">commande Monitor</span><span class="sxs-lookup"><span data-stu-id="606a5-106">monitor command</span></span>

<span data-ttu-id="606a5-107">La commande Monitor spécifie la source de la présentation.</span><span class="sxs-lookup"><span data-stu-id="606a5-107">The monitor command specifies the presentation source.</span></span> <span data-ttu-id="606a5-108">(La source de présentation par défaut est l’espace de travail.) Le fait de basculer la source de présentation change tous les flux audio et vidéo dans la source.</span><span class="sxs-lookup"><span data-stu-id="606a5-108">(The default presentation source is the workspace.) Switching the presentation source switches all audio and video streams in the source.</span></span> <span data-ttu-id="606a5-109">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="606a5-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="606a5-110">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="606a5-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="606a5-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="606a5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="606a5-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="606a5-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="606a5-113">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="606a5-113">Identifier of an MCI device.</span></span> <span data-ttu-id="606a5-114">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="606a5-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="606a5-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span><span class="sxs-lookup"><span data-stu-id="606a5-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="606a5-116">Un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="606a5-116">One or more of the following flags.</span></span>



| <span data-ttu-id="606a5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="606a5-117">Value</span></span>           | <span data-ttu-id="606a5-118">Signification</span><span class="sxs-lookup"><span data-stu-id="606a5-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="606a5-119">fichier</span><span class="sxs-lookup"><span data-stu-id="606a5-119">file</span></span>            | <span data-ttu-id="606a5-120">Spécifie que l’espace de travail est la source de présentation.</span><span class="sxs-lookup"><span data-stu-id="606a5-120">Specifies that the workspace is the presentation source.</span></span> <span data-ttu-id="606a5-121">Il s’agit de la source par défaut.</span><span class="sxs-lookup"><span data-stu-id="606a5-121">This is the default source.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="606a5-122">entrée</span><span class="sxs-lookup"><span data-stu-id="606a5-122">input</span></span>           | <span data-ttu-id="606a5-123">Spécifie que l’entrée externe est la source de la présentation.</span><span class="sxs-lookup"><span data-stu-id="606a5-123">Specifies that the external input is the presentation source.</span></span> <span data-ttu-id="606a5-124">Si une commande de [lecture](play.md) est en cours, elle est d’abord suspendue.</span><span class="sxs-lookup"><span data-stu-id="606a5-124">If a [play](play.md) command is in progress, it is first paused.</span></span> <span data-ttu-id="606a5-125">Si [setvideo](setvideo.md) a la valeur on, cet indicateur affiche une fenêtre masquée par défaut.</span><span class="sxs-lookup"><span data-stu-id="606a5-125">If [setvideo](setvideo.md) is "on", this flag displays a default hidden window.</span></span> <span data-ttu-id="606a5-126">Les appareils peuvent limiter ce que d’autres instances de périphérique peuvent faire lors de l’analyse de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="606a5-126">Devices might limit what other device instances can do while monitoring input.</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="606a5-127">méthode *de méthode*</span><span class="sxs-lookup"><span data-stu-id="606a5-127">method *method*</span></span> | <span data-ttu-id="606a5-128">Lorsqu’il est utilisé avec **Monitor** « Input », cet indicateur sélectionne la méthode de surveillance.</span><span class="sxs-lookup"><span data-stu-id="606a5-128">When used with **monitor** "input", this flag selects the method of monitoring.</span></span> <span data-ttu-id="606a5-129">La *méthode* est « pre », « poster » ou « direct ».</span><span class="sxs-lookup"><span data-stu-id="606a5-129">The *method* is either "pre", "post", or "direct".</span></span> <span data-ttu-id="606a5-130">La surveillance directe demande que l’appareil soit configuré pour une qualité d’affichage optimale pendant la surveillance.</span><span class="sxs-lookup"><span data-stu-id="606a5-130">Direct monitoring requests that the device be configured for optimum display quality during monitoring.</span></span> <span data-ttu-id="606a5-131">La méthode de surveillance directe peut être incompatible avec l’enregistrement vidéo motion. La pré-surveillance et la postérieure à la surveillance autorisent l’enregistrement vidéo.</span><span class="sxs-lookup"><span data-stu-id="606a5-131">The direct monitoring method might be incompatible with motion video recording.Pre- and post-monitoring allow motion video recording.</span></span> <span data-ttu-id="606a5-132">La pré-surveillance affiche l’entrée externe avant la compression, tandis que le suivi de la surveillance affiche l’entrée externe après compression.</span><span class="sxs-lookup"><span data-stu-id="606a5-132">Pre-monitoring shows the external input prior to compression, while post-monitoring shows the external input after compression.</span></span> <span data-ttu-id="606a5-133">En règle générale, différentes méthodes d’analyse ont des implications matérielles différentes.</span><span class="sxs-lookup"><span data-stu-id="606a5-133">Typically, different monitoring methods have different hardware implications.</span></span> <span data-ttu-id="606a5-134">La méthode d’analyse par défaut est sélectionnée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="606a5-134">The default monitoring method is selected by the device.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="606a5-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="606a5-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="606a5-136">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="606a5-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="606a5-137">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="606a5-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="606a5-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="606a5-138">Return Value</span></span>

<span data-ttu-id="606a5-139">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="606a5-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="606a5-140">Notes</span><span class="sxs-lookup"><span data-stu-id="606a5-140">Remarks</span></span>

<span data-ttu-id="606a5-141">La source de la présentation bascule automatiquement vers l’espace de travail après une commande [Play](play.md), [Step](step.md), [Pause](pause.md), [CUE](cue.md) « Output » ou [Seek](seek.md) .</span><span class="sxs-lookup"><span data-stu-id="606a5-141">The presentation source automatically switches to the workspace after a [play](play.md), [step](step.md), [pause](pause.md), [cue](cue.md) "output", or [seek](seek.md) command.</span></span> <span data-ttu-id="606a5-142">La commande d' [enregistrement](record.md) ne change pas automatiquement les sources de présentation, ce qui permet à votre application de ne pas afficher de vidéo lors de son enregistrement.</span><span class="sxs-lookup"><span data-stu-id="606a5-142">The [record](record.md) command does not automatically switch presentation sources, which gives your application the option of not showing video while it is being recorded.</span></span>

## <a name="requirements"></a><span data-ttu-id="606a5-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="606a5-143">Requirements</span></span>



| <span data-ttu-id="606a5-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="606a5-144">Requirement</span></span> | <span data-ttu-id="606a5-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="606a5-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="606a5-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="606a5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="606a5-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="606a5-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="606a5-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="606a5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="606a5-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="606a5-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="606a5-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="606a5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="606a5-151">MCI</span><span class="sxs-lookup"><span data-stu-id="606a5-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="606a5-152">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="606a5-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="606a5-153">signal</span><span class="sxs-lookup"><span data-stu-id="606a5-153">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="606a5-154">pause</span><span class="sxs-lookup"><span data-stu-id="606a5-154">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="606a5-155">répétition</span><span class="sxs-lookup"><span data-stu-id="606a5-155">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="606a5-156">enregistrement</span><span class="sxs-lookup"><span data-stu-id="606a5-156">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="606a5-157">Demandez</span><span class="sxs-lookup"><span data-stu-id="606a5-157">seek</span></span>](seek.md)
</dt> <dt>

[<span data-ttu-id="606a5-158">première</span><span class="sxs-lookup"><span data-stu-id="606a5-158">step</span></span>](step.md)
</dt> </dl>

 

