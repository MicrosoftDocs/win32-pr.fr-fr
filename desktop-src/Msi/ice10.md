---
description: ICE10 vérifie que l’état de publication des fonctionnalités enfants correspond à celui de sa fonctionnalité parente.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80071bdb7f219904c03d7c6b5b947a1bd818af2c3ebc270b0bfb17f2cf185280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581209"
---
# <a name="ice10"></a>ICE10

ICE10 vérifie que l’état de publication des fonctionnalités enfants correspond à celui de sa fonctionnalité parente.

Une fonctionnalité enfant peut ne pas autoriser la publication pendant que sa fonctionnalité parente autorise la publication. La combinaison suivante d’attributs parents et enfants n’est donc pas valide.

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

Cette combinaison n’est pas valide, car elle désactive le parent chaque fois que le parent était supposé être publié. Toutefois, l’inverse est autorisé. Un enfant peut être marqué pour favoriser la publication tandis que le parent est marqué pour interdire la publication.

L’action personnalisée ICE10 détermine l’état des fonctionnalités parent et enfant à partir de la colonne attributs du tableau des [fonctionnalités](feature-table.md) . Notez qu’il est possible d’affecter la valeur 0 à l’état d’une fonctionnalité et de faire en sorte que son parent ou enfant soit configuré pour privilégier ou interdire la publication.

## <a name="result"></a>Résultat

ICE10 publie une erreur si la colonne attributs du tableau des [fonctionnalités](feature-table.md) contient une incompatibilité dans l’état de publication.

## <a name="example"></a>Exemples

ICE10 publie le message d’erreur suivant pour l’exemple indiqué.

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

remarque : dans cet exemple, les Microsoft Excel et Microsoft Word sont des fonctionnalités enfants de Microsoft Office.

Table des [fonctionnalités](feature-table.md) (partielle)



| Caractéristique | Parent de la fonctionnalité \_ | Attributs |
|---------|-----------------|------------|
| Office  | Null            | 4          |
| Excel   | Office          | 4          |
| Word    | Office          | 8          |



 

Dans l’exemple, Word est configuré pour interdire la publication, ce qui est en conflit avec l’état d’autorisation de publication de son parent Office.

Dans certains cas, ICE10 publie l’erreur suivante :

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

Cela fait référence à une référence de clé étrangère non valide. Le correctif consiste à avoir le point « enfant » sur sa fonctionnalité parente correcte, ou à ajouter une entrée pour la fonctionnalité parente « parent » à la table des [fonctionnalités](feature-table.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



