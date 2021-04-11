---
title: Classe MDM_Firewall_FirewallRules02_01
description: La \_ classe FirewallRules02 01 du pare-feu MDM \_ \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.
ms.assetid: b09cbd98-152e-486c-acb5-4e1d83e5f8e2
keywords:
- Classe MDM_Firewall_FirewallRules02_01
- Classe MDM_Firewall_FirewallRules02_01, Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_Firewall_FirewallRules02_01
- MDM_Firewall_FirewallRules02_01.InstanceID
- MDM_Firewall_FirewallRules02_01.ParentID
- MDM_Firewall_FirewallRules02_01.IcmpTypesAndCodes
- MDM_Firewall_FirewallRules02_01.FriendlyName
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 494be18ece91e7a1776780542f988b80cb822e42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103333"
---
# <a name="mdm_firewall_firewallrules02_01-class"></a><span data-ttu-id="b5ae5-105">\_ \_ Classe FirewallRules02 01 du pare-feu MDM \_</span><span class="sxs-lookup"><span data-stu-id="b5ae5-105">MDM\_Firewall\_FirewallRules02\_01 class</span></span>

<span data-ttu-id="b5ae5-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b5ae5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b5ae5-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="b5ae5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b5ae5-108">La \_ classe FirewallRules02 01 du pare-feu MDM \_ \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="b5ae5-108">The MDM\_Firewall\_FirewallRules02\_01 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="b5ae5-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b5ae5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ae5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5ae5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_FirewallRules02_01
{
  string  InstanceID;
  string  ParentID;
  sint32  Protocol;
  string  LocalPortRanges;
  string  RemotePortRanges;
  string  LocalAddressRanges;
  string  RemoteAddressRanges;
  string  Description;
  boolean Enabled;
  sint32  Profiles;
  string  Direction;
  string  InterfaceTypes;
  string  IcmpTypesAndCodes;
  boolean EdgeTraversal;
  string  LocalUserAuthorizedList;
  string  Status;
  string  FriendlyName;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="b5ae5-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b5ae5-111">Members</span></span>

<span data-ttu-id="b5ae5-112">La **classe \_ \_ FirewallRules02 \_ 01 du pare-feu MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b5ae5-112">The **MDM\_Firewall\_FirewallRules02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="b5ae5-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5ae5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5ae5-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5ae5-114">Properties</span></span>

<span data-ttu-id="b5ae5-115">La **classe \_ \_ FirewallRules02 \_ 01 du pare-feu MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b5ae5-115">The **MDM\_Firewall\_FirewallRules02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b5ae5-116">Description</span><span class="sxs-lookup"><span data-stu-id="b5ae5-116">Description</span></span>](/windows/client-management/mdm/firewall-csp#description)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-119">Sens</span><span class="sxs-lookup"><span data-stu-id="b5ae5-119">Direction</span></span>](/windows/client-management/mdm/firewall-csp#direction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-122">EdgeTraversal</span><span class="sxs-lookup"><span data-stu-id="b5ae5-122">EdgeTraversal</span></span>](/windows/client-management/mdm/firewall-csp#edgetraversal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-123">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-125">Enabled</span><span class="sxs-lookup"><span data-stu-id="b5ae5-125">Enabled</span></span>](/windows/client-management/mdm/firewall-csp#enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-126">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5ae5-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b5ae5-131">TBD</span><span class="sxs-lookup"><span data-stu-id="b5ae5-131">TBD</span></span>

</dd> <dt>

<span data-ttu-id="b5ae5-132">**IcmpTypesAndCodes**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-132">**IcmpTypesAndCodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b5ae5-135">TBD</span><span class="sxs-lookup"><span data-stu-id="b5ae5-135">TBD</span></span>

</dd> <dt>

<span data-ttu-id="b5ae5-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ae5-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-139">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b5ae5-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-140">InterfaceTypes</span><span class="sxs-lookup"><span data-stu-id="b5ae5-140">InterfaceTypes</span></span>](/windows/client-management/mdm/firewall-csp#interfacetypes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-143">LocalAddressRanges</span><span class="sxs-lookup"><span data-stu-id="b5ae5-143">LocalAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-146">LocalPortRanges</span><span class="sxs-lookup"><span data-stu-id="b5ae5-146">LocalPortRanges</span></span>](/windows/client-management/mdm/firewall-csp#localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-149">LocalUserAuthorizedList</span><span class="sxs-lookup"><span data-stu-id="b5ae5-149">LocalUserAuthorizedList</span></span>](/windows/client-management/mdm/firewall-csp#localuserauthorizedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-152">Nom</span><span class="sxs-lookup"><span data-stu-id="b5ae5-152">Name</span></span>](/windows/client-management/mdm/firewall-csp#name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5ae5-155">**ID**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ae5-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-158">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b5ae5-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-159">Profils</span><span class="sxs-lookup"><span data-stu-id="b5ae5-159">Profiles</span></span>](/windows/client-management/mdm/firewall-csp#profiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-160">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-161">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-162">Protocole</span><span class="sxs-lookup"><span data-stu-id="b5ae5-162">Protocol</span></span>](/windows/client-management/mdm/firewall-csp#protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-163">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-164">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-165">RemoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="b5ae5-165">RemoteAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-167">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-168">RemotePortRanges</span><span class="sxs-lookup"><span data-stu-id="b5ae5-168">RemotePortRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5ae5-171">État</span><span class="sxs-lookup"><span data-stu-id="b5ae5-171">Status</span></span>](/windows/client-management/mdm/firewall-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ae5-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5ae5-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ae5-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5ae5-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5ae5-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5ae5-174">Requirements</span></span>



| <span data-ttu-id="b5ae5-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5ae5-175">Requirement</span></span> | <span data-ttu-id="b5ae5-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5ae5-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ae5-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ae5-177">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ae5-178">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5ae5-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5ae5-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ae5-179">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ae5-180">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ae5-180">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b5ae5-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b5ae5-181">Namespace</span></span><br/>                | <span data-ttu-id="b5ae5-182">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="b5ae5-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="b5ae5-183">MOF</span><span class="sxs-lookup"><span data-stu-id="b5ae5-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5ae5-184"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5ae5-184"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5ae5-185">DLL</span><span class="sxs-lookup"><span data-stu-id="b5ae5-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5ae5-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5ae5-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

