---
description: ICE47 vérifie la fonctionnalité et les tables FeatureComponents pour les fonctionnalités avec 1600 ou plus de composants.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202750"
---
# <a name="ice47"></a>ICE47

ICE47 vérifie la [fonctionnalité](feature-table.md) et les tables [FeatureComponents](featurecomponents-table.md) pour les fonctionnalités avec 1600 ou plus de composants.

## <a name="result"></a>Résultats

ICE47 publie un message d’erreur si une fonctionnalité dépasse la limite maximale de 1600 composants par fonctionnalité.

## <a name="example"></a>Exemple

ICE47 signale l’avertissement suivant :

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

[Table des fonctionnalités](feature-table.md) (partielle)



| Fonctionnalité  |
|----------|
| Feature1 |



 

[Table FeatureComponents](featurecomponents-table.md) (partielle)



| Action   | Condition     |
|----------|---------------|
| Feature1 | Composant1    |
| Feature1 | Component1600 |



 

Pour résoudre cet avertissement, essayez de fractionner la fonctionnalité en plusieurs fonctionnalités

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



