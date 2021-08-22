---
description: ICE22 utilise la table FeatureComponents pour valider le mappage des fonctionnalités et des composants référencés dans la table PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177fcef5441e5b82738c76face70427cc6865ae59c11542fca080b3dc521c5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529019"
---
# <a name="ice22"></a>ICE22

ICE22 utilise la [table FeatureComponents](featurecomponents-table.md) pour valider le mappage des fonctionnalités et des composants référencés dans la [table PublishComponent](publishcomponent-table.md).

## <a name="result"></a>Résultat

ICE22 publie un message d’erreur si les fonctionnalités et les composants sont mappés de manière incorrecte dans la [table PublishComponent](publishcomponent-table.md).

## <a name="example"></a>Exemples

Dans l’exemple suivant, ICE22 publie une erreur qui {00000003-0004-0000-0000-624474732465} n’a pas le mappage correct pour les \_ colonnes de composants et de fonctionnalités \_ .

[Table PublishComponent](publishcomponent-table.md) (partielle)



| ComponentId                            | Caractéristique\_ | Composant\_ |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | Feat1     | COMP1       |
| {00000003-0004-0000-0000-624474732465} | Feat1     | COMP2       |



 

[Table FeatureComponents](featurecomponents-table.md) (partielle)



| Caractéristique\_ | Composant\_ |
|-----------|-------------|
| Feat1     | COMP1       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



