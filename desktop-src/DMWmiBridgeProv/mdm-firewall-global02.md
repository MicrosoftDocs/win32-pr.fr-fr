---
title: Classe MDM_Firewall_Global02
description: La \_ classe Global02 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.
ms.assetid: 387a60c6-6dc9-4710-a1e3-0468ac004395
keywords:
- Classe MDM_Firewall_Global02
- Classe MDM_Firewall_Global02, Description
topic_type:
- apiref
api_name:
- MDM_Firewall_Global02
- MDM_Firewall_Global02.InstanceID
- MDM_Firewall_Global02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cef2a8b11585848ac10035528db176b78d2e66b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200549"
---
# <a name="mdm_firewall_global02-class"></a><span data-ttu-id="5bd19-105">\_Classe Global02 du pare-feu MDM \_</span><span class="sxs-lookup"><span data-stu-id="5bd19-105">MDM\_Firewall\_Global02 class</span></span>

<span data-ttu-id="5bd19-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="5bd19-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5bd19-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="5bd19-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5bd19-108">La \_ classe Global02 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="5bd19-108">The MDM\_Firewall\_Global02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="5bd19-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5bd19-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd19-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bd19-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Global02
{
  string  InstanceID;
  string  ParentID;
  sint32  PolicyVersionSupported;
  sint32  CurrentProfiles;
  boolean DisableStatefulFtp;
  sint32  SaIdleTime;
  sint32  PresharedKeyEncoding;
  sint32  IPsecExempt;
  sint32  CRLcheck;
  string  PolicyVersion;
  string  BinaryVersionSupported;
  boolean OpportunisticallyMatchAuthSetPerKM;
  sint32  EnablePacketQueue;
};
```

## <a name="members"></a><span data-ttu-id="5bd19-111">Membres</span><span class="sxs-lookup"><span data-stu-id="5bd19-111">Members</span></span>

<span data-ttu-id="5bd19-112">La **classe \_ \_ Global02 du pare-feu MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5bd19-112">The **MDM\_Firewall\_Global02** class has these types of members:</span></span>

-   [<span data-ttu-id="5bd19-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5bd19-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5bd19-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5bd19-114">Properties</span></span>

<span data-ttu-id="5bd19-115">La **classe \_ \_ Global02 du pare-feu MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5bd19-115">The **MDM\_Firewall\_Global02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5bd19-116">BinaryVersionSupported</span><span class="sxs-lookup"><span data-stu-id="5bd19-116">BinaryVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#binaryversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5bd19-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5bd19-119">CRLcheck</span><span class="sxs-lookup"><span data-stu-id="5bd19-119">CRLcheck</span></span>](/windows/client-management/mdm/firewall-csp#crlcheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5bd19-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5bd19-122">CurrentProfiles</span><span class="sxs-lookup"><span data-stu-id="5bd19-122">CurrentProfiles</span></span>](/windows/client-management/mdm/firewall-csp#currentprofiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5bd19-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5bd19-125">DisableStatefulFtp</span><span class="sxs-lookup"><span data-stu-id="5bd19-125">DisableStatefulFtp</span></span>](/windows/client-management/mdm/firewall-csp#disablestatefulftp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-126">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5bd19-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5bd19-128">EnablePacketQueue</span><span class="sxs-lookup"><span data-stu-id="5bd19-128">EnablePacketQueue</span></span>](/windows/client-management/mdm/firewall-csp#enablepacketqueue)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5bd19-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5bd19-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5bd19-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5bd19-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5bd19-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5bd19-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5bd19-135">IPsecExempt</span><span class="sxs-lookup"><span data-stu-id="5bd19-135">IPsecExempt</span></span>](/windows/client-management/mdm/firewall-csp#ipsecexempt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-136">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5bd19-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5bd19-138">OpportunisticallyMatchAuthSetPerKM</span><span class="sxs-lookup"><span data-stu-id="5bd19-138">OpportunisticallyMatchAuthSetPerKM</span></span>](/windows/client-management/mdm/firewall-csp#opportunisticallymatchauthsetperkm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-139">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5bd19-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5bd19-141">**ID**</span><span class="sxs-lookup"><span data-stu-id="5bd19-141">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5bd19-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5bd19-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-144">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5bd19-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5bd19-145">PolicyVersion</span><span class="sxs-lookup"><span data-stu-id="5bd19-145">PolicyVersion</span></span>](/windows/client-management/mdm/firewall-csp#policyversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5bd19-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5bd19-148">PolicyVersionSupported</span><span class="sxs-lookup"><span data-stu-id="5bd19-148">PolicyVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#policyversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-149">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5bd19-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5bd19-151">PresharedKeyEncoding</span><span class="sxs-lookup"><span data-stu-id="5bd19-151">PresharedKeyEncoding</span></span>](/windows/client-management/mdm/firewall-csp#presharedkeyencoding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-152">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5bd19-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5bd19-154">SaIdleTime</span><span class="sxs-lookup"><span data-stu-id="5bd19-154">SaIdleTime</span></span>](/windows/client-management/mdm/firewall-csp#saidletime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd19-155">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5bd19-155">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bd19-156">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5bd19-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5bd19-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bd19-157">Requirements</span></span>



| <span data-ttu-id="5bd19-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bd19-158">Requirement</span></span> | <span data-ttu-id="5bd19-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bd19-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd19-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bd19-160">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd19-161">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bd19-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5bd19-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bd19-162">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd19-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bd19-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="5bd19-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5bd19-164">Namespace</span></span><br/>                | <span data-ttu-id="5bd19-165">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="5bd19-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="5bd19-166">MOF</span><span class="sxs-lookup"><span data-stu-id="5bd19-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bd19-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bd19-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bd19-168">DLL</span><span class="sxs-lookup"><span data-stu-id="5bd19-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bd19-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bd19-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

