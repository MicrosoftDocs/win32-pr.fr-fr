---
title: Classe MDM_Policy_Result01_DeliveryOptimization02
description: La \_ classe Result01 DeliveryOptimization02 de la stratégie MDM \_ \_ représente les stratégies d’optimisation de la remise disponibles.
ms.assetid: 0f8a6de1-0f6c-4ee2-9235-9b5dc855f8c4
keywords:
- Classe MDM_Policy_Result01_DeliveryOptimization02
- Classe MDM_Policy_Result01_DeliveryOptimization02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeliveryOptimization02
- MDM_Policy_Result01_DeliveryOptimization02.InstanceID
- MDM_Policy_Result01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69408228b2ed67c12de83575ddc524387498e91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740685"
---
# <a name="mdm_policy_result01_deliveryoptimization02-class"></a><span data-ttu-id="fd5d0-105">\_Classe DeliveryOptimization02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="fd5d0-105">MDM\_Policy\_Result01\_DeliveryOptimization02 class</span></span>

<span data-ttu-id="fd5d0-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="fd5d0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fd5d0-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="fd5d0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fd5d0-108">La **classe \_ \_ Result01 \_ DeliveryOptimization02 de la stratégie MDM** représente les stratégies d’optimisation de la remise disponibles.</span><span class="sxs-lookup"><span data-stu-id="fd5d0-108">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class represents the delivery optimization policies available.</span></span>

<span data-ttu-id="fd5d0-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fd5d0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd5d0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd5d0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeliveryOptimization02
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

## <a name="members"></a><span data-ttu-id="fd5d0-111">Membres</span><span class="sxs-lookup"><span data-stu-id="fd5d0-111">Members</span></span>

<span data-ttu-id="fd5d0-112">La **classe \_ \_ Result01 \_ DeliveryOptimization02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fd5d0-112">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class has these types of members:</span></span>

-   [<span data-ttu-id="fd5d0-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd5d0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd5d0-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd5d0-114">Properties</span></span>

<span data-ttu-id="fd5d0-115">La **classe \_ \_ Result01 \_ DeliveryOptimization02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd5d0-115">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fd5d0-116">DOAbsoluteMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="fd5d0-116">DOAbsoluteMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-119">DOAllowVPNPeerCaching</span><span class="sxs-lookup"><span data-stu-id="fd5d0-119">DOAllowVPNPeerCaching</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-122">DOCacheHost</span><span class="sxs-lookup"><span data-stu-id="fd5d0-122">DOCacheHost</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-125">DODownloadMode</span><span class="sxs-lookup"><span data-stu-id="fd5d0-125">DODownloadMode</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-128">DOGroupID</span><span class="sxs-lookup"><span data-stu-id="fd5d0-128">DOGroupID</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-131">DOMaxCacheAge</span><span class="sxs-lookup"><span data-stu-id="fd5d0-131">DOMaxCacheAge</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-134">DOMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="fd5d0-134">DOMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-137">DOMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="fd5d0-137">DOMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-140">DOMaxUploadBandwidth</span><span class="sxs-lookup"><span data-stu-id="fd5d0-140">DOMaxUploadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-143">DOMinBackgroundQos</span><span class="sxs-lookup"><span data-stu-id="fd5d0-143">DOMinBackgroundQos</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-146">DOMinBatteryPercentageAllowedToUpload</span><span class="sxs-lookup"><span data-stu-id="fd5d0-146">DOMinBatteryPercentageAllowedToUpload</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-149">DOMinDiskSizeAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="fd5d0-149">DOMinDiskSizeAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-152">DOMinFileSizeToCache</span><span class="sxs-lookup"><span data-stu-id="fd5d0-152">DOMinFileSizeToCache</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-155">DOMinRAMAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="fd5d0-155">DOMinRAMAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-156">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-158">DOModifyCacheDrive</span><span class="sxs-lookup"><span data-stu-id="fd5d0-158">DOModifyCacheDrive</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-161">DOMonthlyUploadDataCap</span><span class="sxs-lookup"><span data-stu-id="fd5d0-161">DOMonthlyUploadDataCap</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-162">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd5d0-164">DOPercentageMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="fd5d0-164">DOPercentageMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd5d0-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fd5d0-167">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-167">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5d0-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-170">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd5d0-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd5d0-171">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fd5d0-171">Identifies the name of the parent node.</span></span> <span data-ttu-id="fd5d0-172">Pour cette classe, la chaîne est « DeliveryOptimization ».</span><span class="sxs-lookup"><span data-stu-id="fd5d0-172">For this class, the string is "DeliveryOptimization".</span></span>

</dd> <dt>

<span data-ttu-id="fd5d0-173">**ID**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5d0-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5d0-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5d0-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5d0-176">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd5d0-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd5d0-177">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fd5d0-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="fd5d0-178">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="fd5d0-178">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd5d0-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd5d0-179">Requirements</span></span>



| <span data-ttu-id="fd5d0-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd5d0-180">Requirement</span></span> | <span data-ttu-id="fd5d0-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd5d0-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5d0-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd5d0-182">Minimum supported client</span></span><br/> | <span data-ttu-id="fd5d0-183">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd5d0-183">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd5d0-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd5d0-184">Minimum supported server</span></span><br/> | <span data-ttu-id="fd5d0-185">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd5d0-185">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fd5d0-186">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd5d0-186">Namespace</span></span><br/>                | <span data-ttu-id="fd5d0-187">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="fd5d0-187">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="fd5d0-188">MOF</span><span class="sxs-lookup"><span data-stu-id="fd5d0-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd5d0-189"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd5d0-189"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd5d0-190">DLL</span><span class="sxs-lookup"><span data-stu-id="fd5d0-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd5d0-191"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd5d0-191"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd5d0-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd5d0-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd5d0-193">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="fd5d0-193">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

