---
title: Classe MicrosoftDNS_DomainDomainContainment
description: La \_ classe DomainDomainContainment MicrosoftDNS est utilisée pour la relation contenant-contenu d’un domaine ; Les domaines DNS peuvent contenir d’autres domaines DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- MicrosoftDNS_DomainDomainContainment de la classe DNS
- MicrosoftDNS_DomainDomainContainment de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033105"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a><span data-ttu-id="8c472-105">MicrosoftDNS \_ DomainDomainContainment, classe</span><span class="sxs-lookup"><span data-stu-id="8c472-105">MicrosoftDNS\_DomainDomainContainment class</span></span>

<span data-ttu-id="8c472-106">La **classe \_ DomainDomainContainment MicrosoftDNS** est utilisée pour la relation contenant-contenu d’un domaine ; Les domaines DNS peuvent contenir d’autres domaines DNS.</span><span class="sxs-lookup"><span data-stu-id="8c472-106">The **MicrosoftDNS\_DomainDomainContainment** class is used for domain containment; DNS domains may contain other DNS domains.</span></span> <span data-ttu-id="8c472-107">Chaque instance de la classe de [**\_ domaine MicrosoftDNS**](microsoftdns-domain.md) peut contenir plusieurs autres instances **du \_ domaine MicrosoftDNS**.</span><span class="sxs-lookup"><span data-stu-id="8c472-107">Every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class may contain multiple other instances of **MicrosoftDNS\_Domain**.</span></span> <span data-ttu-id="8c472-108">Une instance d’un objet de **\_ domaine MicrosoftDNS** est directement contenue dans un seul **\_ domaine MicrosoftDNS** de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="8c472-108">An instance of a **MicrosoftDNS\_Domain** object is directly contained in no more than one higher level **MicrosoftDNS\_Domain**.</span></span>

<span data-ttu-id="8c472-109">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="8c472-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c472-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c472-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="8c472-111">Membres</span><span class="sxs-lookup"><span data-stu-id="8c472-111">Members</span></span>

<span data-ttu-id="8c472-112">La classe **MicrosoftDNS \_ DomainDomainContainment** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8c472-112">The **MicrosoftDNS\_DomainDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="8c472-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8c472-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c472-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8c472-114">Properties</span></span>

<span data-ttu-id="8c472-115">La classe **MicrosoftDNS \_ DomainDomainContainment** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8c472-115">The **MicrosoftDNS\_DomainDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c472-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8c472-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c472-117">Type de données **: \_ domaine MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8c472-117">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="8c472-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c472-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c472-119">Qualificateurs : clé, Max (1), override ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="8c472-119">Qualifiers: Key, Max(1), Override("GroupComponent")</span></span>

<span data-ttu-id="8c472-120">Description : domaine, zone, cache ou RootHints de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="8c472-120">Description: A higher level Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="8c472-121">Hérité du \_ composant CIM</span><span class="sxs-lookup"><span data-stu-id="8c472-121">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="8c472-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8c472-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c472-123">Type de données **: \_ domaine MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8c472-123">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="8c472-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c472-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c472-125">Qualificateurs : clé, remplacement ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="8c472-125">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="8c472-126">Description : domaine contenu par un domaine de niveau supérieur, zone, cache ou RootHints.</span><span class="sxs-lookup"><span data-stu-id="8c472-126">Description: The Domain contained by a higher level Domain, Zone, Cache or RootHints.</span></span>

<span data-ttu-id="8c472-127">Hérité du \_ composant CIM.</span><span class="sxs-lookup"><span data-stu-id="8c472-127">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c472-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c472-128">Requirements</span></span>



| <span data-ttu-id="8c472-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c472-129">Requirement</span></span> | <span data-ttu-id="8c472-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c472-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c472-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c472-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8c472-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c472-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8c472-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c472-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8c472-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c472-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8c472-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8c472-135">Namespace</span></span><br/>                | <span data-ttu-id="8c472-136">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="8c472-136">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8c472-137">MOF</span><span class="sxs-lookup"><span data-stu-id="8c472-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c472-138"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c472-138"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c472-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c472-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c472-140">**MicrosoftDNS \_ DomainResourceRecordContainment**</span><span class="sxs-lookup"><span data-stu-id="8c472-140">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="8c472-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8c472-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="8c472-142">**MicrosoftDNS \_ ServerDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="8c472-142">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





