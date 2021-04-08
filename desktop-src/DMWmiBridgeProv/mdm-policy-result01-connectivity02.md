---
title: Classe MDM_Policy_Result01_Connectivity02
description: La \_ classe Result01 Connectivity02 de la stratégie MDM \_ \_ représente les stratégies de connexion disponibles.
ms.assetid: af5f21f8-8010-4e5a-b75f-30032333d87d
keywords:
- Classe MDM_Policy_Result01_Connectivity02
- Classe MDM_Policy_Result01_Connectivity02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Connectivity02
- MDM_Policy_Result01_Connectivity02.InstanceID
- MDM_Policy_Result01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 723e8fa3287f99994d45fcc0a8bc5a09473a7563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843241"
---
# <a name="mdm_policy_result01_connectivity02-class"></a><span data-ttu-id="5b2cc-105">\_Classe Connectivity02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="5b2cc-105">MDM\_Policy\_Result01\_Connectivity02 class</span></span>

<span data-ttu-id="5b2cc-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5b2cc-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="5b2cc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5b2cc-108">La **classe \_ \_ Result01 \_ Connectivity02 de la stratégie MDM** représente les stratégies de connexion disponibles.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-108">The **MDM\_Policy\_Result01\_Connectivity02** class represents the connection policies available.</span></span>

<span data-ttu-id="5b2cc-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b2cc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b2cc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Connectivity02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBluetooth;
  sint32 AllowCellularData;
  sint32 AllowCellularDataRoaming;
  sint32 AllowVPNOverCellular;
  sint32 AllowVPNRoamingOverCellular;
  string DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards;
  string DisableDownloadingOfPrintDriversOverHTTP;
  string DiablePrintingOverHTTP;
  string HardenedUNCPaths;
  string ProhibitInstallationAndConfigurationOfNetworkBridge;
  sint32 DisallowNetworkConnectivityActiveTests;
  sint32 AllowConnectedDevices;
};
```

## <a name="members"></a><span data-ttu-id="5b2cc-111">Membres</span><span class="sxs-lookup"><span data-stu-id="5b2cc-111">Members</span></span>

<span data-ttu-id="5b2cc-112">La **classe \_ \_ Result01 \_ Connectivity02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5b2cc-112">The **MDM\_Policy\_Result01\_Connectivity02** class has these types of members:</span></span>

-   [<span data-ttu-id="5b2cc-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b2cc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b2cc-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b2cc-114">Properties</span></span>

<span data-ttu-id="5b2cc-115">La **classe \_ \_ Result01 \_ Connectivity02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-115">The **MDM\_Policy\_Result01\_Connectivity02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5b2cc-116">AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="5b2cc-116">AllowBluetooth</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b2cc-119">AllowCellularData</span><span class="sxs-lookup"><span data-stu-id="5b2cc-119">AllowCellularData</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b2cc-122">AllowCellularDataRoaming</span><span class="sxs-lookup"><span data-stu-id="5b2cc-122">AllowCellularDataRoaming</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b2cc-125">AllowConnectedDevices</span><span class="sxs-lookup"><span data-stu-id="5b2cc-125">AllowConnectedDevices</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b2cc-128">AllowVPNOverCellular</span><span class="sxs-lookup"><span data-stu-id="5b2cc-128">AllowVPNOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b2cc-131">AllowVPNRoamingOverCellular</span><span class="sxs-lookup"><span data-stu-id="5b2cc-131">AllowVPNRoamingOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b2cc-134">DiablePrintingOverHTTP</span><span class="sxs-lookup"><span data-stu-id="5b2cc-134">DiablePrintingOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b2cc-137">DisableDownloadingOfPrintDriversOverHTTP</span><span class="sxs-lookup"><span data-stu-id="5b2cc-137">DisableDownloadingOfPrintDriversOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b2cc-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span><span class="sxs-lookup"><span data-stu-id="5b2cc-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b2cc-143">DisallowNetworkConnectivityActiveTests</span><span class="sxs-lookup"><span data-stu-id="5b2cc-143">DisallowNetworkConnectivityActiveTests</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b2cc-146">HardenedUNCPaths</span><span class="sxs-lookup"><span data-stu-id="5b2cc-146">HardenedUNCPaths</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5b2cc-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b2cc-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5b2cc-153">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="5b2cc-154">Pour cette classe, la chaîne est « connectivity ».</span><span class="sxs-lookup"><span data-stu-id="5b2cc-154">For this class, the string is "Connectivity".</span></span>

</dd> <dt>

<span data-ttu-id="5b2cc-155">**ID**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b2cc-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-158">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5b2cc-159">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="5b2cc-160">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="5b2cc-160">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="5b2cc-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span><span class="sxs-lookup"><span data-stu-id="5b2cc-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b2cc-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b2cc-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b2cc-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b2cc-164">Requirements</span></span>



| <span data-ttu-id="5b2cc-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b2cc-165">Requirement</span></span> | <span data-ttu-id="5b2cc-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b2cc-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2cc-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b2cc-167">Minimum supported client</span></span><br/> | <span data-ttu-id="5b2cc-168">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b2cc-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5b2cc-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b2cc-169">Minimum supported server</span></span><br/> | <span data-ttu-id="5b2cc-170">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b2cc-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5b2cc-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5b2cc-171">Namespace</span></span><br/>                | <span data-ttu-id="5b2cc-172">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="5b2cc-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5b2cc-173">MOF</span><span class="sxs-lookup"><span data-stu-id="5b2cc-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b2cc-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b2cc-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b2cc-175">DLL</span><span class="sxs-lookup"><span data-stu-id="5b2cc-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b2cc-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b2cc-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b2cc-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b2cc-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b2cc-178">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="5b2cc-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

