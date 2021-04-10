---
title: MDM_Policy_Result01_Update02, classe
description: La \_ classe Result01 Update02 de la stratégie MDM \_ \_ représente les stratégies de mise à jour disponibles.
ms.assetid: 06604da6-5298-4273-a030-529491c2823c
keywords:
- MDM_Policy_Result01_Update02, classe
- Classe MDM_Policy_Result01_Update02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Update02
- MDM_Policy_Result01_Update02.InstanceID
- MDM_Policy_Result01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0be844bb4ef8fc20e7ab5bbc8b7709cdfde4034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941704"
---
# <a name="mdm_policy_result01_update02-class"></a><span data-ttu-id="c1a73-105">\_Classe Update02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="c1a73-105">MDM\_Policy\_Result01\_Update02 class</span></span>

<span data-ttu-id="c1a73-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c1a73-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c1a73-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c1a73-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c1a73-108">La **classe \_ \_ Result01 \_ Update02 de la stratégie MDM** représente les stratégies de mise à jour disponibles.</span><span class="sxs-lookup"><span data-stu-id="c1a73-108">The **MDM\_Policy\_Result01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="c1a73-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c1a73-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a73-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1a73-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Update02
{
  string InstanceID;
  string ParentID;
  sint32 RequireUpdateApproval;
  sint32 AllowAutoUpdate;
  sint32 AllowAutoWindowsUpdateDownloadOverMeteredNetwork;
  sint32 AllowMUUpdateService;
  sint32 ScheduledInstallDay;
  sint32 ScheduledInstallThirdWeek;
  sint32 ScheduledInstallSecondWeek;
  sint32 ScheduledInstallFourthWeek;
  sint32 ScheduledInstallFirstWeek;
  sint32 ScheduledInstallEveryWeek;
  sint32 ScheduledInstallTime;
  sint32 AllowUpdateService;
  sint32 DeferQualityUpdatesPeriodInDays;
  sint32 DeferFeatureUpdatesPeriodInDays;
  sint32 BranchReadinessLevel;
  string UpdateServiceUrl;
  sint32 SetEDURestart;
  sint32 AutoRestartDeadlinePeriodInDays;
  string UpdateServiceUrlAlternate;
  sint32 FillEmptyContentUrls;
  sint32 AllowNonMicrosoftSignedUpdate;
  sint32 RequireDeferUpgrade;
  sint32 PauseDeferrals;
  sint32 PauseQualityUpdates;
  sint32 PhoneUpdateRestrictions;
  string PauseQualityUpdatesStartTime;
  sint32 PauseFeatureUpdates;
  string PauseFeatureUpdatesStartTime;
  sint32 DeferUpgradePeriod;
  sint32 ExcludeWUDriversInQualityUpdate;
  sint32 IgnoreMOUpdateDownloadLimit;
  sint32 ManagePreviewBuilds;
  sint32 IgnoreMOAppDownloadLimit;
  sint32 DeferUpdatePeriod;
  sint32 ActiveHoursEnd;
  sint32 ActiveHoursStart;
  sint32 DetectionFrequency;
  sint32 DisableDualScan;
  sint32 EngagedRestartDeadline;
  sint32 EngagedRestartSnoozeSchedule;
  sint32 EngagedRestartTransitionSchedule;
  sint32 ScheduleImminentRestartWarning;
  sint32 ScheduleRestartWarning;
  sint32 SetAutoRestartNotificationDisable;
  sint32 AutoRestartNotificationSchedule;
  sint32 AutoRestartRequiredNotificationDismissal;
  sint32 ActiveHoursMaxRange;
};
```

## <a name="members"></a><span data-ttu-id="c1a73-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c1a73-111">Members</span></span>

<span data-ttu-id="c1a73-112">La **classe \_ \_ Result01 \_ Update02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c1a73-112">The **MDM\_Policy\_Result01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="c1a73-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c1a73-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1a73-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c1a73-114">Properties</span></span>

<span data-ttu-id="c1a73-115">La **classe \_ \_ Result01 \_ Update02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c1a73-115">The **MDM\_Policy\_Result01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c1a73-116">ActiveHoursEnd</span><span class="sxs-lookup"><span data-stu-id="c1a73-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-119">ActiveHoursMaxRange</span><span class="sxs-lookup"><span data-stu-id="c1a73-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-122">ActiveHoursStart</span><span class="sxs-lookup"><span data-stu-id="c1a73-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-125">AllowAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="c1a73-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span><span class="sxs-lookup"><span data-stu-id="c1a73-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-131">AllowMUUpdateService</span><span class="sxs-lookup"><span data-stu-id="c1a73-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-134">AllowNonMicrosoftSignedUpdate</span><span class="sxs-lookup"><span data-stu-id="c1a73-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="c1a73-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-140">AutoRestartDeadlinePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c1a73-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-143">AutoRestartNotificationSchedule</span><span class="sxs-lookup"><span data-stu-id="c1a73-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-146">AutoRestartRequiredNotificationDismissal</span><span class="sxs-lookup"><span data-stu-id="c1a73-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="c1a73-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-152">DeferFeatureUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c1a73-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-155">DeferQualityUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c1a73-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-156">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="c1a73-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-159">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-161">DeferUpgradePeriod</span><span class="sxs-lookup"><span data-stu-id="c1a73-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-162">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-164">DetectionFrequency</span><span class="sxs-lookup"><span data-stu-id="c1a73-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-167">DisableDualScan</span><span class="sxs-lookup"><span data-stu-id="c1a73-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-168">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-170">EngagedRestartDeadline</span><span class="sxs-lookup"><span data-stu-id="c1a73-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-171">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-173">EngagedRestartSnoozeSchedule</span><span class="sxs-lookup"><span data-stu-id="c1a73-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-174">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-176">EngagedRestartTransitionSchedule</span><span class="sxs-lookup"><span data-stu-id="c1a73-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-177">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-179">ExcludeWUDriversInQualityUpdate</span><span class="sxs-lookup"><span data-stu-id="c1a73-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-180">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-182">FillEmptyContentUrls</span><span class="sxs-lookup"><span data-stu-id="c1a73-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-183">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-185">IgnoreMOAppDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="c1a73-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-186">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-188">IgnoreMOUpdateDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="c1a73-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-189">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c1a73-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c1a73-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1a73-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1a73-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-194">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c1a73-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c1a73-195">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c1a73-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="c1a73-196">Pour cette classe, la chaîne est « Update ».</span><span class="sxs-lookup"><span data-stu-id="c1a73-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="c1a73-197">ManagePreviewBuilds</span><span class="sxs-lookup"><span data-stu-id="c1a73-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-198">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c1a73-200">**ID**</span><span class="sxs-lookup"><span data-stu-id="c1a73-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1a73-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1a73-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-203">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c1a73-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c1a73-204">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c1a73-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="c1a73-205">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="c1a73-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="c1a73-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="c1a73-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-207">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="c1a73-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-210">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-212">PauseFeatureUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="c1a73-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1a73-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="c1a73-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-216">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-218">PauseQualityUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="c1a73-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1a73-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-221">PhoneUpdateRestrictions</span><span class="sxs-lookup"><span data-stu-id="c1a73-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-222">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="c1a73-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-225">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="c1a73-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-228">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="c1a73-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-231">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-233">ScheduledInstallEveryWeek</span><span class="sxs-lookup"><span data-stu-id="c1a73-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-234">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-235">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-236">ScheduledInstallFirstWeek</span><span class="sxs-lookup"><span data-stu-id="c1a73-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-237">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-238">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-239">ScheduledInstallFourthWeek</span><span class="sxs-lookup"><span data-stu-id="c1a73-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-240">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-241">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-242">ScheduledInstallSecondWeek</span><span class="sxs-lookup"><span data-stu-id="c1a73-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-243">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-244">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-245">ScheduledInstallThirdWeek</span><span class="sxs-lookup"><span data-stu-id="c1a73-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-246">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-247">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="c1a73-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-249">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-250">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-251">ScheduleImminentRestartWarning</span><span class="sxs-lookup"><span data-stu-id="c1a73-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-252">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-253">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-254">ScheduleRestartWarning</span><span class="sxs-lookup"><span data-stu-id="c1a73-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-255">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-256">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-257">SetAutoRestartNotificationDisable</span><span class="sxs-lookup"><span data-stu-id="c1a73-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-258">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-259">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-260">SetEDURestart</span><span class="sxs-lookup"><span data-stu-id="c1a73-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-261">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1a73-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-262">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-263">UpdateServiceUrl</span><span class="sxs-lookup"><span data-stu-id="c1a73-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1a73-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-265">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1a73-266">UpdateServiceUrlAlternate</span><span class="sxs-lookup"><span data-stu-id="c1a73-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a73-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1a73-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1a73-268">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1a73-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1a73-269">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1a73-269">Requirements</span></span>



| <span data-ttu-id="c1a73-270">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1a73-270">Requirement</span></span> | <span data-ttu-id="c1a73-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1a73-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a73-272">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1a73-272">Minimum supported client</span></span><br/> | <span data-ttu-id="c1a73-273">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1a73-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1a73-274">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1a73-274">Minimum supported server</span></span><br/> | <span data-ttu-id="c1a73-275">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1a73-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c1a73-276">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c1a73-276">Namespace</span></span><br/>                | <span data-ttu-id="c1a73-277">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c1a73-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c1a73-278">MOF</span><span class="sxs-lookup"><span data-stu-id="c1a73-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1a73-279"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1a73-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1a73-280">DLL</span><span class="sxs-lookup"><span data-stu-id="c1a73-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1a73-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1a73-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1a73-282">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1a73-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a73-283">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="c1a73-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

