---
title: Classe MicrosoftDNS_RootHints
description: La \_ classe MicrosoftDNS RootHints décrit les RootHints stockés dans un fichier cache sur un serveur DNS. Cette classe simplifie la visualisation de la relation contenant-contenu des objets DNS, plutôt que la représentation d’un objet réel.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- MicrosoftDNS_RootHints de la classe DNS
- MicrosoftDNS_RootHints de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104158"
---
# <a name="microsoftdns_roothints-class"></a><span data-ttu-id="6c9b2-106">MicrosoftDNS \_ RootHints, classe</span><span class="sxs-lookup"><span data-stu-id="6c9b2-106">MicrosoftDNS\_RootHints class</span></span>

<span data-ttu-id="6c9b2-107">La classe **MicrosoftDNS \_ RootHints** décrit les RootHints stockés dans un fichier cache sur un serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="6c9b2-107">The **MicrosoftDNS\_RootHints** class describes the RootHints stored in a Cache file on a DNS Server.</span></span> <span data-ttu-id="6c9b2-108">Cette classe simplifie la visualisation de la relation contenant-contenu des objets DNS, plutôt que la représentation d’un objet réel.</span><span class="sxs-lookup"><span data-stu-id="6c9b2-108">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span>

<span data-ttu-id="6c9b2-109">**MicrosoftDNS \_ RootHints** est un conteneur pour les enregistrements de ressources stockés par le serveur DNS dans un fichier cache.</span><span class="sxs-lookup"><span data-stu-id="6c9b2-109">**MicrosoftDNS\_RootHints** is a container for the resource records stored by the DNS Server in a Cache file.</span></span> <span data-ttu-id="6c9b2-110">Chaque instance de la **classe \_ RootHints MicrosoftDNS** doit être affectée à un seul serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="6c9b2-110">Every instance of the **MicrosoftDNS\_RootHints** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="6c9b2-111">Il peut être associé à plusieurs instances de la [**classe \_ ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="6c9b2-111">It may be associated with multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

<span data-ttu-id="6c9b2-112">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="6c9b2-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c9b2-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c9b2-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="6c9b2-114">Membres</span><span class="sxs-lookup"><span data-stu-id="6c9b2-114">Members</span></span>

<span data-ttu-id="6c9b2-115">La classe **MicrosoftDNS \_ RootHints** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6c9b2-115">The **MicrosoftDNS\_RootHints** class has these types of members:</span></span>

-   [<span data-ttu-id="6c9b2-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6c9b2-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6c9b2-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6c9b2-117">Methods</span></span>

<span data-ttu-id="6c9b2-118">La classe **MicrosoftDNS \_ RootHints** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6c9b2-118">The **MicrosoftDNS\_RootHints** class has these methods.</span></span>



| <span data-ttu-id="6c9b2-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="6c9b2-119">Method</span></span>                        | <span data-ttu-id="6c9b2-120">Description</span><span class="sxs-lookup"><span data-stu-id="6c9b2-120">Description</span></span>                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9b2-121">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="6c9b2-121">**GetDistinguishedName**</span></span>      | <span data-ttu-id="6c9b2-122">Récupère le nom unique de la zone.</span><span class="sxs-lookup"><span data-stu-id="6c9b2-122">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="6c9b2-123">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="6c9b2-123">Qualifiers: Implemented</span></span><br/>   |
| <span data-ttu-id="6c9b2-124">**WriteBackRootHintDatafile**</span><span class="sxs-lookup"><span data-stu-id="6c9b2-124">**WriteBackRootHintDatafile**</span></span> | <span data-ttu-id="6c9b2-125">Réécrit le RootHints dans le fichier cache DNS.</span><span class="sxs-lookup"><span data-stu-id="6c9b2-125">Writes the RootHints back to the DNS Cache file.</span></span> <br/> <span data-ttu-id="6c9b2-126">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="6c9b2-126">Qualifiers: Implemented</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6c9b2-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c9b2-127">Requirements</span></span>



| <span data-ttu-id="6c9b2-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c9b2-128">Requirement</span></span> | <span data-ttu-id="6c9b2-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c9b2-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9b2-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c9b2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6c9b2-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c9b2-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6c9b2-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c9b2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6c9b2-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c9b2-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6c9b2-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6c9b2-134">Namespace</span></span><br/>                | <span data-ttu-id="6c9b2-135">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="6c9b2-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6c9b2-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6c9b2-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c9b2-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c9b2-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c9b2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c9b2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c9b2-139">**\_Domaine MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6c9b2-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="6c9b2-140">**Méthode WriteBackRootHintDatafile de la \_ classe MicrosoftDNS RootHints**</span><span class="sxs-lookup"><span data-stu-id="6c9b2-140">**WriteBackRootHintDatafile Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[<span data-ttu-id="6c9b2-141">**Méthode GetDistinguishedName de la \_ classe MicrosoftDNS RootHints**</span><span class="sxs-lookup"><span data-stu-id="6c9b2-141">**GetDistinguishedName Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





