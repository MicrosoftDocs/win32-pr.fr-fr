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
ms.openlocfilehash: cabd205fea66b198096a9a9427822eb4ba0ccb609fb3e6fef0854fa91848371c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187583"
---
# <a name="indexed-attributes-ad-ds"></a>Attributs indexés (AD DS)

Les attributs peuvent être indexés. L’indexation d’un attribut peut améliorer les performances des requêtes de cet attribut.

Un attribut est indexé lorsque l’attribut [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) dans la définition de schéma de l’attribut a le bit le moins significatif défini sur 1. La définition du bit le moins significatif de la définition de schéma de l’attribut **searchFlags** sur 1 crée un index de manière dynamique. La définition de la valeur 0 pour le bit le moins significatif de la définition du schéma de l’attribut **searchFlags** entraîne la suppression de l’index de l’attribut. L’index est généré automatiquement par un thread d’arrière-plan sur le contrôleur de domaine.

Dans l’idéal, les attributs indexés doivent être à valeur unique, avec des valeurs extrêmement uniques réparties uniformément sur l’ensemble des instances. Moins les valeurs d’un attribut sont uniques, moins l’index sera efficace.

Les attributs à valeurs multiples peuvent également être indexés, mais le coût de création de l’index pour un attribut à valeurs multiples est plus important en termes de durée de stockage, de mise à jour et de recherche. L’unicité requise pour une propriété à valeurs multiples est identique à celle d’une propriété à valeur unique. plus les valeurs sont uniques, plus l’index est efficace.

Plus une classe possède d’attributs indexés, plus il faut de temps pour créer de nouvelles instances de la classe.

Les index s’appliquent aux attributs, pas aux classes. Autrement dit, lorsqu’un attribut est marqué comme indexé, toutes les instances de l’attribut sont ajoutées à l’index, pas seulement les instances qui sont membres d’une classe particulière.

Pour vérifier qu’un serveur utilise un index pour traiter une requête, affectez la valeur 4 à la valeur de Registre suivante sur un contrôleur de domaine. Exécutez ensuite une requête sur ce contrôleur de domaine et recherchez dans le journal des événements de l’annuaire des données relatives aux index, le cas échéant, utilisés pour traiter la requête.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

Pour plus d’informations sur les autres bits dans la propriété [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) , consultez [caractéristiques des attributs](characteristics-of-attributes.md).

 

 