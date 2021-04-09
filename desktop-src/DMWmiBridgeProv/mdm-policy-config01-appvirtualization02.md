---
title: Classe MDM_Policy_Config01_AppVirtualization02
description: La \_ classe Config01 AppVirtualization02 de la stratégie MDM \_ \_ configure les stratégies de virtualisation des applications disponibles.
ms.assetid: d270704c-8652-4f97-89f7-fcb6e68ee6fe
keywords:
- Classe MDM_Policy_Config01_AppVirtualization02
- Classe MDM_Policy_Config01_AppVirtualization02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_AppVirtualization02
- MDM_Policy_Config01_AppVirtualization02.InstanceID
- MDM_Policy_Config01_AppVirtualization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871d09b306cff2833601100d9a645cde5c59e33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103325"
---
# <a name="mdm_policy_config01_appvirtualization02-class"></a><span data-ttu-id="a510f-105">\_Classe AppVirtualization02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="a510f-105">MDM\_Policy\_Config01\_AppVirtualization02 class</span></span>

<span data-ttu-id="a510f-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a510f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a510f-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a510f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a510f-108">La \_ classe Config01 AppVirtualization02 de la stratégie MDM \_ \_ configure les stratégies de virtualisation des applications disponibles.</span><span class="sxs-lookup"><span data-stu-id="a510f-108">The MDM\_Policy\_Config01\_AppVirtualization02 class configures the available app virtualization policies.</span></span>

