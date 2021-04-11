---
title: Classe MicrosoftDNS_Domain
description: La \_ classe de domaine MicrosoftDNS représente un domaine dans une hiérarchie DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- MicrosoftDNS_Domain de la classe DNS
- MicrosoftDNS_Domain de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103708"
---
# <a name="microsoftdns_domain-class"></a><span data-ttu-id="c2a1d-105">\_Classe de domaine MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c2a1d-105">MicrosoftDNS\_Domain class</span></span>

<span data-ttu-id="c2a1d-106">La classe de **\_ domaine MicrosoftDNS** représente un domaine dans une hiérarchie DNS.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-106">The **MicrosoftDNS\_Domain** class represents a Domain in a DNS hierarchy.</span></span>

<span data-ttu-id="c2a1d-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a1d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2a1d-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="c2a1d-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c2a1d-109">Members</span></span>

<span data-ttu-id="c2a1d-110">La classe de **\_ domaine MicrosoftDNS** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c2a1d-110">The **MicrosoftDNS\_Domain** class has these types of members:</span></span>

-   [<span data-ttu-id="c2a1d-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c2a1d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c2a1d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c2a1d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c2a1d-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c2a1d-113">Methods</span></span>

<span data-ttu-id="c2a1d-114">La classe de **\_ domaine MicrosoftDNS** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-114">The **MicrosoftDNS\_Domain** class has these methods.</span></span>



| <span data-ttu-id="c2a1d-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="c2a1d-115">Method</span></span>                   | <span data-ttu-id="c2a1d-116">Description</span><span class="sxs-lookup"><span data-stu-id="c2a1d-116">Description</span></span>                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a1d-117">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-117">**GetDistinguishedName**</span></span> | <span data-ttu-id="c2a1d-118">Obtient le nom unique du service d’annuaire pour la zone.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-118">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="c2a1d-119">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="c2a1d-119">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c2a1d-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c2a1d-120">Properties</span></span>

<span data-ttu-id="c2a1d-121">La classe de **\_ domaine MicrosoftDNS** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-121">The **MicrosoftDNS\_Domain** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2a1d-122">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-122">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a1d-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2a1d-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2a1d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2a1d-125">Nom du conteneur du domaine, qui peut être une zone, un cache ou une RootHints.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-125">Name of the container of the domain, which could be a Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="c2a1d-126">Dans les cas où le conteneur est une zone (une instance de la classe de [**\_ zone MicrosoftDNS**](microsoftdns-zone.md) ), cette propriété contient le nom de domaine complet de la zone.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-126">In cases where the Container is a Zone (an instance of the [**MicrosoftDNS\_Zone**](microsoftdns-zone.md) class), this property contains the FQDN of the Zone.</span></span>

<span data-ttu-id="c2a1d-127">Lorsque le conteneur est la zone racine, la chaîne \\ \\ doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-127">When the Container is the root zone, the string \\.\\ should be used.</span></span>

<span data-ttu-id="c2a1d-128">Dans les cas où le conteneur est le cache DNS des enregistrements de ressource (une instance de la classe de [**\_ cache MicrosoftDNS**](microsoftdns-cache.md) ), cette propriété est définie sur la chaîne \\ . Cache \\ .</span><span class="sxs-lookup"><span data-stu-id="c2a1d-128">In cases where the Container is the DNS cache of resource records (an instance of the [**MicrosoftDNS\_Cache**](microsoftdns-cache.md) class), this property is set to the string \\..Cache\\.</span></span>

<span data-ttu-id="c2a1d-129">Si le conteneur est RootHints (une instance de la classe [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md) ), cette propriété doit avoir la valeur \\ .. RootHints \\ .</span><span class="sxs-lookup"><span data-stu-id="c2a1d-129">If the Container is RootHints (an instance of the [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md) class), this property should be set to \\..RootHints\\.</span></span>

</dd> <dt>

<span data-ttu-id="c2a1d-130">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a1d-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2a1d-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2a1d-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2a1d-133">Nom de domaine complet ou adresse IP du serveur DNS qui contient le domaine.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-133">FQDN or IP address of the DNS Server that contains the domain.</span></span>

</dd> <dt>

<span data-ttu-id="c2a1d-134">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a1d-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2a1d-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2a1d-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2a1d-137">Nom de domaine complet du domaine.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-137">FQDN of the domain.</span></span>

<span data-ttu-id="c2a1d-138">Pour les instances de cache DNS ou RootHints, les chaînes \\ .. Cache \\ et \\ .. RootHints \\ doit être utilisé, respectivement.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-138">For instances of DNS Cache or RootHints, the strings \\..Cache\\ and \\..RootHints\\ should be used, respectively.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2a1d-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2a1d-139">Requirements</span></span>



| <span data-ttu-id="c2a1d-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2a1d-140">Requirement</span></span> | <span data-ttu-id="c2a1d-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2a1d-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a1d-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2a1d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a1d-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2a1d-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c2a1d-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2a1d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a1d-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2a1d-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c2a1d-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c2a1d-146">Namespace</span></span><br/>                | <span data-ttu-id="c2a1d-147">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="c2a1d-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c2a1d-148">MOF</span><span class="sxs-lookup"><span data-stu-id="c2a1d-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2a1d-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2a1d-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2a1d-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2a1d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a1d-151">**Méthode GetDistinguishedName de la \_ classe de domaine MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-151">**GetDistinguishedName Method of the MicrosoftDNS\_Domain Class**</span></span>](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





