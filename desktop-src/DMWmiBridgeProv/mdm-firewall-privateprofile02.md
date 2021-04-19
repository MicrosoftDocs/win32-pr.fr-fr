---
title: Classe MDM_Firewall_PrivateProfile02
description: La \_ classe PrivateProfile02 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.
ms.assetid: 9d25c181-e9a8-4f63-b276-b22676842667
keywords:
- Classe MDM_Firewall_PrivateProfile02
- Classe MDM_Firewall_PrivateProfile02, Description
topic_type:
- apiref
api_name:
- MDM_Firewall_PrivateProfile02
- MDM_Firewall_PrivateProfile02.InstanceID
- MDM_Firewall_PrivateProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57812ef7c8550937b009e4ff4855321983391585
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510954"
---
# <a name="mdm_firewall_privateprofile02-class"></a><span data-ttu-id="cfa94-105">\_Classe PrivateProfile02 du pare-feu MDM \_</span><span class="sxs-lookup"><span data-stu-id="cfa94-105">MDM\_Firewall\_PrivateProfile02 class</span></span>

<span data-ttu-id="cfa94-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="cfa94-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cfa94-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="cfa94-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cfa94-108">La \_ classe PrivateProfile02 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="cfa94-108">The MDM\_Firewall\_PrivateProfile02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="cfa94-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cfa94-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa94-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfa94-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_PrivateProfile02
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

## <a name="members"></a><span data-ttu-id="cfa94-111">Membres</span><span class="sxs-lookup"><span data-stu-id="cfa94-111">Members</span></span>

<span data-ttu-id="cfa94-112">La **classe \_ \_ PrivateProfile02 du pare-feu MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cfa94-112">The **MDM\_Firewall\_PrivateProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="cfa94-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cfa94-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cfa94-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cfa94-114">Properties</span></span>

<span data-ttu-id="cfa94-115">La **classe \_ \_ PrivateProfile02 du pare-feu MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cfa94-115">The **MDM\_Firewall\_PrivateProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cfa94-116">AllowLocalIpsecPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="cfa94-116">AllowLocalIpsecPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalipsecpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-119">AllowLocalPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="cfa94-119">AllowLocalPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-122">AuthAppsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="cfa94-122">AuthAppsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#authappsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-125">DefaultInboundAction</span><span class="sxs-lookup"><span data-stu-id="cfa94-125">DefaultInboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultinboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-128">DefaultOutboundAction</span><span class="sxs-lookup"><span data-stu-id="cfa94-128">DefaultOutboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultoutboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-131">DisableInboundNotifications</span><span class="sxs-lookup"><span data-stu-id="cfa94-131">DisableInboundNotifications</span></span>](/windows/client-management/mdm/firewall-csp#disableinboundnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-134">DisableStealthMode</span><span class="sxs-lookup"><span data-stu-id="cfa94-134">DisableStealthMode</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-137">DisableStealthModeIpsecSecuredPacketExemption</span><span class="sxs-lookup"><span data-stu-id="cfa94-137">DisableStealthModeIpsecSecuredPacketExemption</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmodeipsecsecuredpacketexemption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-140">DisableUnicastResponsesToMulticastBroadcast</span><span class="sxs-lookup"><span data-stu-id="cfa94-140">DisableUnicastResponsesToMulticastBroadcast</span></span>](/windows/client-management/mdm/firewall-csp#disableunicastresponsestomulticastbroadcast)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-143">EnableFirewall</span><span class="sxs-lookup"><span data-stu-id="cfa94-143">EnableFirewall</span></span>](/windows/client-management/mdm/firewall-csp#enablefirewall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-146">GlobalPortsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="cfa94-146">GlobalPortsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#globalportsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cfa94-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cfa94-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cfa94-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cfa94-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cfa94-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cfa94-153">**ID**</span><span class="sxs-lookup"><span data-stu-id="cfa94-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cfa94-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cfa94-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-156">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cfa94-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cfa94-157">Protégé</span><span class="sxs-lookup"><span data-stu-id="cfa94-157">Shielded</span></span>](/windows/client-management/mdm/firewall-csp#shielded)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa94-158">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cfa94-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa94-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cfa94-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfa94-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfa94-160">Requirements</span></span>



| <span data-ttu-id="cfa94-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfa94-161">Requirement</span></span> | <span data-ttu-id="cfa94-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfa94-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa94-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfa94-163">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa94-164">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfa94-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cfa94-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfa94-165">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa94-166">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfa94-166">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="cfa94-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cfa94-167">Namespace</span></span><br/>                | <span data-ttu-id="cfa94-168">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="cfa94-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="cfa94-169">MOF</span><span class="sxs-lookup"><span data-stu-id="cfa94-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfa94-170"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfa94-170"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfa94-171">DLL</span><span class="sxs-lookup"><span data-stu-id="cfa94-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfa94-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfa94-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

