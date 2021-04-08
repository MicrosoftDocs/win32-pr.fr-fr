---
title: Interrogation de groupes dans un domaine
description: Les groupes peuvent être placés dans n’importe quel conteneur ou unité d’organisation d’un domaine, ainsi que la racine du domaine.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Interrogation de groupes dans un domaine AD
- Groupes Active Directory, interrogation de groupes dans un domaine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3abd4ec393fbeca1308ed59e08131b9b73e6b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842037"
---
# <a name="querying-for-groups-in-a-domain"></a><span data-ttu-id="ebaa0-105">Interrogation de groupes dans un domaine</span><span class="sxs-lookup"><span data-stu-id="ebaa0-105">Querying for Groups in a Domain</span></span>

<span data-ttu-id="ebaa0-106">Les groupes peuvent être placés dans n’importe quel conteneur ou unité d’organisation d’un domaine, ainsi que la racine du domaine.</span><span class="sxs-lookup"><span data-stu-id="ebaa0-106">Groups can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="ebaa0-107">Les groupes ne peuvent pas toujours se trouver dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="ebaa0-107">Groups may not always be in one container.</span></span> <span data-ttu-id="ebaa0-108">Par conséquent, il est nécessaire d’effectuer une recherche dans l’ensemble du domaine pour trouver tous les groupes dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="ebaa0-108">Therefore, it is necessary to search the entire domain to find all groups in the domain.</span></span>

<span data-ttu-id="ebaa0-109">Pour rechercher tous les groupes d’un domaine, définissez le point de départ de la recherche sur la racine du domaine, définissez la zone de recherche sur sous-arborescence et recherchez tous les objets ayant une valeur [**objectClass**](/windows/desktop/ADSchema/a-objectclass) égale à « Group ».</span><span class="sxs-lookup"><span data-stu-id="ebaa0-109">To search for all groups in a domain, set the search start point to the root of the domain, set the search scope to subtree and search for all objects that have an [**objectClass**](/windows/desktop/ADSchema/a-objectclass) value of "group".</span></span>

<span data-ttu-id="ebaa0-110">Si des groupes qui contiennent des valeurs [**\_ \_ \_ enum de type groupe ad**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) spécifiques doivent être trouvés, le **bit de règle de \_ correspondance LDAP \_ \_ \_ et** l’opérateur de règle de correspondance peuvent être utilisés pour rechercher des groupes qui ont des bits particuliers définis dans l’attribut [**GroupType**](/windows/desktop/ADSchema/a-grouptype) .</span><span class="sxs-lookup"><span data-stu-id="ebaa0-110">If groups that contain particular [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) values must be found, the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator can be used to search for groups that have particular bits set in the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="ebaa0-111">Pour plus d’informations sur l’utilisation des règles de correspondance, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="ebaa0-111">For more information about using matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="ebaa0-112">Pour plus d’informations et pour obtenir un exemple de code qui montre comment rechercher des groupes dans un domaine, consultez l' [exemple de code pour rechercher des groupes dans un domaine](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="ebaa0-112">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

 

 