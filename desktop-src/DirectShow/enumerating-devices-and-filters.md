---
description: Énumération des appareils et des filtres
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Énumération des appareils et des filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846601"
---
# <a name="enumerating-devices-and-filters"></a>Énumération des appareils et des filtres

Parfois, une application doit localiser un filtre particulier sur le système de l’utilisateur. Par exemple, une application de capture vidéo peut afficher une liste des périphériques de capture disponibles. Étant donné que DirectShow utilise une architecture basée sur des composants, vous ne pouvez pas savoir au moment de la conception quels filtres sont installés sur le système de l’utilisateur. Cela est particulièrement vrai pour les filtres qui représentent des périphériques matériels. DirectShow fournit deux composants qui localisent les filtres enregistrés :

-   L' [énumérateur de périphérique système](system-device-enumerator.md) recherche les filtres par catégorie.
-   Le [Mappeur de filtre](filter-mapper.md) recherche les filtres en fonction des critères de recherche fournis par l’application.

Les énumérateurs abordés dans cette section suivent le formulaire standard utilisé par les interfaces d’énumération COM. Pour plus d’informations, consultez la rubrique « IEnumXXXX » dans le kit de développement logiciel (SDK) de la plate-forme Microsoft.

Cette section contient les rubriques suivantes :

-   [Utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md)
-   [Utilisation du mappeur de filtre](using-the-filter-mapper.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de base de DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



