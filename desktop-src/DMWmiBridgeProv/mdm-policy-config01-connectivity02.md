---
title: Classe MDM_Policy_Config01_Connectivity02
description: La \_ classe Config01 Connectivity02 de la stratégie MDM \_ \_ représente les stratégies de connexion disponibles.
ms.assetid: 670e48c2-1af1-45e9-81c6-cdf3a310240f
keywords:
- Classe MDM_Policy_Config01_Connectivity02
- Classe MDM_Policy_Config01_Connectivity02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Connectivity02
- MDM_Policy_Config01_Connectivity02.InstanceID
- MDM_Policy_Config01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b39b897998bf47c5f5411456ccae7fcb6927aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740965"
---
# <a name="mdm_policy_config01_connectivity02-class"></a><span data-ttu-id="63a49-105">\_Classe Connectivity02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="63a49-105">MDM\_Policy\_Config01\_Connectivity02 class</span></span>

<span data-ttu-id="63a49-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="63a49-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="63a49-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="63a49-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="63a49-108">La **classe \_ \_ Config01 \_ Connectivity02 de la stratégie MDM** représente les stratégies de connexion disponibles.</span><span class="sxs-lookup"><span data-stu-id="63a49-108">The **MDM\_Policy\_Config01\_Connectivity02** class represents the connection policies available.</span></span>

<span data-ttu-id="63a49-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="63a49-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a49-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63a49-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Connectivity02
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

## <a name="members"></a><span data-ttu-id="63a49-111">Membres</span><span class="sxs-lookup"><span data-stu-id="63a49-111">Members</span></span>

<span data-ttu-id="63a49-112">La **classe \_ \_ Config01 \_ Connectivity02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="63a49-112">The **MDM\_Policy\_Config01\_Connectivity02** class has these types of members:</span></span>

-   [<span data-ttu-id="63a49-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63a49-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63a49-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63a49-114">Properties</span></span>

<span data-ttu-id="63a49-115">La **classe \_ \_ Config01 \_ Connectivity02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="63a49-115">The **MDM\_Policy\_Config01\_Connectivity02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="63a49-116">AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="63a49-116">AllowBluetooth</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="63a49-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63a49-119">AllowCellularData</span><span class="sxs-lookup"><span data-stu-id="63a49-119">AllowCellularData</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="63a49-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63a49-122">AllowCellularDataRoaming</span><span class="sxs-lookup"><span data-stu-id="63a49-122">AllowCellularDataRoaming</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="63a49-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63a49-125">AllowConnectedDevices</span><span class="sxs-lookup"><span data-stu-id="63a49-125">AllowConnectedDevices</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="63a49-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63a49-128">AllowVPNOverCellular</span><span class="sxs-lookup"><span data-stu-id="63a49-128">AllowVPNOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="63a49-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63a49-131">AllowVPNRoamingOverCellular</span><span class="sxs-lookup"><span data-stu-id="63a49-131">AllowVPNRoamingOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="63a49-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63a49-134">DiablePrintingOverHTTP</span><span class="sxs-lookup"><span data-stu-id="63a49-134">DiablePrintingOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63a49-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63a49-137">DisableDownloadingOfPrintDriversOverHTTP</span><span class="sxs-lookup"><span data-stu-id="63a49-137">DisableDownloadingOfPrintDriversOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63a49-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63a49-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span><span class="sxs-lookup"><span data-stu-id="63a49-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63a49-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63a49-143">DisallowNetworkConnectivityActiveTests</span><span class="sxs-lookup"><span data-stu-id="63a49-143">DisallowNetworkConnectivityActiveTests</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="63a49-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63a49-146">HardenedUNCPaths</span><span class="sxs-lookup"><span data-stu-id="63a49-146">HardenedUNCPaths</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63a49-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="63a49-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="63a49-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63a49-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63a49-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a49-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63a49-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63a49-153">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="63a49-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="63a49-154">Pour cette classe, la chaîne est « connectivity ».</span><span class="sxs-lookup"><span data-stu-id="63a49-154">For this class, the string is "Connectivity".</span></span>

</dd> <dt>

<span data-ttu-id="63a49-155">**ID**</span><span class="sxs-lookup"><span data-stu-id="63a49-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63a49-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63a49-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a49-158">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63a49-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63a49-159">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="63a49-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="63a49-160">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="63a49-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="63a49-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span><span class="sxs-lookup"><span data-stu-id="63a49-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a49-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63a49-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a49-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63a49-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63a49-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63a49-164">Requirements</span></span>



| <span data-ttu-id="63a49-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63a49-165">Requirement</span></span> | <span data-ttu-id="63a49-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="63a49-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63a49-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63a49-167">Minimum supported client</span></span><br/> | <span data-ttu-id="63a49-168">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63a49-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63a49-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63a49-169">Minimum supported server</span></span><br/> | <span data-ttu-id="63a49-170">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="63a49-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="63a49-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63a49-171">Namespace</span></span><br/>                | <span data-ttu-id="63a49-172">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="63a49-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="63a49-173">MOF</span><span class="sxs-lookup"><span data-stu-id="63a49-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63a49-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63a49-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="63a49-175">DLL</span><span class="sxs-lookup"><span data-stu-id="63a49-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63a49-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63a49-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a49-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63a49-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a49-178">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="63a49-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

