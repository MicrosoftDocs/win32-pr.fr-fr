---
title: Propriétés et jeux de propriétés
description: bien que les types de propriétés d’exécution que l’automatisation et les contrôles Microsoft ActiveX offrent soient importants, ils ne répondent pas directement à la nécessité de stocker des informations avec des objets stockés de manière permanente dans le système de fichiers.
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- structured Stockage Strctd Stg, fundamentals, properties et property sets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df2ef4b3e4d91cc908d82b58a0ec0156a60de23208cfd8dde2718fa62eaab60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662259"
---
# <a name="properties-and-property-sets"></a>Propriétés et jeux de propriétés

bien que les types de propriétés d’exécution que l’automatisation et les contrôles Microsoft ActiveX offrent soient importants, ils ne répondent pas directement à la nécessité de stocker des informations avec des objets stockés de manière permanente dans le système de fichiers. Ces entités peuvent inclure des fichiers (structurés, composés, etc.), des répertoires et des catalogues de résumé. COM fournit un format sérialisé standard pour ces propriétés persistantes, ainsi qu’un ensemble d’interfaces et de fonctions qui vous permettent de créer et de manipuler les jeux de propriétés et leurs propriétés.

Les propriétés persistantes sont stockées en tant que jeux et un ou plusieurs jeux peuvent être associés à une entité du système de fichiers. Ces jeux de propriétés persistants sont destinés à être utilisés pour stocker des données qui conviennent pour être représentées sous la forme d’une collection de valeurs affinées. Ils ne sont pas destinés à être utilisés en tant que base de données volumineuse. Elles peuvent être utilisées pour stocker des informations de synthèse sur un objet sur le système, qui est ensuite accessible par tout autre objet qui comprend la manière d’interpréter ce jeu de propriétés.

Les versions précédentes de COM n’ont pas été spécifiées très peu en ce qui concerne les propriétés et leur utilisation, mais définissent un format sérialisé qui permettait aux développeurs de stocker les propriétés et les jeux de propriétés dans une instance [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Les identificateurs de propriété et la sémantique d’un ensemble de propriétés unique, utilisé pour les informations récapitulatives relatives à un document, ont également été définis. À ce moment-là, il était nécessaire de créer et de manipuler directement cette structure comme un flux de données. consultez [structured Stockage serialized Property Set Format](structured-storage-serialized-property-set-format.md).

Désormais, COM définit deux interfaces principales pour gérer les jeux de propriétés :

-   [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Il n’est plus nécessaire de traiter le format sérialisé directement lorsque ces interfaces sont implémentées sur un objet qui prend en charge l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) (comme les fichiers composés). L’écriture de propriétés via [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) crée des données qui se conforment exactement au format du jeu de propriétés com, tel qu’il est affiché à l’aide des méthodes **IStorage** . L’inverse est également vrai : les propriétés écrites dans le format de jeu de propriétés COM à l’aide de **IStorage** sont visibles via **IPropertySetStorage** et **IPropertyStorage** (même si vous ne pouvez pas vous attendre à écrire dans [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) et faire en sorte que les propriétés via **IPropertyStorage** soient immédiatement disponibles, ou vice versa).

L’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) définit les méthodes qui créent et gèrent les jeux de propriétés. L’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manipule directement les propriétés dans un jeu de propriétés. En appelant les méthodes de ces interfaces, un développeur d’applications peut gérer tous les jeux de propriétés appropriés pour une entité de système de fichiers donnée. L’utilisation de ces interfaces fournit une implémentation de lecture et d’écriture pour les propriétés, plutôt que d’avoir une implémentation dans chaque application, où il peut y avoir des goulots d’étranglement de performances tels que la recherche de incessant. Vous pouvez implémenter les interfaces pour améliorer les performances, de sorte que les propriétés puissent être lues et écrites plus rapidement par, par exemple, une mise en cache plus efficace. En outre, **IPropertyStorage** et **IPropertySetStorage** permettent de manipuler des propriétés sur des entités qui ne prennent pas en charge [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), bien qu’en général, la plupart des applications ne le font pas.

Cette section contient les rubriques suivantes :

-   [La propriété informations de résumé définie](the-summary-information-property-set.md)
-   [Identificateurs de format de jeu de propriétés prédéfinis](predefined-property-set-format-identifiers.md)
-   [Jeux de propriétés DocumentSummaryInformation et UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Implémentations de jeux de propriétés dans COM](property-set-implementations-in-com.md)
</dt> <dt>

[Considérations relatives aux jeux de propriétés](property-set-considerations.md)
</dt> <dt>

[Gestion des propriétés](managing-properties.md)
</dt> <dt>

[Gestion des jeux de propriétés](managing-property-sets.md)
</dt> <dt>

[Stockage des jeux de propriétés](storing-property-sets.md)
</dt> <dt>

[Caractéristiques de performances](performance-characteristics.md)
</dt> </dl>

 

 




