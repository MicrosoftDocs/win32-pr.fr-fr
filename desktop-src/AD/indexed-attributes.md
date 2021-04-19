---
title: Attributs indexés (AD DS)
description: Les attributs peuvent être indexés. L’indexation d’un attribut peut améliorer les performances des requêtes de cet attribut.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Attributs indexés Active Directory
- Attributs AD, indexés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "106511885"
---
# <a name="indexed-attributes-ad-ds"></a><span data-ttu-id="e7b5d-106">Attributs indexés (AD DS)</span><span class="sxs-lookup"><span data-stu-id="e7b5d-106">Indexed Attributes (AD DS)</span></span>

<span data-ttu-id="e7b5d-107">Les attributs peuvent être indexés.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-107">Attributes may be indexed.</span></span> <span data-ttu-id="e7b5d-108">L’indexation d’un attribut peut améliorer les performances des requêtes de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-108">Indexing an attribute can improve the performance of queries for that attribute.</span></span>

<span data-ttu-id="e7b5d-109">Un attribut est indexé lorsque l’attribut [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) dans la définition de schéma de l’attribut a le bit le moins significatif défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-109">An attributes is indexed when the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute in the attribute's schema definition has the least significant bit set to 1.</span></span> <span data-ttu-id="e7b5d-110">La définition du bit le moins significatif de la définition de schéma de l’attribut **searchFlags** sur 1 crée un index de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-110">Setting the least significant bit of the **searchFlags** attribute schema definition to 1 will dynamically build an index.</span></span> <span data-ttu-id="e7b5d-111">La définition de la valeur 0 pour le bit le moins significatif de la définition du schéma de l’attribut **searchFlags** entraîne la suppression de l’index de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-111">Setting the least significant bit of the **searchFlags** attribute schema definition to 0 will cause the index for the attribute to be removed.</span></span> <span data-ttu-id="e7b5d-112">L’index est généré automatiquement par un thread d’arrière-plan sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-112">The index will be built automatically by a background thread on the domain controller.</span></span>

<span data-ttu-id="e7b5d-113">Dans l’idéal, les attributs indexés doivent être à valeur unique, avec des valeurs extrêmement uniques réparties uniformément sur l’ensemble des instances.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-113">Ideally, indexed attributes should be single valued with highly unique values evenly distributed across the set of instances.</span></span> <span data-ttu-id="e7b5d-114">Moins les valeurs d’un attribut sont uniques, moins l’index sera efficace.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-114">The less unique the values of an attribute are, the less effective the index will be.</span></span>

<span data-ttu-id="e7b5d-115">Les attributs à valeurs multiples peuvent également être indexés, mais le coût de création de l’index pour un attribut à valeurs multiples est plus important en termes de durée de stockage, de mise à jour et de recherche.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-115">Multi-valued attributes can also be indexed, but the cost to build the index for a multi-valued attribute is larger in terms of storage, update, and search time.</span></span> <span data-ttu-id="e7b5d-116">L’unicité requise pour une propriété à valeurs multiples est identique à celle d’une propriété à valeur unique. plus les valeurs sont uniques, plus l’index est efficace.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-116">The uniqueness requirement for a multi-valued property is the same as that for a single-valued property—the more unique the values are the more effective the index.</span></span>

<span data-ttu-id="e7b5d-117">Plus une classe possède d’attributs indexés, plus il faut de temps pour créer de nouvelles instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-117">The more indexed attributes a class has, the more time is required to create new instances of the class.</span></span>

<span data-ttu-id="e7b5d-118">Les index s’appliquent aux attributs, pas aux classes.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-118">Indexes apply to attributes, not to classes.</span></span> <span data-ttu-id="e7b5d-119">Autrement dit, lorsqu’un attribut est marqué comme indexé, toutes les instances de l’attribut sont ajoutées à l’index, pas seulement les instances qui sont membres d’une classe particulière.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-119">That is, when an attribute is marked as indexed, all instances of the attribute are added to the index, not just the instances that are members of a particular class.</span></span>

<span data-ttu-id="e7b5d-120">Pour vérifier qu’un serveur utilise un index pour traiter une requête, affectez la valeur 4 à la valeur de Registre suivante sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-120">To verify that a server is using an index to process a query, set the following registry value on a domain controller to 4.</span></span> <span data-ttu-id="e7b5d-121">Exécutez ensuite une requête sur ce contrôleur de domaine et recherchez dans le journal des événements de l’annuaire des données relatives aux index, le cas échéant, utilisés pour traiter la requête.</span><span class="sxs-lookup"><span data-stu-id="e7b5d-121">Then perform a query on that domain controller and look in the directory event log for data about the indexes, if any, used to process the query.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

<span data-ttu-id="e7b5d-122">Pour plus d’informations sur les autres bits dans la propriété [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) , consultez [caractéristiques des attributs](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e7b5d-122">For more information about other bits in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) property, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

 

 