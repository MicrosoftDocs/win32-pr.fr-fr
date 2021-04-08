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
# <a name="querying-for-groups-in-a-domain"></a>Interrogation de groupes dans un domaine

Les groupes peuvent être placés dans n’importe quel conteneur ou unité d’organisation d’un domaine, ainsi que la racine du domaine. Les groupes ne peuvent pas toujours se trouver dans un conteneur. Par conséquent, il est nécessaire d’effectuer une recherche dans l’ensemble du domaine pour trouver tous les groupes dans le domaine.

Pour rechercher tous les groupes d’un domaine, définissez le point de départ de la recherche sur la racine du domaine, définissez la zone de recherche sur sous-arborescence et recherchez tous les objets ayant une valeur [**objectClass**](/windows/desktop/ADSchema/a-objectclass) égale à « Group ».

Si des groupes qui contiennent des valeurs [**\_ \_ \_ enum de type groupe ad**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) spécifiques doivent être trouvés, le **bit de règle de \_ correspondance LDAP \_ \_ \_ et** l’opérateur de règle de correspondance peuvent être utilisés pour rechercher des groupes qui ont des bits particuliers définis dans l’attribut [**GroupType**](/windows/desktop/ADSchema/a-grouptype) . Pour plus d’informations sur l’utilisation des règles de correspondance, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax).

Pour plus d’informations et pour obtenir un exemple de code qui montre comment rechercher des groupes dans un domaine, consultez l' [exemple de code pour rechercher des groupes dans un domaine](example-code-for-performing-a-query-in-a-domain.md).

 

 