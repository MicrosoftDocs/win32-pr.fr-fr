---
description: Énumération d’objets dans un filtre Graph
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Énumération d’objets dans un filtre Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239082"
---
# <a name="enumerating-objects-in-a-filter-graph"></a>Énumération d’objets dans un filtre Graph

Une application peut avoir besoin de localiser un filtre particulier dans le graphique de filtre, ou même un code PIN particulier sur un filtre. Par exemple, il peut utiliser une interface exposée par un filtre particulier. Il peut également construire un graphique de filtres spécialisé et avoir besoin d’appeler des méthodes sur des broches individuelles pour connecter les filtres. à cet effet, DirectShow fournit plusieurs méthodes pour énumérer des objets dans un graphique de filtre.

Les énumérateurs abordés dans cette section suivent le formulaire standard utilisé par les interfaces d’énumération COM. Pour plus d’informations, consultez la rubrique « IEnumXXXX » dans le kit de développement logiciel (SDK) de plateforme. Pour plus d’informations sur l’énumération des filtres inscrits sur l’ordinateur de l’utilisateur, mais qui ne sont pas encore dans le graphique de filtre, consultez [énumération d’appareils et de filtres](enumerating-devices-and-filters.md).

Cet article contient les rubriques suivantes :

-   [Énumération des filtres](enumerating-filters.md)
-   [Énumération des codes confidentiels](enumerating-pins.md)
-   [Énumération des types de média](enumerating-media-types.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[tâches de base DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



