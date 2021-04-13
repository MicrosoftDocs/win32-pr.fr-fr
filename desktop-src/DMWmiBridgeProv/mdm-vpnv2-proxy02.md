---
title: Classe MDM_VPNv2_Proxy02
description: La \_ \_ classe Proxy02 MDM VPNv2 définit un objet de configuration pour activer la prise en charge de proxy après connexion pour le VPN.
ms.assetid: 243f0824-4951-41c4-b8b4-b5c39aefd8ff
keywords:
- Classe MDM_VPNv2_Proxy02
- Classe MDM_VPNv2_Proxy02, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02.InstanceID
- MDM_VPNv2_Proxy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf8197379f5b1ff69433baa845af2cd53bb9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465342"
---
# <a name="mdm_vpnv2_proxy02-class"></a><span data-ttu-id="a546b-105">\_ \_ Classe PROXY02 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="a546b-105">MDM\_VPNv2\_Proxy02 class</span></span>

<span data-ttu-id="a546b-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a546b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a546b-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a546b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a546b-108">La **classe \_ \_ Proxy02 MDM VPNv2** définit un objet de configuration pour activer la prise en charge de proxy après connexion pour le VPN.</span><span class="sxs-lookup"><span data-stu-id="a546b-108">The **MDM\_VPNv2\_Proxy02** class defines a configuration object to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="a546b-109">Le proxy défini pour ce profil est appliqué lorsque ce profil est actif et connecté.</span><span class="sxs-lookup"><span data-stu-id="a546b-109">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

<span data-ttu-id="a546b-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a546b-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a546b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a546b-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Proxy02
{
  string InstanceID;
  string ParentID;
  string AutoConfigUrl;
};
```

## <a name="members"></a><span data-ttu-id="a546b-112">Membres</span><span class="sxs-lookup"><span data-stu-id="a546b-112">Members</span></span>

<span data-ttu-id="a546b-113">La **classe \_ VPNv2 \_ Proxy02 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a546b-113">The **MDM\_VPNv2\_Proxy02** class has these types of members:</span></span>

-   [<span data-ttu-id="a546b-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a546b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a546b-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a546b-115">Properties</span></span>

<span data-ttu-id="a546b-116">La **classe \_ VPNv2 \_ Proxy02 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a546b-116">The **MDM\_VPNv2\_Proxy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a546b-117">AutoConfigUrl</span><span class="sxs-lookup"><span data-stu-id="a546b-117">AutoConfigUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-autoconfigurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a546b-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a546b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a546b-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a546b-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a546b-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a546b-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a546b-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a546b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a546b-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a546b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a546b-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a546b-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a546b-124">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a546b-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="a546b-125">Collection d’objets de configuration permettant d’activer la prise en charge d’un proxy après connexion pour le VPN.</span><span class="sxs-lookup"><span data-stu-id="a546b-125">A collection of configuration objects to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="a546b-126">Le proxy défini pour ce profil est appliqué lorsque ce profil est actif et connecté.</span><span class="sxs-lookup"><span data-stu-id="a546b-126">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

</dd> <dt>

<span data-ttu-id="a546b-127">**ID**</span><span class="sxs-lookup"><span data-stu-id="a546b-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a546b-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a546b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a546b-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a546b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a546b-130">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a546b-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a546b-131">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a546b-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="a546b-132">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*»</span><span class="sxs-lookup"><span data-stu-id="a546b-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a546b-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a546b-133">Requirements</span></span>



| <span data-ttu-id="a546b-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a546b-134">Requirement</span></span> | <span data-ttu-id="a546b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="a546b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a546b-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a546b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a546b-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a546b-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a546b-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a546b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a546b-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a546b-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a546b-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a546b-140">Namespace</span></span><br/>                | <span data-ttu-id="a546b-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="a546b-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a546b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a546b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a546b-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a546b-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a546b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a546b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a546b-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a546b-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a546b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a546b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a546b-147">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="a546b-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

