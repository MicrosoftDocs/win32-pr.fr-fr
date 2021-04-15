---
title: MDM_Policy_Config01_Update02, classe
description: La \_ classe Config01 Update02 de la stratégie MDM \_ \_ représente les stratégies de mise à jour disponibles.
ms.assetid: 7324912c-7ac5-42fd-baee-f7e2d81de023
keywords:
- MDM_Policy_Config01_Update02, classe
- Classe MDM_Policy_Config01_Update02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Update02
- MDM_Policy_Config01_Update02.InstanceID
- MDM_Policy_Config01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3044fc527fd23d49fac383dc25778d3a978b2788
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465442"
---
# <a name="mdm_policy_config01_update02-class"></a><span data-ttu-id="1eead-105">\_Classe Update02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="1eead-105">MDM\_Policy\_Config01\_Update02 class</span></span>

<span data-ttu-id="1eead-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="1eead-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1eead-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="1eead-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1eead-108">La **classe \_ \_ Config01 \_ Update02 de la stratégie MDM** représente les stratégies de mise à jour disponibles.</span><span class="sxs-lookup"><span data-stu-id="1eead-108">The **MDM\_Policy\_Config01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="1eead-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1eead-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eead-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eead-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Update02
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

## <a name="members"></a><span data-ttu-id="1eead-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1eead-111">Members</span></span>

<span data-ttu-id="1eead-112">La **classe \_ \_ Config01 \_ Update02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1eead-112">The **MDM\_Policy\_Config01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="1eead-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1eead-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1eead-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1eead-114">Properties</span></span>

<span data-ttu-id="1eead-115">La **classe \_ \_ Config01 \_ Update02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1eead-115">The **MDM\_Policy\_Config01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1eead-116">ActiveHoursEnd</span><span class="sxs-lookup"><span data-stu-id="1eead-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-119">ActiveHoursMaxRange</span><span class="sxs-lookup"><span data-stu-id="1eead-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-122">ActiveHoursStart</span><span class="sxs-lookup"><span data-stu-id="1eead-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-125">AllowAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="1eead-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span><span class="sxs-lookup"><span data-stu-id="1eead-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-131">AllowMUUpdateService</span><span class="sxs-lookup"><span data-stu-id="1eead-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-134">AllowNonMicrosoftSignedUpdate</span><span class="sxs-lookup"><span data-stu-id="1eead-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="1eead-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-140">AutoRestartDeadlinePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1eead-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-143">AutoRestartNotificationSchedule</span><span class="sxs-lookup"><span data-stu-id="1eead-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-146">AutoRestartRequiredNotificationDismissal</span><span class="sxs-lookup"><span data-stu-id="1eead-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="1eead-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-152">DeferFeatureUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1eead-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-155">DeferQualityUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1eead-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-156">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="1eead-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-159">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-161">DeferUpgradePeriod</span><span class="sxs-lookup"><span data-stu-id="1eead-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-162">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-164">DetectionFrequency</span><span class="sxs-lookup"><span data-stu-id="1eead-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-167">DisableDualScan</span><span class="sxs-lookup"><span data-stu-id="1eead-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-168">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-170">EngagedRestartDeadline</span><span class="sxs-lookup"><span data-stu-id="1eead-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-171">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-173">EngagedRestartSnoozeSchedule</span><span class="sxs-lookup"><span data-stu-id="1eead-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-174">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-176">EngagedRestartTransitionSchedule</span><span class="sxs-lookup"><span data-stu-id="1eead-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-177">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-179">ExcludeWUDriversInQualityUpdate</span><span class="sxs-lookup"><span data-stu-id="1eead-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-180">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-182">FillEmptyContentUrls</span><span class="sxs-lookup"><span data-stu-id="1eead-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-183">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-185">IgnoreMOAppDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="1eead-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-186">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-188">IgnoreMOUpdateDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="1eead-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-189">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1eead-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1eead-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1eead-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1eead-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eead-194">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1eead-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1eead-195">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="1eead-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="1eead-196">Pour cette classe, la chaîne est « Update ».</span><span class="sxs-lookup"><span data-stu-id="1eead-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="1eead-197">ManagePreviewBuilds</span><span class="sxs-lookup"><span data-stu-id="1eead-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-198">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1eead-200">**ID**</span><span class="sxs-lookup"><span data-stu-id="1eead-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1eead-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1eead-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eead-203">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1eead-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1eead-204">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="1eead-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="1eead-205">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="1eead-205">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="1eead-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="1eead-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-207">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="1eead-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-210">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-212">PauseFeatureUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="1eead-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1eead-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="1eead-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-216">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-218">PauseQualityUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="1eead-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1eead-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-221">PhoneUpdateRestrictions</span><span class="sxs-lookup"><span data-stu-id="1eead-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-222">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="1eead-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-225">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="1eead-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-228">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="1eead-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-231">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-233">ScheduledInstallEveryWeek</span><span class="sxs-lookup"><span data-stu-id="1eead-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-234">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-235">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-236">ScheduledInstallFirstWeek</span><span class="sxs-lookup"><span data-stu-id="1eead-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-237">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-238">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-239">ScheduledInstallFourthWeek</span><span class="sxs-lookup"><span data-stu-id="1eead-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-240">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-241">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-242">ScheduledInstallSecondWeek</span><span class="sxs-lookup"><span data-stu-id="1eead-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-243">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-244">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-245">ScheduledInstallThirdWeek</span><span class="sxs-lookup"><span data-stu-id="1eead-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-246">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-247">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="1eead-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-249">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-250">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-251">ScheduleImminentRestartWarning</span><span class="sxs-lookup"><span data-stu-id="1eead-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-252">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-253">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-254">ScheduleRestartWarning</span><span class="sxs-lookup"><span data-stu-id="1eead-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-255">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-256">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-257">SetAutoRestartNotificationDisable</span><span class="sxs-lookup"><span data-stu-id="1eead-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-258">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-259">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-260">SetEDURestart</span><span class="sxs-lookup"><span data-stu-id="1eead-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-261">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1eead-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-262">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-263">UpdateServiceUrl</span><span class="sxs-lookup"><span data-stu-id="1eead-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1eead-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-265">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1eead-266">UpdateServiceUrlAlternate</span><span class="sxs-lookup"><span data-stu-id="1eead-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eead-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1eead-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eead-268">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1eead-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1eead-269">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1eead-269">Requirements</span></span>



| <span data-ttu-id="1eead-270">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eead-270">Requirement</span></span> | <span data-ttu-id="1eead-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eead-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eead-272">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eead-272">Minimum supported client</span></span><br/> | <span data-ttu-id="1eead-273">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1eead-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1eead-274">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eead-274">Minimum supported server</span></span><br/> | <span data-ttu-id="1eead-275">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eead-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1eead-276">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1eead-276">Namespace</span></span><br/>                | <span data-ttu-id="1eead-277">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="1eead-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1eead-278">MOF</span><span class="sxs-lookup"><span data-stu-id="1eead-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eead-279"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1eead-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eead-280">DLL</span><span class="sxs-lookup"><span data-stu-id="1eead-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eead-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eead-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eead-282">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eead-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eead-283">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="1eead-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

