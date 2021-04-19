---
description: Décrit comment mettre à jour le système d’exploitation sur un appareil.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: Énumération UpdateAssessmentStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 790077118db7704bdd04801758f44cbb50cc54b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517311"
---
# <a name="updateassessmentstatus-enumeration"></a><span data-ttu-id="889f1-103">Énumération UpdateAssessmentStatus</span><span class="sxs-lookup"><span data-stu-id="889f1-103">UpdateAssessmentStatus enumeration</span></span>

<span data-ttu-id="889f1-104">Décrit comment mettre à jour le système d’exploitation sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="889f1-104">Describes how up-to-date the OS on a device is.</span></span> <span data-ttu-id="889f1-105">**UpdateAssessmentStatus** est utilisé par les structures [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) et [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , dans les membres **assessmentForCurrent**, **assessmentForUpToDate** et **securityStatus** .</span><span class="sxs-lookup"><span data-stu-id="889f1-105">**UpdateAssessmentStatus** is used by the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, in the **assessmentForCurrent**, **assessmentForUpToDate**, and **securityStatus** members.</span></span> <span data-ttu-id="889f1-106">Une seule constante est retournée.</span><span class="sxs-lookup"><span data-stu-id="889f1-106">Exactly one constant is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="889f1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="889f1-107">Syntax</span></span>


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a><span data-ttu-id="889f1-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="889f1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="889f1-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_ Dernière version**</span><span class="sxs-lookup"><span data-stu-id="889f1-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span> **UpdateAssessmentStatus\_Latest**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-110">Ce résultat dans **assessmentForCurrent** implique que l’appareil se trouve sur les dernières mises à jour de fonctionnalités et mise à jour de qualité disponibles pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="889f1-110">This result within **assessmentForCurrent** implies that the device is on the latest feature update and quality update available for that device.</span></span> <span data-ttu-id="889f1-111">Dans **assessmentForUpToDate**, ce résultat implique que l’appareil se trouve sur la dernière mise à jour de qualité pour la version de Windows qu’il exécute.</span><span class="sxs-lookup"><span data-stu-id="889f1-111">Within **assessmentForUpToDate**, this result implies that the device is on the latest quality update for the release of Windows it is running.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestSoftRestriction**</span><span class="sxs-lookup"><span data-stu-id="889f1-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestSoftRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-113">La dernière mise à jour de la fonctionnalité n’a pas été installée en raison d’une restriction logicielle.</span><span class="sxs-lookup"><span data-stu-id="889f1-113">The latest feature update has not been installed due to a soft restriction.</span></span> <span data-ttu-id="889f1-114">Lorsqu’une restriction logicielle a été placée sur une mise à jour, la mise à jour n’est pas installée automatiquement. un utilisateur doit lancer automatiquement le téléchargement au sein de l’expérience utilisateur de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="889f1-114">When a soft restriction has been placed on an update, the update will not be automatically installed; a user must self-initiate the download within the Update UX.</span></span> <span data-ttu-id="889f1-115">Cet État s’applique uniquement à **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="889f1-115">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestHardRestriction**</span><span class="sxs-lookup"><span data-stu-id="889f1-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestHardRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-117">La dernière mise à jour de la fonctionnalité n’a pas été installée en raison d’une restriction matérielle.</span><span class="sxs-lookup"><span data-stu-id="889f1-117">The latest feature update has not been installed due to a hard restriction.</span></span> <span data-ttu-id="889f1-118">Lorsqu’une restriction matérielle a été placée sur une mise à jour, la mise à jour n’est pas applicable à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="889f1-118">When a hard restriction has been placed on an update, the update is not applicable to the device.</span></span> <span data-ttu-id="889f1-119">Cet État s’applique uniquement à **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="889f1-119">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_ NotLatestEndOfSupport**</span><span class="sxs-lookup"><span data-stu-id="889f1-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span> **UpdateAssessmentStatus\_NotLatestEndOfSupport**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-121">L’appareil n’est pas dans la dernière mise à jour, car la mise à jour des fonctionnalités de l’appareil n’est plus prise en charge par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="889f1-121">The device is not on the latest update because the device's feature update is no longer supported by Microsoft.</span></span> <span data-ttu-id="889f1-122">Lorsque Microsoft arrête de prendre en charge une version de fonctionnalité, cet État est renvoyé pour **assessmentForCurrent** et **assessmentForUpToDate**.</span><span class="sxs-lookup"><span data-stu-id="889f1-122">When Microsoft stops supporting a feature release, this status will be returned for both **assessmentForCurrent** and **assessmentForUpToDate**.</span></span>

> [!Note]  
> <span data-ttu-id="889f1-123">Lorsque **UpdateAssessmentStatus \_ NotLatestEndOfSupport** est retourné, le **UpdateImpactLevel** de l’évaluation est toujours **UpdateImpactLevel \_ élevé**.</span><span class="sxs-lookup"><span data-stu-id="889f1-123">When **UpdateAssessmentStatus\_NotLatestEndOfSupport** is returned, the assessment's **UpdateImpactLevel** is always **UpdateImpactLevel\_High**.</span></span>

 

</dd> <dt>

<span data-ttu-id="889f1-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_ NotLatestServicingTrain**</span><span class="sxs-lookup"><span data-stu-id="889f1-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span> **UpdateAssessmentStatus\_NotLatestServicingTrain**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-125">L’appareil n’est pas sur la dernière mise à jour des fonctionnalités, car le train de maintenance de l’appareil limite la mise à jour de l’appareil à la dernière mise à jour de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="889f1-125">The device is not on the latest feature update because the device's servicing train limits the device from updating to the latest feature update.</span></span> <span data-ttu-id="889f1-126">Par exemple : si un appareil se trouve sur Current Branch for Business (CBB) et qu’une nouvelle mise à jour de fonctionnalité a été publiée pour Current Branch (CB), cette opération est retournée.</span><span class="sxs-lookup"><span data-stu-id="889f1-126">For example: if a device is on Current Branch for Business (CBB) and a new feature update has been released for Current Branch (CB), this will be returned.</span></span> <span data-ttu-id="889f1-127">Cet État s’applique uniquement à **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="889f1-127">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestDeferredFeature**</span><span class="sxs-lookup"><span data-stu-id="889f1-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestDeferredFeature**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-129">La dernière mise à jour de la fonctionnalité n’a pas été installée en raison de la stratégie de report des mises à jour Windows Update pour les fonctionnalités d’entreprise de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="889f1-129">The latest feature update has not been installed due to the device's Windows Update for Business Feature Update Deferral policy.</span></span> <span data-ttu-id="889f1-130">La détermination des **daysOutOfDate** prend en compte les stratégies de report. **daysOutOfDate** ne commence pas à s’incrémenter tant que la période de report n’a pas expiré.</span><span class="sxs-lookup"><span data-stu-id="889f1-130">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span> <span data-ttu-id="889f1-131">Cet État s’applique uniquement à **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="889f1-131">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestDeferredQuality**</span><span class="sxs-lookup"><span data-stu-id="889f1-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestDeferredQuality**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-133">L’appareil n’est pas sur la dernière mise à jour de qualité en raison de la Windows Update de l’appareil pour la stratégie de report de mise à jour de qualité professionnelle.</span><span class="sxs-lookup"><span data-stu-id="889f1-133">The device is not on the latest quality update due to the device's Windows Update for Business Quality Update Deferral policy.</span></span> <span data-ttu-id="889f1-134">La détermination des **daysOutOfDate** prend en compte les stratégies de report. **daysOutOfDate** ne commence pas à s’incrémenter tant que la période de report n’a pas expiré.</span><span class="sxs-lookup"><span data-stu-id="889f1-134">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestPausedFeature**</span><span class="sxs-lookup"><span data-stu-id="889f1-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestPausedFeature**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-136">L’appareil n’est pas sur la dernière mise à jour des fonctionnalités, car l’appareil a des mises à jour de fonctionnalités suspendues.</span><span class="sxs-lookup"><span data-stu-id="889f1-136">The device is not on the latest feature update due to the device having paused Feature Updates.</span></span> <span data-ttu-id="889f1-137">Le fait qu’un appareil soit mis en pause n’est pas pris en compte dans le calcul de **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="889f1-137">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="889f1-138">Cet État s’applique uniquement à **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="889f1-138">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestPausedQuality**</span><span class="sxs-lookup"><span data-stu-id="889f1-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestPausedQuality**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-140">L’appareil n’est pas sur la dernière mise à jour de qualité, car l’appareil a des mises à jour qualité suspendues.</span><span class="sxs-lookup"><span data-stu-id="889f1-140">The device is not on the latest quality update due to the device having paused Quality Updates.</span></span> <span data-ttu-id="889f1-141">Le fait qu’un appareil soit mis en pause n’est pas pris en compte dans le calcul de **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="889f1-141">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="889f1-142">**daysOutOfDate** ne détermine pas si un appareil est mis en pause dans son calcul.</span><span class="sxs-lookup"><span data-stu-id="889f1-142">**daysOutOfDate** does not factor whether a device is paused into its calculation.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_ NotLatestManaged**</span><span class="sxs-lookup"><span data-stu-id="889f1-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span> **UpdateAssessmentStatus\_NotLatestManaged**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-144">L’appareil n’est pas sur la dernière mise à jour, car l’approbation des mises à jour n’est pas effectuée par le biais de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="889f1-144">The device is not on the latest update because the approval of updates is not done through Windows Update.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_ NotLatestUnknown**</span><span class="sxs-lookup"><span data-stu-id="889f1-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span> **UpdateAssessmentStatus\_NotLatestUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-146">L’appareil n’est pas sur la dernière mise à jour en raison d’une raison qui ne peut pas être déterminée par l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="889f1-146">The device is not on the latest update due to a reason that cannot be determined by the assessment.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_ NotLatestTargetedVersion**</span><span class="sxs-lookup"><span data-stu-id="889f1-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span> **UpdateAssessmentStatus\_NotLatestTargetedVersion**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-148">L’appareil n’est pas sur la dernière mise à jour des fonctionnalités en raison de la stratégie de version cible de l’Windows Update de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="889f1-148">The device is not on the latest feature update due to the device's Windows Update for Business Target Version policy.</span></span> <span data-ttu-id="889f1-149">Cette stratégie conserve l’appareil sur la version de la fonctionnalité ciblée.</span><span class="sxs-lookup"><span data-stu-id="889f1-149">This policy is keeping the device on the targeted feature release version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="889f1-150">Notes</span><span class="sxs-lookup"><span data-stu-id="889f1-150">Remarks</span></span>

<span data-ttu-id="889f1-151">Cette énumération est utilisée le plus souvent avec les structures [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) et [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , qui sont utilisées à leur tour avec la méthode [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) pour [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span><span class="sxs-lookup"><span data-stu-id="889f1-151">This enumeration is used most often with the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, which are in turn used with the [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) method for [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span></span>

## <a name="requirements"></a><span data-ttu-id="889f1-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="889f1-152">Requirements</span></span>



| <span data-ttu-id="889f1-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="889f1-153">Requirement</span></span> | <span data-ttu-id="889f1-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="889f1-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="889f1-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="889f1-155">Minimum supported client</span></span><br/> | <span data-ttu-id="889f1-156">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="889f1-156">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="889f1-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="889f1-157">Minimum supported server</span></span><br/> | <span data-ttu-id="889f1-158">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="889f1-158">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="889f1-159">MIDL</span><span class="sxs-lookup"><span data-stu-id="889f1-159">IDL</span></span><br/>                      | <dl> <span data-ttu-id="889f1-160"><dt>WaaSAPI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="889f1-160"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




