---
title: Classe MDM_VPNv2_TrafficFilterList02_App04
description: La \_ \_ classe App04 MDM TrafficFilterList02 fournit la configuration des applications autorisées sur l’interface VPN.
ms.assetid: a56d004b-8fe3-4187-8aad-962f1cab8f7f
keywords:
- Classe MDM_VPNv2_TrafficFilterList02_App04
- Classe MDM_VPNv2_TrafficFilterList02_App04, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_App04
- MDM_VPNv2_TrafficFilterList02_App04.InstanceID
- MDM_VPNv2_TrafficFilterList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b1cd3edbfec5fa270f8404983af57dba4fad31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104953"
---
# <a name="mdm_vpnv2_trafficfilterlist02_app04-class"></a><span data-ttu-id="1be8d-105">\_ \_ Classe App04 VPNV2 TrafficFilterList02 MDM \_</span><span class="sxs-lookup"><span data-stu-id="1be8d-105">MDM\_VPNv2\_TrafficFilterList02\_App04 class</span></span>

<span data-ttu-id="1be8d-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="1be8d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1be8d-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="1be8d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1be8d-108">La **classe \_ \_ App04 MDM TrafficFilterList02** fournit la configuration des applications autorisées sur l’interface VPN.</span><span class="sxs-lookup"><span data-stu-id="1be8d-108">The **MDM\_TrafficFilterList02\_App04** class provides configuration of the apps that are allowed over the VPN interface.</span></span>

<span data-ttu-id="1be8d-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1be8d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1be8d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1be8d-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="1be8d-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1be8d-111">Members</span></span>

<span data-ttu-id="1be8d-112">La **classe \_ \_ \_ App04 VPNv2 TrafficFilterList02 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1be8d-112">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="1be8d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1be8d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1be8d-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1be8d-114">Properties</span></span>

<span data-ttu-id="1be8d-115">La **classe \_ \_ \_ App04 VPNv2 TrafficFilterList02 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1be8d-115">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1be8d-116">Id</span><span class="sxs-lookup"><span data-stu-id="1be8d-116">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be8d-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1be8d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1be8d-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1be8d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1be8d-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1be8d-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be8d-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1be8d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1be8d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1be8d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1be8d-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1be8d-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1be8d-123">Par règle VPN d’application.</span><span class="sxs-lookup"><span data-stu-id="1be8d-123">Per app VPN rule.</span></span> <span data-ttu-id="1be8d-124">Cela permet d’autoriser uniquement les applications spécifiées sur l’interface VPN.</span><span class="sxs-lookup"><span data-stu-id="1be8d-124">This will allow only the apps specified to be allowed over the VPN interface.</span></span> <span data-ttu-id="1be8d-125">Pour cette classe, la chaîne est « app ».</span><span class="sxs-lookup"><span data-stu-id="1be8d-125">For this class, the string is "App"</span></span>

</dd> <dt>

<span data-ttu-id="1be8d-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="1be8d-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be8d-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1be8d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1be8d-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1be8d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1be8d-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1be8d-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1be8d-130">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="1be8d-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="1be8d-131">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*»</span><span class="sxs-lookup"><span data-stu-id="1be8d-131">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span></span>

</dd> <dt>

[<span data-ttu-id="1be8d-132">Type</span><span class="sxs-lookup"><span data-stu-id="1be8d-132">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be8d-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1be8d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1be8d-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1be8d-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1be8d-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1be8d-135">Requirements</span></span>



| <span data-ttu-id="1be8d-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1be8d-136">Requirement</span></span> | <span data-ttu-id="1be8d-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="1be8d-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1be8d-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1be8d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1be8d-139">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1be8d-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1be8d-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1be8d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1be8d-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1be8d-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1be8d-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1be8d-142">Namespace</span></span><br/>                | <span data-ttu-id="1be8d-143">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="1be8d-143">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1be8d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="1be8d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1be8d-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1be8d-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1be8d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1be8d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1be8d-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1be8d-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1be8d-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1be8d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be8d-149">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="1be8d-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

