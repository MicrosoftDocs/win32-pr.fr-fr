---
title: Classe MDM_Policy_Config01_Defender02
description: La \_ stratégie MDM \_ Config01 \_ Defender02class représente les stratégies associées à Windows Defender.
ms.assetid: 6d9d4edd-fcb6-45ea-bc5d-1bffb9cf8740
keywords:
- Classe MDM_Policy_Config01_Defender02
- Classe MDM_Policy_Config01_Defender02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Defender02
- MDM_Policy_Config01_Defender02.InstanceID
- MDM_Policy_Config01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b184008fc0ce7fc44dcb7106ceec3abc0e91450d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464842"
---
# <a name="mdm_policy_config01_defender02-class"></a><span data-ttu-id="01a71-105">\_Classe Defender02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="01a71-105">MDM\_Policy\_Config01\_Defender02 class</span></span>

<span data-ttu-id="01a71-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="01a71-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="01a71-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="01a71-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="01a71-108">La classe Defender02 de la **\_ stratégie MDM \_ Config01 \_** représente des stratégies liées à Windows Defender</span><span class="sxs-lookup"><span data-stu-id="01a71-108">The **MDM\_Policy\_Config01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="01a71-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="01a71-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a71-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01a71-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Defender02
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
  sint32 ScanParameter;
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
};
```

## <a name="members"></a><span data-ttu-id="01a71-111">Membres</span><span class="sxs-lookup"><span data-stu-id="01a71-111">Members</span></span>

<span data-ttu-id="01a71-112">La **classe \_ \_ Config01 \_ Defender02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="01a71-112">The **MDM\_Policy\_Config01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="01a71-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01a71-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01a71-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01a71-114">Properties</span></span>

<span data-ttu-id="01a71-115">La **classe \_ \_ Config01 \_ Defender02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="01a71-115">The **MDM\_Policy\_Config01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="01a71-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="01a71-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="01a71-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="01a71-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="01a71-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="01a71-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="01a71-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="01a71-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="01a71-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="01a71-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="01a71-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="01a71-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="01a71-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="01a71-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-155">AttackSurfaceReductionOnlyExclusions</span><span class="sxs-lookup"><span data-stu-id="01a71-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01a71-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-158">AttackSurfaceReductionRules</span><span class="sxs-lookup"><span data-stu-id="01a71-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01a71-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="01a71-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-162">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-164">CloudBlockLevel</span><span class="sxs-lookup"><span data-stu-id="01a71-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-167">CloudExtendedTimeout</span><span class="sxs-lookup"><span data-stu-id="01a71-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-168">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-170">ControlledFolderAccessAllowedApplications</span><span class="sxs-lookup"><span data-stu-id="01a71-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01a71-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-173">ControlledFolderAccessProtectedFolders</span><span class="sxs-lookup"><span data-stu-id="01a71-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01a71-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="01a71-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-177">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-179">EnableControlledFolderAccess</span><span class="sxs-lookup"><span data-stu-id="01a71-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-180">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-182">EnableNetworkProtection</span><span class="sxs-lookup"><span data-stu-id="01a71-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-183">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="01a71-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01a71-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="01a71-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01a71-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="01a71-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01a71-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-193">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="01a71-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="01a71-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01a71-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01a71-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01a71-197">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01a71-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01a71-198">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="01a71-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="01a71-199">Pour cette classe, la chaîne est « Defender ».</span><span class="sxs-lookup"><span data-stu-id="01a71-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="01a71-200">**ID**</span><span class="sxs-lookup"><span data-stu-id="01a71-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01a71-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01a71-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01a71-203">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01a71-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01a71-204">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="01a71-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="01a71-205">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="01a71-205">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="01a71-206">PUAProtection</span><span class="sxs-lookup"><span data-stu-id="01a71-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-207">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="01a71-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-210">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="01a71-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-213">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="01a71-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-216">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="01a71-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-219">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="01a71-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-222">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="01a71-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-225">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="01a71-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-228">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a71-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a71-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="01a71-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a71-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01a71-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a71-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01a71-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01a71-233">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01a71-233">Requirements</span></span>



| <span data-ttu-id="01a71-234">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01a71-234">Requirement</span></span> | <span data-ttu-id="01a71-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="01a71-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a71-236">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01a71-236">Minimum supported client</span></span><br/> | <span data-ttu-id="01a71-237">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01a71-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01a71-238">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01a71-238">Minimum supported server</span></span><br/> | <span data-ttu-id="01a71-239">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="01a71-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="01a71-240">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="01a71-240">Namespace</span></span><br/>                | <span data-ttu-id="01a71-241">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="01a71-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="01a71-242">MOF</span><span class="sxs-lookup"><span data-stu-id="01a71-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01a71-243"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01a71-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="01a71-244">DLL</span><span class="sxs-lookup"><span data-stu-id="01a71-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01a71-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01a71-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a71-246">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01a71-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a71-247">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="01a71-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

