---
description: ICE21 valide que chaque composant de la table de composants appartient à une fonctionnalité. Elle utilise la table FeatureComponents pour vérifier ce mappage.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c5c517bd41c7d777f327606b3672f90b57a821dbbef028fa985acd043e6768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529029"
---
# <a name="ice21"></a>ICE21

ICE21 valide que chaque composant de la [table de composants](component-table.md) appartient à une fonctionnalité. Elle utilise la [table FeatureComponents](featurecomponents-table.md) pour vérifier ce mappage.

## <a name="result"></a>Résultat

ICE21 publie un message d’erreur si le package d’installation contient un composant qui n’appartient pas à une fonctionnalité.

## <a name="example"></a>Exemples

Dans l’exemple suivant, ICE21 publie un message d’erreur indiquant que le composant COMP1 n’est mappé à aucune fonctionnalité.

[Table des composants](component-table.md) (partielle)



| Composant |
|-----------|
| COMP1     |
| COMP2     |



 

[Table FeatureComponents](featurecomponents-table.md) (partielle)



| Caractéristique  | Composant |
|----------|-----------|
| Feature1 | COMP2     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



