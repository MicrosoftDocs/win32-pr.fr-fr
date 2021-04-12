---
title: Classe MicrosoftDNS_DomainResourceRecordContainment
description: La \_ classe DomainResourceRecordContainment MicrosoftDNS est utilisée pour la relation contenant-contenu des RR ; chaque instance du \_ domaine MicrosoftDNS peut contenir plusieurs instances de la \_ classe ResourceRecord MicrosoftDNS.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- MicrosoftDNS_DomainResourceRecordContainment de la classe DNS
- MicrosoftDNS_DomainResourceRecordContainment de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465334"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a><span data-ttu-id="21484-105">MicrosoftDNS \_ DomainResourceRecordContainment, classe</span><span class="sxs-lookup"><span data-stu-id="21484-105">MicrosoftDNS\_DomainResourceRecordContainment class</span></span>

<span data-ttu-id="21484-106">La **classe \_ DomainResourceRecordContainment MicrosoftDNS** est utilisée pour la relation contenant-contenu des RR ; chaque instance du [**\_ domaine MicrosoftDNS**](microsoftdns-domain.md) peut contenir plusieurs instances de la classe [**\_ ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="21484-106">The **MicrosoftDNS\_DomainResourceRecordContainment** class is used for RR containment; every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) may contain multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span> <span data-ttu-id="21484-107">Chaque instance de la **classe \_ ResourceRecord MicrosoftDNS** appartient à une instance unique de la classe de **\_ domaine MicrosoftDNS** et est définie comme étant faible à cette instance.</span><span class="sxs-lookup"><span data-stu-id="21484-107">Every instance of the **MicrosoftDNS\_ResourceRecord** class belongs to a single instance of the **MicrosoftDNS\_Domain** class, and is defined to be weak to that instance.</span></span>

<span data-ttu-id="21484-108">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="21484-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="21484-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21484-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="21484-110">Membres</span><span class="sxs-lookup"><span data-stu-id="21484-110">Members</span></span>

<span data-ttu-id="21484-111">La classe **MicrosoftDNS \_ DomainResourceRecordContainment** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="21484-111">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="21484-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="21484-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21484-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="21484-113">Properties</span></span>

<span data-ttu-id="21484-114">La classe **MicrosoftDNS \_ DomainResourceRecordContainment** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="21484-114">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21484-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="21484-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21484-116">Type de données **: \_ domaine MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="21484-116">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="21484-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="21484-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21484-118">Qualificateurs : clé, substitution ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="21484-118">Qualifiers: Key, Override("GroupComponent")</span></span>

<span data-ttu-id="21484-119">Description : zone, cache, RootHints ou domaine directement contenant l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="21484-119">Description: The Zone, Cache, RootHints or Domain directly containing the Resource Record.</span></span>

<span data-ttu-id="21484-120">Hérité du \_ composant CIM</span><span class="sxs-lookup"><span data-stu-id="21484-120">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="21484-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="21484-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21484-122">Type de données : **MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="21484-122">Data type: **MicrosoftDNS\_ResourceRecord**</span></span>
</dt> <dt>

<span data-ttu-id="21484-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="21484-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21484-124">Qualificateurs : clé, remplacement ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="21484-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="21484-125">Description : l’enregistrement de ressource contenu dans un domaine, une zone, un cache ou un RootHints.</span><span class="sxs-lookup"><span data-stu-id="21484-125">Description: The resource record contained in a Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="21484-126">Hérité du \_ composant CIM.</span><span class="sxs-lookup"><span data-stu-id="21484-126">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21484-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21484-127">Requirements</span></span>



| <span data-ttu-id="21484-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21484-128">Requirement</span></span> | <span data-ttu-id="21484-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="21484-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21484-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21484-130">Minimum supported client</span></span><br/> | <span data-ttu-id="21484-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="21484-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="21484-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21484-132">Minimum supported server</span></span><br/> | <span data-ttu-id="21484-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21484-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="21484-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="21484-134">Namespace</span></span><br/>                | <span data-ttu-id="21484-135">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="21484-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="21484-136">MOF</span><span class="sxs-lookup"><span data-stu-id="21484-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21484-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21484-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21484-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21484-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21484-139">**MicrosoftDNS \_ ServerDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="21484-139">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="21484-140">**MicrosoftDNS \_ DomainDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="21484-140">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="21484-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="21484-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





