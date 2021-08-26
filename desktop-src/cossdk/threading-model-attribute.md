---
description: COM+ gère les threads pour vous. Chaque composant COM a une propriété ThreadingModel que vous pouvez spécifier lors du développement du composant. Cette propriété détermine comment les objets de composants sont assignés aux threads pour l’exécution de la méthode.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Attribut de modèle de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba6ae625e4413516066f7180a4eb6870fe4f90df38947fc2476cfbcc7dfadb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070239"
---
# <a name="threading-model-attribute"></a>Attribut de modèle de thread

COM+ gère les threads pour vous. Chaque composant COM a une propriété **ThreadingModel** que vous pouvez spécifier lors du développement du composant. Cette propriété détermine comment les objets du composant sont assignés aux threads pour l’exécution de la méthode.

Vous pouvez utiliser l’outil d’administration Services de composants pour afficher la propriété de modèle de thread en cliquant avec le bouton droit sur un composant dans le dossier **composants** , en cliquant sur **Propriétés**, puis sur l’onglet **accès concurrentiel** . Dans le **modèle de thread**, les valeurs possibles sont les suivantes :

-   **Cloisonnement du thread principal**
-   **Cloisonnement de thread unique**
-   **Cloisonnement de threads libre**
-   **Cloisonnement neutre**
-   **Tout cloisonnement**

Le modèle de thread préféré pour COM+ est le [cloisonnement neutre](neutral-apartments.md). Toutefois, si vous ne spécifiez pas de modèle de thread pour votre composant, COM+ utilise le thread cloisonné principal, qui est la valeur par défaut.

> [!Note]  
> Pour plus d’informations, consultez [choix du modèle de thread](/windows/desktop/com/choosing-the-threading-model).

 

Le tableau suivant présente le modèle de programmation pour les cloisonnements dans COM+.



| Modèle                     | STA                                                 | Gratuit                               | Les deux                               | Neutre                      | Non spécifié                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| À thread unique, non principal | Créé dans le cloisonnement actuel                              | Créé dans un cloisonnement multithread | Créé dans le cloisonnement actuel       | Créé dans le cloisonnement neutre | Créé dans le thread cloisonné principal |
| À thread unique, main     | Créé dans le cloisonnement actuel                              | Créé dans un cloisonnement multithread | Créé dans le cloisonnement actuel       | Créé dans le cloisonnement neutre | Créé dans le cloisonnement actuel       |
| Multithread             | Créé dans l’hôte du cloisonnement à thread unique                 | Créé dans un cloisonnement multithread | Créé dans un cloisonnement multithread | Créé dans le cloisonnement neutre | Créé dans le thread cloisonné principal |
| Neutral (sur thread STA)   | Créé dans l’hôte du cloisonnement à thread unique pour ce thread | Créé dans un cloisonnement multithread | Créé dans le cloisonnement neutre       | Créé dans le cloisonnement neutre | Créé dans le thread cloisonné principal |
| Neutral (sur thread MTA)   | Créé dans l’hôte du cloisonnement à thread unique                 | Créé dans un cloisonnement multithread | Créé dans le cloisonnement neutre       | Créé dans le cloisonnement neutre | Créé dans le thread cloisonné principal |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
