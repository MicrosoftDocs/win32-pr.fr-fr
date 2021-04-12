---
title: Classe MDM_VPNv2_AppTriggerList02_App04
description: La \_ classe VPNv2AppTriggerList02 \_ App04 MDM décrit une liste d’applications définies pour déclencher le VPN.
ms.assetid: d17ec7b9-8a66-47da-8373-81b56168b495
keywords:
- Classe MDM_VPNv2_AppTriggerList02_App04
- Classe MDM_VPNv2_AppTriggerList02_App04, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_AppTriggerList02_App04
- MDM_VPNv2_AppTriggerList02_App04.InstanceID
- MDM_VPNv2_AppTriggerList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62685ea94b99e843625e87e7c653a2ff19ab737d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104167"
---
# <a name="mdm_vpnv2_apptriggerlist02_app04-class"></a><span data-ttu-id="e4c01-105">\_ \_ Classe App04 VPNV2 AppTriggerList02 MDM \_</span><span class="sxs-lookup"><span data-stu-id="e4c01-105">MDM\_VPNv2\_AppTriggerList02\_App04 class</span></span>

<span data-ttu-id="e4c01-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="e4c01-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e4c01-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="e4c01-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e4c01-108">La **classe \_ VPNv2AppTriggerList02 \_ App04 MDM** décrit une liste d’applications définies pour déclencher le VPN.</span><span class="sxs-lookup"><span data-stu-id="e4c01-108">The **MDM\_VPNv2AppTriggerList02\_App04** class describes a list of applications set to trigger the VPN.</span></span>

<span data-ttu-id="e4c01-109">Si l’une de ces applications est lancée et que le profil VPN est actuellement le profil actif, ce profil VPN est déclenché pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="e4c01-109">If any of these apps are launched and the VPN profile is currently the active profile, this VPN profile will be triggered to connect.</span></span>

<span data-ttu-id="e4c01-110">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e4c01-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c01-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4c01-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_AppTriggerList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="e4c01-112">Membres</span><span class="sxs-lookup"><span data-stu-id="e4c01-112">Members</span></span>

<span data-ttu-id="e4c01-113">La **classe \_ \_ \_ App04 VPNv2 AppTriggerList02 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e4c01-113">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="e4c01-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e4c01-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4c01-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e4c01-115">Properties</span></span>

<span data-ttu-id="e4c01-116">La **classe \_ \_ \_ App04 VPNv2 AppTriggerList02 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e4c01-116">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e4c01-117">Id</span><span class="sxs-lookup"><span data-stu-id="e4c01-117">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e4c01-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e4c01-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4c01-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e4c01-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e4c01-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4c01-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e4c01-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-124">Nœud d’application sous l’ID de ligne.</span><span class="sxs-lookup"><span data-stu-id="e4c01-124">App Node under the Row Id.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="e4c01-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e4c01-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4c01-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e4c01-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="e4c01-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="e4c01-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*»</span><span class="sxs-lookup"><span data-stu-id="e4c01-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span></span>

</dd> <dt>

[<span data-ttu-id="e4c01-131">Type</span><span class="sxs-lookup"><span data-stu-id="e4c01-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e4c01-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e4c01-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4c01-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4c01-134">Requirements</span></span>



| <span data-ttu-id="e4c01-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4c01-135">Requirement</span></span> | <span data-ttu-id="e4c01-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4c01-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c01-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4c01-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c01-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4c01-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4c01-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4c01-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c01-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4c01-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e4c01-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e4c01-141">Namespace</span></span><br/>                | <span data-ttu-id="e4c01-142">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="e4c01-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="e4c01-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e4c01-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4c01-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4c01-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4c01-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e4c01-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4c01-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4c01-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4c01-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4c01-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c01-148">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="e4c01-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

