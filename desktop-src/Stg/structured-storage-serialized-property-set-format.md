---
title: Format de jeu de propriétés sérialisé Stockage sérialisé
description: Les jeux de propriétés persistantes fournissent une option pour stocker les données dans les entités du système de fichiers. Pour les créer et les gérer, il est recommandé d’utiliser les interfaces IPropertySetStorage et IPropertyStorage décrites dans Propriétés et jeux de propriétés.
ms.assetid: f22abe40-535f-4178-9460-59bbe26ff178
keywords:
- structured Stockage Strctd Stg, fundamentals, format de jeu de propriétés sérialisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5acbc5300c04b4fe5a9b2a9ce2610eefc8608b3921ef52968a7165c4362ff7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959773"
---
# <a name="structured-storage-serialized-property-set-format"></a>Format de jeu de propriétés sérialisé Stockage sérialisé

Les jeux de propriétés persistantes fournissent une option pour stocker les données dans les entités du système de fichiers. Pour les créer et les gérer, il est recommandé d’utiliser les interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) décrites dans [Propriétés et jeux](properties-and-property-sets.md)de propriétés.

Les jeux de propriétés sont composés d’une section avec balises de valeurs, avec la section identifiée de façon unique par un identificateur de format (FMTID). Chaque propriété se compose d’un identificateur de propriété et d’un indicateur de type qui représente une valeur. Chaque valeur stockée dans un jeu de propriétés a un identificateur de propriété unique qui distingue la propriété. L’indicateur de type décrit la représentation des données dans la valeur.

Lorsque vous utilisez les interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , vous n’avez pas à gérer la structure de format du jeu de propriétés sérialisé com. Pour plus d’informations, consultez les rubriques suivantes :

Tous les éléments de données d’un jeu de propriétés sont stockés dans la représentation Intel (c’est-à-dire, dans l’ordre de primauté des octets de poids faible).

COM définit un format de données sérialisé standard pour les jeux de propriétés. Lors du traitement du format sérialisé, et non avec les interfaces, les jeux de propriétés présentent les caractéristiques suivantes :

-   Les jeux de propriétés permettent à différentes applications de créer leurs propres jeux de propriétés indépendants pour servir l’application.
-   Les jeux de propriétés peuvent être stockés dans une instance [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) unique ou dans une instance [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) qui contient plusieurs flux. Les jeux de propriétés sont simplement un autre type de données qui peut être stocké dans de nombreuses formes différentes d’un stockage en mémoire ou sur disque. pour plus d’informations et pour connaître les conventions recommandées pour la création du nom de chaîne pour l’objet de stockage, consultez [conventions d’affectation des noms d’objets Stockage](storage-object-naming-conventions.md).
-   Les jeux de propriétés permettent d’inclure un dictionnaire de noms complets qui décrivent le contenu. Il est recommandé d’avoir un ensemble de conventions pour choisir des noms de propriétés. Pour plus d’informations sur ce dictionnaire facultatif, consultez [identificateurs de propriété réservés](reserved-property-identifiers.md), y compris l' [ID de propriété 0](/windows/desktop/Stg/reserved-property-identifiers).

Le flux de jeu de propriétés est divisé en trois parties principales :

-   En-tête
-   Paire FORMATID/décalage
-   Section contenant les valeurs réelles du jeu de propriétés

La longueur totale du flux de jeu de propriétés doit être inférieure ou égale à 256 Ko. Les sections suivantes, [en-tête de jeu de propriétés](property-set-header.md), [paire identificateur de format/décalage](format-identifier-offset-pair.md)et [section](section.md) (y compris les [identificateurs de propriété/décalage](property-identifiers-offset-pairs.md)), avec les rubriques de prise en charge, décrivent les composants individuels qui composent le format de données de l’ensemble de propriétés.

> [!Note]  
> Les versions précédentes de ce document décrivaient les extensions du flux de jeu de propriétés avec plusieurs sections autorisées, mais qui ont été révisées pour fournir une section dans le flux de propriété. La seule exception concerne [les jeux de propriétés DocumentSummaryInformation et UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

 

 