<span data-ttu-id="a510f-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a510f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a510f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a510f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_AppVirtualization02
{
  string InstanceID;
  string ParentID;
  string AllowAppVClient;
  string AllowDynamicVirtualization;
  string AllowPackageCleanup;
  string AllowPackageScripts;
  string AllowPublishingRefreshUX;
  string AllowReportingServer;
  string AllowRoamingFileExclusions;
  string AllowRoamingRegistryExclusions;
  string AllowStreamingAutoload;
  string ClientCoexistenceAllowMigrationmode;
  string IntegrationAllowRootGlobal;
  string IntegrationAllowRootUser;
  string PublishingAllowServer1;
  string PublishingAllowServer2;
  string PublishingAllowServer3;
  string PublishingAllowServer4;
  string PublishingAllowServer5;
  string StreamingAllowCertificateFilterForClient_SSL;
  string StreamingAllowHighCostLaunch;
  string StreamingAllowLocationProvider;
  string StreamingAllowPackageInstallationRoot;
  string StreamingAllowPackageSourceRoot;
  string StreamingAllowReestablishmentInterval;
  string StreamingAllowReestablishmentRetries;
  string StreamingSharedContentStoreMode;
  string StreamingSupportBranchCache;
  string StreamingVerifyCertificateRevocationList;
  string VirtualComponentsAllowList;
};
```

## <a name="members"></a><span data-ttu-id="a510f-111">Membres</span><span class="sxs-lookup"><span data-stu-id="a510f-111">Members</span></span>

<span data-ttu-id="a510f-112">La **classe \_ \_ Config01 \_ AppVirtualization02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a510f-112">The **MDM\_Policy\_Config01\_AppVirtualization02** class has these types of members:</span></span>

-   [<span data-ttu-id="a510f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a510f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a510f-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a510f-114">Properties</span></span>

<span data-ttu-id="a510f-115">La **classe \_ \_ Config01 \_ AppVirtualization02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a510f-115">The **MDM\_Policy\_Config01\_AppVirtualization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a510f-116">AllowAppVClient</span><span class="sxs-lookup"><span data-stu-id="a510f-116">AllowAppVClient</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowappvclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-119">AllowDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="a510f-119">AllowDynamicVirtualization</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowdynamicvirtualization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-122">AllowPackageCleanup</span><span class="sxs-lookup"><span data-stu-id="a510f-122">AllowPackageCleanup</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagecleanup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-125">AllowPackageScripts</span><span class="sxs-lookup"><span data-stu-id="a510f-125">AllowPackageScripts</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagescripts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-128">AllowPublishingRefreshUX</span><span class="sxs-lookup"><span data-stu-id="a510f-128">AllowPublishingRefreshUX</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpublishingrefreshux)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-131">AllowReportingServer</span><span class="sxs-lookup"><span data-stu-id="a510f-131">AllowReportingServer</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowreportingserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-134">AllowRoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="a510f-134">AllowRoamingFileExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingfileexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-137">AllowRoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="a510f-137">AllowRoamingRegistryExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingregistryexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-140">AllowStreamingAutoload</span><span class="sxs-lookup"><span data-stu-id="a510f-140">AllowStreamingAutoload</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowstreamingautoload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-143">ClientCoexistenceAllowMigrationmode</span><span class="sxs-lookup"><span data-stu-id="a510f-143">ClientCoexistenceAllowMigrationmode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-clientcoexistenceallowmigrationmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a510f-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a510f-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a510f-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a510f-149">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a510f-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-150">IntegrationAllowRootGlobal</span><span class="sxs-lookup"><span data-stu-id="a510f-150">IntegrationAllowRootGlobal</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootglobal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-153">IntegrationAllowRootUser</span><span class="sxs-lookup"><span data-stu-id="a510f-153">IntegrationAllowRootUser</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootuser)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a510f-156">**ID**</span><span class="sxs-lookup"><span data-stu-id="a510f-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a510f-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a510f-159">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a510f-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-160">PublishingAllowServer1</span><span class="sxs-lookup"><span data-stu-id="a510f-160">PublishingAllowServer1</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver1)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-162">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-163">PublishingAllowServer2</span><span class="sxs-lookup"><span data-stu-id="a510f-163">PublishingAllowServer2</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver2)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-166">PublishingAllowServer3</span><span class="sxs-lookup"><span data-stu-id="a510f-166">PublishingAllowServer3</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-168">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-169">PublishingAllowServer4</span><span class="sxs-lookup"><span data-stu-id="a510f-169">PublishingAllowServer4</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-171">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-172">PublishingAllowServer5</span><span class="sxs-lookup"><span data-stu-id="a510f-172">PublishingAllowServer5</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver5)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-174">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-175">StreamingAllowCertificateFilterForClient \_ SSL</span><span class="sxs-lookup"><span data-stu-id="a510f-175">StreamingAllowCertificateFilterForClient\_SSL</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowcertificatefilterforclient-ssl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-177">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-177">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-178">StreamingAllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="a510f-178">StreamingAllowHighCostLaunch</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowhighcostlaunch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-180">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-180">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-181">StreamingAllowLocationProvider</span><span class="sxs-lookup"><span data-stu-id="a510f-181">StreamingAllowLocationProvider</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowlocationprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-183">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-183">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-184">StreamingAllowPackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="a510f-184">StreamingAllowPackageInstallationRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackageinstallationroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-186">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-186">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-187">StreamingAllowPackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="a510f-187">StreamingAllowPackageSourceRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackagesourceroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-189">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-190">StreamingAllowReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="a510f-190">StreamingAllowReestablishmentInterval</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-192">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-193">StreamingAllowReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="a510f-193">StreamingAllowReestablishmentRetries</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentretries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-195">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-196">StreamingSharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="a510f-196">StreamingSharedContentStoreMode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsharedcontentstoremode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-198">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-199">StreamingSupportBranchCache</span><span class="sxs-lookup"><span data-stu-id="a510f-199">StreamingSupportBranchCache</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsupportbranchcache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-201">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-202">StreamingVerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="a510f-202">StreamingVerifyCertificateRevocationList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingverifycertificaterevocationlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-204">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a510f-205">VirtualComponentsAllowList</span><span class="sxs-lookup"><span data-stu-id="a510f-205">VirtualComponentsAllowList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-virtualcomponentsallowlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a510f-206">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a510f-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a510f-207">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a510f-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a510f-208">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a510f-208">Requirements</span></span>



| <span data-ttu-id="a510f-209">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a510f-209">Requirement</span></span> | <span data-ttu-id="a510f-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="a510f-210">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a510f-211">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a510f-211">Minimum supported client</span></span><br/> | <span data-ttu-id="a510f-212">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a510f-212">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a510f-213">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a510f-213">Minimum supported server</span></span><br/> | <span data-ttu-id="a510f-214">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a510f-214">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a510f-215">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a510f-215">Namespace</span></span><br/>                | <span data-ttu-id="a510f-216">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="a510f-216">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a510f-217">MOF</span><span class="sxs-lookup"><span data-stu-id="a510f-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a510f-218"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a510f-218"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a510f-219">DLL</span><span class="sxs-lookup"><span data-stu-id="a510f-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a510f-220"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a510f-220"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

