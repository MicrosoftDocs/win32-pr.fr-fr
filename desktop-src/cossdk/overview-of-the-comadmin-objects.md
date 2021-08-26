---
description: Les objets comadmin offrent un modèle objet simple qui vous permet d’accéder au catalogue COM+.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Vue d’ensemble des objets comadmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad382fcfab6e53a2eb8bfec9914a070d8a78e6ef2a29253005c324c8df8257e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070389"
---
# <a name="overview-of-the-comadmin-objects"></a>Vue d’ensemble des objets comadmin

Les objets comadmin offrent un modèle objet simple qui vous permet d’accéder au catalogue COM+. Dans ce cas, ils servent à modéliser toutes les fonctionnalités fournies par l’outil d’administration Services de composants. Chaque fois que vous effectuez une administration COM+, vous interagissez avec le catalogue COM+. Pour obtenir une description du catalogue, consultez [accès au catalogue com+](accessing-the-com--catalog.md).

Les informations que vous obtenez à partir de l’outil d’administration Services de composants ou à l’aide des objets comadmin sont structurées de la même façon, et les actions que vous effectuez dans l’un ou l’autre contexte sont analogues. La corrélation de base entre l’utilisation du composant logiciel enfichable Services de composants et l’administration par programme est que les dossiers de l’arborescence de la console du composant logiciel enfichable correspondent aux regroupements dans le catalogue COM+. Autrement dit, chaque dossier du composant logiciel enfichable contient tous les éléments d’un même type ; par exemple, les **applications com+** contiennent des applications com+ installées : chaque collection du catalogue com+ contient des éléments d’un type uniforme. De plus, tout comme chaque élément d’un dossier a des propriétés que vous pouvez définir sur une feuille de propriétés, chaque élément d’une collection expose des propriétés que vous pouvez définir.

Pour vous permettre de configurer des objets dans cette structure, les objets comadmin vous fournissent les moyens d’effectuer les opérations suivantes :

-   Accéder au catalogue COM+
-   Accéder aux regroupements dans le catalogue
-   Accéder aux éléments dans les collections
-   Accéder aux propriétés des éléments des collections

Pour prendre en charge ces actions, la bibliothèque comadmin fournit les trois classes suivantes :

-   [**COMAdminCatalog**](comadmincatalog.md), qui représente le catalogue lui-même.
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md), qui représente n’importe quelle collection.
-   [**COMAdminCatalogObject**](comadmincatalogobject.md), qui représente tout élément d’une collection.

Pour obtenir une description plus complète de ces classes, consultez [Description Résumé des classes comadmin](summary-description-of-the-comadmin-classes.md) dans cette section.

Pour obtenir une idée rapide des actions classiques que vous effectuez dans l’administration par programme, consultez [exemple d’introduction à l’aide du catalogue d’administration com+](introductory-example-using-the-com--administration-catalog.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Opérations d’administration COM+ dans les transactions](com--administration-operations-within-transactions.md)
</dt> <dt>

[Gestion des erreurs d’administration COM+](handling-com--administration-errors.md)
</dt> <dt>

[Exemple d’introduction utilisant le catalogue d’administration COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Récupération des regroupements sur le catalogue COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Définition des propriétés et enregistrement des modifications dans le catalogue COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



