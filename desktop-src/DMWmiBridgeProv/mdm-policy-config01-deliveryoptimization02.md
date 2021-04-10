---
title: Classe MDM_Policy_Config01_DeliveryOptimization02
description: La \_ classe Config01 DeliveryOptimization02 de la stratégie MDM \_ \_ représente les stratégies d’optimisation de la remise disponibles.
ms.assetid: 10dfb751-f044-4f30-90e0-af0fcb0931fb
keywords:
- Classe MDM_Policy_Config01_DeliveryOptimization02
- Classe MDM_Policy_Config01_DeliveryOptimization02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeliveryOptimization02
- MDM_Policy_Config01_DeliveryOptimization02.InstanceID
- MDM_Policy_Config01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb9675f87a5bf9951e125bded69ae5eb10feb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103308"
---
# <a name="mdm_policy_config01_deliveryoptimization02-class"></a><span data-ttu-id="55a9f-105">\_Classe DeliveryOptimization02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="55a9f-105">MDM\_Policy\_Config01\_DeliveryOptimization02 class</span></span>

<span data-ttu-id="55a9f-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="55a9f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="55a9f-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="55a9f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="55a9f-108">La **classe \_ \_ Config01 \_ DeliveryOptimization02 de la stratégie MDM** représente les stratégies d’optimisation de la remise disponibles.</span><span class="sxs-lookup"><span data-stu-id="55a9f-108">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class represents the delivery optimization policies available.</span></span>

<span data-ttu-id="55a9f-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="55a9f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a9f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55a9f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeliveryOptimization02
{
  string InstanceID;
  string ParentID;
  sint32 DOAbsoluteMaxCacheSize;
  sint32 DOAllowVPNPeerCaching;
  string DOCacheHost;
  string DOGroupID;
  sint32 DOMaxUploadBandwidth;
  sint32 DOPercentageMaxDownloadBandwidth;
  sint32 DOMonthlyUploadDataCap;
  string DOModifyCacheDrive;
  sint32 DOMinBackgroundQos;
  sint32 DOMinRAMAllowedToPeer;
  sint32 DOMinFileSizeToCache;
  sint32 DOMinDiskSizeAllowedToPeer;
  sint32 DOMinBatteryPercentageAllowedToUpload;
  sint32 DOMaxCacheSize;
  sint32 DOMaxDownloadBandwidth;
  sint32 DOMaxCacheAge;
  sint32 DODownloadMode;
};
```

## <a name="members"></a><span data-ttu-id="55a9f-111">Membres</span><span class="sxs-lookup"><span data-stu-id="55a9f-111">Members</span></span>

<span data-ttu-id="55a9f-112">La **classe \_ \_ Config01 \_ DeliveryOptimization02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="55a9f-112">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class has these types of members:</span></span>

-   [<span data-ttu-id="55a9f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="55a9f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55a9f-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="55a9f-114">Properties</span></span>

<span data-ttu-id="55a9f-115">La **classe \_ \_ Config01 \_ DeliveryOptimization02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="55a9f-115">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="55a9f-116">DOAbsoluteMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="55a9f-116">DOAbsoluteMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-119">DOAllowVPNPeerCaching</span><span class="sxs-lookup"><span data-stu-id="55a9f-119">DOAllowVPNPeerCaching</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-122">DOCacheHost</span><span class="sxs-lookup"><span data-stu-id="55a9f-122">DOCacheHost</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55a9f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-125">DODownloadMode</span><span class="sxs-lookup"><span data-stu-id="55a9f-125">DODownloadMode</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-128">DOGroupID</span><span class="sxs-lookup"><span data-stu-id="55a9f-128">DOGroupID</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55a9f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-131">DOMaxCacheAge</span><span class="sxs-lookup"><span data-stu-id="55a9f-131">DOMaxCacheAge</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-134">DOMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="55a9f-134">DOMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-137">DOMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="55a9f-137">DOMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-140">DOMaxUploadBandwidth</span><span class="sxs-lookup"><span data-stu-id="55a9f-140">DOMaxUploadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-143">DOMinBackgroundQos</span><span class="sxs-lookup"><span data-stu-id="55a9f-143">DOMinBackgroundQos</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-146">DOMinBatteryPercentageAllowedToUpload</span><span class="sxs-lookup"><span data-stu-id="55a9f-146">DOMinBatteryPercentageAllowedToUpload</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-149">DOMinDiskSizeAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="55a9f-149">DOMinDiskSizeAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-152">DOMinFileSizeToCache</span><span class="sxs-lookup"><span data-stu-id="55a9f-152">DOMinFileSizeToCache</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-155">DOMinRAMAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="55a9f-155">DOMinRAMAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-156">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-158">DOModifyCacheDrive</span><span class="sxs-lookup"><span data-stu-id="55a9f-158">DOModifyCacheDrive</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55a9f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-161">DOMonthlyUploadDataCap</span><span class="sxs-lookup"><span data-stu-id="55a9f-161">DOMonthlyUploadDataCap</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-162">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a9f-164">DOPercentageMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="55a9f-164">DOPercentageMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="55a9f-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55a9f-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="55a9f-167">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="55a9f-167">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55a9f-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="55a9f-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-170">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55a9f-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="55a9f-171">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="55a9f-171">Identifies the name of the parent node.</span></span> <span data-ttu-id="55a9f-172">Pour cette classe, la chaîne est « DeliveryOptimization ».</span><span class="sxs-lookup"><span data-stu-id="55a9f-172">For this class, the string is "DeliveryOptimization".</span></span>

</dd> <dt>

<span data-ttu-id="55a9f-173">**ID**</span><span class="sxs-lookup"><span data-stu-id="55a9f-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9f-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55a9f-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="55a9f-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55a9f-176">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55a9f-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="55a9f-177">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="55a9f-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="55a9f-178">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="55a9f-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55a9f-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55a9f-179">Requirements</span></span>



| <span data-ttu-id="55a9f-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55a9f-180">Requirement</span></span> | <span data-ttu-id="55a9f-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="55a9f-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a9f-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55a9f-182">Minimum supported client</span></span><br/> | <span data-ttu-id="55a9f-183">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55a9f-183">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55a9f-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55a9f-184">Minimum supported server</span></span><br/> | <span data-ttu-id="55a9f-185">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="55a9f-185">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="55a9f-186">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="55a9f-186">Namespace</span></span><br/>                | <span data-ttu-id="55a9f-187">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="55a9f-187">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="55a9f-188">MOF</span><span class="sxs-lookup"><span data-stu-id="55a9f-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55a9f-189"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55a9f-189"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="55a9f-190">DLL</span><span class="sxs-lookup"><span data-stu-id="55a9f-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55a9f-191"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a9f-191"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a9f-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55a9f-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a9f-193">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="55a9f-193">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

