---
description: ICE21 valide que chaque composant de la table de composants appartient à une fonctionnalité. Elle utilise la table FeatureComponents pour vérifier ce mappage.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538908"
---
# <a name="ice21"></a>ICE21

ICE21 valide que chaque composant de la [table de composants](component-table.md) appartient à une fonctionnalité. Elle utilise la [table FeatureComponents](featurecomponents-table.md) pour vérifier ce mappage.

## <a name="result"></a>Résultats

ICE21 publie un message d’erreur si le package d’installation contient un composant qui n’appartient pas à une fonctionnalité.

## <a name="example"></a>Exemple

Dans l’exemple suivant, ICE21 publie un message d’erreur indiquant que le composant COMP1 n’est mappé à aucune fonctionnalité.

[Table des composants](component-table.md) (partielle)



| Composant |
|-----------|
| COMP1     |
| COMP2     |



 

[Table FeatureComponents](featurecomponents-table.md) (partielle)



| Fonctionnalité  | Composant |
|----------|-----------|
| Feature1 | COMP2     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



