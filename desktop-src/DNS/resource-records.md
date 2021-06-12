---
title: Enregistrements de ressources
description: En savoir plus sur les enregistrements de ressources. Un enregistrement de ressource est l’unité d’entrée d’informations dans les fichiers de zone DNS, qui permet de résoudre toutes les requêtes DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84bd000e2d88884bbb387748eaced1d0d58a324
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010672"
---
# <a name="resource-records"></a><span data-ttu-id="3af66-104">Enregistrements de ressources</span><span class="sxs-lookup"><span data-stu-id="3af66-104">Resource Records</span></span>

<span data-ttu-id="3af66-105">Un enregistrement de ressource, communément appelé RR, est l’unité d’entrée d’informations dans les fichiers de zone DNS. Les RR sont les blocs de construction de base des informations IP et de nom d’hôte et sont utilisés pour résoudre toutes les requêtes DNS.</span><span class="sxs-lookup"><span data-stu-id="3af66-105">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="3af66-106">Les enregistrements de ressources existent sous la forme de plusieurs types pour fournir des services de résolution de noms étendus.</span><span class="sxs-lookup"><span data-stu-id="3af66-106">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="3af66-107">Les différents types de RR ont des formats différents, car ils contiennent des données différentes.</span><span class="sxs-lookup"><span data-stu-id="3af66-107">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="3af66-108">En général, toutefois, de nombreux RR partagent un format commun, comme l’illustre l’exemple d’enregistrement de ressource d’adresse suivant.</span><span class="sxs-lookup"><span data-stu-id="3af66-108">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="3af66-109">L’exemple fictif suivant explique les champs trouvés dans un enregistrement de ressource A :</span><span class="sxs-lookup"><span data-stu-id="3af66-109">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="3af66-110">Le premier champ (microsoft.com) indique le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="3af66-110">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="3af66-111">Le deuxième champ (600) est le paramètre de durée de vie (TTL, Time-to-Live), en secondes.</span><span class="sxs-lookup"><span data-stu-id="3af66-111">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="3af66-112">Le troisième champ (dans) est le champ de classe qui représente la famille de protocoles, qui est presque toujours dans, pour la classe Internet.</span><span class="sxs-lookup"><span data-stu-id="3af66-112">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="3af66-113">Le quatrième champ (A) est le type de ressource que le RR représente.</span><span class="sxs-lookup"><span data-stu-id="3af66-113">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="3af66-114">Le cinquième champ (150.150.150.1) est les données de ressource, ou RDATA.</span><span class="sxs-lookup"><span data-stu-id="3af66-114">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="3af66-115">Ce champ est un type de variable qui fournit des informations appropriées pour le type de ressource ; dans ce cas, il s’agit d’une adresse IP 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3af66-115">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="3af66-116">Les types d’enregistrements de ressources suivants sont couramment utilisés dans DNS :</span><span class="sxs-lookup"><span data-stu-id="3af66-116">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="3af66-117">SOA (Start of Authority)</span><span class="sxs-lookup"><span data-stu-id="3af66-117">Start of authority (SOA)</span></span>
-   <span data-ttu-id="3af66-118">Serveur de noms (NS)</span><span class="sxs-lookup"><span data-stu-id="3af66-118">Name server (NS)</span></span>
-   <span data-ttu-id="3af66-119">[*Enregistrement de pointeur*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="3af66-119">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="3af66-120">Adresse (A)</span><span class="sxs-lookup"><span data-stu-id="3af66-120">Address (A)</span></span>
-   <span data-ttu-id="3af66-121">Adresse IPv6 (AAAA)</span><span class="sxs-lookup"><span data-stu-id="3af66-121">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="3af66-122">Exchange mail (MX)</span><span class="sxs-lookup"><span data-stu-id="3af66-122">Mail exchange (MX)</span></span>
-   <span data-ttu-id="3af66-123">[*Nom canonique*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="3af66-123">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="3af66-124">Windows Internet Service de nommage (WINS)</span><span class="sxs-lookup"><span data-stu-id="3af66-124">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="3af66-125">Recherche inversée WINS (WINSr)</span><span class="sxs-lookup"><span data-stu-id="3af66-125">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="3af66-126">Il existe de nombreux autres types d’enregistrements de ressources dans DNS.</span><span class="sxs-lookup"><span data-stu-id="3af66-126">There are many other resource record types in DNS.</span></span> <span data-ttu-id="3af66-127">Pour plus d’informations, consultez [Référence du fournisseur WMI DNS](dns-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3af66-127">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




