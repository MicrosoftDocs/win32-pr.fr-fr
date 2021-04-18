---
title: Classe MDM_Firewall_PublicProfile02
description: La \_ classe PublicProfile02 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.
ms.assetid: 5524b931-10fa-43dc-8901-238312ecb6a8
keywords:
- Classe MDM_Firewall_PublicProfile02
- Classe MDM_Firewall_PublicProfile02, Description
topic_type:
- apiref
api_name:
- MDM_Firewall_PublicProfile02
- MDM_Firewall_PublicProfile02.InstanceID
- MDM_Firewall_PublicProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530bac28c33b9ed3937f962a7f040e82b2ee1919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464859"
---
# <a name="mdm_firewall_publicprofile02-class"></a><span data-ttu-id="edd79-105">\_Classe PublicProfile02 du pare-feu MDM \_</span><span class="sxs-lookup"><span data-stu-id="edd79-105">MDM\_Firewall\_PublicProfile02 class</span></span>

<span data-ttu-id="edd79-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="edd79-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="edd79-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="edd79-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="edd79-108">La \_ classe PublicProfile02 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="edd79-108">The MDM\_Firewall\_PublicProfile02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="edd79-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="edd79-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd79-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edd79-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_PublicProfile02
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

## <a name="members"></a><span data-ttu-id="edd79-111">Membres</span><span class="sxs-lookup"><span data-stu-id="edd79-111">Members</span></span>

<span data-ttu-id="edd79-112">La **classe \_ \_ PublicProfile02 du pare-feu MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="edd79-112">The **MDM\_Firewall\_PublicProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="edd79-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="edd79-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="edd79-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="edd79-114">Properties</span></span>

<span data-ttu-id="edd79-115">La **classe \_ \_ PublicProfile02 du pare-feu MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="edd79-115">The **MDM\_Firewall\_PublicProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="edd79-116">AllowLocalIpsecPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="edd79-116">AllowLocalIpsecPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalipsecpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-119">AllowLocalPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="edd79-119">AllowLocalPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-122">AuthAppsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="edd79-122">AuthAppsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#authappsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-125">DefaultInboundAction</span><span class="sxs-lookup"><span data-stu-id="edd79-125">DefaultInboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultinboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-128">DefaultOutboundAction</span><span class="sxs-lookup"><span data-stu-id="edd79-128">DefaultOutboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultoutboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-131">DisableInboundNotifications</span><span class="sxs-lookup"><span data-stu-id="edd79-131">DisableInboundNotifications</span></span>](/windows/client-management/mdm/firewall-csp#disableinboundnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-134">DisableStealthMode</span><span class="sxs-lookup"><span data-stu-id="edd79-134">DisableStealthMode</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-137">DisableStealthModeIpsecSecuredPacketExemption</span><span class="sxs-lookup"><span data-stu-id="edd79-137">DisableStealthModeIpsecSecuredPacketExemption</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmodeipsecsecuredpacketexemption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-140">DisableUnicastResponsesToMulticastBroadcast</span><span class="sxs-lookup"><span data-stu-id="edd79-140">DisableUnicastResponsesToMulticastBroadcast</span></span>](/windows/client-management/mdm/firewall-csp#disableunicastresponsestomulticastbroadcast)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-143">EnableFirewall</span><span class="sxs-lookup"><span data-stu-id="edd79-143">EnableFirewall</span></span>](/windows/client-management/mdm/firewall-csp#enablefirewall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-146">GlobalPortsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="edd79-146">GlobalPortsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#globalportsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="edd79-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="edd79-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="edd79-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="edd79-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="edd79-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="edd79-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="edd79-153">**ID**</span><span class="sxs-lookup"><span data-stu-id="edd79-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="edd79-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="edd79-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="edd79-156">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="edd79-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edd79-157">Protégé</span><span class="sxs-lookup"><span data-stu-id="edd79-157">Shielded</span></span>](/windows/client-management/mdm/firewall-csp#shielded)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edd79-158">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="edd79-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edd79-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="edd79-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="edd79-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edd79-160">Requirements</span></span>



| <span data-ttu-id="edd79-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edd79-161">Requirement</span></span> | <span data-ttu-id="edd79-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="edd79-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd79-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edd79-163">Minimum supported client</span></span><br/> | <span data-ttu-id="edd79-164">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edd79-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="edd79-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edd79-165">Minimum supported server</span></span><br/> | <span data-ttu-id="edd79-166">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="edd79-166">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="edd79-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="edd79-167">Namespace</span></span><br/>                | <span data-ttu-id="edd79-168">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="edd79-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="edd79-169">MOF</span><span class="sxs-lookup"><span data-stu-id="edd79-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edd79-170"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="edd79-170"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="edd79-171">DLL</span><span class="sxs-lookup"><span data-stu-id="edd79-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edd79-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd79-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

