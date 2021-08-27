---
description: Les types de qualificateurs fournissent des informations supplémentaires sur un qualificateur, par exemple si une classe ou une instance dérivée peut substituer la valeur d’origine des qualificateurs.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Types de qualificateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a48c5ed3c7b695b19c182bcf05a9ce55b31b0bb94081570c58c8d55f7e48994c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050477"
---
# <a name="qualifier-flavors"></a>Types de qualificateurs

Les versions de qualificateur fournissent des informations supplémentaires sur un qualificateur, par exemple si une classe ou une instance dérivée peut substituer la valeur d’origine du qualificateur.

Les versions de qualificateur peuvent être ajoutées au début du fichier MOF, à l’aide de la syntaxe suivante, en provoquant leur application dans la définition. Par exemple :

``` syntax
Qualifier Description : ToSubClass Amended;
```

Le **ToSubClass** et les versions **modifiées** s’appliquent à tous les qualificateurs de **Description** dans le MOF.

Le tableau suivant répertorie les versions de qualificateur.



| Version du qualificateur    | Signification                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modifiées**         | Le qualificateur n’est pas requis dans la définition de classe de base et peut être transféré à l’avenant à localiser.                                                                                                                                  |
| **DisableOverride** | Le qualificateur ne peut pas être écrasé dans une classe ou une instance dérivée. Notez que la possibilité d’écraser un qualificateur propagé est activée par défaut.                                                                                                      |
| **EnableOverride**  | En cas de propagation vers une classe ou une instance dérivée, la valeur du qualificateur peut être substituée. La définition de **EnableOverride** est facultative, car la possibilité de remplacer la valeur de qualificateur est la fonctionnalité par défaut pour les qualificateurs propagés. |
| **NotToInstance**   | Le qualificateur n’est pas propagé aux instances de classe.                                                                                                                                                                                             |
| **NotToSubClass**   | Le qualificateur n’est pas propagé aux classes dérivées.                                                                                                                                                                                             |
| **Restreint**      | Le qualificateur n’est pas propagé aux instances ou aux classes dérivées.                                                                                                                                                                                |
| **ToInstance**      | Le qualificateur est propagé aux instances.                                                                                                                                                                                                       |
| **ToSubClass**      | Le qualificateur est propagé aux classes dérivées. Cette version est uniquement appropriée pour les qualificateurs définis pour une classe et ne peut pas être attachée à un qualificateur décrivant une instance de classe.                                                           |



 

 

 



