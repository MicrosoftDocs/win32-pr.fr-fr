---
title: Imbrication/délégation
description: Le mécanisme le plus courant pour la réutilisation d’objets dans COM est la relation contenant-contenu et la délégation.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2d90d3439bcb9fb6038940d860533a090ac68fbdee6ca9b2a832afb2803d03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678859"
---
# <a name="containmentdelegation"></a>Imbrication/délégation

Le mécanisme le plus courant pour la réutilisation d’objets dans COM est la *relation contenant-contenu et la délégation*. Ce type de réutilisation est un concept familier trouvé dans la plupart des langages et systèmes orientés objet. L’objet externe, qui doit utiliser l’objet interne, agit comme un client d’objet pour l’objet interne. L’objet externe « contient » l’objet interne et, lorsque l’objet externe requiert les services de l’objet interne, l’objet externe délègue explicitement l’implémentation aux méthodes de l’objet interne. Autrement dit, l’objet externe utilise les services de l’objet interne pour implémenter lui-même.

Il n’est pas nécessaire que les objets externes et internes prennent en charge les mêmes interfaces, bien qu’il soit certainement raisonnable de contenir un objet qui implémente une interface que l’objet externe n’utilise pas et qui implémentent simplement les méthodes de l’objet externe comme des appels aux méthodes correspondantes dans l’objet interne. Toutefois, lorsque la complexité des objets externes et internes diffère sensiblement, l’objet externe peut implémenter certaines des méthodes de ses interfaces en déléguant les appels aux méthodes d’interface implémentées dans l’objet interne.

Il est facile d’implémenter la relation contenant-contenu pour un objet externe. L’objet externe crée les objets internes qu’il doit utiliser comme n’importe quel autre client. Ce n’est rien de nouveau : le processus est comme un objet C++ qui contient lui-même un objet de chaîne C++ qu’il utilise pour exécuter certaines fonctions de chaîne, même si l’objet externe n’est pas considéré comme un objet de chaîne dans son propre droit. Ensuite, à l’aide de son pointeur vers l’objet interne, un appel à une méthode dans l’objet externe génère un appel à une méthode d’objet interne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Agrégation](aggregation.md)
</dt> </dl>

 

 




