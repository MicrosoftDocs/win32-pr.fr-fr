---
title: Classe MDM_VPNv2_RouteList02_01
description: La \_ classe MDM VPNv2 \_ RouteList02 \_ 01 contient une liste facultative d’itinéraires à ajouter à la table de routage pour l’interface VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- Classe MDM_VPNv2_RouteList02_01
- Classe MDM_VPNv2_RouteList02_01, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033079"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a><span data-ttu-id="6a50d-105">\_Classe VPNv2 \_ ROUTELIST02 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="6a50d-105">MDM\_VPNv2\_RouteList02\_01 class</span></span>

<span data-ttu-id="6a50d-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="6a50d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6a50d-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="6a50d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6a50d-108">La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** contient une liste facultative d’itinéraires à ajouter à la table de routage pour l’interface VPN.</span><span class="sxs-lookup"><span data-stu-id="6a50d-108">The **MDM\_VPNv2\_RouteList02\_01** class contains an optional list of routes to be added to the routing table for the VPN interface.</span></span>

<span data-ttu-id="6a50d-109">Cela est nécessaire pour le cas de tunneling fractionné où le site du serveur VPN a plus de sous-réseaux que le sous-réseau par défaut en fonction de l’adresse IP affectée à l’interface.</span><span class="sxs-lookup"><span data-stu-id="6a50d-109">This is required for split tunneling case where the VPN server site has more subnets that the default subnet based on the IP assigned to the interface.</span></span>

<span data-ttu-id="6a50d-110">Chaque ordinateur qui exécute TCP/IP prend des décisions de routage.</span><span class="sxs-lookup"><span data-stu-id="6a50d-110">Every computer that runs TCP/IP makes routing decisions.</span></span> <span data-ttu-id="6a50d-111">Ces décisions sont contrôlées par la table de routage IP.</span><span class="sxs-lookup"><span data-stu-id="6a50d-111">These decisions are controlled by the IP routing table.</span></span> <span data-ttu-id="6a50d-112">L’ajout de valeurs sous ce nœud met à jour la table de routage avec des itinéraires pour l’interface VPN après la connexion.</span><span class="sxs-lookup"><span data-stu-id="6a50d-112">Adding values under this node updates the routing table with routes for the VPN interface post connection.</span></span> <span data-ttu-id="6a50d-113">Les valeurs sous ce nœud représentent le préfixe de destination des itinéraires IP.</span><span class="sxs-lookup"><span data-stu-id="6a50d-113">The values under this node represent the destination prefix of IP routes.</span></span> <span data-ttu-id="6a50d-114">Un préfixe de destination se compose d’un préfixe d’adresse IP et d’une longueur de préfixe.</span><span class="sxs-lookup"><span data-stu-id="6a50d-114">A destination prefix consists of an IP address prefix and a prefix length.</span></span>

<span data-ttu-id="6a50d-115">L’ajout d’un itinéraire ici permet à la pile de mise en réseau d’identifier le trafic qui doit passer par l’interface VPN pour le VPN de tunnel fractionné.</span><span class="sxs-lookup"><span data-stu-id="6a50d-115">Adding a route here allows the networking stack to identify the traffic that needs to go over the VPN interface for split tunnel VPN.</span></span> <span data-ttu-id="6a50d-116">Certains serveurs VPN peuvent le configurer pendant la négociation de connexion et n’ont pas besoin de ces informations dans le profil VPN.</span><span class="sxs-lookup"><span data-stu-id="6a50d-116">Some VPN servers can configure this during connect negotiation and do not need this information in the VPN Profile.</span></span> <span data-ttu-id="6a50d-117">Vérifiez auprès de votre administrateur de serveur VPN si vous avez besoin de ces informations dans le profil VPN.</span><span class="sxs-lookup"><span data-stu-id="6a50d-117">Please check with your VPN server administrator to determine whether you need this information in the VPN profile.</span></span>

<span data-ttu-id="6a50d-118">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6a50d-118">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a50d-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a50d-119">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a><span data-ttu-id="6a50d-120">Membres</span><span class="sxs-lookup"><span data-stu-id="6a50d-120">Members</span></span>

<span data-ttu-id="6a50d-121">La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6a50d-121">The **MDM\_VPNv2\_RouteList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="6a50d-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6a50d-122">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a50d-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6a50d-123">Properties</span></span>

<span data-ttu-id="6a50d-124">La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6a50d-124">The **MDM\_VPNv2\_RouteList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6a50d-125">Adresse</span><span class="sxs-lookup"><span data-stu-id="6a50d-125">Address</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a50d-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a50d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a50d-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6a50d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6a50d-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6a50d-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a50d-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a50d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a50d-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a50d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a50d-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6a50d-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6a50d-132">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="6a50d-132">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="6a50d-133">**ID**</span><span class="sxs-lookup"><span data-stu-id="6a50d-133">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a50d-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a50d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a50d-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a50d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a50d-136">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6a50d-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6a50d-137">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="6a50d-137">Describes the full path to the parent node.</span></span> <span data-ttu-id="6a50d-138">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/RouteList »</span><span class="sxs-lookup"><span data-stu-id="6a50d-138">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span></span>

</dd> <dt>

[<span data-ttu-id="6a50d-139">PrefixSize</span><span class="sxs-lookup"><span data-stu-id="6a50d-139">PrefixSize</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a50d-140">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6a50d-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a50d-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6a50d-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a50d-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a50d-142">Requirements</span></span>



| <span data-ttu-id="6a50d-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a50d-143">Requirement</span></span> | <span data-ttu-id="6a50d-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a50d-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a50d-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a50d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6a50d-146">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a50d-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6a50d-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a50d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6a50d-148">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a50d-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6a50d-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6a50d-149">Namespace</span></span><br/>                | <span data-ttu-id="6a50d-150">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="6a50d-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6a50d-151">MOF</span><span class="sxs-lookup"><span data-stu-id="6a50d-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a50d-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a50d-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a50d-153">DLL</span><span class="sxs-lookup"><span data-stu-id="6a50d-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a50d-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a50d-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a50d-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a50d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a50d-156">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="6a50d-156">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

