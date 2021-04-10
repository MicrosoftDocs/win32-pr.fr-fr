---
title: Classe MDM_VPNv2_DomainNameInformationList02_01
description: La \_ classe MDM VPNv2 \_ DomainNameInformationList02 \_ 01 décrit les règles de table de stratégie de résolution de noms (NRPT) pour le profil VPN.
ms.assetid: ed6863aa-f85e-4f65-9312-ddf60a8c0d5a
keywords:
- Classe MDM_VPNv2_DomainNameInformationList02_01
- Classe MDM_VPNv2_DomainNameInformationList02_01, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01.InstanceID
- MDM_VPNv2_DomainNameInformationList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2fa2b6fd4216256a085caa23333bccc5f386d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942692"
---
# <a name="mdm_vpnv2_domainnameinformationlist02_01-class"></a><span data-ttu-id="3b2f4-105">\_Classe VPNv2 \_ DOMAINNAMEINFORMATIONLIST02 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="3b2f4-105">MDM\_VPNv2\_DomainNameInformationList02\_01 class</span></span>

<span data-ttu-id="3b2f4-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3b2f4-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="3b2f4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3b2f4-108">La classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** décrit les règles de table de stratégie de résolution de noms (NRPT) pour le profil VPN.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-108">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class describes the Name Resolution Policy Table (NRPT) rules for the VPN profile.</span></span>

<span data-ttu-id="3b2f4-109">La table de stratégie de résolution de noms (NRPT) est une table d’espaces de noms et les paramètres correspondants stockés dans le Registre Windows qui déterminent le comportement du client DNS lors de l’émission de requêtes et du traitement des réponses.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-109">The Name Resolution Policy Table (NRPT) is a table of namespaces and corresponding settings stored in the Windows registry that determines the DNS client behavior when issuing queries and processing responses.</span></span> <span data-ttu-id="3b2f4-110">Chaque ligne de la table NRPT représente une règle pour une partie de l’espace de noms pour lequel le client DNS émet des requêtes.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-110">Each row in the NRPT represents a rule for a portion of the namespace for which the DNS client issues queries.</span></span> <span data-ttu-id="3b2f4-111">Avant d’émettre des requêtes de résolution de noms, le client DNS consulte la table NRPT pour déterminer si des indicateurs supplémentaires doivent être définis dans la requête.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-111">Before issuing name resolution queries, the DNS client consults the NRPT to determine if any additional flags must be set in the query.</span></span> <span data-ttu-id="3b2f4-112">Une fois la réponse reçue, le client consulte à nouveau la table NRPT pour vérifier s’il existe des exigences de traitement ou de stratégie spéciales.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-112">After receiving the response, the client again consults the NRPT to check for any special processing or policy requirements.</span></span> <span data-ttu-id="3b2f4-113">En l’absence de la table NRPT, le client opère en fonction des suffixes et des serveurs DNS définis sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-113">In the absence of the NRPT, the client operates based on the DNS servers and suffixes set on the interface.</span></span>

<span data-ttu-id="3b2f4-114">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b2f4-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b2f4-115">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DomainNameInformationList02_01
{
  string InstanceID;
  string ParentID;
  string DomainName;
  string DomainNameType;
  string DnsServers;
  string WebProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="3b2f4-116">Membres</span><span class="sxs-lookup"><span data-stu-id="3b2f4-116">Members</span></span>

<span data-ttu-id="3b2f4-117">La classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3b2f4-117">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="3b2f4-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b2f4-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b2f4-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b2f4-119">Properties</span></span>

<span data-ttu-id="3b2f4-120">La classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-120">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3b2f4-121">DnsServers</span><span class="sxs-lookup"><span data-stu-id="3b2f4-121">DnsServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-dnsservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2f4-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b2f4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b2f4-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b2f4-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b2f4-124">DomainName</span><span class="sxs-lookup"><span data-stu-id="3b2f4-124">DomainName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2f4-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b2f4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b2f4-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b2f4-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b2f4-127">DomainNameType</span><span class="sxs-lookup"><span data-stu-id="3b2f4-127">DomainNameType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainnametype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2f4-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b2f4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b2f4-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b2f4-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b2f4-130">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b2f4-130">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2f4-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b2f4-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b2f4-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b2f4-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b2f4-133">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b2f4-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3b2f4-134">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-134">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="3b2f4-135">**ID**</span><span class="sxs-lookup"><span data-stu-id="3b2f4-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2f4-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b2f4-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b2f4-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b2f4-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b2f4-138">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b2f4-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3b2f4-139">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="3b2f4-139">Describes the full path to the parent node.</span></span> <span data-ttu-id="3b2f4-140">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*»</span><span class="sxs-lookup"><span data-stu-id="3b2f4-140">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="3b2f4-141">WebProxyServers</span><span class="sxs-lookup"><span data-stu-id="3b2f4-141">WebProxyServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-webproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2f4-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b2f4-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b2f4-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b2f4-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b2f4-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b2f4-144">Requirements</span></span>



| <span data-ttu-id="3b2f4-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b2f4-145">Requirement</span></span> | <span data-ttu-id="3b2f4-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b2f4-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b2f4-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b2f4-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3b2f4-148">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b2f4-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b2f4-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b2f4-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3b2f4-150">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b2f4-150">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3b2f4-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3b2f4-151">Namespace</span></span><br/>                | <span data-ttu-id="3b2f4-152">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="3b2f4-152">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3b2f4-153">MOF</span><span class="sxs-lookup"><span data-stu-id="3b2f4-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b2f4-154"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b2f4-154"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b2f4-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3b2f4-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b2f4-156"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b2f4-156"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b2f4-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b2f4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b2f4-158">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="3b2f4-158">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

