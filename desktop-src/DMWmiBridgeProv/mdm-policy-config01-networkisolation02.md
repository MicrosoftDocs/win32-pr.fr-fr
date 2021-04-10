---
title: Classe MDM_Policy_Config01_NetworkIsolation02
description: La \_ classe Config01 NetworkIsolation02 de la stratégie MDM \_ \_ représente les stratégies de navigateur disponibles.
ms.assetid: f25ecbef-d232-4731-bac8-38a7d597db00
keywords:
- Classe MDM_Policy_Config01_NetworkIsolation02
- Classe MDM_Policy_Config01_NetworkIsolation02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_NetworkIsolation02
- MDM_Policy_Config01_NetworkIsolation02.InstanceID
- MDM_Policy_Config01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9062d150de07860fd9d5b2510269ddcc3d2f8a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032836"
---
# <a name="mdm_policy_config01_networkisolation02-class"></a><span data-ttu-id="d296a-105">\_Classe NetworkIsolation02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="d296a-105">MDM\_Policy\_Config01\_NetworkIsolation02 class</span></span>

<span data-ttu-id="d296a-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d296a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d296a-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d296a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d296a-108">La **classe \_ \_ Config01 \_ NetworkIsolation02 de la stratégie MDM** représente les stratégies de navigateur disponibles.</span><span class="sxs-lookup"><span data-stu-id="d296a-108">The **MDM\_Policy\_Config01\_NetworkIsolation02** class represents the browser policies available.</span></span>

<span data-ttu-id="d296a-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d296a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d296a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d296a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string NeutralResources;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="d296a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d296a-111">Members</span></span>

<span data-ttu-id="d296a-112">La **classe \_ \_ Config01 \_ NetworkIsolation02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d296a-112">The **MDM\_Policy\_Config01\_NetworkIsolation02** class has these types of members:</span></span>

-   [<span data-ttu-id="d296a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d296a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d296a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d296a-114">Properties</span></span>

<span data-ttu-id="d296a-115">La **classe \_ \_ Config01 \_ NetworkIsolation02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d296a-115">The **MDM\_Policy\_Config01\_NetworkIsolation02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d296a-116">EnterpriseCloudResources</span><span class="sxs-lookup"><span data-stu-id="d296a-116">EnterpriseCloudResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d296a-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d296a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d296a-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d296a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d296a-119">EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="d296a-119">EnterpriseInternalProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d296a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d296a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d296a-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d296a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d296a-122">EnterpriseIPRange</span><span class="sxs-lookup"><span data-stu-id="d296a-122">EnterpriseIPRange</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d296a-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d296a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d296a-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d296a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d296a-125">EnterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="d296a-125">EnterpriseIPRangesAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d296a-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d296a-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d296a-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d296a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d296a-128">EnterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="d296a-128">EnterpriseNetworkDomainNames</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d296a-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d296a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d296a-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d296a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d296a-131">EnterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="d296a-131">EnterpriseProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d296a-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d296a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d296a-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d296a-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d296a-134">EnterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="d296a-134">EnterpriseProxyServersAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d296a-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d296a-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d296a-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d296a-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d296a-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d296a-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d296a-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d296a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d296a-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d296a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d296a-140">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d296a-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d296a-141">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d296a-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="d296a-142">Pour cette classe, la chaîne est « NetworkIsolation ».</span><span class="sxs-lookup"><span data-stu-id="d296a-142">For this class, the string is "NetworkIsolation".</span></span>

</dd> <dt>

[<span data-ttu-id="d296a-143">NeutralResources</span><span class="sxs-lookup"><span data-stu-id="d296a-143">NeutralResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d296a-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d296a-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d296a-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d296a-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d296a-146">**ID**</span><span class="sxs-lookup"><span data-stu-id="d296a-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d296a-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d296a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d296a-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d296a-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d296a-149">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d296a-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d296a-150">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d296a-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="d296a-151">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="d296a-151">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d296a-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d296a-152">Requirements</span></span>



| <span data-ttu-id="d296a-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d296a-153">Requirement</span></span> | <span data-ttu-id="d296a-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="d296a-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d296a-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d296a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="d296a-156">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d296a-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d296a-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d296a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="d296a-158">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d296a-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d296a-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d296a-159">Namespace</span></span><br/>                | <span data-ttu-id="d296a-160">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d296a-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d296a-161">MOF</span><span class="sxs-lookup"><span data-stu-id="d296a-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d296a-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d296a-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d296a-163">DLL</span><span class="sxs-lookup"><span data-stu-id="d296a-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d296a-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d296a-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

