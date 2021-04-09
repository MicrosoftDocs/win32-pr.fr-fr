---
title: Classe MDM_Firewall_DomainProfile02
description: La \_ classe DomainProfile02 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.
ms.assetid: 1d82ba2f-b61d-4976-a44b-4ae2054f9df5
keywords:
- Classe MDM_Firewall_DomainProfile02
- Classe MDM_Firewall_DomainProfile02, Description
topic_type:
- apiref
api_name:
- MDM_Firewall_DomainProfile02
- MDM_Firewall_DomainProfile02.InstanceID
- MDM_Firewall_DomainProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea6f87597148b01be38ae092302d3098d7eeace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032682"
---
# <a name="mdm_firewall_domainprofile02-class"></a><span data-ttu-id="5f380-105">\_Classe DomainProfile02 du pare-feu MDM \_</span><span class="sxs-lookup"><span data-stu-id="5f380-105">MDM\_Firewall\_DomainProfile02 class</span></span>

<span data-ttu-id="5f380-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="5f380-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5f380-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="5f380-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5f380-108">La \_ classe DomainProfile02 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="5f380-108">The MDM\_Firewall\_DomainProfile02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="5f380-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5f380-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f380-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f380-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_DomainProfile02
{
  string InstanceID;
  string ParentID;
  sint32 EnableFirewall;
  sint32 DisableStealthMode;
  sint32 Shielded;
  sint32 DisableUnicastResponsesToMulticastBroadcast;
  sint32 DisableInboundNotifications;
  sint32 AuthAppsAllowUserPrefMerge;
  sint32 GlobalPortsAllowUserPrefMerge;
  sint32 AllowLocalPolicyMerge;
  sint32 AllowLocalIpsecPolicyMerge;
  sint32 DefaultOutboundAction;
  sint32 DefaultInboundAction;
  sint32 DisableStealthModeIpsecSecuredPacketExemption;
};
```

## <a name="members"></a><span data-ttu-id="5f380-111">Membres</span><span class="sxs-lookup"><span data-stu-id="5f380-111">Members</span></span>

<span data-ttu-id="5f380-112">La **classe \_ \_ DomainProfile02 du pare-feu MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5f380-112">The **MDM\_Firewall\_DomainProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="5f380-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f380-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f380-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f380-114">Properties</span></span>

<span data-ttu-id="5f380-115">La **classe \_ \_ DomainProfile02 du pare-feu MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5f380-115">The **MDM\_Firewall\_DomainProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5f380-116">AllowLocalIpsecPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="5f380-116">AllowLocalIpsecPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalipsecpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-119">AllowLocalPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="5f380-119">AllowLocalPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-122">AuthAppsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="5f380-122">AuthAppsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#authappsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-125">DefaultInboundAction</span><span class="sxs-lookup"><span data-stu-id="5f380-125">DefaultInboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultinboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-128">DefaultOutboundAction</span><span class="sxs-lookup"><span data-stu-id="5f380-128">DefaultOutboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultoutboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-131">DisableInboundNotifications</span><span class="sxs-lookup"><span data-stu-id="5f380-131">DisableInboundNotifications</span></span>](/windows/client-management/mdm/firewall-csp#disableinboundnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-134">DisableStealthMode</span><span class="sxs-lookup"><span data-stu-id="5f380-134">DisableStealthMode</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-137">DisableStealthModeIpsecSecuredPacketExemption</span><span class="sxs-lookup"><span data-stu-id="5f380-137">DisableStealthModeIpsecSecuredPacketExemption</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmodeipsecsecuredpacketexemption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-140">DisableUnicastResponsesToMulticastBroadcast</span><span class="sxs-lookup"><span data-stu-id="5f380-140">DisableUnicastResponsesToMulticastBroadcast</span></span>](/windows/client-management/mdm/firewall-csp#disableunicastresponsestomulticastbroadcast)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-143">EnableFirewall</span><span class="sxs-lookup"><span data-stu-id="5f380-143">EnableFirewall</span></span>](/windows/client-management/mdm/firewall-csp#enablefirewall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-146">GlobalPortsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="5f380-146">GlobalPortsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#globalportsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5f380-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5f380-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f380-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f380-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f380-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f380-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5f380-153">**ID**</span><span class="sxs-lookup"><span data-stu-id="5f380-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f380-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f380-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f380-156">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f380-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f380-157">Protégé</span><span class="sxs-lookup"><span data-stu-id="5f380-157">Shielded</span></span>](/windows/client-management/mdm/firewall-csp#shielded)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f380-158">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f380-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f380-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5f380-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f380-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f380-160">Requirements</span></span>



| <span data-ttu-id="5f380-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f380-161">Requirement</span></span> | <span data-ttu-id="5f380-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f380-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f380-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f380-163">Minimum supported client</span></span><br/> | <span data-ttu-id="5f380-164">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f380-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f380-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f380-165">Minimum supported server</span></span><br/> | <span data-ttu-id="5f380-166">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f380-166">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="5f380-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5f380-167">Namespace</span></span><br/>                | <span data-ttu-id="5f380-168">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="5f380-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="5f380-169">MOF</span><span class="sxs-lookup"><span data-stu-id="5f380-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f380-170"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f380-170"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f380-171">DLL</span><span class="sxs-lookup"><span data-stu-id="5f380-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f380-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f380-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

