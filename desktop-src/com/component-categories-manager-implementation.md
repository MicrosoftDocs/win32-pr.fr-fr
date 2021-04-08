---
title: Implémentation du gestionnaire de catégories de composants
description: À mesure que le nombre de composants disponibles augmente, il devient de plus en plus difficile de gérer ces composants. En ce qui concerne les interfaces qu’ils exposent, ainsi que les tâches qu’ils effectuent, de nombreux composants offrent des fonctionnalités similaires.
ms.assetid: c2c67129-bf19-465b-8354-193922aeafaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2414567beba159c05ea08b3561f0a97ddda1cb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940316"
---
# <a name="component-categories-manager-implementation"></a>Implémentation du gestionnaire de catégories de composants

À mesure que le nombre de composants disponibles augmente, il devient de plus en plus difficile de gérer ces composants. En ce qui concerne les interfaces qu’ils exposent, ainsi que les tâches qu’ils effectuent, de nombreux composants offrent des fonctionnalités similaires.

Il est souvent nécessaire d’énumérer les composants qui peuvent être utilisés dans un certain contexte. Voici quelques exemples : la boîte de dialogue **Insérer un objet** utilisée dans les documents composés OLE et la boîte de dialogue **Insérer un contrôle** utilisée dans les contrôles OLE. Ces boîtes de dialogue répertorient tous les composants qui remplissent (ou revendiquent de satisfaire) les contrats d’interface pour les documents ou les contrôles composés. Ces catégories existantes (document OLE, contrôle OLE) n’impliquent pas une signature d’interface exacte. Les documents OLE doivent exposer un certain ensemble d’interfaces de base (par exemple, [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) ou [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)), mais peuvent également exposer des interfaces supplémentaires telles que [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink).

Dans le passé, les composants ont été balisés en ajoutant un nom explicite (« Insertable », « contrôle », etc.) en tant que sous-clé du **\_ CLSID racine des classes HKEY \_ \\ \\ {...}** clé de Registre correspondant au composant. Cela fonctionne bien pour une définition centrale des catégories, mais présente des risques de collisions de noms lorsque de nombreuses parties indépendantes définissent de nouvelles catégories. Comme dans d’autres domaines de COM, la solution pour fournir un espace de noms extensible réside dans l’utilisation d’identificateurs globaux uniques (GUID). Au lieu d’utiliser un nom explicite, un nombre unique (CATID) est affecté à chaque catégorie.

Une autre limitation à la catégorisation existante est qu’elle est limitée à l’expression des fonctionnalités du composant lui-même. De nombreux composants requièrent certaines fonctionnalités des conteneurs. Lorsqu’un tel composant est inséré dans un conteneur, l’insertion peut échouer ou se comporter de manière inattendue, même si le composant respecte les contrats de l’une de ses catégories. Pour énumérer les composants qui peuvent être utilisés avec succès dans certaines situations, les fonctionnalités du composant et du conteneur doivent être prises en compte.

En raison de ces considérations, les modifications suivantes ont été apportées à la catégorisation existante :

-   Les catégories sont indiquées à l’aide de CATID qui sont des identificateurs globaux uniques.
-   Dans la sous-clé **Components** de la clé de Registre **HKEY \_ classes \_ racine \\ CLSID** , deux sous-clés distinctes, « Categories Implemented » et « categories required », ont été développées. Ces sous-clés contiennent les listes de CATID fournis par le composant ou que le conteneur du composant doit fournir.

Pour faciliter la gestion des catégories de composants, les catégories sont répertoriées à un emplacement central dans le registre : **\_ catégories du \_ \\ composant racine des classes HKEY**. Cette clé répertorie les catégories installées avec leur CATID et avec des noms localisés et explicites.

Pour plus d'informations, voir les rubriques suivantes :

-   [Catégorisation par fonctionnalités de composant](categorizing-by-component-capabilities.md)
-   [Catégorisation par fonctionnalités de conteneur](categorizing-by-container-capabilities.md)
-   [Gestionnaire de catégories de composants](the-component-categories-manager.md)
-   [Classes et associations par défaut](default-classes-and-associations.md)
-   [Définition des catégories de composants](defining-component-categories.md)
-   [Association d’icônes à une catégorie](associating-icons-with-a-category.md)

 

 




