---
title: Classe MDM_Policy_Result01_Defender02
description: La \_ stratégie MDM \_ Result01 \_ Defender02class représente les stratégies associées à Windows Defender.
ms.assetid: 82c8a7a2-8369-46c4-aa87-b44b742a274d
keywords:
- Classe MDM_Policy_Result01_Defender02
- Classe MDM_Policy_Result01_Defender02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Defender02
- MDM_Policy_Result01_Defender02.InstanceID
- MDM_Policy_Result01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae898751a9f15af1c945efd3e6a473dfe07c7cd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464758"
---
# <a name="mdm_policy_result01_defender02-class"></a><span data-ttu-id="31d89-105">\_Classe Defender02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="31d89-105">MDM\_Policy\_Result01\_Defender02 class</span></span>

<span data-ttu-id="31d89-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="31d89-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="31d89-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="31d89-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="31d89-108">La classe Defender02 de la **\_ stratégie MDM \_ Result01 \_** représente des stratégies liées à Windows Defender</span><span class="sxs-lookup"><span data-stu-id="31d89-108">The **MDM\_Policy\_Result01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="31d89-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="31d89-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d89-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31d89-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Defender02
{
  string InstanceID;
  string ParentID;
  sint32 AllowArchiveScanning;
  sint32 AllowBehaviorMonitoring;
  sint32 AllowCloudProtection;
  sint32 AllowEmailScanning;
  sint32 AllowFullScanOnMappedNetworkDrives;
  sint32 AllowFullScanRemovableDriveScanning;
  sint32 AllowIntrusionPreventionSystem;
  sint32 AllowIOAVProtection;
  sint32 AllowOnAccessProtection;
  sint32 AllowRealtimeMonitoring;
  sint32 AllowScanningNetworkFiles;
  sint32 AllowScriptScanning;
  sint32 AllowUserUIAccess;
  string AttackSurfaceReductionRules;
  string AttackSurfaceReductionOnlyExclusions;
  sint32 AVGCPULoadFactor;
  sint32 CloudExtendedTimeout;
  string ControlledFolderAccessProtectedFolders;
  string ControlledFolderAccessAllowedApplications;
  sint32 CloudBlockLevel;
  sint32 DaysToRetainCleanedMalware;
  sint32 EnableControlledFolderAccess;
  sint32 EnableNetworkProtection;
  sint32 PUAProtection;
  string ExcludedProcesses;
  string ExcludedPaths;
  string ExcludedExtensions;
  sint32 RealTimeScanDirection;
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
  sint32 ScanParameter;
};
```

## <a name="members"></a><span data-ttu-id="31d89-111">Membres</span><span class="sxs-lookup"><span data-stu-id="31d89-111">Members</span></span>

<span data-ttu-id="31d89-112">La **classe \_ \_ Result01 \_ Defender02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="31d89-112">The **MDM\_Policy\_Result01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="31d89-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="31d89-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31d89-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="31d89-114">Properties</span></span>

<span data-ttu-id="31d89-115">La **classe \_ \_ Result01 \_ Defender02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="31d89-115">The **MDM\_Policy\_Result01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="31d89-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="31d89-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="31d89-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="31d89-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="31d89-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="31d89-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="31d89-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="31d89-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="31d89-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="31d89-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="31d89-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="31d89-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="31d89-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="31d89-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-155">AttackSurfaceReductionOnlyExclusions</span><span class="sxs-lookup"><span data-stu-id="31d89-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31d89-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-158">AttackSurfaceReductionRules</span><span class="sxs-lookup"><span data-stu-id="31d89-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31d89-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="31d89-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-162">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-164">CloudBlockLevel</span><span class="sxs-lookup"><span data-stu-id="31d89-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-167">CloudExtendedTimeout</span><span class="sxs-lookup"><span data-stu-id="31d89-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-168">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-170">ControlledFolderAccessAllowedApplications</span><span class="sxs-lookup"><span data-stu-id="31d89-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31d89-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-173">ControlledFolderAccessProtectedFolders</span><span class="sxs-lookup"><span data-stu-id="31d89-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31d89-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="31d89-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-177">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-179">EnableControlledFolderAccess</span><span class="sxs-lookup"><span data-stu-id="31d89-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-180">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-182">EnableNetworkProtection</span><span class="sxs-lookup"><span data-stu-id="31d89-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-183">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="31d89-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31d89-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="31d89-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31d89-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="31d89-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31d89-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-193">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31d89-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="31d89-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31d89-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31d89-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d89-197">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="31d89-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="31d89-198">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="31d89-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="31d89-199">Pour cette classe, la chaîne est « Defender ».</span><span class="sxs-lookup"><span data-stu-id="31d89-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="31d89-200">**ID**</span><span class="sxs-lookup"><span data-stu-id="31d89-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31d89-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31d89-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d89-203">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="31d89-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="31d89-204">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="31d89-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="31d89-205">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="31d89-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="31d89-206">PUAProtection</span><span class="sxs-lookup"><span data-stu-id="31d89-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-207">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="31d89-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-210">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="31d89-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-213">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="31d89-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-216">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="31d89-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-219">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="31d89-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-222">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="31d89-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-225">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="31d89-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-228">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31d89-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31d89-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="31d89-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d89-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31d89-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d89-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d89-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31d89-233">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31d89-233">Requirements</span></span>



| <span data-ttu-id="31d89-234">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31d89-234">Requirement</span></span> | <span data-ttu-id="31d89-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="31d89-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31d89-236">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31d89-236">Minimum supported client</span></span><br/> | <span data-ttu-id="31d89-237">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31d89-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31d89-238">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31d89-238">Minimum supported server</span></span><br/> | <span data-ttu-id="31d89-239">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="31d89-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="31d89-240">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="31d89-240">Namespace</span></span><br/>                | <span data-ttu-id="31d89-241">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="31d89-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="31d89-242">MOF</span><span class="sxs-lookup"><span data-stu-id="31d89-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31d89-243"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31d89-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="31d89-244">DLL</span><span class="sxs-lookup"><span data-stu-id="31d89-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31d89-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31d89-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d89-246">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31d89-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d89-247">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="31d89-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

