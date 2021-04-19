---
title: Classe MDM_VPNv2_DeviceCompliance02
description: Réservé pour une utilisation ultérieure. | Classe MDM_VPNv2_DeviceCompliance02
ms.assetid: f84f4812-3083-46c4-a60c-919ec92c844f
keywords:
- Classe MDM_VPNv2_DeviceCompliance02
- Classe MDM_VPNv2_DeviceCompliance02, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_DeviceCompliance02
- MDM_VPNv2_DeviceCompliance02.InstanceID
- MDM_VPNv2_DeviceCompliance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a454a5cce3a40066c7cf14a60bdeeb81dcabab9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531302"
---
# <a name="mdm_vpnv2_devicecompliance02-class"></a><span data-ttu-id="61fdd-106">\_ \_ Classe DEVICECOMPLIANCE02 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="61fdd-106">MDM\_VPNv2\_DeviceCompliance02 class</span></span>

<span data-ttu-id="61fdd-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="61fdd-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="61fdd-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="61fdd-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="61fdd-109">Réservé pour un usage ultérieur</span><span class="sxs-lookup"><span data-stu-id="61fdd-109">Reserved for Future Use</span></span>

<span data-ttu-id="61fdd-110">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="61fdd-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61fdd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61fdd-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DeviceCompliance02
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
};
```

## <a name="members"></a><span data-ttu-id="61fdd-112">Membres</span><span class="sxs-lookup"><span data-stu-id="61fdd-112">Members</span></span>

<span data-ttu-id="61fdd-113">La **classe \_ VPNv2 \_ DeviceCompliance02 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="61fdd-113">The **MDM\_VPNv2\_DeviceCompliance02** class has these types of members:</span></span>

-   [<span data-ttu-id="61fdd-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="61fdd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61fdd-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="61fdd-115">Properties</span></span>

<span data-ttu-id="61fdd-116">La **classe \_ VPNv2 \_ DeviceCompliance02 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="61fdd-116">The **MDM\_VPNv2\_DeviceCompliance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="61fdd-117">Enabled</span><span class="sxs-lookup"><span data-stu-id="61fdd-117">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="61fdd-118">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="61fdd-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61fdd-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="61fdd-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="61fdd-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="61fdd-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61fdd-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="61fdd-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61fdd-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="61fdd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61fdd-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61fdd-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61fdd-124">Ajouté dans Windows 10, version 1607.</span><span class="sxs-lookup"><span data-stu-id="61fdd-124">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="61fdd-125">Les nœuds sous DeviceCompliance peuvent être utilisés pour activer l’accès conditionnel basé sur AAD pour VPN.</span><span class="sxs-lookup"><span data-stu-id="61fdd-125">Nodes under DeviceCompliance can be used to enable AAD-based Conditional Access for VPN.</span></span>

</dd> <dt>

<span data-ttu-id="61fdd-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="61fdd-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61fdd-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="61fdd-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61fdd-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="61fdd-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61fdd-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61fdd-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61fdd-130">Ajouté dans Windows 10, version 1607.</span><span class="sxs-lookup"><span data-stu-id="61fdd-130">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="61fdd-131">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="61fdd-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="61fdd-132">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*»</span><span class="sxs-lookup"><span data-stu-id="61fdd-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61fdd-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61fdd-133">Requirements</span></span>



| <span data-ttu-id="61fdd-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61fdd-134">Requirement</span></span> | <span data-ttu-id="61fdd-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="61fdd-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fdd-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61fdd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="61fdd-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61fdd-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61fdd-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61fdd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="61fdd-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="61fdd-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="61fdd-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="61fdd-140">Namespace</span></span><br/>                | <span data-ttu-id="61fdd-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="61fdd-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="61fdd-142">MOF</span><span class="sxs-lookup"><span data-stu-id="61fdd-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61fdd-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61fdd-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="61fdd-144">DLL</span><span class="sxs-lookup"><span data-stu-id="61fdd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61fdd-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61fdd-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61fdd-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61fdd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61fdd-147">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="61fdd-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

