---
description: Énumération d’objets dans un filtre Graph
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Énumération d’objets dans un filtre Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6206a583daaa984ef67af297c11c125128e58fec410ec1251afaca3987f582
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965469"
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

 

 



