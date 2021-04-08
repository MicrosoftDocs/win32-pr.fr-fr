---
title: Classe MDM_VPNv2_NativeProfile02
description: La \_ \_ classe NativeProfile2 MDM VPNv2 définit les informations de profil lors de l’utilisation d’un protocole VPN de boîte aux lettres Windows (IKEV2, PPTP, L2TP).
ms.assetid: 50c4adc6-baef-437c-8223-9aeaaec813af
keywords:
- Classe MDM_VPNv2_NativeProfile02
- Classe MDM_VPNv2_NativeProfile02, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02.InstanceID
- MDM_VPNv2_NativeProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8573975c488df6e5c759e719d5c687f6a71c505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844165"
---
# <a name="mdm_vpnv2_nativeprofile02-class"></a><span data-ttu-id="de400-105">\_ \_ Classe NATIVEPROFILE02 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="de400-105">MDM\_VPNv2\_NativeProfile02 class</span></span>

<span data-ttu-id="de400-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="de400-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="de400-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="de400-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="de400-108">La **classe \_ \_ NativeProfile2 MDM VPNv2** définit les informations de profil lors de l’utilisation d’un protocole VPN de boîte aux lettres Windows (IKEV2, PPTP, L2TP).</span><span class="sxs-lookup"><span data-stu-id="de400-108">The **MDM\_VPNv2\_NativeProfile2** class defines profile information when using a Windows Inbox VPN Protocol (IKEv2, PPTP, L2TP).</span></span>

<span data-ttu-id="de400-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="de400-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de400-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de400-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_NativeProfile02
{
  string InstanceID;
  string ParentID;
  string Servers;
  string RoutingPolicyType;
  string NativeProtocolType;
  string L2tpPsk;
};
```

## <a name="members"></a><span data-ttu-id="de400-111">Membres</span><span class="sxs-lookup"><span data-stu-id="de400-111">Members</span></span>

<span data-ttu-id="de400-112">La **classe \_ VPNv2 \_ NativeProfile02 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="de400-112">The **MDM\_VPNv2\_NativeProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="de400-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de400-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de400-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de400-114">Properties</span></span>

<span data-ttu-id="de400-115">La **classe \_ VPNv2 \_ NativeProfile02 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="de400-115">The **MDM\_VPNv2\_NativeProfile02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de400-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="de400-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de400-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de400-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de400-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de400-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de400-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de400-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de400-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="de400-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="de400-121">L2tpPsk</span><span class="sxs-lookup"><span data-stu-id="de400-121">L2tpPsk</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-l2tppsk)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de400-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de400-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de400-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de400-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de400-124">NativeProtocolType</span><span class="sxs-lookup"><span data-stu-id="de400-124">NativeProtocolType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-nativeprotocoltype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de400-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de400-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de400-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de400-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de400-127">**ID**</span><span class="sxs-lookup"><span data-stu-id="de400-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de400-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de400-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de400-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de400-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de400-130">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de400-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de400-131">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="de400-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="de400-132">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*»</span><span class="sxs-lookup"><span data-stu-id="de400-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="de400-133">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="de400-133">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de400-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de400-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de400-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de400-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de400-136">Serveurs</span><span class="sxs-lookup"><span data-stu-id="de400-136">Servers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-servers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de400-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de400-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de400-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de400-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de400-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de400-139">Requirements</span></span>



| <span data-ttu-id="de400-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de400-140">Requirement</span></span> | <span data-ttu-id="de400-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="de400-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de400-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de400-142">Minimum supported client</span></span><br/> | <span data-ttu-id="de400-143">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de400-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de400-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de400-144">Minimum supported server</span></span><br/> | <span data-ttu-id="de400-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="de400-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="de400-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="de400-146">Namespace</span></span><br/>                | <span data-ttu-id="de400-147">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="de400-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="de400-148">MOF</span><span class="sxs-lookup"><span data-stu-id="de400-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de400-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de400-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="de400-150">DLL</span><span class="sxs-lookup"><span data-stu-id="de400-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de400-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de400-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de400-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de400-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de400-153">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="de400-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

