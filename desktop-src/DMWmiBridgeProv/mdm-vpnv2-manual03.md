---
title: Classe MDM_VPNv2_Manual03
description: MDM \_ VPNv2 \_ Manual03class est un nœud facultatif qui contient les paramètres de serveur manuels.
ms.assetid: c294c5a2-35e2-46ca-b7d8-9c63f9d3cdd6
keywords:
- Classe MDM_VPNv2_Manual03
- Classe MDM_VPNv2_Manual03, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03.InstanceID
- MDM_VPNv2_Manual03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e36d9a048e3a5a523770b9a3987a346fe2283
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942691"
---
# <a name="mdm_vpnv2_manual03-class"></a><span data-ttu-id="a6b85-105">\_ \_ Classe MANUAL03 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="a6b85-105">MDM\_VPNv2\_Manual03 class</span></span>

<span data-ttu-id="a6b85-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a6b85-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a6b85-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a6b85-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a6b85-108">La **classe \_ VPNv2 \_ Manual03 MDM** est un nœud facultatif qui contient les paramètres de serveur manuels.</span><span class="sxs-lookup"><span data-stu-id="a6b85-108">The **MDM\_VPNv2\_Manual03** class is an optional node containing the manual server settings.</span></span>

<span data-ttu-id="a6b85-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a6b85-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6b85-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6b85-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Manual03
{
  string InstanceID;
  string ParentID;
  string Server;
};
```

## <a name="members"></a><span data-ttu-id="a6b85-111">Membres</span><span class="sxs-lookup"><span data-stu-id="a6b85-111">Members</span></span>

<span data-ttu-id="a6b85-112">La **classe \_ VPNv2 \_ Manual03 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a6b85-112">The **MDM\_VPNv2\_Manual03** class has these types of members:</span></span>

-   [<span data-ttu-id="a6b85-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a6b85-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6b85-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a6b85-114">Properties</span></span>

<span data-ttu-id="a6b85-115">La **classe \_ VPNv2 \_ Manual03 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a6b85-115">The **MDM\_VPNv2\_Manual03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6b85-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a6b85-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b85-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6b85-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b85-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6b85-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6b85-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a6b85-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a6b85-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a6b85-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="a6b85-121">**ID**</span><span class="sxs-lookup"><span data-stu-id="a6b85-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b85-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6b85-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b85-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6b85-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6b85-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a6b85-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a6b85-125">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a6b85-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="a6b85-126">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/proxy/ »</span><span class="sxs-lookup"><span data-stu-id="a6b85-126">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/Proxy/"</span></span>

</dd> <dt>

[<span data-ttu-id="a6b85-127">Serveur</span><span class="sxs-lookup"><span data-stu-id="a6b85-127">Server</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-manual-server)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b85-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6b85-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b85-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a6b85-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6b85-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6b85-130">Requirements</span></span>



| <span data-ttu-id="a6b85-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6b85-131">Requirement</span></span> | <span data-ttu-id="a6b85-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6b85-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b85-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6b85-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a6b85-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6b85-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6b85-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6b85-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a6b85-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6b85-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a6b85-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a6b85-137">Namespace</span></span><br/>                | <span data-ttu-id="a6b85-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="a6b85-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a6b85-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a6b85-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6b85-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6b85-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6b85-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a6b85-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6b85-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6b85-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6b85-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6b85-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6b85-144">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="a6b85-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

