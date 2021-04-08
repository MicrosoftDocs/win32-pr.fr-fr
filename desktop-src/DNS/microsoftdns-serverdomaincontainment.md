---
title: Classe MicrosoftDNS_ServerDomainContainment
description: Chaque instance de la \_ classe WMI de l’Association de serveurs MicrosoftDNS peut contenir plusieurs instances de la classe de domaine MicrosoftDNS \_ .
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- MicrosoftDNS_ServerDomainContainment de la classe DNS
- MicrosoftDNS_ServerDomainContainment de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740268"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a><span data-ttu-id="d71ba-105">MicrosoftDNS \_ ServerDomainContainment, classe</span><span class="sxs-lookup"><span data-stu-id="d71ba-105">MicrosoftDNS\_ServerDomainContainment class</span></span>

<span data-ttu-id="d71ba-106">Chaque instance de la classe WMI de l’Association de [**\_ serveurs MicrosoftDNS**](microsoftdns-server.md) peut contenir plusieurs instances de la classe de [**\_ domaine MicrosoftDNS**](microsoftdns-domain.md) .</span><span class="sxs-lookup"><span data-stu-id="d71ba-106">Every instance of the [**MicrosoftDNS\_Server**](microsoftdns-server.md) association WMI class may contain multiple instances of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class.</span></span> <span data-ttu-id="d71ba-107">Chaque instance de la classe de **\_ domaine MicrosoftDNS** appartient à une instance unique de la classe de **\_ serveur MicrosoftDNS** et est définie comme étant faible à ce serveur.</span><span class="sxs-lookup"><span data-stu-id="d71ba-107">Every instance of the **MicrosoftDNS\_Domain** class belongs to a single instance of the **MicrosoftDNS\_Server** class, and is defined to be weak to that server.</span></span>

<span data-ttu-id="d71ba-108">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d71ba-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d71ba-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d71ba-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d71ba-110">Membres</span><span class="sxs-lookup"><span data-stu-id="d71ba-110">Members</span></span>

<span data-ttu-id="d71ba-111">La classe **MicrosoftDNS \_ ServerDomainContainment** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d71ba-111">The **MicrosoftDNS\_ServerDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="d71ba-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d71ba-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d71ba-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d71ba-113">Properties</span></span>

<span data-ttu-id="d71ba-114">La classe **MicrosoftDNS \_ ServerDomainContainment** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d71ba-114">The **MicrosoftDNS\_ServerDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d71ba-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d71ba-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d71ba-116">Type de données **: \_ serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d71ba-116">Data type: **MicrosoftDNS\_Server**</span></span>
</dt> <dt>

<span data-ttu-id="d71ba-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d71ba-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d71ba-118">Qualificateurs : clé, remplacement ("GroupComponent"), min (1), Max (1)</span><span class="sxs-lookup"><span data-stu-id="d71ba-118">Qualifiers: Key, Override ("GroupComponent"), Min (1), Max (1)</span></span>

<span data-ttu-id="d71ba-119">Description : serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="d71ba-119">Description: The DNS Server.</span></span>

<span data-ttu-id="d71ba-120">Hérité du **\_ composant CIM**.</span><span class="sxs-lookup"><span data-stu-id="d71ba-120">Inherited from **CIM\_Component**.</span></span>

</dd> <dt>

<span data-ttu-id="d71ba-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d71ba-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d71ba-122">Type de données **: \_ domaine MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d71ba-122">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="d71ba-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d71ba-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d71ba-124">Qualificateurs : clé, remplacement ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="d71ba-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="d71ba-125">Description : domaine, zone, cache ou RootHints géré par le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="d71ba-125">Description: A Domain, Zone, Cache, or RootHints managed by the DNS Server.</span></span>

<span data-ttu-id="d71ba-126">Hérité du **\_ composant CIM**.</span><span class="sxs-lookup"><span data-stu-id="d71ba-126">Inherited from **CIM\_Component**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d71ba-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d71ba-127">Remarks</span></span>

<span data-ttu-id="d71ba-128">La classe **MicrosoftDNS \_ ServerDomainContainment** est dérivée de la classe de **\_ composant CIM** .</span><span class="sxs-lookup"><span data-stu-id="d71ba-128">The **MicrosoftDNS\_ServerDomainContainment** class is derived from the **CIM\_Component** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d71ba-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d71ba-129">Requirements</span></span>



| <span data-ttu-id="d71ba-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d71ba-130">Requirement</span></span> | <span data-ttu-id="d71ba-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d71ba-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d71ba-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d71ba-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d71ba-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d71ba-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d71ba-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d71ba-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d71ba-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d71ba-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d71ba-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d71ba-136">Namespace</span></span><br/>                | <span data-ttu-id="d71ba-137">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="d71ba-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d71ba-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d71ba-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d71ba-139"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d71ba-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d71ba-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d71ba-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d71ba-141">**MicrosoftDNS \_ DomainDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="d71ba-141">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="d71ba-142">**MicrosoftDNS \_ DomainResourceRecordContainment**</span><span class="sxs-lookup"><span data-stu-id="d71ba-142">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="d71ba-143">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d71ba-143">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





