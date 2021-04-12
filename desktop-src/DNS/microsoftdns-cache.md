---
title: Classe MicrosoftDNS_Cache
description: La \_ classe de cache MicrosoftDNS décrit un cache existant sur un serveur DNS.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- MicrosoftDNS_Cache de la classe DNS
- MicrosoftDNS_Cache de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032870"
---
# <a name="microsoftdns_cache-class"></a><span data-ttu-id="05676-105">\_Classe de cache MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="05676-105">MicrosoftDNS\_Cache class</span></span>

<span data-ttu-id="05676-106">La classe de **\_ cache MicrosoftDNS** décrit un cache existant sur un serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="05676-106">The **MicrosoftDNS\_Cache** class describes a cache existing on a DNS Server.</span></span> <span data-ttu-id="05676-107">Cette classe simplifie la visualisation de la relation contenant-contenu des objets DNS, plutôt que la représentation d’un objet réel.</span><span class="sxs-lookup"><span data-stu-id="05676-107">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span> <span data-ttu-id="05676-108">La classe de **\_ cache MicrosoftDNS** est un conteneur pour les enregistrements de ressource mis en cache par le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="05676-108">The **MicrosoftDNS\_Cache** class is a container for the resource records cached by the DNS Server.</span></span> <span data-ttu-id="05676-109">Ne confondez pas cela avec un fichier cache qui contient des indications de racine.</span><span class="sxs-lookup"><span data-stu-id="05676-109">Do not confuse this with a Cache file that contains root hints.</span></span>

<span data-ttu-id="05676-110">Chaque instance du **\_ cache** de la classe MicrosoftDNS doit être affectée à un seul serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="05676-110">Every instance of the class **MicrosoftDNS\_Cache** must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="05676-111">Il peut être associé à plusieurs instances de classes [**MicrosoftDNS \_ Domain**](microsoftdns-domain.md) ou [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="05676-111">It may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="05676-112">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="05676-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="05676-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05676-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="05676-114">Membres</span><span class="sxs-lookup"><span data-stu-id="05676-114">Members</span></span>

<span data-ttu-id="05676-115">La classe de **\_ cache MicrosoftDNS** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="05676-115">The **MicrosoftDNS\_Cache** class has these types of members:</span></span>

-   [<span data-ttu-id="05676-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="05676-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="05676-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="05676-117">Methods</span></span>

<span data-ttu-id="05676-118">La classe de **\_ cache MicrosoftDNS** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="05676-118">The **MicrosoftDNS\_Cache** class has these methods.</span></span>



| <span data-ttu-id="05676-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="05676-119">Method</span></span>                   | <span data-ttu-id="05676-120">Description</span><span class="sxs-lookup"><span data-stu-id="05676-120">Description</span></span>                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05676-121">**ClearCache**</span><span class="sxs-lookup"><span data-stu-id="05676-121">**ClearCache**</span></span>           | <span data-ttu-id="05676-122">Efface le cache du serveur DNS des enregistrements de ressources.</span><span class="sxs-lookup"><span data-stu-id="05676-122">Clears the DNS Server cache of resource records.</span></span> <br/> <span data-ttu-id="05676-123">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="05676-123">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="05676-124">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="05676-124">**GetDistinguishedName**</span></span> | <span data-ttu-id="05676-125">Récupère le nom unique de la zone.</span><span class="sxs-lookup"><span data-stu-id="05676-125">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="05676-126">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="05676-126">Qualifiers: Implemented</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="05676-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05676-127">Requirements</span></span>



| <span data-ttu-id="05676-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05676-128">Requirement</span></span> | <span data-ttu-id="05676-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="05676-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05676-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05676-130">Minimum supported client</span></span><br/> | <span data-ttu-id="05676-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="05676-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="05676-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05676-132">Minimum supported server</span></span><br/> | <span data-ttu-id="05676-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05676-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="05676-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="05676-134">Namespace</span></span><br/>                | <span data-ttu-id="05676-135">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="05676-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="05676-136">MOF</span><span class="sxs-lookup"><span data-stu-id="05676-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05676-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05676-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05676-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05676-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05676-139">**\_Domaine MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="05676-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="05676-140">**Méthode ClearCache de la \_ classe de cache MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="05676-140">**ClearCache Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-clearcache.md)
</dt> <dt>

[<span data-ttu-id="05676-141">**Méthode GetDistinguishedName de la \_ classe de cache MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="05676-141">**GetDistinguishedName Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





