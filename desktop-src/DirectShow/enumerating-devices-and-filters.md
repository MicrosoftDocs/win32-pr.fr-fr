---
description: Énumération des appareils et des filtres
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Énumération des appareils et des filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53f4a36e2bf994cfeab34a49444d104b2213a839bb1fa8bd2aa4d70e0003b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401773"
---
# <a name="enumerating-devices-and-filters"></a>Énumération des appareils et des filtres

Parfois, une application doit localiser un filtre particulier sur le système de l’utilisateur. Par exemple, une application de capture vidéo peut afficher une liste des périphériques de capture disponibles. étant donné que DirectShow utilise une architecture basée sur des composants, vous ne pouvez pas savoir au moment de la conception quels filtres sont installés sur le système de l’utilisateur. Cela est particulièrement vrai pour les filtres qui représentent des périphériques matériels. DirectShow fournit deux composants qui localisent les filtres enregistrés :

-   L' [énumérateur de périphérique système](system-device-enumerator.md) recherche les filtres par catégorie.
-   Le [Mappeur de filtre](filter-mapper.md) recherche les filtres en fonction des critères de recherche fournis par l’application.

Les énumérateurs abordés dans cette section suivent le formulaire standard utilisé par les interfaces d’énumération COM. Pour plus d’informations, consultez la rubrique « IEnumXXXX » dans le kit de développement logiciel (SDK) de la plate-forme Microsoft.

Cette section contient les rubriques suivantes :

-   [Utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md)
-   [Utilisation du mappeur de filtre](using-the-filter-mapper.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[tâches de base DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



