---
title: Classe MDM_Policy_Result01_System02
description: La \_ classe Result01 System02 de la stratégie MDM \_ \_ représente les stratégies système disponibles.
ms.assetid: 9A0D9688-9062-429F-897F-75705DC8FD79
keywords:
- Classe MDM_Policy_Result01_System02
- Classe MDM_Policy_Result01_System02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_System02
- MDM_Policy_Result01_System02.InstanceID
- MDM_Policy_Result01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffedc3c4e0eda857c071a3174690ad9677fd97da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741196"
---
# <a name="mdm_policy_result01_system02-class"></a><span data-ttu-id="fa751-105">\_Classe System02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="fa751-105">MDM\_Policy\_Result01\_System02 class</span></span>

<span data-ttu-id="fa751-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="fa751-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fa751-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="fa751-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fa751-108">La **classe \_ \_ Result01 \_ System02 de la stratégie MDM** représente les stratégies système disponibles.</span><span class="sxs-lookup"><span data-stu-id="fa751-108">The **MDM\_Policy\_Result01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="fa751-109">Ces stratégies déterminent les configurations système autorisées.</span><span class="sxs-lookup"><span data-stu-id="fa751-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="fa751-110">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fa751-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa751-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa751-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_System02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBuildPreview;
  sint32 AllowEmbeddedMode;
  sint32 AllowExperimentation;
  sint32 AllowFontProviders;
  sint32 AllowLocation;
  sint32 AllowStorageCard;
  sint32 AllowTelemetry;
  string TelemetryProxy;
  sint32 AllowUserToResetPhone;
  string BootStartDriverInitialization;
  sint32 DisableEnterpriseAuthProxy;
  sint32 DisableOneDriveFileSync;
  string DisableSystemRestore;
  sint32 LimitEnhancedDiagnosticDataWindowsAnalytics;
  sint32 FeedbackHubAlwaysSaveDiagnosticsLocally;
};
```

## <a name="members"></a><span data-ttu-id="fa751-112">Membres</span><span class="sxs-lookup"><span data-stu-id="fa751-112">Members</span></span>

<span data-ttu-id="fa751-113">La **classe \_ \_ Result01 \_ System02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fa751-113">The **MDM\_Policy\_Result01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="fa751-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa751-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa751-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa751-115">Properties</span></span>

<span data-ttu-id="fa751-116">La **classe \_ \_ Result01 \_ System02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fa751-116">The **MDM\_Policy\_Result01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fa751-117">AllowBuildPreview</span><span class="sxs-lookup"><span data-stu-id="fa751-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-118">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-120">AllowEmbeddedMode</span><span class="sxs-lookup"><span data-stu-id="fa751-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-121">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-123">AllowExperimentation</span><span class="sxs-lookup"><span data-stu-id="fa751-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-124">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-126">AllowFontProviders</span><span class="sxs-lookup"><span data-stu-id="fa751-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-127">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="fa751-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-130">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="fa751-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-133">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="fa751-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-136">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-138">AllowUserToResetPhone</span><span class="sxs-lookup"><span data-stu-id="fa751-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-139">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-141">BootStartDriverInitialization</span><span class="sxs-lookup"><span data-stu-id="fa751-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa751-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="fa751-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-145">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-146">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-147">DisableOneDriveFileSync</span><span class="sxs-lookup"><span data-stu-id="fa751-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-148">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-149">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-150">DisableSystemRestore</span><span class="sxs-lookup"><span data-stu-id="fa751-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa751-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa751-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span><span class="sxs-lookup"><span data-stu-id="fa751-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-154">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fa751-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fa751-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa751-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa751-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa751-159">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa751-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa751-160">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fa751-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="fa751-161">Pour cette classe, la chaîne est « System ».</span><span class="sxs-lookup"><span data-stu-id="fa751-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="fa751-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="fa751-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-163">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa751-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-164">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fa751-165">**ID**</span><span class="sxs-lookup"><span data-stu-id="fa751-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa751-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa751-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa751-168">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa751-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa751-169">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fa751-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="fa751-170">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="fa751-170">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="fa751-171">TelemetryProxy</span><span class="sxs-lookup"><span data-stu-id="fa751-171">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa751-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa751-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa751-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa751-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa751-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa751-174">Requirements</span></span>



| <span data-ttu-id="fa751-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa751-175">Requirement</span></span> | <span data-ttu-id="fa751-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa751-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa751-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa751-177">Minimum supported client</span></span><br/> | <span data-ttu-id="fa751-178">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa751-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa751-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa751-179">Minimum supported server</span></span><br/> | <span data-ttu-id="fa751-180">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa751-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fa751-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fa751-181">Namespace</span></span><br/>                | <span data-ttu-id="fa751-182">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="fa751-182">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="fa751-183">MOF</span><span class="sxs-lookup"><span data-stu-id="fa751-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa751-184"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa751-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa751-185">DLL</span><span class="sxs-lookup"><span data-stu-id="fa751-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa751-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa751-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa751-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa751-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa751-188">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="fa751-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

