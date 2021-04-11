---
title: Classe MDM_VPNv2_TrafficFilterList02_01
description: La \_ classe MDM VPNv2 \_ TrafficFilterList02 \_ 01 contient une liste facultative de règles. Seul le trafic conforme à ces règles peut être envoyé via l’interface VPN.
ms.assetid: 3cffe96d-7454-43a1-aa5b-33e820369e7e
keywords:
- Classe MDM_VPNv2_TrafficFilterList02_01
- Classe MDM_VPNv2_TrafficFilterList02_01, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_01
- MDM_VPNv2_TrafficFilterList02_01.InstanceID
- MDM_VPNv2_TrafficFilterList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3005026a85aa118a4122e073579fcb06389a9fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104956"
---
# <a name="mdm_vpnv2_trafficfilterlist02_01-class"></a><span data-ttu-id="c4c11-106">\_Classe VPNv2 \_ TRAFFICFILTERLIST02 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="c4c11-106">MDM\_VPNv2\_TrafficFilterList02\_01 class</span></span>

<span data-ttu-id="c4c11-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c4c11-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c4c11-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c4c11-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c4c11-109">La classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** contient une liste facultative de règles.</span><span class="sxs-lookup"><span data-stu-id="c4c11-109">The **MDM\_VPNv2\_TrafficFilterList02\_01** class contains an optional list of rules.</span></span> <span data-ttu-id="c4c11-110">Seul le trafic conforme à ces règles peut être envoyé via l’interface VPN.</span><span class="sxs-lookup"><span data-stu-id="c4c11-110">Only traffic that matches these rules can be sent via the VPN Interface.</span></span>

<span data-ttu-id="c4c11-111">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c4c11-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c11-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4c11-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_01
{
  string InstanceID;
  string ParentID;
  string Claims;
  sint32 Protocol;
  string LocalPortRanges;
  string RemotePortRanges;
  string LocalAddressRanges;
  string RemoteAddressRanges;
  string RoutingPolicyType;
};
```

## <a name="members"></a><span data-ttu-id="c4c11-113">Membres</span><span class="sxs-lookup"><span data-stu-id="c4c11-113">Members</span></span>

<span data-ttu-id="c4c11-114">La classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c4c11-114">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="c4c11-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4c11-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4c11-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4c11-116">Properties</span></span>

<span data-ttu-id="c4c11-117">La classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c4c11-117">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c4c11-118">Revendications</span><span class="sxs-lookup"><span data-stu-id="c4c11-118">Claims</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-claims)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4c11-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4c11-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4c11-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c4c11-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c4c11-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4c11-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4c11-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c4c11-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4c11-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c4c11-125">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c4c11-125">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="c4c11-126">LocalAddressRanges</span><span class="sxs-lookup"><span data-stu-id="c4c11-126">LocalAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4c11-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4c11-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4c11-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c4c11-129">LocalPortRanges</span><span class="sxs-lookup"><span data-stu-id="c4c11-129">LocalPortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4c11-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4c11-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4c11-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c4c11-132">**ID**</span><span class="sxs-lookup"><span data-stu-id="c4c11-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4c11-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4c11-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c4c11-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-135">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4c11-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c4c11-136">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c4c11-136">Describes the full path to the parent node.</span></span> <span data-ttu-id="c4c11-137">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList »</span><span class="sxs-lookup"><span data-stu-id="c4c11-137">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span></span>

</dd> <dt>

[<span data-ttu-id="c4c11-138">Protocole</span><span class="sxs-lookup"><span data-stu-id="c4c11-138">Protocol</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4c11-139">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c4c11-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4c11-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c4c11-141">RemoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="c4c11-141">RemoteAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4c11-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4c11-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4c11-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c4c11-144">RemotePortRanges</span><span class="sxs-lookup"><span data-stu-id="c4c11-144">RemotePortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4c11-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4c11-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-146">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4c11-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c4c11-147">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="c4c11-147">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4c11-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4c11-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4c11-149">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4c11-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4c11-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4c11-150">Requirements</span></span>



| <span data-ttu-id="c4c11-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4c11-151">Requirement</span></span> | <span data-ttu-id="c4c11-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4c11-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c11-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4c11-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c11-154">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4c11-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4c11-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4c11-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c11-156">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4c11-156">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c4c11-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c4c11-157">Namespace</span></span><br/>                | <span data-ttu-id="c4c11-158">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c4c11-158">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c4c11-159">MOF</span><span class="sxs-lookup"><span data-stu-id="c4c11-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4c11-160"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4c11-160"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4c11-161">DLL</span><span class="sxs-lookup"><span data-stu-id="c4c11-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4c11-162"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4c11-162"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4c11-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4c11-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c11-164">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="c4c11-164">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

